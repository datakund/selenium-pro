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
	driver.find_element_by_pro('CeXdmw3TEirTHdG').click()
	# to type content in input field
	driver.find_element_by_pro('PmNWC2MonGG5cMz').send_keys('shirt')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('k7CEnmqXR1aFT3E')
	for list_element in list_elements:
	    # to fetch the text of element
	    title 1=list_element.find_element_by_pro('ezEY4KFBLZ7vkHH').text
	    # to fetch the link of element
	    link1=list_element.find_element_by_pro('I46gT7tz6imRpv4').get_attribute('href')
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('q8IRZ9AcTlXiyh2').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('FZkMjsIzi3PLs3T').text
	    # to fetch the text of element
	    description 2=list_element.find_element_by_pro('YGpnl6zPQB3yqwj').text
	    # to fetch the text of element
	    title 2=list_element.find_element_by_pro('lYzdPiZuezfC4y5').text
	    # to fetch the link of element
	    link2=list_element.find_element_by_pro('Dyykl9JnBD2tGJv').get_attribute('href')

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
