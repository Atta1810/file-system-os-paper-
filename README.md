🗂️ File System Project
This project is a simple implementation of a file system designed to simulate core file operations such as creating, reading, writing, and deleting files and directories. It's intended for learning and experimentation with how file systems work under the hood.

🚀 Features
File and directory creation

Read/write operations

Deletion of files and directories

Directory navigation (cd, ls, etc.)

File metadata handling (e.g., size, creation date)

In-memory or disk-backed storage (depending on implementation)

🛠️ Tech Stack
Language: [Your Programming Language] (e.g., C, Python, Java)

Storage Model: [In-Memory / Disk-Based]

Data Structures: Trees, Linked Lists, Bitmaps (if applicable)

Optional: Command Line Interface for interaction

📁 Project Structure
/file-system/
│
├── src/                    # Core source files
│   ├── filesystem.c        # Main file system logic
│   ├── file.c              # File handling
│   ├── directory.c         # Directory handling
│   └── utils.c             # Utility functions
│
├── include/                # Header files (if C/C++)
│
├── tests/                  # Test cases
│
├── README.md               # Project documentation
└── Makefile / build.sh     # Build script
🔧 Installation
git clone https://github.com/Atta1810/file-system-os-paper-
cd file-system
make 
💻 Usage
./filesystem
Once inside the CLI, you can use commands like:
> mkdir docs
> cd docs
> touch notes.txt
> write notes.txt "Hello, world!"
> read notes.txt
> ls
> rm notes.txt
🧪 Testing
Run the test suite with:
> make test   # or use your own test framework

