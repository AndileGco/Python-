# Python-
Library System 
# Library Book and Member Management System (LBMMS)

## Overview
The Library Book and Member Management System (LBMMS) is a Python-based desktop application designed to manage a library's core operations efficiently. It provides a user-friendly Graphical User Interface (GUI) built with `tkinter` and uses a lightweight SQLite database for persistent data storage[cite: 3, 5]. This project was developed as the SSX361 Project[cite: 5].

## Features
The application is split into two main modules: Book Management and Member Management.

### 📚 Book Management
* **Add new books:** Record a book's ISBN, Title, Author, Genre, and Availability status[cite: 1, 2].
* **Update book details:** Modify existing records in the database[cite: 1].
* **Delete books:** Remove books from the system securely with a confirmation prompt[cite: 1].
* **Search and View:** View all books in a structured table (Treeview) or search for specific books using keywords (Title, Author, ISBN, or Genre)[cite: 1, 2].

### 👥 Member Management
* **Register members:** Add members using their Membership ID, Name, Contact Info, and Membership Type (Student, Senior, Staff)[cite: 6, 7].
* **Update member details:** Edit existing member profiles[cite: 7].
* **Remove members:** Delete members from the system via their Membership ID[cite: 7].
* **Search and View:** View all registered members or search for them by Name, Membership ID, or Contact[cite: 6, 7].

## Project Structure
The source code is organized into distinct classes to separate the GUI code from database logic:

* **`main.py`** (Entry Point): Contains the `LibraryManagementSystem` class which acts as the main dashboard to navigate to the Books or Members interfaces[cite: 5].
* **`Database.py`**: Contains the `Database` class responsible for initializing the SQLite database (`library.db`) and ensuring the `Books` and `Members` tables exist[cite: 3].
* **`Books.py`**: Contains the `BooksCRUD` class that handles all SQL database interactions (Create, Read, Update, Delete, Search) specifically for books[cite: 1].
* **`Books_window.py`**: Contains the `BooksWindow` class that renders the Tkinter GUI for book operations[cite: 2].
* **`Memebers.py`**: Contains the `MembersCRUD` class that handles all SQL database interactions for members[cite: 7].
* **`Members_window.py`**: Contains the `MembersWindow` class that renders the Tkinter GUI for member operations[cite: 6].
* **`library.db`**: The SQLite database file automatically generated to store application data[cite: 3, 4].

## Prerequisites
To run this application, you must have the following installed:
* Python 3.x
* The `tkinter` library (usually comes pre-installed with standard Python distributions)
* The `sqlite3` library (built-in Python module)

## How to Run
1. Ensure all the python scripts (`Database.py`, `Books.py`, `Books_window.py`, `Memebers.py`, `Members_window.py`, and the main file) are in the same directory.
2. Open your terminal or command prompt.
3. Navigate to the project directory.
4. Run the main application script:
   ```bash
   python main.py
