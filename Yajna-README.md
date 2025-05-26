### Self Intro

Hi, I’m Velmurugan currently staying in Bengaluru.<br><br>
I completed my B.Sc. in Mathematics from Madurai Kamaraj University in 2020.
<br><br>
After completing my degree in 2020, I worked in the banking sector for 4 years after the COVID lockdown.<br><br>
But I’ve always had a strong interest and passion for Linux and open-source technologies.
<br><br>
Being enthusiastic about it, I explored a few Linux distros on my own and later joined a Linux training at Besant Technologies, Bengaluru from September last year to build my skills further.

<br><br><br><br><br><br><br>
🔐 1\. Sticky Bit
-----------------

### ✅ **Definition (Interview):**

A sticky bit is a special permission on a directory that allows **only the file owner or root** to delete or rename files inside it.

* * *

### ❓ **Sub-questions & Answers**

**Q1. Where is sticky bit used?**
Used in shared directories like `/tmp`.

**Q2. How to identify a sticky bit?**
With `ls -ld`, look for `t` in the permission, e.g. `drwxrwxrwt`.

* * *

### 💻 **Commands**

    chmod +t /shared-folder     # Add sticky bit
    chmod -t /shared-folder     # Remove sticky bit
    ls -ld /shared-folder       # View permissions


* * *

### 📘 **Explanation for You:**

If many users can write in a folder (like `/tmp`), sticky bit makes sure they **can’t delete each other’s files**. Only the **file creator** can delete their file.


🔒 3\. Linux File Permissions
-----------------------------

### ✅ **Definition (Interview):**

Linux uses **read, write, and execute** permissions for **owner, group, and others** to control access to files and folders.

* * *

### ❓ **Sub-questions & Answers**

**Q1. What does 755 mean?**
Owner: all permissions; Group & Others: read and execute

**Q2. How do you change permissions?**
With `chmod`, e.g. `chmod 644 file`

* * *

### 💻 **Commands**

    ls -l filename           # View permissions
    chmod 755 file           # Set permission
    chown user:group file    # Change owner


* * *

### 📘 **Explanation for You:**

Every file has **3 permission sets**: one for **owner**, one for **group**, and one for **others**.
Each can have **r (4), w (2), x (1)** — total is like math: `rwx = 7`.

* * *

🏠 4\. Private IP Address Range Types
-------------------------------------

### ✅ **Definition (Interview):**

Private IPs are reserved IP ranges used **within internal networks**, not routable over the internet.

* * *

### ❓ **Sub-questions & Answers**

**Q1. Name the private IP ranges.**

* Class A: 10.0.0.0 – 10.255.255.255
* Class B: 172.16.0.0 – 172.31.255.255
* Class C: 192.168.0.0 – 192.168.255.255

**Q2. Why use private IPs?**
To save public IPs and increase security.

* * *

### 💻 **Commands**

    ip a                  # Shows current IP
    ip route              # Shows routing table


* * *

### 📘 **Explanation for You:**

Private IPs are like **house numbers in a colony** — they work inside but can’t be accessed from the outside internet without NAT (like a guard who maps your house to public).

* * *

🌍 5\. DNS (Domain Name System)
-------------------------------

### ✅ **Definition (Interview):**

DNS translates **domain names** like `google.com` into **IP addresses**, enabling access to websites using human-readable names.

* * *

### ❓ **Sub-questions & Answers**

**Q1. What is `/etc/resolv.conf`?**
File that stores DNS server IPs used by the system.

**Q2. What is a DNS record?**
DNS records (A, CNAME, MX) map domains to IPs, services, or other domains.

* * *

### 💻 **Commands**

    dig google.com           # DNS query
    nslookup google.com      # DNS lookup
    cat /etc/resolv.conf     # View DNS servers


* * *

### 📘 **Explanation for You:**

DNS is like **a phonebook** — you don’t need to remember IPs, just names. It finds the number (IP) behind a name (domain).

* * *

🔐 6\. SSH (Secure Shell)
-------------------------

### ✅ **Definition (Interview):**

SSH is a secure protocol used to **remotely access and manage** Linux systems over an encrypted connection.

* * *

### ❓ **Sub-questions & Answers**

**Q1. What port does SSH use?**
Port 22 by default

**Q2. How do you generate SSH keys?**
Using `ssh-keygen`

