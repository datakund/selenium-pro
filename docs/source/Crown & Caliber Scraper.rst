Crown & Caliber Scraper
########################

Scraper
************

What it does?
=============

It scrape watch details

How it works?
=============

It open crown&calliber website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.crownandcaliber.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('QQU5xEx8Azc0CyL').click()
	# to type content in input field
	driver.find_element_by_pro('d4lGJS8lXZBe9lv').send_keys('watch')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('HWO460SxWxNuy5n')
	for list_element in list_elements:
	    # to fetch the text of element
	    title 1=list_element.find_element_by_pro('DOPgDxcA1RVZanE').text
	    # to fetch the text of element
	    title 2=list_element.find_element_by_pro('RsFGkI9Lcr9xWUq').text
	    # to fetch the text of element
	    title 3=list_element.find_element_by_pro('hujWbPOijCPpKEI').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('PsTGoPAesqFhWaT').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('VN2IitAGIgjOmbr').get_attribute('href')

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
