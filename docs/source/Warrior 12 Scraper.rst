Warrior 12 Scraper
########################

Scraper
************

What it does?
=============

It scrape clothes details

How it works?
=============

It open warrior12 website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://warrior12.com/')
	time.sleep(3)
	# to click on the element(Search) found
	driver.find_element_by_pro('OskiFwQDOhSLxD4').click()
	# to type content in input field
	driver.find_element_by_pro('bWcSyhl0mycZ6d7').send_keys('shirt')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('05oXgT7jspxl77Z')
	for list_element in list_elements:
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('dL8n9w98vu6Olur').text
	    # to fetch the text of element
	    descriiption=list_element.find_element_by_pro('UFwV6uXTBXW7Pmc').text
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('Jw1DIwcNsMVfH0i').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('exTOjoCLs845H9Z').get_attribute('href')

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
