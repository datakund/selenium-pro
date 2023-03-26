BlendJet Scraper
########################

Scraper
************

What it does?
=============

It scrape blendjet details

How it works?
=============

It open  blendjet website, search for given keyword and it scrape product name, link ,price

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
	driver.get('https://blendjet.com/products/blendjet-2?nbt=nb%3Aadwords%3Ag%3A1672565746%3A68558248287%3A579821569157&nb_adtype=&nb_kwd=blendjet&nb_ti=kwd-549197371663&nb_mi=&nb_pc=&nb_pi=&nb_ppi=&nb_placement=&nb_si=%7Bsourceid%7D&nb_li_ms=&nb_lp_ms=&nb_fii=&nb_ap=&nb_mt=e&gclid=EAIaIQobChMI96bwybyW-gIV0lVgCh2GBAqXEAAYASAAEgIwO_D_BwE&variant=32478639390786')
	time.sleep(3)
	# to click on the element found
	driver.find_element_by_pro('43HCaWHwcwS8YEa').click_pro()
	# to click on input field
	driver.find_element_by_pro('3m9dvDAnAhJIJ1s').click_pro()
	# to type content in input field
	driver.find_element_by_pro('4D3zuEpGtXBU9U2').type('jet')
	# press Enter key
	driver.switch_to.active_element.type('Enter')
	time.sleep(3)
	list_elements=driver.find_elements_by_pro('psx4tdGv172ZqLM')
	for list_element in list_elements:
	    # to fetch the text of element
	    title=list_element.find_element_by_pro('dXoytRTdUqWU309').text
	    # to fetch the text of element
	    price=list_element.find_element_by_pro('o3Qcx4PV4WNLpgA').text
	    # to fetch the text of element
	    review=list_element.find_element_by_pro('bePoBAcYayWI9gG').text
	    # to fetch the link of element
	    link=list_element.find_element_by_pro('dvinZDCBJrwElMB').get_attribute('href')

Selenium pro
==============

Selenium pro is intelligent & powerful cloud native selenium.
You dont need to inspect HTML to deal with xapth,css,id etc.
All of that is done under the hood
Just use Selenium Code Generator extension to get code written automatically for you
Selenium Pro (Link to library)
Selenium Pro Auto Code Generator (Link to chrome extension)
