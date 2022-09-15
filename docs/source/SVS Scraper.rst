Scraper
************

SVS Scraper
########################

What it does?
=============

It scrape speaker details

How it works?
=============

It open svs  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.svsound.com/')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('5xT4JQDXuMb3Z1E').click()
	# to type content in input field
	driver.find_element_by_pro('2moaUh4ZbEOb8EH').send_keys('speaker')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('2y8ZGITedjBqaIL')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('JfSSeJWNorx8ctO').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('vCpWFresX49ZXY6').get_attribute('href')
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('QfjJygY7pfeHdTz').text

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
