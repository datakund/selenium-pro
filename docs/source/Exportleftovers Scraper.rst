Exportleftovers Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open exportleftovers website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.exportleftovers.com/')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('4VhFBEKLQDj3Ck4').click()
	# to type content in input field
	driver.find_element_by_pro('B0woAVwAZp09rVo').send_keys('shirt')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('2Z1ogpt4OfIkeDh')
	for list_element in list_elements:
	    # to fetch the text of element
	    title 1=list_element.find_element_by_pro('mNhVZCTnC1x2U34').text
	    # to fetch the link of element
	    link1=list_element.find_element_by_pro('iNzDQoNOs4dYcXW').get_attribute('href')
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('97ScGZkBQXtHASN').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('ngRyX71k4z8wvOM').text
	    # to fetch the text of element
	    description 2=list_element.find_element_by_pro('EXwfswjAy07GPY0').text
	    # to fetch the text of element
	    title 2=list_element.find_element_by_pro('Zo0TZbJcnwcAmL0').text
	    # to fetch the link of element
	    link2=list_element.find_element_by_pro('HLUyhVY1XkXucPx').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
