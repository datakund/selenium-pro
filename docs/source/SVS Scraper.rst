SVS Scraper
########################

Scraper
************

What it does?
=============

It scrape speaker details

How it works?
=============

It open svs  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.svsound.com/')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('83JAEEl34kA999v').click()
	# to type content in input field
	driver.find_element_by_pro('SWnHNq57TLRyVFU').send_keys('speaker')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('9nsJuNtfLE8WEnd')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('zuzXsuxfHiWUksI').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('qEaPeaVcRt09p2a').get_attribute('href')
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('xcU3PbjRv6WfTc1').text

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
