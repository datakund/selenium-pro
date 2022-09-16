Eatcake Scraper
########################

Scraper
************

What it does?
=============

It scrapes cakes details

How it works?
=============

It open eatcake website, search for given keyword and it scrape product name, price ,link and description

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
	driver.get('https://www.eatcaketoday.com/?gclid=EAIaIQobChMI9MSQ4JuS-gIVKMIWBR2DzQT4EAAYASAAEgLJJfD_BwE')
	time.sleep(3)
	# to click on input field
	driver.find_element_by_pro('vn9S9uAv2TAygcG').click()
	# to type content in input field
	driver.find_element_by_pro('tP0wyaGckkt3wJV').send_keys('cake')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('NPXpQizvFWO9RI6')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('QWeEKi3k3CEMFpu').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('uzJJavf8g4TVXHv').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('9a1D2kYSPLyzM8j').get_attribute('href')

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
