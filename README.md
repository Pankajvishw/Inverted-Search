```markdown
# 🔍 Inverted Search Project (C)

## 📘 Overview
The **Inverted Search Project** is a C-based text indexing and searching program that demonstrates the core principles of how search engines organize and retrieve information.  

It uses **hash tables** and **linked lists** to build an **inverted index** — a data structure that maps words to the files they appear in, enabling efficient and fast word-based search operations across multiple text files.

---

## 🧑‍💻 Author
**Name:** Pankaj Kumar  
**Roll No:** 25008_018  
**Date:** 14-Sep-2025  

---

## ⚙️ Features
- ✅ **Command-line file validation:** Accepts multiple `.txt` files as input.  
- 🗂️ **Dynamic Database Creation:** Builds a word-to-file mapping using a hash table.  
- 🧾 **Display Database:** Prints all words with their corresponding file occurrences.  
- 🔎 **Search Functionality:** Quickly searches for a word across all indexed files.  
- 💾 **Save Database:** Saves the generated index to a backup file for future use.  
- 🔁 **Update Database:** Adds new files to an existing database (without rebuilding).  
- 🧩 **Modular Design:** All features are separated into logical modules for clarity.  
- 🚫 **Input Validation:** Prevents invalid or duplicate database operations.  

---

## 🧱 Core Concepts & Data Structures
| Component | Description |
|------------|-------------|
| **Hash Table** | Used to store words efficiently based on computed hash values. |
| **Linked List (FileList)** | Stores valid filenames passed as arguments. |
| **Structures** | Define word nodes, file nodes, and hash buckets. |
| **Flags** | Used to control duplicate creation or updates of the database. |

---
```
## 🗂️ Project Structure

| File / Folder        | Description                                      |
|-----------------------|--------------------------------------------------|
| `main.c`              | Entry point with menu-driven interface           |
| `list.c / list.h`     | Manages file list using linked lists             |
| `validate.c / validate.h` | Validates input files and command-line arguments |
| `database.c / database.h` | Core database creation and management logic     |
| `hash.c / hash.h`     | Implements hash table for word indexing          |
| `search.c`            | Searches a word in the inverted database         |
| `display.c`           | Displays the complete inverted index             |
| `save.c`              | Saves the database to a backup file              |
| `update.c`            | Updates the existing database with new files     |
| `files/`              | Directory containing input text files            |
| `README.md`           | Project documentation                            |


---

## 🧠 Program Flow
### **1. Command-Line Validation**
- Program expects at least one file name as an argument.
- Example:
  ```bash
  ./inverted_search file1.txt file2.txt file3.txt
  ```

2. Menu Options

Once started, the user interacts through a menu-driven interface:

Option	Description
---
1	Create Database (build inverted index)
2	Display Database (view all indexed data)
3	Search Word (find word occurrence across files)
4	Save Database (store to backup file)
5	Update Database (add new files)
0	Exit program

💻 Compilation & Execution
Compile

Use GCC or any C compiler:

```bash
gcc main.c list.c validate.c database.c hash.c search.c display.c save.c update.c -o inverted_search
```

RUN
```bash
./inverted_search file1.txt file2.txt file3.txt
```

Sample Ecexution
```mathematica
$ ./inverted_search file1.txt file2.txt

Valid files:
file1.txt
file2.txt

===== MENU =====
1. Create Database
2. Display Database
3. Search Word
4. Save Database
5. Update Database
0. Exit
Enter choice: 1

INFO: Database created successfully!
```

🧾 Example Output

```markdown
=============================
        INVERTED INDEX
=============================
Word       | File Count | Files
--------------------------------
data       |     2      | file1.txt, file2.txt
search     |     1      | file1.txt
engine     |     1      | file2.txt
--------------------------------
```

🧰 Functions Used
Function	Description
initialize_hashTable()	Initializes the hash table with NULL values.
read_and_validate_args()	Validates and creates the list of valid input files.
create_database()	Builds the inverted index.
display_database()	Displays the complete hash table contents.
search_word()	Searches for a specific word.
save_database()	Saves the database to a file.
update_database()	Adds new files to the existing database.

🪄 Future Enhancements

Add case-insensitive search support.

Implement word frequency counting per file.

Integrate stop word filtering (ignore words like “the”, “is”, etc.).

Add persistent storage using binary files.

Develop a web or GUI interface for easier interaction.