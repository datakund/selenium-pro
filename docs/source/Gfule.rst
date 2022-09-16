Gfule
########################

Scraper
************

What it does?
=============

It scrape juice details

How it works?
=============

It open  gfuel  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://gfuel.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('o8EUju1GcUXo7Ar').click()
	# to type content in input field
	driver.find_element_by_pro('lE7zZ3tuU0q7NYI').send_keys('ca')
	# to type content in input field
	driver.find_element_by_pro('7xEhKVz4THuwrzP').send_keys('n')
	# to type content in input field
	driver.find_element_by_pro('o3ynaEKVFfQIXnf').send_keys('s')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('hIK5WQAjU9fcNJd')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('8kM5Qf0fUuNxMv9').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('X8JvIs2mnhyl8ve').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('AiaudE2Ljri9hYq').get_attribute('href')
	    # to fetch the text of element
	    name=list_element.find_element_by_pro('ULnQJMlYPUuvadX').text

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
