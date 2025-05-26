* * *

🧰 **Basic Ubuntu Commands with Simple Explanation and Example**
================================================================

* * *

🔹 1\. `pwd` – Print Working Directory
--------------------------------------

👉 Shows the folder (directory) you are in right now.

    pwd


🧾 Example output:
`/home/yourname/Documents`

* * *

🔹 2\. `ls` – List Files and Folders
------------------------------------

👉 Shows what's inside the current folder.

    ls


🧾 Example:
Shows files like `file1.txt`, `photo.jpg`, etc.

Add `-l` for details:

    ls -l


* * *

🔹 3\. `cd` – Change Directory
------------------------------

👉 Go to another folder.

    cd /home/yourname/Desktop


📌 Tip:
Use `cd ..` to go back (up one level).

* * *

🔹 4\. `mkdir` – Make Directory
-------------------------------

👉 Create a new folder.

    mkdir my_folder


* * *

🔹 5\. `touch` – Create a New Empty File
----------------------------------------

    touch myfile.txt


* * *

🔹 6\. `cp` – Copy Files or Folders
-----------------------------------

👉 Copy one file to another location.

    cp file.txt /home/yourname/Desktop/


To copy a folder:

    cp -r myfolder/ /home/yourname/Desktop/


* * *

🔹 7\. `mv` – Move or Rename Files
----------------------------------

👉 Move file or rename it.

    mv file.txt /home/yourname/Desktop/


Rename:

    mv oldname.txt newname.txt


* * *

🔹 8\. `rm` – Remove (Delete) Files or Folders
----------------------------------------------

    rm myfile.txt


To delete a folder and its contents:

    rm -r myfolder/


⚠️ Be careful, this is permanent.

* * *

🔹 9\. `cat` – Show File Content
--------------------------------

    cat notes.txt


* * *

🔹 10\. `clear` – Clean the Terminal Screen
-------------------------------------------

    clear


* * *

🔹 11\. `echo` – Show Message or Save Text to File
--------------------------------------------------

    echo "Hello World"


Save to file:

    echo "Hello" > hello.txt


* * *

🔹 12\. `nano` – Simple Text Editor in Terminal
-----------------------------------------------

    nano myfile.txt


✏️ Press `Ctrl + X` to exit and save.

* * *

🔹 13\. `df -h` – Show Disk Space
---------------------------------

    df -h


🧾 Shows how full your disk is in human-readable form (GB/MB).

* * *

🔹 14\. `free -h` – Show RAM Usage
----------------------------------

    free -h


* * *

🔹 15\. `top` – Show Live Running Processes
-------------------------------------------

    top


Use `q` to quit.

* * *

🔹 16\. `ps aux` – List All Running Processes
---------------------------------------------

    ps aux


* * *

🔹 17\. `kill` – Stop a Process
-------------------------------

    kill 1234


(Where 1234 is the process ID)

* * *

🔹 18\. `sudo` – Run Command as Administrator (Superuser)
---------------------------------------------------------

    sudo apt update


🧾 Use when a command needs permission (like installing software).

* * *

🔹 19\. `apt` – Install or Manage Software (Packages)
-----------------------------------------------------

Update package info:

    sudo apt update


Install a program:

    sudo apt install vlc


Remove a program:

    sudo apt remove vlc


* * *

🔹 20\. `which` – Find Location of a Command
--------------------------------------------

    which python


* * *

🔹 21\. `man` – Manual (Help) for Any Command
---------------------------------------------

    man ls


Press `q` to quit.

* * *

🔹 22\. `chmod` – Change File Permission
----------------------------------------

    chmod +x script.sh


(Makes script.sh executable)

* * *

🔹 23\. `chown` – Change File Owner
-----------------------------------

    sudo chown yourname file.txt


* * *

🔹 24\. `hostname` – Show Computer Name
---------------------------------------

    hostname


* * *

🔹 25\. `uname -a` – Show System Info
-------------------------------------

    uname -a


* * *

🔹 26\. `ifconfig` or `ip a` – Show Network Info
------------------------------------------------

    ip a


* * *

🔹 27\. `ping` – Test Internet or Server Connection
---------------------------------------------------

    ping google.com


Press `Ctrl + C` to stop.

* * *

🔹 28\. `history` – Show Command History
----------------------------------------

    history


