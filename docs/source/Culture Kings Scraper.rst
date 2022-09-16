Culture Kings Scraper
########################

Scraper
************

What it does?
=============

It scrape shoes details

How it works?
=============

It open culture website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.culturekings.com.au/')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('dhgT500dBO2Lqxn').click()
	# to type content in input field
	driver.find_element_by_pro('OKoqlBj85yOvdJs').send_keys('nike')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('eq1MF3BvlH4wcl3')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('e4kWp3FAqbI1fHl').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('rlvBI69TsWbXaTF').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('gocD77wMm3zkCme').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
