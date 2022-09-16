Example Scraper
########################

Scraper
************

What it does?
=============

It scrape invest details

How it works?
=============

It open investopedia website, search for given keyword, and scrape title ,link ,description

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
	driver.get('https://www.investopedia.com/terms/c/calloption.asp')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('P7uwdAE7rMUzaYG').click()
	# to type content in input field
	driver.find_element_by_pro('BXVRWl1kuBjnc2B').send_keys('call')
	# press Enter key
	driver.switch_to.active_element.send_keys(Keys.ENTER)
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('N4skWRvXJwsfSJd')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('xwF1r5xCht7iIpi').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('oBBO9gHH9wFFDxp').text
	    # to fetch the text of element
	    name=list_element.find_element_by_pro('usWqWaOTAaY0unt').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('5ph6MkNn8V9QV1a').get_attribute('href')

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
