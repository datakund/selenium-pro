Brentwood  Scraper
########################

Scraper
************

What it does?
=============

It scrape bed details

How it works?
=============

It open brentwood homes  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.brentwoodhome.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('nYV2Z373CBh88RB').click()
	# to type content in input field
	driver.find_element_by_pro('XiA0OYHnMd7t3Ft').send_keys('bed')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('T3O0au3Vr4umhbY')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('GtAwcJMdw50dPRy').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('zuLHwTbG3zIpkyY').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('K1YlWqzGytsquAs').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
