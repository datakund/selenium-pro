VICI Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open vici website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.vicicollection.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('LuLbHjM9xek4VSw').click()
	# to type content in input field
	driver.find_element_by_pro('DJxmLA0QndvmsUH').send_keys('top')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('YeAhj7xcDFRaItF')
	for list_element in list_elements:
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('okdxcRYN7j9zczt').text
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('LlgIsT12ZMAwCCL').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('UCykA8uRQiGN4tj').get_attribute('href')
	    # to scroll down
	    
	# to click on the element found
	driver.find_element_by_pro('tfUBgPeS3apK87x').click()
	time.sleep(3)

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
