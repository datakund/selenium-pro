Staticnail Scraper
########################

Scraper
************

What it does?
=============

It scrape nails details

How it works?
=============

It open static nails website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://staticnails.com/')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('APdoovuEIqhoc4K').click()
	# to click on input field
	driver.find_element_by_pro('C1WiMYfgJ6V7ZF2').click()
	# to type content in input field
	driver.find_element_by_pro('RUVYHkcm1yeP6ts').send_keys('nail')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('QxK5Es6vyz6XWhw')
	for list_element in list_elements:
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('gRJUotst0bsEjBf').text
	    # to fetch the text of element
	    name=list_element.find_element_by_pro('88ziMjV8u0EoPZS').text
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('CkMqR3Qezbo9qzZ').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('whQPDXzEAs7Ic67').get_attribute('href')

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
