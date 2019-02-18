import csv
import requests 
from bs4 import BeautifulSoup
url = "http://www.pga.com/golf-courses/search?searchbox=Course+Name&searchbox_zip=ZIP&distance=50&price_range=0&course_type=both&has_events=0"
r = requests.get(url)

soup = BeautifulSoup(r.content)

g_data1=soup.find_all("div",{"class":"views-field-nothing-1"})
g_data2=soup.find_all("div",{"class":"views-field-nothing"})


for item in g_data1:
     try:
          print (item.contents[1].find_all("div",{"class":"views-field-counter"})[0].text)
     except:
          pass  
     try:
          print (item.contents[1].find_all("div",{"class":"views-field-course-type"})[0].text)
     except:
          pass

for item in g_data2:
   try:
      print (item.contents[1].find_all("div",{"class":"views-field-title"})[0].text)
   except:
      pass
   try:
      print (item.contents[1].find_all("div",{"class":"views-field-address"})[0].text)
   except:
      pass
   try:
      print (item.contents[1].find_all("div",{"class":"views-field-city-state-zip"})[0].text)
   except:
      pass
