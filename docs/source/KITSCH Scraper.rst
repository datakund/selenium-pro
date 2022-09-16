KITSCH Scraper
########################

Scraper
************

What it does?
=============

It scrape hair accessories details

How it works?
=============

It open mykitsch  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://mykitsch.com/collections/best-sellers')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('uGchhua3vbngGhm').click()
	# to type content in input field
	driver.find_element_by_pro('RyTyrGGiEI41lFX').send_keys('clip')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('vAPd9XnRCsiMxHo')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('EYA50aSo9QtN1uF').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('TYH8K0M9glo6oYi').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('PPbLChbuQ1PMT2D').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('QGO6rWu6UfoXUuG').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