* * *

### 💻 **Commands**

    ssh user@hostname          # Connect via SSH
    ssh-keygen                 # Create SSH key
    systemctl status ssh       # Check SSH service


* * *

### 📘 **Explanation for You:**

SSH is like **remote control for Linux** — you can sit anywhere and work on your server securely. You log in with **password** or **key pair**.

* * *

🌐 1\. **Port Numbers (FTP, SSH, HTTP, HTTPS, TELNET)**
-------------------------------------------------------

### ✅ **Definition (Interview):**

Ports are **logical endpoints** for communication; different services use different **port numbers** to listen for network traffic.

* * *

### ❓ **Sub-questions & Answers**

**Q1. What are the default ports for common services?**

* FTP: 21
* SSH: 22
* HTTP: 80
* HTTPS: 443
* Telnet: 23

**Q2. Can you change default ports?**
Yes, but it’s done in the service’s config file.

* * *

### 💻 **Commands**

    ss -tuln                # Show listening ports
    netstat -tuln           # (older) Show ports
    ufw allow 22/tcp        # Allow SSH in firewall


* * *

### 📘 **Explanation for You:**

Imagine ports like **TV channels** — each service listens on a certain “channel.” If you send data to port 22, you’re talking to SSH.

* * *

📊 2\. **`top` Command**
------------------------

### ✅ **Definition (Interview):**

`top` is a **real-time command-line tool** to monitor system processes, CPU usage, memory, and load average.

* * *

### ❓ **Sub-questions & Answers**

**Q1. How to sort by memory in `top`?**
Press `Shift + M` while `top` is running.

**Q2. How to kill a process in `top`?**
Press `k` and enter the PID.

* * *

### 💻 **Commands**

    top                    # Start live system monitor
    htop                   # (Better version, if installed)


* * *

### 📘 **Explanation for You:**

`top` is like **Task Manager** in Windows. It shows which programs are running and using your system’s CPU or RAM in real time.

* * *

💾 3\. **`df -TH` Command**
---------------------------

### ✅ **Definition (Interview):**

`df -TH` shows **disk space usage** for all mounted file systems, using **human-readable** and **terabyte/gigabyte units**.

* * *

### ❓ **Sub-questions & Answers**

**Q1. What does `-T` do in `df -TH`?**
Shows the file system type (ext4, xfs, etc.)

**Q2. What is `/dev/sda1` in `df` output?**
It’s a partition on a storage disk.

* * *

### 💻 **Commands**

    df -TH                 # Show total disk usage
    df -h                  # Without filesystem type


* * *

### 📘 **Explanation for You:**

`df` shows **how much disk is used** and free. `-T` shows type of filesystem. `-H` makes sizes easier to read (like GB or MB instead of blocks).

* * *

🧠 4\. **`free -h` Command**
----------------------------

### ✅ **Definition (Interview):**

`free -h` shows **available and used RAM** and **swap memory** in a human-readable format.

* * *

### ❓ **Sub-questions & Answers**

**Q1. What is swap memory?**
A reserved space on disk used when RAM is full.

**Q2. What does `-h` do in `free -h`?**
Shows sizes in human-readable format like MB/GB.

* * *

### 💻 **Commands**

    free -h               # Shows RAM + Swap usage


* * *

### 📘 **Explanation for You:**

Think of `free` like a **memory meter**. It tells you how much RAM you are using, how much is free, and how much "virtual RAM" (swap) is being used.

* * *

📦 5\. **`du -sh` Command**
---------------------------

### ✅ **Definition (Interview):**

`du -sh` shows the **disk usage** of a directory or file in **summary form and human-readable format**.

* * *

### ❓ **Sub-questions & Answers**

**Q1. What does `-s` and `-h` mean?**
`-s`: summary, `-h`: human-readable sizes.

**Q2. How to see size of all folders in a directory?**
Use `du -sh *`

* * *

### 💻 **Commands**

    du -sh /folder         # Size of folder
    du -sh *               # Size of everything in current dir


* * *

### 📘 **Explanation for You:**

`du` checks how much space a folder is using. `-s` keeps it short. `-h` means sizes like 1G or 200M instead of raw bytes.


* * *

📦 **Package Manager (Ubuntu – `apt`, RHEL/CentOS – `yum` or `dnf`)**
---------------------------------------------------------------------

