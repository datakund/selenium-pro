Staticnail Scraper
########################

Scraper
************

What it does?
=============

It scrape nails details

How it works?
=============

It open static nails website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://staticnails.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('FIXVCrp1zyXmiJz').click()
	# to click on input field
	driver.find_element_by_pro('L1GFvIvfxjPQzC0').click()
	# to type content in input field
	driver.find_element_by_pro('pxfSbjSg1SYal7N').send_keys('nail')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('w5wTL4cU26Mx2zt')
	for list_element in list_elements:
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('oyxXuTaKLw6jbnw').text
	    # to fetch the text of element
	    name=list_element.find_element_by_pro('oIFjQxMIKayd3qd').text
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('sqtu0sukj6xXzwg').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('Vj7r7IuwZi3Yljy').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
