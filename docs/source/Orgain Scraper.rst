Orgain Scraper
########################

Scraper
************

What it does?
=============

It scrape Shake details

How it works?
=============

It open orgain  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://orgain.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('e5U7RtQIyOjGZoX').click()
	# to type content in input field
	driver.find_element_by_pro('MyR2a8OxD24q3HV').send_keys('shake')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('SlfR5bMUOOgjrDn')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('7SIZaGolHsTnipX').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('eyW33pm2sS8KHgV').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('bDIgIjCW1k35RMC').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
