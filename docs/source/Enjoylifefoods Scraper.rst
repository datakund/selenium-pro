Enjoylifefoods Scraper
########################

Scraper
************

What it does?
=============

It scrape food product details

How it works?
=============

It open enjoylifefoods  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://enjoylifefoods.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('54sYJsntWDioBUC').click()
	# to type content in input field
	driver.find_element_by_pro('GGR25xs2p5A7QgK').send_keys('snacks')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('AJK1dWzdlo7XhNB')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('cdaN74J4Fj9XZag').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('4Yii3QsVJssmtfd').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('hbDbp80T1bX2v6K').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
