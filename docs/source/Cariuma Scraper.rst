Cariuma Scraper
########################

Scraper
************

What it does?
=============

It scrape Shoes details

How it works?
=============

It open Cariuma website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://cariuma.com/')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('DeImyDsXyRsKmLB').click()
	# to type content in input field
	driver.find_element_by_pro('LLmFOBtumaiaQPn').send_keys('shirt')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('ZSbDTYH25ptEsyk')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('Mqi8x4kS8RkRtCl').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('LInXqTojnyuJ8V7').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('TtZgcUJxyHq2TTb').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
