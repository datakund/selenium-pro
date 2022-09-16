Heatonist Scraper
########################

Scraper
************

What it does?
=============

It scrape Sauces details

How it works?
=============

It open Heatonist website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://heatonist.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('40YyA5s9XNWY9A1').click()
	# to click on input field
	driver.find_element_by_pro('S14IZMhzU1O7M9t').click()
	# to type content in input field
	driver.find_element_by_pro('5Sg9catyooUPCrW').send_keys('sauce')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('WlFplHZk7WQx6pD')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('QtN3frxAeEQR97g').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('FrOGOrG2DmHpSW4').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('IivLOslunxbWBRT').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('AAGRHKYK9pVrGgL').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
