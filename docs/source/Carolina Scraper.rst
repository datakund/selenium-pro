Carolina Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open carolina website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://shopcarolinagirls.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('hNQj1YHg7tKfn6S').click()
	# to type content in input field
	driver.find_element_by_pro('3PRAXXhCBda1MsD').send_keys('bag')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('Fcivoz9aAgW7xFp')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('Tg8YXehTkX4JDYG').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('cFKEhQm5nSFndId').get_attribute('href')
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('NlvOqUglJnEgr9F').text
	    # to scroll down
	    
	# to click on the element found
	driver.find_element_by_pro('AckrDRGoeaIwhse').click()
	time.sleep(3)

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
