Jonathan Scraper
########################

Scraper
************

What it does?
=============

It scrape furniture details

How it works?
=============

It open jonathan website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://jonathanadler.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('Bd46vDCSfhg7aJw').click()
	# to type content in input field
	driver.find_element_by_pro('um1xqUvh7hZlRMs').send_keys('art')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('eAScFqgKnLBfM59')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('z6bI8pQ2K86Hcv8').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('6ZueCrI1ND3PQ8q').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('VkalvFlywR5SzLx').get_attribute('href')
	    # to scroll down
	    
	# to click on the element(>) found
	driver.find_element_by_pro('Hthk3Kcp3HBfj1P').click()
	time.sleep(3)

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
