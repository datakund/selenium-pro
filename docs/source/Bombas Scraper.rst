Bombas Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open Bombas website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://bombas.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('r2oRiwnw8JWgNpB').click()
	# to type content in input field
	driver.find_element_by_pro('AYBv7ao2SHKU1uo').send_keys('shirt')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('RCw3EnGdMIiCmkj')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('UwYd6V2RABLOmV0').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('PycFWGKupF8zve3').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('8z1r0EWAZL0UdYm').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