### ✅ **Definition (Interview):**

A **package manager** is a tool that installs, updates, removes, and manages software packages in Linux.

* Ubuntu/Debian uses: `apt`
* RHEL/CentOS uses: `yum` (or `dnf` in newer versions)

* * *

### ❓ **Sub-questions & Answers**

**Q1. What is a package?**
A compressed file containing software and its dependencies.

**Q2. Difference between `apt` and `yum`?**
They work similarly but are used on different Linux distributions (`apt` for Debian-based, `yum/dnf` for RHEL-based).

**Q3. What is the difference between `yum` and `dnf`?**
`dnf` is the modern replacement for `yum` with better performance and dependency handling.

* * *

### 💻 **Common `apt` Commands (Ubuntu)**

    sudo apt update            # Refresh package list from internet
    sudo apt upgrade           # Upgrade installed packages
    sudo apt install nginx     # Install a package (e.g., nginx)
    sudo apt remove nginx      # Remove a package
    sudo apt search nginx      # Search for a package
    sudo apt list --installed  # List installed packages


* * *

### 💻 **Common `yum` Commands (RHEL/CentOS)**

    sudo yum check-update        # Check for updates
    sudo yum update              # Update all packages
    sudo yum install nginx       # Install a package
    sudo yum remove nginx        # Remove a package
    sudo yum search nginx        # Search for a package
    sudo yum list installed      # List installed packages


> ✅ In **newer RHEL versions**, use `dnf` instead of `yum`.
> Example: `sudo dnf install nginx`

* * *

### 🧠 **Explanation for You (Simple)**

A **package manager is like a Play Store for Linux**.
When you want to install or update software, instead of downloading from a website, you use `apt` or `yum` to do it for you.

* `apt` works on Ubuntu (like `.deb` files)
* `yum` or `dnf` works on Red Hat systems (like `.rpm` files)

* * *

Let me know if you want a mini quiz, or shall we go to the next topic like **Systemd**, **crontab**, **firewall**, etc.?

Then basic linux command Like creating file and folder Viewing file and editing file Removing file touch, mkdir, cat, vim or nano

Perfect! Let’s now cover **basic Linux commands** — the ones every beginner **must know** for daily use. These are often asked in interviews and **used all the time** in real work.

* * *

📝 **File & Directory Commands**
--------------------------------

### ✅ **Definition (Interview):**

Linux provides basic commands to **create**, **view**, **edit**, and **delete** files and folders using the terminal.

* * *

### 🔧 **1\. `touch` – Create a file**

> ✅ **Use:** Creates an empty file or updates a file’s timestamp.

    touch file.txt           # Creates a new file


📘 **Simple Explanation:** It’s like clicking "New File" in your file explorer.

* * *

### 📁 **2\. `mkdir` – Make a directory (folder)**

> ✅ **Use:** Creates a new folder.

    mkdir myfolder           # Create a folder
    mkdir -p a/b/c           # Create nested folders


📘 **Simple Explanation:** Like making a new folder on your computer.

* * *

### 👁️ **3\. `cat` – View file content**

> ✅ **Use:** Displays the content of a text file.

    cat file.txt             # Show contents


📘 **Simple Explanation:** Like double-clicking a file to read it.

* * *

### 📝 **4\. `nano` or `vim` – Edit file in terminal**

#### 🔹 `nano` (beginner-friendly editor)

    nano file.txt            # Open and edit the file


📘 **Explanation:** Easy, like Notepad in terminal. Use arrow keys, `Ctrl+O` to save, `Ctrl+X` to exit.

#### 🔹 `vim` (advanced editor)

    vim file.txt             # Open in Vim


📘 **Explanation:** Powerful, but has a learning curve.

* Press `i` to insert (start typing)
* Press `Esc`, then type `:wq` to save and exit
* Type `:q!` to quit without saving

* * *

### ❌ **5\. `rm` – Remove file or directory**

> ✅ **Use:** Deletes files or folders.

    rm file.txt              # Remove file
    rm -r myfolder/          # Remove folder (recursive)
    rm -rf myfolder/         # Force delete folder and contents


📘 **Simple Explanation:** Like sending a file/folder to the trash — but it’s gone forever.

⚠️ **Warning:** No "Undo" — deleted means permanently gone!

* * *

### ✅ **Mini Interview Q&A**

