Scraper
************

Mistore Scraper
########################

What it does?
=============

It scrape watch details

How it works?
=============

It open mistore website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://mistore.pk/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('1GlarpudQXDNKNo').click()
	# to type content in input field
	driver.find_element_by_pro('Vh1jGDvIRqxA22B').send_keys('phone')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('fy0LAicDcrNfo1t')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('WqKr8SCxLe32bMC').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('w1F292KGxICBpxg').get_attribute('href')
	    # to fetch the text of element
	    price 1=list_element.find_element_by_pro('P0Djj0f4bK53yeg').text
	    # to fetch the text of element
	    price 2=list_element.find_element_by_pro('TqMOIlt5ANzq9OT').text
	    # to scroll down

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
