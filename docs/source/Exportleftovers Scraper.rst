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
	driver.find_element_by_pro('THKWD8N400fZK0N').click()
	# to type content in input field
	driver.find_element_by_pro('Dy2aDYxTfLkjjbA').send_keys('shirt')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('Ksh4wC2qtFHT2Ok')
	for list_element in list_elements:
	    # to fetch the text of element
	    title 1=list_element.find_element_by_pro('CEGhbPofYcoTdzS').text
	    # to fetch the link of element
	    link1=list_element.find_element_by_pro('pJv6xS8Xp94xAjk').get_attribute('href')
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('GtZySE45tKKYKjB').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('vdcXtyHNqJQI8Va').text
	    # to fetch the text of element
	    description 2=list_element.find_element_by_pro('7r4BG1RxchRDKr5').text
	    # to fetch the text of element
	    title 2=list_element.find_element_by_pro('V4OehfTBPcS5QNo').text
	    # to fetch the link of element
	    link2=list_element.find_element_by_pro('fiCWLamv7YrshCi').get_attribute('href')

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
