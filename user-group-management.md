# 👥 User and Group Management in Linux

Linux systems are multi-user environments. Managing users and groups helps control access, security, and resource permissions.

---

## 👤 User Management

### ✅ Create a New User

sudo adduser john
##Creates a user named john and sets up their home directory and basic profile.

⚙️ Create User with Custom Options

sudo useradd -m -s /bin/bash john
-m: Creates a home directory
-s: Sets login shell (e.g., /bin/bash)

🔐 Set Password for a User
sudo passwd john
##Promotes u to set password to user

❌ Delete a User
sudo deluser john
##Removes the user but keeps the home directory.

sudo deluser --remove-home john
##Removes user and deletes the home directory.

👪 Group Management
➕ Create a New Group
sudo addgroup devs

👤➕ Add User to a Group
sudo usermod -aG devs john
-a: Append (do not remove from other groups)

-G: Specify the group

👁️ View a User’s Group Membership
groups john

➖ Remove User from a Group
sudo gpasswd -d john devs

❌ Delete a Group
sudo delgroup devs

📄 View User and Group Info
🧑 View All Users
cat /etc/passwd

👨‍👩‍👧 View All Groups
cat /etc/group

🔁 Switching Users
🔄 Switch to Another User
su - john

🧠 Run a Command as Another User
sudo -u john whoami

🧠 Summary Table
| Action                      | Command                             |
| --------------------------- | ----------------------------------- |
| Create user                 | `sudo adduser john`                 |
| Delete user                 | `sudo deluser john`                 |
| Create group                | `sudo addgroup devs`                |
| Add user to group           | `sudo usermod -aG devs john`        |
| Remove user from group      | `sudo gpasswd -d john devs`         |
| View user/group info        | `cat /etc/passwd`, `cat /etc/group` |
| Switch user                 | `su - john`                         |
| Run command as another user | `sudo -u john command`              |


