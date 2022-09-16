Youtube video comments
########################

Youtube
************

What it does?
=============

It scrapes youtub video comments

How it works?
=============

It opens youtube and searches for the keyword given and scrapes comments of the particular video

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
	from selenium_pro.webdriver.common.keys import Keys
	import time
	driver = webdriver.Start()
	# press pagedown key
	driver.switch_to.active_element.send_keys(Keys.PAGE_DOWN)
	time.sleep(3)
	# press pagedown key
	driver.switch_to.active_element.send_keys(Keys.PAGE_DOWN)
	time.sleep(1)
	# press pagedown key
	driver.switch_to.active_element.send_keys(Keys.PAGE_DOWN)
	time.sleep(1)
	list_elements=driver.find_elements_by_pro('qmNXZG67h4iAhXj')
	for list_element in list_elements:
	    # to fetch the text of element
	    user=list_element.find_element_by_pro('yr3bFC3RKDFANr8').text
	    # to fetch the text of element
	    Comment=list_element.find_element_by_pro('5bKe84vJGgeBJjR').text
	    # to fetch the link of element
	    UserLink=list_element.find_element_by_pro('cCLsRV97pLZT3sI').get_attribute('href')
	    # to fetch the text of element
	    Likes=list_element.find_element_by_pro('3GDs5JtGDxVCdSj').text
	    # to fetch the text of element
	    Time=list_element.find_element_by_pro('OSS6XE2sL0Dr0Zy').text

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
