# Inverted Search in C

An efficient **Inverted Search Engine** implemented in **C** using **Hash Tables** and **Linked Lists**. The application indexes words from multiple text files, enabling fast keyword-based searches by storing each word along with the files in which it appears and its frequency.

---

## Overview

An **Inverted Index** is a fundamental data structure used by search engines to perform fast and efficient text searches. Instead of scanning every file for each search query, the application creates an index that maps each unique word to the files containing that word and records the number of occurrences.

This project demonstrates core concepts of **data structures**, **file handling**, **hashing**, and **dynamic memory management** through a menu-driven command-line application.

---

## Features

* Create an inverted index from multiple text files
* Display the complete indexed database
* Search for any word in the database
* Update the database with new files
* Save the database to a backup file
* Efficient hashing for faster search operations
* Dynamic memory allocation using linked lists
* Modular and maintainable C implementation

---

## Technologies Used

| Category             | Technology                                                                |
| -------------------- | ------------------------------------------------------------------------- |
| Programming Language | C                                                                         |
| Compiler             | GCC                                                                       |
| Platform             | Linux / Unix                                                              |
| Data Structures      | Hash Table, Linked List                                                   |
| Concepts             | File Handling, Dynamic Memory Allocation, Hashing, Command-Line Arguments |

---

## Project Structure

```text
INVERTED-SEARCH/
├── main.c
├── create_db.c
├── display_db.c
├── search_db.c
├── update_db.c
├── save_db.c
├── file_list.c
├── common.c
├── colors.h
├── main.h
├── file1.txt
├── file2.txt
├── Makefile
└── README.md
```

---

## Working Principle

The application reads one or more text files and creates an **inverted index**.

For every unique word encountered:

* The word is hashed into an index.
* A main node is created if the word is new.
* A linked list stores the filenames where the word appears.
* The occurrence count for each file is maintained.

This structure enables searching for words in nearly constant time without scanning every file repeatedly.

---

## Operations

### 1. Create Database

Creates the inverted index by reading all input text files.

**Functionality**

* Reads each file passed through the command line.
* Extracts individual words.
* Stores unique words in a hash table.
* Maintains:

  * Word
  * Number of files containing the word
  * File names
  * Occurrence count

---

### 2. Display Database

Displays the complete inverted index in a structured format.

**Information Displayed**

* Hash Index
* Indexed Word
* Number of Files
* File Names
* Word Frequency

---

### 3. Search Database

Searches for a user-specified word in the database.

If the word exists, the application displays:

* Word searched
* File names containing the word
* Number of occurrences in each file

If the word does not exist, an appropriate message is displayed.

---

### 4. Update Database

Updates the existing database by adding one or more new text files.

Instead of recreating the entire database, only the new files are processed and merged into the existing inverted index.

---

### 5. Save Database

Stores the current database into a backup file.

The saved database can later be restored without rebuilding the entire index from the original text files.

---

## Build Instructions

Clone the repository:

```bash
git clone https://github.com/Shrinidhi-Khanchanale/INVERTED-SEARCH.git
cd INVERTED-SEARCH
```

Compile the project:

```bash
gcc *.c -o inverted_search
```

Or, if a Makefile is available:

```bash
make
```

---

## Usage

Run the application by providing input text files as command-line arguments.

```bash
./inverted_search file1.txt file2.txt file3.txt
```

---

## Sample Menu

```text
----------- Inverted Search -----------

1. Create Database
2. Display Database
3. Search Database
4. Update Database
5. Save Database
6. Exit

Enter your choice:
```

---

## Sample Search Output

```text
Enter the word to search: embedded

Word Found!

Word           : embedded
Files          : file1.txt, file2.txt
Occurrences    : 5, 3
```

---

## Data Structures Used

* Hash Table
* Singly Linked List
* Dynamic Memory Allocation

---

## Concepts Demonstrated

* Hashing
* Inverted Indexing
* File Handling
* Linked Lists
* Dynamic Memory Allocation
* String Manipulation
* Command-Line Argument Processing
* Modular Programming
* Searching Algorithms

---

## Learning Outcomes

This project provided practical experience in:

* Designing efficient search data structures
* Implementing hash tables using linked lists
* Processing multiple text files
* Managing dynamic memory
* Developing modular applications in C
* Optimizing search performance using indexing

---

## Future Enhancements

* Case-insensitive searching
* Phrase-based searching
* Wildcard and prefix search
* Stop-word filtering
* Stemming and lemmatization
* Export database in JSON or CSV format
* Graphical User Interface (GUI)

---

## Author

**Shrinidhi Khanchanale**

Embedded Systems Trainee | C Programmer | IoT & Embedded Systems Enthusiast

GitHub: https://github.com/Shrinidhi-Khanchanale

---

## License

This project is intended for educational purposes and demonstrates the implementation of an inverted indexing system using C, hash tables, and linked lists.