**Q: How do you create multiple folders at once?**
`mkdir folder1 folder2 folder3`

**Q: How do you edit a file without a GUI?**
Using `nano` or `vim` in the terminal.

**Q: What is the difference between `rm` and `rmdir`?**
`rmdir` removes **empty folders** only; `rm -r` removes folders with contents.


* * *

🧱 **LVM – Logical Volume Manager**
-----------------------------------

### ✅ **Definition (Interview):**

LVM (Logical Volume Manager) allows flexible management of disk space by creating logical volumes on top of physical storage.

It lets you **resize**, **create**, and **combine** partitions without restarting the system.

* * *

### 🔍 **Sub-questions and Answers (under 2 lines each)**

**Q: What is the use of LVM?**
To manage storage flexibly — you can resize, extend, shrink, and combine disks without unmounting.

**Q: What is a Physical Volume (PV)?**
A physical disk or partition prepared for LVM using `pvcreate`.

**Q: What is a Volume Group (VG)?**
A group of one or more physical volumes that act as a storage pool.

**Q: What is a Logical Volume (LV)?**
The usable space (like a partition) created from the volume group.

* * *

### 🧱 **LVM Structure**

    Hard Disk → PV → VG → LV → Mount → Use


Like:

    [ /dev/sdb ] → [ PV ] → [ VG_data ] → [ LV_docs ] → [ /mnt/docs ]


* * *

### 💻 **LVM Commands (with explanation)**

    # Step 1: Create a Physical Volume
    sudo pvcreate /dev/sdb

    # Step 2: Create a Volume Group
    sudo vgcreate vgdata /dev/sdb

    # Step 3: Create a Logical Volume (5GB)
    sudo lvcreate -L 5G -n lvdata vgdata

    # Step 4: Format the LV with ext4 filesystem
    sudo mkfs.ext4 /dev/vgdata/lvdata

    # Step 5: Mount the volume
    sudo mkdir /mnt/lvdata
    sudo mount /dev/vgdata/lvdata /mnt/lvdata

    # (Optional) Resize Logical Volume
    sudo lvextend -L +2G /dev/vgdata/lvdata
    sudo resize2fs /dev/vgdata/lvdata


* * *

### 📘 **Explanation for Beginners**

* **LVM is like combining multiple drives into one big flexible drawer.**
* You don’t need to worry about fixed partition sizes.
* You can add new drives later and just expand the space — no need to move files or reformat.

* * *

### ✅ **Common Interview Points**

* You can **extend** volumes without unmounting.
* LVM makes it easy to **take snapshots** for backup.
* Useful in servers and cloud environments where storage changes often.

* * *

### 📋 Summary

| Term | Description |
| --- | --- |
| PV  | Physical Volume (disk prepared for LVM) |
| VG  | Volume Group (pool of PVs) |
| LV  | Logical Volume (usable storage space) |

* * *

Would you like a **diagram or mini quiz** on LVM, or should we continue to **next topic** like `df`, `mount`, or disk partitioning with `fdisk`/`lsblk`?

next topic like df, mount, or disk partitioning with fdisk/lsblk

Awesome! Let's now dive into **Disk Management Tools** in Linux – very important for **system administration**, **troubleshooting**, and **interviews**.

* * *

🔧 Disk Partitioning and Monitoring in Linux
--------------------------------------------

We'll cover these essential commands:

1.  **`df`** – Check disk usage
2.  **`mount` / `umount`** – Mount and unmount disks
3.  **`fdisk`** – Create or delete disk partitions
4.  **`lsblk`** – View block devices (disks)
5.  **`blkid`** – Show UUIDs and filesystem types
6.  **`mount -a`**, `/etc/fstab` – Auto-mount at boot

* * *

### ✅ 1\. `df` – Disk Free

> Shows **disk usage** of all mounted filesystems.

    df -h


📘 `-h` = human readable (shows GB, MB)

✅ **Example Output**:

    Filesystem      Size  Used Avail Use% Mounted on
    /dev/sda1        50G   20G   27G  43% /


* * *

### ✅ 2\. `mount` / `umount` – Attach/detach storage

#### 🟢 Mount:

    sudo mount /dev/sdb1 /mnt/data


✅ Mounts a partition (like USB or extra drive) to a folder.

#### 🔴 Unmount:

    sudo umount /mnt/data


