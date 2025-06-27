👥 User and Group Management in Linux
Managing users and groups is essential for controlling access to system resources and ensuring security in Linux environments.

🧑‍💻 User Management
✅ Create a New User
bash
Copy
Edit
sudo adduser john
Creates a new user with home directory /home/john

Prompts for password and other details

🧾 Add User Without Prompt
bash
Copy
Edit
sudo useradd -m -s /bin/bash john
-m: Create home directory

-s: Set default shell

🔐 Set or Change Password
bash
Copy
Edit
sudo passwd john
❌ Delete a User
bash
Copy
Edit
sudo deluser john             # Deletes user only
sudo deluser --remove-home john  # Deletes user and their home directory
👪 Group Management
✅ Create a New Group
bash
Copy
Edit
sudo addgroup devs
🧑‍🤝‍🧑 Add User to Group
bash
Copy
Edit
sudo usermod -aG devs john
-aG: Append user to group(s) (important: don’t omit -a!)

👁️ View Group Membership
bash
Copy
Edit
groups john
❌ Remove User from Group
bash
Copy
Edit
sudo gpasswd -d john devs
❌ Delete a Group
bash
Copy
Edit
sudo delgroup devs
🗂️ View User and Group Details
🔍 View All Users
bash
Copy
Edit
cat /etc/passwd
🔍 View All Groups
bash
Copy
Edit
cat /etc/group
🔄 Switch & Act as Another User
🔁 Switch to Another User
bash
Copy
Edit
su - john
⚡ Run Command as Another User
bash
Copy
Edit
sudo -u john command
🧠 Summary
Task	Command
Create user	sudo adduser <username>
Delete user	sudo deluser <username>
Create group	sudo addgroup <groupname>
Add user to group	sudo usermod -aG group user
Remove user from group	sudo gpasswd -d user group
Switch user	su - username
Run command as another user	sudo -u username command
