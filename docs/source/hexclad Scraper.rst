hexclad Scraper
########################

Scraper
************

What it does?
=============

It scrape cookware details

How it works?
=============

It open  hexclad  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://hexclad.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('Mn7rWJx2gvrbAl6').click()
	# to click on input field
	driver.find_element_by_pro('YPW5X5u8HUF2oN9').click()
	# to type content in input field
	driver.find_element_by_pro('D2U7VQpnyqxEUAd').send_keys('bowl')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('lbuhKfzxDy9AVvY')
	for list_element in list_elements:
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('JwWGamMWCu7qE0y').text
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('ZXJ4LVAQtvcHGjm').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('FlG3NPEBWkfteQi').get_attribute('href')

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
