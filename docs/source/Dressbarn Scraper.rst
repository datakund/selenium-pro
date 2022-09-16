Dressbarn Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open dressbarn  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://dressbarn.com/')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('0CpF3bBbhH6T0ZQ').click()
	# to type content in input field
	driver.find_element_by_pro('MJsFCDe7w7YwjSt').send_keys('dress')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('kYiDxNDYXocmIrI')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('Y6mOrZwTuC1BTAq').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('EfKVqmnSBsjVSJg').get_attribute('href')
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('gFTVRNtBgZOXekO').text
	    # to fetch the text of element
	    sale price=list_element.find_element_by_pro('yTPqeNWUVBU7EU2').text
	    # to scroll down
	    
	# to click on the element(2) found
	driver.find_element_by_pro('DuMKnNE5xqrtGxY').click()
	time.sleep(3)

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
