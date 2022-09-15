Scraper
************

Tomboy Scraper
########################

What it does?
=============

It scrape clothes details

How it works?
=============

It open tomboy website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://tomboyx.com/?irclickid=yqSR%3AozWAxyNTpPzoKRIEQ4NUkDWg9xKTQRL3c0&utm_source=impact&utm_medium=affiliate&utm_campaign=Cloudtraffic&utm_content=631f3014dee98500010966c1&utm_term=2031198&irgwc=1&ir_partnerid=2031198&ir_adid=1162522&ir_campaignid=14705')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('cmplDTA9lL0C17s').click()
	# to type content in input field
	driver.find_element_by_pro('3DjoIy0csYpEDii').send_keys('swim')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('wbeaRsRWg4fwjFX')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('krevwjHHUTKA6ur').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('5XUBXRffIYyxjWe').get_attribute('href')
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('h3A7s27lXZvzsCF').text
	    # to scroll down
	    
	# to click on the element(2) found
	driver.find_element_by_pro('yly4RDy8spbFcE6').click()
	time.sleep(3)

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
