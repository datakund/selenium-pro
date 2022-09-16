Roolee Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open roolee  clothing website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://roolee.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('p2eh5D9whmOCDGm').click()
	# to type content in input field
	driver.find_element_by_pro('5H65QJeeZ75TAD5').send_keys('top')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('OXL5MFW2tnfmoJs')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('do6pjx0MFfnPVAC').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('4rM198aZAej86Qr').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('6aYe99OOAf8XYzu').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
