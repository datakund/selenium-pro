myjewels Scraper
########################

Scraper
************

What it does?
=============

It scrape jewelry details

How it works?
=============

It open myjewels website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://my-jewels.com/')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('EW3WH4eU4YT5Iuv').click()
	# to type content in input field
	driver.find_element_by_pro('xRnOsErr6EWOXci').send_keys('chain')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('tWcL3QqV9Slsi3N')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('1s52mn4IQrM3Ra0').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('oBiQLPWkdebqwYq').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
