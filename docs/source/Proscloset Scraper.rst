Proscloset Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open proscloset website, search for given keyword and it scrape product name, link ,price

Import
=============

``from selenium_pro import webdriver``


Start Browser
=============

``driver=webdriver.Start()``


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
	driver.get('https://www.theproscloset.com/')
	time.sleep(3)
	# to click on the element(Search) found
	driver.find_element_by_pro('CLKVMzhzvrKybb7').click()
	# to type content in input field
	driver.find_element_by_pro('geq7QP888IIPRpV').send_keys('bike')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('Jv3OTA2L5TrJIVU')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('Q2CU1h5tJk88M10').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('d3CQAxXB5td2sDq').get_attribute('href')
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('2XB3MS2CqMs01UZ').text
	    # to scroll down
	    
	# to click on the element(») found
	driver.find_element_by_pro('wXojWPyj204ALFa').click()
	time.sleep(3)

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
