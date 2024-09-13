Overview  

This project, Assistant Bot Address Book, is a simple command-line utility for managing contacts with phone numbers and birthdays. 
It allows users to add, edit, and retrieve contact information, including upcoming birthday notifications. The data is persisted using a pickle-based storage system.

Features  
-Add Contacts: Add contacts with a name and phone number.  
-Edit Phone Numbers: Update an existing phone number for a contact.  
-Show Contact: Display the contact's name and phone number(s).  
-Add Birthdays: Store and manage birthdays for contacts.  
-Show Upcoming Birthdays: Retrieve a list of upcoming birthdays within the next 7 days.  
-Save and Load Data: Persist and retrieve data from a .pkl file.  

Commands  
-add [name] [phone]: Adds a new contact with the specified phone number.  
-change [name] [old_phone] [new_phone]: Updates the old phone number with a new one for a given contact.  
-phone [name]: Shows the phone number(s) of the specified contact.  
-all: Displays all contacts with their phone numbers.  
-add-bd [name] [birthday]: Adds a birthday to a contact. Format: DD.MM.YYYY.  
-show-birthday [name]: Shows the birthday of the specified contact.  
-birthdays: Displays contacts with birthdays occurring in the next 7 days.  
-close or exit: Saves the data and exits the program.  

Exception Handling  
The program handles various input errors gracefully using decorators:  
-Invalid phone numbers (must be 10 digits).  
-Invalid date format for birthdays (must be in DD.MM.YYYY format).  
-Missing or incorrect arguments for commands.  

Data Persistence  
The contact data is saved and loaded from a file named addressbook.pkl using the pickle module.  
-save_data(book, filename): Saves the current state of the address book.  
-load_data(filename): Loads the address book from the specified file. If no file exists, a new address book is created.  
