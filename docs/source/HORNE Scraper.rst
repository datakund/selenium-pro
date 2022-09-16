HORNE Scraper
########################

Scraper
************

What it does?
=============

It scrape horne details

How it works?
=============

It open horne website, search for given keyword and it scrape  title ,  link ,description

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
	driver.get('https://horne.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('1XRp6aFUTahA8uO').click()
	# to type content in input field
	driver.find_element_by_pro('0nHkN6Yyv3eMQS5').send_keys('tax')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('PJnT1lrOKGAOcEj')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('xoOrxE2OZFbnSVD').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('Jct4I1CJ7Qg79JB').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('g1AwVhblIGZhjSs').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
