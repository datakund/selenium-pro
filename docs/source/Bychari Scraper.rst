Bychari Scraper
########################

Scraper
************

What it does?
=============

It scrape jewelry details

How it works?
=============

It open bychari website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://bychari.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('dZ09DhZIUEQRKRC').click()
	# to type content in input field
	driver.find_element_by_pro('Bhb4mBdWBKxvVbo').send_keys('chain')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('jlTwkxdqAZhcWEU')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('9LgEkKLQ07V6rFd').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('7PEBfh4sqXyQKog').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('gUql4ad3cQiIo8P').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
