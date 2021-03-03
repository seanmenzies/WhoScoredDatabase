# WhoScoredDatabase
Searchable desktop app uing data scraped from whoscored.com

# from selenium import webdriver
# from selenium.webdriver.common.keys import Keys
import requests
from bs4 import BeautifulSoup
# PATH = "C:\Program Files (x86)\chromedriver.exe"
# driver = webdriver.Chrome(PATH)

source = requests.get("https://www.whoscored.com/Regions/81/Tournaments/3/Seasons/8279/Stages/18762/PlayerStatistics/Germany-Bundesliga-2020-2021")
soup = BeautifulSoup(source.text, "lxml")

search = soup.find_all("tbody", id="player-table-statistics-body")
print(soup)

# class Player:
#
#     def __init__(self, name, club, age, position, apps, mins, goals, assists, yel, red,
#                 SpG, PS, AerialsWon, MotM, Rating):
#         self.name = name
#         self.club = club
#         self.age = age
#         self.position = position
#         self.apps = apps
#         self.mins = mins
#         self.goals = goals
#         self.assists = assists
#         self.yel = yel
#         self.red = red
#         self.SpG = SpG
#         self.PS = PS
#         self.AerialsWon = AerialsWon
#         self.MotM = MotM
#         self.Rating = Rating
#
#     def name(self):
#         return self.name()

# driver.get("www.google.co.uk")  # opens up website
# driver.close()  # closes current tab
# driver.quit()  # closes all of Chrome
#
# driver.title()  # saves webpage title as an object
# driver.page_source  # access the whole source code
