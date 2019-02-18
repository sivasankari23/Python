import bs4 as bs
import urllib.request
sauce=urllib.request.urlopen("http://epaper.indianexpress.com/").read()

soup = bs.BeautifulSoup(sauce,'lxml')

print(soup.get_text())




