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


Login with Cookies
===================

``Cookies not required``


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
	list_elements=driver.find_elements_by_pro('uLrtVhgBE4aqtEO')
	for list_element in list_elements:
	    # to fetch the text of element
	    user=list_element.find_element_by_pro('vMMCCSi9jhSDEkQ').text
	    # to fetch the text of element
	    Comment=list_element.find_element_by_pro('mIbla4AVARg5QXH').text
	    # to fetch the link of element
	    UserLink=list_element.find_element_by_pro('OLAVParyDfXkBEk').get_attribute('href')
	    # to fetch the text of element
	    Likes=list_element.find_element_by_pro('StVF398L4g1QVyn').text
	    # to fetch the text of element
	    Time=list_element.find_element_by_pro('bcwMf9Pm7GMt5Lh').text

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
