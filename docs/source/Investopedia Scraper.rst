Investopedia Scraper
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
	driver.find_element_by_pro('jHuK1rFQxEx6zm7').click_pro()
	# to type content in input field
	driver.find_element_by_pro('f0sX8KeKFQMqFTt').type('call')
	# press Enter key
	driver.switch_to.active_element.type('Enter')
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('tCyIPzG3jabaDHx')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('V0eQmkkiFNTvdgW').text
	    # to fetch the text of element
	    description=list_element.find_element_by_pro('5A9q3u2zLwxU2zv').text
	    # to fetch the text of element
	    name=list_element.find_element_by_pro('M9ztqXdL8JhgDQC').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('y6NPtKC6hrJQH5a').get_attribute('href')

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
