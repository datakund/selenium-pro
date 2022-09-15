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
list_elements=driver.find_elements_by_pro('z330PuqyGbQxXNL')
for list_element in list_elements:
    # to fetch the text of element
    user=list_element.find_element_by_pro('hHhlSlGAJ2tYNaG').text
    # to fetch the text of element
    Comment=list_element.find_element_by_pro('fMZPRW4c7D2arOX').text
    # to fetch the link of element
    UserLink=list_element.find_element_by_pro('J4TBSmMjmk8rzk6').get_attribute('href')
    # to fetch the text of element
    Likes=list_element.find_element_by_pro('b8knqeA3nLLh9DA').text
    # to fetch the text of element
    Time=list_element.find_element_by_pro('Fm1OifOe4RoHScj').text

Selenium pro
==============

selenium-pro is advanced version on selenium which does not require any html elements