⚠️ Must unmount before formatting or removing the drive safely.

* * *

### ✅ 3\. `fdisk` – Partitioning Tool (for MBR disks)

    sudo fdisk /dev/sdb


➡️ Interactive menu:

* `n` – new partition
* `d` – delete
* `w` – write changes
* `p` – print partition table

📘 After creating a new partition, format it using:

    sudo mkfs.ext4 /dev/sdb1


* * *

### ✅ 4\. `lsblk` – List block devices

    lsblk


✅ Shows all disks and their partitions in tree view.

Example:

    NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
    sda      8:0    0   50G  0 disk
    ├─sda1   8:1    0   50G  0 part /
    sdb      8:16   0  100G  0 disk


* * *

### ✅ 5\. `blkid` – Show block device UUIDs

    sudo blkid


✅ Helps when configuring permanent mounts in `/etc/fstab`.

* * *

### ✅ 6\. Auto Mounting at Boot – `/etc/fstab`

To mount a drive permanently at boot:

    sudo nano /etc/fstab


Add line like:

    UUID=xxxx-xxxx   /mnt/data  ext4  defaults  0  2


Use `blkid` to get UUID.

Then test with:

    sudo mount -a


* * *

### 📘 Simple Analogy:

* `df` – Like checking how full your cupboard is
* `mount` – Like plugging in a USB drive
* `fdisk` – Like dividing your hard disk into rooms
* `lsblk` – Like looking at a map of all rooms in your house
* `fstab` – Like setting up auto-plugins on startup

* * *

### 🔎 Mini Interview Q&A

**Q: How to check disk usage?**
Use `df -h`

**Q: How to mount a USB drive?**
Use `mount /dev/sdb1 /mnt/usb`

**Q: How to see partitions and structure?**
Use `lsblk` or `fdisk -l`

**Q: How to make a new partition?**
Use `fdisk /dev/sdX`

**Q: How to mount permanently?**
Edit `/etc/fstab` with UUID and mount point

* * *

### ✅ Commands Recap

    df -h                  # Check disk space
    mount /dev/sdb1 /mnt   # Mount a drive
    umount /mnt            # Unmount it
    fdisk /dev/sdb         # Partition a disk
    lsblk                  # Show disk structure
    blkid                  # Show UUIDs of drives
    mount -a               # Test fstab file


* * *

Explain the OSI layer and its items

* * *

🌐 2\. OSI Model
----------------

### ✅ **Definition (Interview):**

The OSI model is a **7-layer framework** that describes how data travels over a network, from **application to hardware**.

* * *

### ❓ **Sub-questions & Answers**

**Q1. Name the 7 layers of OSI.**
App, Presentation, Session, Transport, Network, Data Link, Physical

**Q2. Which layer does IP belong to?**
Network Layer

**Q3. Which layer does TCP/UDP belong to?**
Transport Layer

* * *

### 💻 **Commands (To see layer 3 & 4 info)**

    ip a             # Shows IP info (Layer 3)
    netstat -tunlp   # Shows TCP/UDP ports (Layer 4)


* * *

### 📘 **Explanation for You:**

Think of OSI like **postal system**:
App writes letter → puts in envelope (Transport) → gets address (Network) → goes to delivery (Physical).
Each layer handles part of the journey.

* * *


🌐 What is the OSI Model?
-------------------------

> **Definition (Interview Answer):**
> The **OSI model** (Open Systems Interconnection model) is a 7-layer framework that describes how data moves from one device to another over a network.

It helps standardize how different devices and software communicate.

* * *

🧱 7 Layers of the OSI Model (from top to bottom)
-------------------------------------------------

| Layer | Name | Function (Simple English) | Example |
| --- | --- | --- | --- |
| 7   | **Application** | Where users interact with software | Browser, Email app |
| 6   | **Presentation** | Translates and formats data | Encryption, JPEG |
| 5   | **Session** | Starts and ends communication between devices | Login sessions |
| 4   | **Transport** | Ensures reliable data delivery (TCP/UDP) | TCP, UDP |
| 3   | **Network** | Chooses the best path for data (routing) | IP address, Router |
| 2   | **Data Link** | Transfers data between connected devices | MAC address |
| 1   | **Physical** | Sends raw bits through cables or Wi-Fi | Ethernet cable, Wi-Fi signal |

* * *

