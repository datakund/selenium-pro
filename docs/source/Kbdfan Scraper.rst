Kbdfan Scraper
########################

Scraper
************

What it does?
=============

It scrape electronic product details

How it works?
=============

It open kbdfan website, search for given keyword and it scrape product name, link ,price

Import
=============

``from selenium_pro import webdriver``


Start Browser
=============

``driver=webdriver.Start()``


Login with Cookies
===================

``Cookies not required``


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
	driver.get('https://kbdfans.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('L3rKRy2XRTZ2k0I').click()
	# to type content in input field
	driver.find_element_by_pro('D4WXfjaaCSVwTE9').send_keys('pcb')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('pHgLNAxm3PPE4h3')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('3a85JCDBoqmd4op').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('jcXKz2iMZtM0WVD').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('R3tbqVaPsAM4jMc').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
