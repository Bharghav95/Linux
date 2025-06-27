👥 User and Group Management in Linux
Managing users and groups is essential for controlling access to system resources and ensuring security in Linux environments.

🧑‍💻 User Management
✅ Create a New User

sudo adduser john
Creates a new user with home directory /home/john

Prompts for password and other details

🧾 Add User Without Prompt

sudo useradd -m -s /bin/bash john
-m: Create home directory
-s: Set default shell

🔐 Set or Change Password
sudo passwd john

❌ Delete a User

sudo deluser john             # Deletes user only
sudo deluser --remove-home john  # Deletes user and their home directory

👪 Group Management
✅ Create a New Group

sudo addgroup devs

🧑‍🤝‍🧑 Add User to Group

sudo usermod -aG devs john
-aG: Append user to group(s) (important: don’t omit -a!)

👁️ View Group Membership
groups john
❌ Remove User from Group

sudo gpasswd -d john devs

❌ Delete a Group

sudo delgroup devs

🗂️ View User and Group Details
🔍 View All Users

cat /etc/passwd

🔍 View All Groups

cat /etc/group

🔄 Switch & Act as Another User
🔁 Switch to Another User

su - john

⚡ Run Command as Another User

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
