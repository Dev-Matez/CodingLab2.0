# CodingLab2.0

#From Contacts.py import Contacts = [...]
from contacts import contacts

# Basic GUI Created Called MAIN_MENU
MAIN_MENU = """--- CONTACTS-App ---

Please, Choose One Of These Options:

1) Search-For-Contact.
2) Exit-The-Program.

Your Selection: """

# Function for each election created
def mainMenu():
    while (user_input := input(MAIN_MENU)) != "2":
        if user_input == "1":
            NumeroDUE()
        elif user_input == "2":
            NumeroUNO()
        else:
            print("Invalid Input, Please Try Agaian!")

# GUI Created for Search Menu
SEARCH_MENU = """--- SEARCH-MENU ---

Please, Choose One Of These Options:

1) Go-To-Search.
q) Go Back.

Your Selection: """

# Function for the Options
def NumeroDUE():
     while (user_input := input(SEARCH_MENU)) != "q":
        if user_input == "1":
            search()
        else:
            print("Invalid Input, Please Try Agaian!")

# Trying to Create Function for Search... .. .
def search():
    input("Enter-Search: ")
# mainMenu Function called. 
mainMenu()

# Unable to bring Dictionery Data from COntatcs.py
# Any Advice will be greatly Appreciated... .. .
# -Moeezs