### 🔍 Simple Analogy – **Sending a Letter**

* Layer 7 – You write the message (application)
* Layer 6 – Translate it if needed (presentation)
* Layer 5 – Start/End conversation (session)
* Layer 4 – Ensure it’s delivered correctly (transport)
* Layer 3 – Choose route to send (network)
* Layer 2 – Address it to the right person (data link)
* Layer 1 – Physically send it via post (physical)

* * *

🎯 Interview Questions & Answers
--------------------------------

**Q: What layer is responsible for routing?**
A: Network layer (Layer 3)

**Q: What layer uses TCP and UDP?**
A: Transport layer (Layer 4)

**Q: What is the difference between MAC and IP?**
A: MAC is hardware address (Layer 2), IP is logical address (Layer 3)

**Q: Which layer handles encryption and compression?**
A: Presentation layer (Layer 6)

**Q: At which layer do users interact?**
A: Application layer (Layer 7)

* * *

🛠️ Related Commands
--------------------

    ping google.com          # Tests Layer 3 (Network)
    traceroute google.com    # Shows routing path (Layer 3)
    netstat -tunlp           # Shows ports and services (Layer 4)
    curl http://site.com     # Tests Application layer (Layer 7)


* * *

### 🔁 Recap Chart

| Layer No | Layer Name | Protocols / Examples |
| --- | --- | --- |
| 7   | Application | HTTP, FTP, SMTP |
| 6   | Presentation | SSL, TLS, JPEG, GIF |
| 5   | Session | NetBIOS, RPC |
| 4   | Transport | TCP, UDP |
| 3   | Network | IP, ICMP, Routers |
| 2   | Data Link | Ethernet, MAC, Switches |
| 1   | Physical | Cables, Hubs, Fiber, Wi-Fi Signal |

* * *


Explain TCP and UDP

Sure! Let’s understand **TCP and UDP** – they are very important networking concepts, especially for Linux or Cloud administrators. These are part of the **Transport Layer (Layer 4)** in the OSI Model.

* * *

📌 What is TCP and UDP?
-----------------------

> **Definition (Interview Style):**
> **TCP (Transmission Control Protocol)** and **UDP (User Datagram Protocol)** are two transport layer protocols used to send data over a network.
> TCP is **reliable and connection-oriented**, while UDP is **faster and connectionless**.

* * *

🔄 Comparison: TCP vs UDP (Simple Table)
----------------------------------------

| Feature | TCP | UDP |
| --- | --- | --- |
| Connection Type | Connection-oriented (handshake) | Connectionless |
| Reliability | Reliable (guarantees delivery) | Not reliable (no guarantee) |
| Speed | Slower | Faster |
| Error Checking | Yes (retransmits lost data) | Minimal |
| Order of Data | Maintains order | Order not guaranteed |
| Use Cases | Web (HTTP), Email, FTP | Streaming, DNS, VoIP |
| Overhead | More | Less |

* * *

### 🎯 Simple Analogy:

* **TCP is like a phone call** ☎️

    * You say hello (handshake), talk, confirm messages, then hang up.
* **UDP is like a postcard** 📨

    * You just send it. If it gets lost, no one knows.

* * *

🔧 Commands to Test TCP and UDP
-------------------------------

### 🔹 TCP Example:

    telnet google.com 80      # Tests TCP port 80 (HTTP)


### 🔹 UDP Example:

    nc -u 8.8.8.8 53           # Tests UDP to DNS server on port 53


* * *

✅ Interview Questions & Answers
-------------------------------

**Q: What is TCP?**
A: TCP is a connection-based protocol that ensures reliable, ordered delivery of data.

**Q: What is UDP?**
A: UDP is a connectionless protocol that sends data faster but without guarantee of delivery.

**Q: Where is TCP used?**
A: Used in web (HTTP/HTTPS), FTP, emails – where data reliability matters.

**Q: Where is UDP used?**
A: Used in live streaming, DNS, VoIP – where speed is more important than accuracy.

**Q: Can you name a port that uses TCP and another that uses UDP?**
A: Port 80 uses TCP (HTTP), Port 53 uses UDP (DNS).

* * *

🧠 Summary (One-liner)
----------------------

* **TCP** = Reliable, slow, ordered (Web, Email)
* **UDP** = Fast, unreliable, unordered (Streaming, DNS)

* * *
