Gymshark UK Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open gymshark website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.gymshark.com/')
	time.sleep(3)
	# to click on the element(Search) found
	driver.find_element_by_pro('5WsZfEqSh8GLkZO').click()
	# to type content in input field
	driver.find_element_by_pro('gBCbTr9jb1OFFP0').send_keys('top')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('n79svIpHTSR4Usd')
	for list_element in list_elements:
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('wOtt1Mpi8duifiS').text
	    # to fetch the text of element
	    name=list_element.find_element_by_pro('z6UQi6WnfXtW1gZ').text
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('5FvLrNcluvU8pLH').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('shuEMD23DX6Wq8U').get_attribute('href')

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
