Windsorstore Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open windsorstore website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.windsorstore.com/pages/search?q=top')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('Zy8AzwtimrsfTYO').click()
	# to type content in input field
	driver.find_element_by_pro('1KsgUp8Ysx901BR').send_keys('top')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('rcjG8scQUPpgYGx')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('HwCXDYv5SC8Wxnh').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('BCIkgEflCrsfAHF').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('RR8iHaj9JMSHLLW').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
