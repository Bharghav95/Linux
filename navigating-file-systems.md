# 📁 Navigating the File Systems in Linux

Understanding and navigating the Linux file system is essential for working efficiently in the command line. This note covers the Linux directory structure, navigation commands, file/directory operations, hidden file tricks, and more.

---

## 📂 Linux Directory Structure (Overview)

| Directory  | Description                                |
|------------|--------------------------------------------|
| `/`        | Root directory – base of the file system   |
| `/home`    | Home directories for users                 |
| `/etc`     | System configuration files                 |
| `/bin`     | Essential user binaries (commands)         |
| `/usr`     | Secondary hierarchy for user programs      |
| `/var`     | Variable data – logs, mail, etc.           |
| `/tmp`     | Temporary files                            |
| `/root`    | Home directory of the root user            |
| `/dev`     | Device files                               |
| `/mnt`     | Mount points for temporary mounts          |
| `/proc`    | Virtual filesystem with system info        |

---

## 🧭 Basic Navigation Commands

| Command               | Description                               |
|-----------------------|-------------------------------------------|
| `pwd`                 | Show current working directory            |
| `ls`                  | List files in a directory                 |
| `ls -l`               | Long listing format (details)            |
| `ls -a`               | Show hidden files                        |
| `cd <directory>`      | Change to a directory                     |
| `cd ..`               | Move one directory up                     |
| `cd /`                | Go to root directory                      |
| `cd ~` or `cd`        | Go to home directory                      |
| `cd -`                | Switch to previous directory              |
| `clear`               | Clear the terminal screen                 |

---

## 🛠️ File & Directory Operations

### 📁 Create Directories

mkdir folder-name             # Create a directory
mkdir -p parent/child         # Create nested directories

📝 Create Files

touch file.txt                # Create a blank file
nano file.txt                 # Create/edit file using nano

📂 Copy Files & Folders

cp file.txt backup.txt        # Copy a file
cp -r dir1/ dir2/             # Copy a folder recursively

🔁 Move or Rename Files

mv file.txt /path/to/dir/     # Move file to another folder
mv oldname.txt newname.txt    # Rename file

🗑️ Delete Files & Folders

rm file.txt                   # Delete a file
rm -r folder/                 # Delete a folder and its contents
rm -rf folder/                # Force delete without prompt (⚠️ dangerous!)

📑 Viewing and Reading Files

Command	Description
cat filename	Display content of a file
less filename	View large files one screen at a time
more filename	Similar to less, but more limited
head filename	Show the first 10 lines
tail filename	Show the last 10 lines
tail -f filename	Monitor file changes in real time (logs)

🗂️ Path Types
Absolute Path: Starts from root (/) — e.g., /home/user/file.txt

Relative Path: Starts from current directory — e.g., ../docs/file.txt

🤫 Hidden Files & Tricks
Hidden Files: Files/folders starting with a . (dot)

ls -a                  # Show hidden files
touch .hidden.txt      # Create hidden file
cat .bashrc            # View hidden file

Directory Navigation Shortcuts

cd -                  # Jump to previous directory
cd ~/Downloads        # Use ~ for home

List Files with Human Readable Sizes
ls -lh

List by Modified Time
ls -lt

Use Autocomplete with Tab
Type part of a command or filename and press Tab

🔥 Bonus Productivity Tricks
Use tree to show folder structure

sudo apt install tree     # Install (Debian/Ubuntu)
tree                      # Show directory tree

View command history  - history

Run previous command
!!                       # Runs the last command again
!45                      # Run command number 45 from history

Create command aliases
alias cls='clear'
alias l='ls -lah'
