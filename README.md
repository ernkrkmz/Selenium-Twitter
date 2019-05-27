# Selenium-Twitter

# Selenium twitter Like Bot

# !!!!!!!!!!!!!!!!!!!
# USE python IDE 
# !!!!!!!!!!!!!!!!!!!

# CODE...
import time
import random
import login
from selenium import webdriver

browser = webdriver.Firefox()
url = "https://twitter.com/"
browser.get(url)
time.sleep(2)

giris_yap = browser.find_element_by_xpath("//*[@id='doc']/div/div[1]/div[1]/div[2]/div[2]/div/a[2]")
giris_yap.click()
time.sleep(3)

username = browser.find_element_by_xpath("/html/body/div[1]/div[2]/div/div/div[1]/form/fieldset/div[1]/input")
password = browser.find_element_by_xpath("/html/body/div[1]/div[2]/div/div/div[1]/form/fieldset/div[2]/input")

# Write here your username and password
username.send_keys(***)
password.send_keys(***)


giris_yap = browser.find_element_by_xpath("//*[@id='page-container']/div/div[1]/form/div[2]/button")
giris_yap.click()

# Write here twitter url who you want
browser.get("https://twitter.com/***")

# Scroll Code (javascript)
lenOfPage = browser.execute_script("window.scrollTo(0, document.body.scrollHeight);var lenOfPage=document.body.scrollHeight;return lenOfPage;")
match=False
while(match==False):
    lastCount = lenOfPage
    time.sleep(3)
    lenOfPage = browser.execute_script("window.scrollTo(0, document.body.scrollHeight);var lenOfPage=document.body.scrollHeight;return lenOfPage;")
    if lastCount==lenOfPage:
        match=True
time.sleep(2)

#***************IF you want like Open it
elements  = browser.find_elements_by_css_selector(".ProfileTweet-actionButton.js-actionButton.js-actionFavorite")

#*****************DONT OPEN BOTH

#***************if you want bring back like Open it
#elements  = browser.find_elements_by_css_selector(".ProfileTweet-actionButtonUndo.ProfileTweet-action--unfavorite.u-linkClean.js-actionButton.js-actionFavorite")



time.sleep(2)
for element in elements:
    try:
        element.click()
    except Exception:
        print("OK")



#scrollCounter = 0
#while scrollCounter <= 5:
    #browser.execute_script("window.scrollTo(0, document.body.scrollHeight);")
    #scrollCounter += 1
    #time.sleep(2)

time.sleep(10)

browser.close()

