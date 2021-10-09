# CodingLab2.0
We Create Future... .. .
#the contacts list
from contacts import contacts

#Creating a simple menu called MAIN_MENU to navigate through other menus for each table[ARTIST, ALBUM, SONG & GENRE]& quit.
MAIN_MENU = """--- Contacts_App ---

Please, Choose One Of These Options:

1) Search.
2) quit.


Your Selection: """

#Actual Interactive mainMenu
def mainMenu():
    connection = contacts.connect()
    database.contacts(connection)

    while (user_input := input(MAIN_MENU)) != "q":
        if user_input == "1":
            search()
        elif user_input == "2":
            leave()
        else:
            print("Invalid Input, Please Try Agaian!")

search = """--- Search ---

Please, Choose One Of These Options:

1) Search for an Employee.
q) Go Back.

Your Selection: """

def mainSearch():
    connection = contacts.connect()
    database.contacts(connection)          

    while (user_input := input(search)) != "q":
        if user_input == "1":
            prompt_add_new_artist(connection)
        else:
            print("Invalid Input, Please Try Agaian!")


def prompt_add_new_artist(connection):
    name = input("Enter Artist Name: ")
    age = int(input("Enter Artist Age: "))
    nationality = input("Enter Artist Nationality: ")
    gender = input("Enter Artist Gender: ")

    database.add_artist(connection, name, age, nationality, gender)

mainMenu()
