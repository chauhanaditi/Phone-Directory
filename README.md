# Phone-Directory
A phone directory application implemented in C using Trie data structures.
The project supports efficient storage and fast prefix-based search of contacts by name and phone number, using two separate tries.  
  
__Features__  
->Add new contacts (name + 10-digit number)  
->Search contacts:  
->by name (using Name Trie)  
->by number (using Number Trie)  
->Display all contacts in lexicographic order  
->Delete contacts (name or number)  
->Input validation for names, spaces, and digits  
->File-based initialization from sample_data.txt  
  
__Data Structures Used__  
__1. Name Trie__  
Supports lowercase letters + spaces (27 children per node)  
Stores names and maps them to phone numbers  
Enables prefix-based search  
Efficient lexicographic printing  
  
__2. Number Trie__  
Stores digits 0–9 (10 children per node)  
Maps phone numbers to names  
Provides fast numeric search  
Supports deletion with node cleanup  

__How to Run__  
gcc main.c -o phone_directory  
./phone_directory  

__How It Works__  
The program loads initial contacts from sample_data.txt.  

Each contact is inserted into:  
Name Trie (key = name, value = number)  
Number Trie (key = number, value = name)  
Users can interact through a menu-driven interface:  
Add new contact  
Search contact  
Display all contacts  
Delete contact  
Exit  
