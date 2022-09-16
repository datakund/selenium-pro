Eatcake Scraper
########################

Scraper
************

What it does?
=============

It scrapes cakes details

How it works?
=============

It open eatcake website, search for given keyword and it scrape product name, price ,link and description

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
	driver.get('https://www.eatcaketoday.com/?gclid=EAIaIQobChMI9MSQ4JuS-gIVKMIWBR2DzQT4EAAYASAAEgLJJfD_BwE')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('eVrZQC9cDU8qoJZ').click()
	# to type content in input field
	driver.find_element_by_pro('CJwHOsfEJdQDHcl').send_keys('cake')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('NVATBWNyeeCcD0o')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('LFaP5w9uQfWBEKK').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('t2h1bAJXgAuGgW6').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('8mvBsfWg7cjrPrN').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
