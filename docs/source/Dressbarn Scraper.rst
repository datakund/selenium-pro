Scraper
************

Dressbarn Scraper
########################

What it does?
=============

It scrape clothes details

How it works?
=============

It open dressbarn  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://dressbarn.com/')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('x0h7vxBpyNZ86md').click()
	# to type content in input field
	driver.find_element_by_pro('eKN8oTSgrlvzRdh').send_keys('dress')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('0QtI5156MMd2G1M')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('zbV6GJgckC3enbj').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('ImGjtggf3g7UGUW').get_attribute('href')
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('OyrR2C2is0sEyrn').text
	    # to fetch the text of element
	    sale price=list_element.find_element_by_pro('bw8sibfpCiMAIYi').text
	    # to scroll down
	    
	# to click on the element(2) found
	driver.find_element_by_pro('LTvUyn6yfxwhnV9').click()
	time.sleep(3)

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
