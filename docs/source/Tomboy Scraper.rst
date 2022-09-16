Tomboy Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open tomboy website, search for given keyword and it scrape product name, link ,price

Import
=============

``from selenium_pro import webdriver``


Start Browser
=============

``driver=webdriver.Start()``


Code
===========

.. tabs::

   .. code-tab:: py

        #pip install selenium_pro
        from selenium_pro import webdriver
	import time
	from selenium_pro.webdriver.common.keys import Keys
	driver = webdriver.Start()
	# to open the url in browser
	driver.get('https://tomboyx.com/?irclickid=yqSR%3AozWAxyNTpPzoKRIEQ4NUkDWg9xKTQRL3c0&utm_source=impact&utm_medium=affiliate&utm_campaign=Cloudtraffic&utm_content=631f3014dee98500010966c1&utm_term=2031198&irgwc=1&ir_partnerid=2031198&ir_adid=1162522&ir_campaignid=14705')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('kFFEhcEQ1DfW0EI').click()
	# to type content in input field
	driver.find_element_by_pro('ydU4btLZ8xbM935').send_keys('swim')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('q8Z73RpBtFr3yhH')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('GfybUKidCSDPnys').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('xoqyarKMJYSpxdS').get_attribute('href')
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('0wsQqc5X406fYdt').text
	    # to scroll down
	    
	# to click on the element(2) found
	driver.find_element_by_pro('mqODPgqIIozk9o0').click()
	time.sleep(3)

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
