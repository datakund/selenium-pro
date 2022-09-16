Gfule
########################

Scraper
************

What it does?
=============

It scrape juice details

How it works?
=============

It open  gfuel  website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://gfuel.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('7L1fZukxzCdBJCn').click()
	# to type content in input field
	driver.find_element_by_pro('7gTBQcyKhuNfFJe').send_keys('ca')
	# to type content in input field
	driver.find_element_by_pro('krZuPLPqiF717nh').send_keys('n')
	# to type content in input field
	driver.find_element_by_pro('7CYRrxqw8CKM2g4').send_keys('s')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('iknrdZF0MSbxPkA')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('or12RGN3I3WjXtc').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('dgExZN3t6Y4a9KA').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('jk9QVORlg5IIbGT').get_attribute('href')
	    # to fetch the text of element
	    name=list_element.find_element_by_pro('hMHH0fWJ9WhiWNc').text

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
