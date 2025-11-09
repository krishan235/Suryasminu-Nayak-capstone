# 🧭 File Explorer Application (Linux OS)

## 📘 Objective
The goal of this project is to *develop a console-based file explorer application in C++* that interacts with the *Linux Operating System* to manage files and directories.  
The application performs essential file operations such as *listing, copying, moving, deleting, creating, searching, and managing file permissions* through a simple text-based interface.

---

## 🧩 Overview
This File Explorer acts like a mini command-line interface built using C++.  
It allows the user to perform Linux-like file operations programmatically using *system calls* and *C++ standard libraries*.

---

## 🗓 Day-wise Task Implementation

### 🗓 *Day 1 – Application Setup and Basic File Listing*
- Designed the structure of the application.
- Set up the Linux-based C++ environment.
- Implemented the `listFiles()` function to display files and directories using `opendir()` and `readdir()`.

### 🗓 *Day 2 – Directory Navigation*
- Added directory traversal and basic navigation features.
- Displayed directory structures with user-friendly formatting.

### 🗓 *Day 3 – File Manipulation*
- Implemented:
  - *Copy file* using `ifstream` and `ofstream`
  - *Move file* using `rename()`
  - *Delete file* using `remove()`
  - *Create file* using `ofstream`

### 🗓 *Day 4 – Search Functionality*
- Added recursive search:
  - **`searchFile()`** – finds files/folders by name using recursion and `stat()`.

### 🗓 *Day 5 – File Permission Management*
- Added:
  - **`viewPermissions()`** – displays permissions as `rwxr-xr-x`
  - **`changePermissions()`** – modifies permissions using octal input (e.g., 644, 755)
- Implemented using `chmod()` and `stat()`.

---

## ⚙ Features Implemented

| Feature | Description |
|----------|-------------|
| *List Files* | Lists files and directories. |
| *Copy File* | Copies a file to another location. |
| *Move File* | Moves or renames a file. |
| *Delete File* | Removes a file permanently. |
| *Create File* | Creates a new file. |
| *Search File* | Recursively searches by name. |
| *View Permissions* | Displays symbolic file permissions. |
| *Change Permissions* | Updates permissions using octal values. |
| *Exit* | Closes the application. |

---

## 🧮 Command Reference

| Command | Description |
|----------|-------------|
| `list` | Lists all files/folders. |
| `copy` | Copies a file. |
| `move` | Moves or renames a file. |
| `delete` | Deletes a file. |
| `create` | Creates a new file. |
| `search` | Searches for a file/folder. |
| `perm` | Shows file permissions. |
| `chmod` | Changes file permissions. |
| `exit` | Exits the program. |

---

🖥 How to Run the Application
🔧 Step 1: Compile
g++ blooma1.cpp -o explorer

▶ Step 2: Execute

Run the program:

./explorer

💬 Step 3: Use Commands

Example session:

Available commands: list | copy | move | delete | create | search | perm | chmod | exit

Enter command: list
file1.txt
Documents
main.cpp

Enter command: create
Enter new file name: newfile.txt
File created successfully!

Enter command: search
Enter file name or keyword to search: main
Found: ./main.cpp

Enter command: perm
Enter file or path to view permissions: main.cpp
-rw-r--r--  1024 bytes  main.cpp

Enter command: chmod
Enter file or path to change permissions: main.cpp
Enter numeric mode (e.g. 644 or 0755): 755
Permissions changed successfully.
-rwxr-xr-x  1024 bytes  main.cpp

🧠 Technical Concepts Used

File I/O: ifstream, ofstream

Directory Access: opendir(), readdir(), closedir()

File Metadata: stat() structure to fetch file type, size, and permissions

File Permission Handling: chmod() and symbolic representation (rwx)

Recursive Search: Depth-first search for file name matching

Error Handling: perror() and input validation

C++ String and I/O Manipulation: string, setw, stoi, etc.

🧰 Libraries Used
#include <iostream>
#include <fstream>
#include <dirent.h>
#include <sys/stat.h>
#include <unistd.h>
#include <iomanip>
#include <cstring>
#include <string>

📄 Example Output
Available commands: list | copy | move | delete | create | search | perm | chmod | exit
Enter command: list
main.cpp
notes.txt
data/
Enter command: copy
Enter source file: notes.txt
Enter destination file: backup_notes.txt
File copied successfully!
Enter command: exit
Exiting File Explorer...

🧰 System Requirements

Operating System: Linux / Ubuntu / WSL

Compiler: g++ (GNU Compiler Collection)

Language Standard: C++11 or above

🏁 Conclusion

The File Explorer Application effectively simulates fundamental file management operations in a Linux environment.
It demonstrates how C++ interacts with the underlying Linux file system using system calls and standard libraries to perform file handling and permission management operations efficiently.

✅ Final Step

After you fix the formatting:

git add README.md
git commit -m "Fixed markdown formatting in README"
git push

---

### 🧩 Summary:
✅ Yes, paste this full content into your `README.md`  
⚠️ Make sure the code blocks (```bash``` or ```cpp```) are **properly closed** with three backticks.  
💡 After saving, push changes using:
```bash
git add README.md
git commit -m "Updated full README with complete sections"
git push
