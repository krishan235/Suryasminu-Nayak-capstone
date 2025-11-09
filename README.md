# 🧭 File Explorer Application (Linux OS)

![C++](https://img.shields.io/badge/Language-C%2B%2B-blue)
![Platform](https://img.shields.io/badge/Platform-Linux-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

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
|----------|--------------|
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

## 🖥 How to Run the Application

### 🔧 *Step 1: Compile*
```bash
g++ blooma1.cpp -o explorer
