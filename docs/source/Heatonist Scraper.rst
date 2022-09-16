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
	driver.find_element_by_pro('fRSkvPGepth2RvG').click()
	# to click on input field
	driver.find_element_by_pro('YP8ioWxpbP0x45I').click()
	# to type content in input field
	driver.find_element_by_pro('mbXZKzKdoGzhCCb').send_keys('sauce')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('kwHUFh9ZiQsxig9')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('NjJ4fxGr6WuQIyC').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('auZT0HDqQsYT7rb').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('1hoyJncDep90XpT').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('rUATUXXErUXYnC3').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