* * *

🔹 29\. `tar` – Compress or Extract .tar Files
----------------------------------------------

Create archive:

    tar -cvf mybackup.tar foldername/


Extract:

    tar -xvf mybackup.tar


* * *

🔹 30\. `shutdown` or `reboot` – Power Off or Restart
-----------------------------------------------------

Shutdown:

    sudo shutdown now


Reboot:

    sudo reboot


* * *

✅ Summary for You
-----------------

Here’s a grouped view:

| Type | Commands |
| --- | --- |
| Navigation | `pwd`, `cd`, `ls`, `mkdir` |
| File Ops | `cp`, `mv`, `rm`, `touch`, `cat`, `nano`, `echo` |
| System Info | `df`, `free`, `top`, `ps`, `uname`, `hostname` |
| Process | `kill`, `history` |
| Software | `sudo`, `apt`, `which`, `man` |
| Network | `ip a`, `ping` |
| Permissions | `chmod`, `chown` |
| Archive | `tar` |
| Power | `shutdown`, `reboot` |

* * *

Would you like me to:

* Test you with a few questions now?
* Or go deeper into one group, like **file handling** or **networking**?

Let me know!

Okay give me next setup of commands

Perfect! Since you've understood the basic commands and want to move forward, let’s now dive into the **next level** of useful Ubuntu commands, grouped by category — with simple explanations and examples again.

* * *

🧰 Intermediate Ubuntu Commands – Step 2
========================================

> ✅ These help you with **searching**, **permissions**, **archives**, **services**, and **system management**.

* * *

🔍 **Searching and Finding Files**
----------------------------------

### 🔹 `find` – Search for files and folders

    find /home/yourname -name "*.txt"


📄 Finds all `.txt` files inside `/home/yourname`.

* * *

### 🔹 `locate` – Quickly find files (uses a database)

    locate vlc


⚠️ May need to run `sudo updatedb` first.

* * *

### 🔹 `grep` – Search text inside files

    grep "hello" myfile.txt


🔍 Finds all lines in `myfile.txt` that contain the word "hello".

* * *

🔐 **Permissions and Ownership**
--------------------------------

### 🔹 `ls -l` – View permissions

Shows this format:

    -rw-r--r-- 1 user group  1234 Jan 1 09:00 file.txt


### 🔹 `chmod` – Change who can read/write/execute a file

    chmod 755 script.sh


### 🔹 `chown` – Change file ownership

    sudo chown yourname:yourname file.txt


* * *

📦 **Compress and Extract Files**
---------------------------------

### 🔹 `tar` – Archive/unarchive `.tar` files

Create:

    tar -cvf backup.tar folder/


Extract:

    tar -xvf backup.tar


### 🔹 `zip` and `unzip` – Work with `.zip` files

    zip myzip.zip file1 file2
    unzip myzip.zip


* * *

🛠️ **System Services (Background Programs)**
---------------------------------------------

### 🔹 `systemctl` – Manage services

Check if a service is running:

    systemctl status apache2


Start a service:

    sudo systemctl start apache2


Enable at boot:

    sudo systemctl enable apache2


Stop or disable:

    sudo systemctl stop apache2
    sudo systemctl disable apache2


* * *

⚙️ **System Info and Logs**
---------------------------

### 🔹 `dmesg` – View kernel messages (hardware-related)

    dmesg | less


### 🔹 `journalctl` – View system logs

    journalctl -xe


🔧 Shows recent logs and errors.

* * *

🌐 **Networking and Downloads**
-------------------------------

### 🔹 `wget` – Download files from the internet

    wget http://example.com/file.txt


### 🔹 `curl` – Get data from a web address (more flexible than wget)

    curl https://ipinfo.io


* * *

📜 **Package and Software Management (Advanced)**
-------------------------------------------------

### 🔹 `dpkg` – Install local `.deb` packages

    sudo dpkg -i package.deb


Fix missing dependencies:

    sudo apt -f install


* * *

🧰 **Miscellaneous Useful Commands**
------------------------------------

### 🔹 `alias` – Create shortcut for a command

    alias cls='clear'


Now you can type `cls` instead of `clear`.

### 🔹 `whoami` – Shows your current user

    whoami


### 🔹 `uptime` – Shows how long your computer has been running

    uptime

* * *