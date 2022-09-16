Skims Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open Skims website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://www.net-a-porter.com/en-in/shop/designer/skims?cm_mmc=GoogleIN--c-_-NAP_EN_IN-_-NAP%20-%20APAC%20-%20TIER%202%20-%20By%20Designer%20-%20Alone%20-%20Skims%20-%20IKC%20-%20(full%20price)--APAC%20-%20EN%20-%20TIER%202%20-%20By%20Designer%20-%20Alone%20-%20Skims_exact-_-skims_e_kwd-298437942148_APAC&gclid=EAIaIQobChMI656DvLiW-gIVZZhmAh26XA8fEAAYASAAEgICAvD_BwE&gclsrc=aw.ds')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('yq3a9kw3z6uqqRq').click()
	# to type content in input field
	driver.find_element_by_pro('OxZsJ1W0j5IG73t').send_keys('jeans')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('5ib2c1aghDnStFa')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('apiX3ZAx6YCCiKR').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('ewOVQgPhObYOt5g').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('IQW60YTgeqS90mb').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('Z8k5WnJPasF0CPR').get_attribute('href')

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
