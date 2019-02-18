import time

# Register
def register():
    while True:
        username = input("New username: ")
        if not len(username) > 0:
            print("Username can't be blank")
            continue
        else:
            file = open("Login.txt","a")
            file.write (username)
            file.write (",")
            file.close()
            break
    while True:
        password = input("New password: ")
        if not len(password) > 0:
            print("Password can't be blank")
            continue
        else:
            file = open("Login.txt","a")
            file.write (password)
            file.write("\n")
            file.close()
            break
    print("Creating account...")
    print("Account has been created")


# Login
def login():
    logged_in = False
    with open('Login.txt', 'r') as file:
        supplied_username = input("Username: ")
        supplied_password = input("Password: ")
        for line in file:
            username, password = line.split('\n')
            if username == supplied_username:
                logged_in = password == supplied_password
                break
    if logged_in:
        print("Sucess")
    else:
        print("Failed")
    
# On start
print("Welcome to the system. Please register or login.")
print("Options: register | login | exit")
while True:
    option = input("> ")
    if option == "login":
        login()
    elif option == "register":
        register()
    elif option == "exit":
        break
    else:
        print(option + " is not an option")

# On exit
print("Shutting down...")
time.sleep(1)
