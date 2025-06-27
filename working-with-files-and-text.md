📝 Working with Files and Text Processing in Linux
Linux offers a wide range of commands to create, view, edit, filter, and manipulate text files. These tools are essential for system administrators, DevOps engineers, and shell scripting.

📄 File Creation & Viewing
Create Files

touch file.txt — Create a blank file

nano file.txt — Open a simple text editor in the terminal

vim file.txt — Powerful editor (press i to insert, :wq to save & exit)

View File Contents

cat file.txt — Display contents of a file

less file.txt — Scrollable viewer (use q to quit)

more file.txt — Similar to less, but older

head file.txt — View first 10 lines

tail file.txt — View last 10 lines

tail -f logfile.log — Live view of a file (useful for logs)

🧹 Editing Files Using Commands
Append or Overwrite

echo "Hello World" > file.txt — Overwrites file

echo "New line" >> file.txt — Appends to file

Combine Files

cat file1.txt file2.txt > combined.txt

Sort Contents

sort file.txt — Alphabetical sort

sort -r file.txt — Reverse sort

🔍 Searching & Filtering Text
Search Using grep

grep "word" file.txt — Search for word in file

grep -i "word" file.txt — Case-insensitive search

grep -n "word" file.txt — Show line numbers

grep -r "error" /var/log/ — Recursively search in folder

Find & Replace Using sed

sed 's/old/new/' file.txt — Replace first occurrence per line

sed 's/old/new/g' file.txt — Replace all occurrences globally

sed -i 's/old/new/g' file.txt — Edit file in-place

🪓 Cutting & Formatting Text
Using cut

cut -d':' -f1 /etc/passwd — Cut first field using ':' as delimiter

Using awk

awk '{print $1}' file.txt — Print first column (space-separated)

awk -F: '{print $1}' /etc/passwd — Print first field using ':' delimiter

Using tr

tr 'a-z' 'A-Z' < file.txt — Convert lowercase to uppercase

tr -d 'aeiou' < file.txt — Delete vowels

📊 Counting Words, Lines, and Characters
wc file.txt — Show lines, words, characters

wc -l file.txt — Only lines

wc -w file.txt — Only words

🧪 Comparing & Checking Files
diff file1.txt file2.txt — Show differences line by line

cmp file1.txt file2.txt — Compare byte by byte

md5sum file.txt — Generate checksum

📂 Redirects and Piping (|)
Output Redirection

command > file.txt — Send output to a file (overwrite)

command >> file.txt — Append output to file

Input Redirection

command < file.txt — Take input from file

Pipe Between Commands

cat file.txt | grep "error" | sort | uniq

⚡ Bonus: Quick Cheats
ls *.log | wc -l — Count number of .log files

uniq file.txt — Display only unique lines

sort file.txt | uniq — Remove duplicate lines (sorted)

expand file.txt — Replace tabs with spaces

nl file.txt — Number all lines in a file

tac file.txt — Reverse line order in file

🧠 Summary
Linux provides a rich toolbox for working with text files.

Commands like cat, grep, awk, sed, cut, and wc are essential.

These tools help in writing efficient scripts, processing logs, and automating tasks.
