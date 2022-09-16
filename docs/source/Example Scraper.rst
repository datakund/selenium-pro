Example Scraper
########################

Scraper
************

What it does?
=============

It scrape invest details

How it works?
=============

It open investopedia website, search for given keyword, and scrape title ,link ,description

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
	driver.get('https://www.investopedia.com/terms/c/calloption.asp')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('yyjQJLJxNVkYrTg').click()
	# to type content in input field
	driver.find_element_by_pro('RMi6EeZHSs3NAnY').send_keys('call')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('qROC72OjMbCMpHw')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('TWGK9fUiKAIgCQq').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('dna284SOhDHAorL').text
	    # to fetch the text of element
	    name=list_element.find_element_by_pro('NwIB1kJ9GS4SCZb').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('edFDwKXv61Lwe52').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
