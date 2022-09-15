Youtube
************

Youtube video comments
########################

What it does?
=============

it scrapes youtube comments

How it works?
=============

it opens youtube and scrapes all the comments available for a video

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
		list_elements=driver.find_elements_by_pro('acg8z4J5iWFPfJX')
		for list_element in list_elements:
		    # to fetch the text of element
		    user=list_element.find_element_by_pro('Mnh3LdrbYjGLVte').text
		    # to fetch the text of element
		    Comment=list_element.find_element_by_pro('Cm0BE826u7EJ3cn').text
		    # to fetch the link of element
		    UserLink=list_element.find_element_by_pro('g9bDq3vcRSUIUnc').get_attribute('href')
		    # to fetch the text of element
		    Likes=list_element.find_element_by_pro('ka3dNtFw4C8vxMA').text
		    # to fetch the text of element
		    Time=list_element.find_element_by_pro('6S298GBV7B3uIDU').text

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
