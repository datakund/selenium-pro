Sapphire Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open sapphire website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://pk.sapphireonline.pk/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('63UfZgmlz4SMdCW').click()
	# to click on input field
	driver.find_element_by_pro('y2MGdYAaJlwXaCX').click()
	# to type content in input field
	driver.find_element_by_pro('2SGk645w4KWdztx').send_keys('dress')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('dQf2TdTGcn20nF5')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('A0wF9Ail4CvceP8').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('Ry4HEUQxHrgJwWV').text
	    # to fetch the text of element
	    name=list_element.find_element_by_pro('ZcHXT1gTgvnptnY').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('ZKoi8STMnnPcMeh').get_attribute('href')
	    # to scroll down
	    
	# to click on the element(2) found
	driver.find_element_by_pro('WvseOjGELPjpvGR').click()
	time.sleep(3)

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
