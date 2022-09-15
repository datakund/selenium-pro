Scraper
************

Whitefox Scraper
########################

What it does?
=============

It scrape clothes details

How it works?
=============

It open whitefox website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://whitefoxboutique.com.au/')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('l7zNyIIZDNTcsEZ').click()
	# to type content in input field
	driver.find_element_by_pro('6y3KZ8EbAjD5tyh').send_keys('swim')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('YCOLKf9U7d2yvsp')
	for list_element in list_elements:
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('YSQ4WSIhh0hOYe1').text
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('llK3fTCeKk8I8yw').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('K9MCCWPynwWS00G').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
