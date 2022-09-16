Gymshark UK Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open gymshark website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.gymshark.com/')
	time.sleep(3)
	# to click on the element(Search) found
	driver.find_element_by_pro('DmshuIrrEGBhyzQ').click()
	# to type content in input field
	driver.find_element_by_pro('CbKyEuCQLc6fPDe').send_keys('top')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('ZYfeJKz3lQNpbv8')
	for list_element in list_elements:
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('zCiOzYuKQznTFFZ').text
	    # to fetch the text of element
	    name=list_element.find_element_by_pro('H0EHuJfMnB83ocw').text
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('iKqrhcJey8z9rWm').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('i49Na8NtiAsR1MM').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
