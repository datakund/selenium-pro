hexclad Scraper
########################

Scraper
************

What it does?
=============

It scrape cookware details

How it works?
=============

It open  hexclad  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://hexclad.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('hhAL5YYqDzZR8Um').click()
	# to click on input field
	driver.find_element_by_pro('W6qhdaHZF1gMNLt').click()
	# to type content in input field
	driver.find_element_by_pro('ZjPq8J0I7g9IfHZ').send_keys('bowl')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('dvZLv7iFYrs4fn2')
	for list_element in list_elements:
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('xrr8yTkyQ9ITJuB').text
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('IRgK4JxAbMmYiAu').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('cqkpYY81jkgZjKs').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
