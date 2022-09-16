Crown & Caliber Scraper
########################

Scraper
************

What it does?
=============

It scrape watch details

How it works?
=============

It open crown&calliber website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.crownandcaliber.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('cGTM85TzXepWL7Z').click()
	# to type content in input field
	driver.find_element_by_pro('DxcdGTDW1TKqRAu').send_keys('watch')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('e59nxNhXjUSOHDg')
	for list_element in list_elements:
	    # to fetch the text of element
	    title 1=list_element.find_element_by_pro('1JU0DebrC2nSgVr').text
	    # to fetch the text of element
	    title 2=list_element.find_element_by_pro('k65HaMYbtHVOYqy').text
	    # to fetch the text of element
	    title 3=list_element.find_element_by_pro('iEf43kVDFUzGLpn').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('GsgD1g9u1y35ZHM').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('IBy1gekBvjUStxL').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
