import time
import bs4 as bs
import urllib.request
import requests
# All accounts
users = {
    "root": {
        "password": "gucci-mane",
        "group": "admin",
        "mail": []
    }
}

# Form validation
def validate(form):
    if len(form) > 0:
        return False
    return True

# Login authorization
def loginauth(username, password):
    if username in users:
        if password == users[username]["password"]:
            print("Login successful")
            return True
    return False

# Login
def login():
    while True:
        username = input("Username: ")
        if not len(username) > 0:
            print("Username can't be blank")
        else:
            break
    while True:
        password = input("Password: ")
        if not len(password) > 0:
            print("Password can't be blank")
        else:
            break

    if loginauth(username, password):
        rl=input("Which news paper u want to scrap \n1.THE HINDU\n2.THE INDIAN EXPRESS\n3.GOOGLE NEWS\nEnter your choice:")
        if rl == "1":
            lang=input("Choose in which state the news-paper is to be scraped \n1.SOUTH\n2.NORTH\nEnter ur choice:");
            if lang == "1":
                res = requests.get('http://www.thehindu.com/todays-paper/tp-national/tp-tamilnadu/')
                res.raise_for_status()
                playFile = open('RomeoAndJuliet.txt', 'wb')
                for chunk in res.iter_content(100000):
                    playFile.write(chunk)
                playFile.close()
            if lang == "2":
                sauce=urllib.request.urlopen("http://www.thehindu.com/news/cities/Delhi/").read()
                soup = bs.BeautifulSoup(sauce,'lxml')
                print(soup)
        elif rl == "2":
            lang=input("Choose in which language the news-paper is to be scraped \n1.SOUTH\n2.NORTH\nEnter ur choice:");
            if lang == "1":
                sauce=urllib.request.urlopen("http://indianexpress.com/about/south-india/").read()
                soup = bs.BeautifulSoup(sauce,'lxml')
                print(soup)
            if lang == "2":
                sauce=urllib.request.urlopen("http://indianexpress.com/").read()
                soup = bs.BeautifulSoup(sauce,'lxml')
                print(soup)
        elif rl == "3":
            lang=input("Choose in which language the news-paper is to be scraped \n1.SOUTH\n2.NORTH\nEnter ur choice:");
            if lang == "1":
                sauce=urllib.request.urlopen("http://www.thehindu.com/todays-paper/tp-national/tp-tamilnadu/").read()
                soup = bs.BeautifulSoup(sauce,'lxml')
                print(soup)
            if lang == "2":
                sauce=urllib.request.urlopen("https://news.google.com/news/?gl=US&ned=us&hl=en").read()
                soup = bs.BeautifulSoup(sauce,'lxml')
                print(soup)
    else:
        print("Invalid username or password")

# Register
def register():
    while True:
        username = input("New username: ")
        if not len(username) > 0:
            print("Username can't be blank")
            continue
        else:
            break
    while True:
        password = input("New password: ")
        if not len(password) > 0:
            print("Password can't be blank")
            continue
        else:
            break
    print("Creating account...")
    users[username] = {}
    users[username]["password"] = password
    users[username]["group"] = "user"
    users[username]["mail"] = []
    time.sleep(1)
    print("Account has been created")

# On start
print("\n\t\t\tWelcome to the system.\n\n \t\tPlease register or login.\n")
print("\n\t\t\tOptions:\n\t\t\t1.REGISTER\n\t\t\t2.LOGIN\n\t\t\t3.EXIT\n\t\t\tEnter ur choice:")
while True:
    option = input("> ")
    if option == "2":
        login()
    elif option == "1":
        register()
    elif option == "3":
        break
    else:
        print(option + " is not an option")

# On exit
print("Shutting down...")
time.sleep(1)
