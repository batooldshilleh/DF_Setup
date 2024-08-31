# DF_Setup

This repository contains the solution for the Gaza Sky Geeks Take Home Task #1. The task involves installing Ubuntu, setting up directories for forensic projects, and downloading and converting specific tools to executables.

## Table of Contents
- [Task Overview](#task-overview)
- [System Setup](#system-setup)
- [Directory Structure](#directory-structure)
- [Tool Installation](#tool-installation)
- [Screenshots](#screenshots)

## Task Overview
- **Ubuntu Installation:**
  - RAM: 4GB
  - Hard Disk: 45GB
  - Manual installation with partitions: swap, /, /boot, /home

- **Directory Structure:**
  - Main directory: `Forensics_Projects`
  - Subdirectories: `Case_01`, `Case_02`, `Case_03`
  - Further subdirectories: `Evidence`, `Reports`, `Scripts`

- **Tool Installation:**
  - Sleuth Kit
  - EWF (try `ewfacquire`)

## System Setup

### 1. Ubuntu Installation
`Note: My device runs on Ubuntu Linux. I don't use any VM tools; it's the system on the physical device.`
To check the partitions and the space each one occupies on the hard drive in an Ubuntu system, we use the following command in the terminal:

 ```bash
df -h
 ```

Install Ubuntu 24 with the specified RAM and hard disk size. During the installation, manually create the following partitions:
- `swap`
- `/`
- `/boot`
- `/home`

### 2. Applying Updates and Upgrades
After installation, update and upgrade the system using the following commands:
```bash
sudo apt-get update
sudo apt-get upgrade
```
- **Note 1: Why use `sudo`?**  
  We use the `sudo` command to execute commands with superuser privileges, allowing us to perform administrative tasks like installing or updating software. It temporarily elevates our user privileges to those of the root user, which is necessary for system-level operations.

- **Note 2: Why enter the password?**  
  Typically, when using `sudo`, we would be prompted to enter our user password as a security measure. However, since we're working in the same terminal session, we weren't asked to enter the password again.

- **Additional Note:**  
  If you'd like to clear the previous commands from the terminal screen, use the `clear` command.

## Directory Structure

### 3. Creating Directories
```bash
mkdir -p ~/Forensics_Projects/{Case_01/{Evidence,Reports,Scripts},Case_02/{Evidence,Reports,Scripts},Case_03/{Evidence,Reports,Scripts}}
```
or 
```bash
mkdir Forensics_Projects
cd Forensics_Projects
mkdir Case_01
cd Case_01
mkdir Evidence
mkdir Reports
mkdir Scripts
cd ..
mkdir Case_02
cd Case_02
mkdir Evidence
mkdir Reports
mkdir Scripts
cd ..
mkdir Case_03
cd Case_03
mkdir Evidence
mkdir Reports
mkdir Scripts
```

## Tool Installation

### 4. Installing Necessary Requirements

Install the necessary packages for converting source code to executables:
```bash
sudo apt-get install build-essential
```

### 5. Download and Install Sleuth Kit

Download Sleuth Kit from GitHub and convert it to an executable:
```bash
git clone https://github.com/sleuthkit/sleuthkit.git
cd sleuthkit
./bootstrap
./configure
make
sudo make install
```

### 6. Download and Install EWF

Download EWF from GitHub and convert it to an executable:
```bash
git clone https://github.com/libyal/libewf.git
cd libewf
./synclibs.sh
./autogen.sh
./configure
make
sudo make install
sudo ewfacquire
```

## Screenshots

### 7. Ubuntu Installation Screenshots
- Screenshot showing the partitions created during the installation.
   <br>
  <br>
![image](https://github.com/user-attachments/assets/5059955c-bfcb-4bfb-bbe0-a844cb43b21a)

### 8. System Update and Upgrade Screenshots
- Screenshot after running `sudo apt-get update` and `sudo apt-get upgrade`.
   <br>
  <br>
  ![image](https://github.com/user-attachments/assets/40d7cde0-3dd1-4fc1-babf-6f1fc42ce263)

  <br>
  <br>

![image](https://github.com/user-attachments/assets/f2dda66c-ae16-4ec1-b9c8-2312efd17f9c)



### 9. Directory Structure Screenshots
- Screenshot of the directory structure for `Forensics_Projects`, showing all subdirectories.
  <br>
  <br>
1.  Create a main directory called Forensics_Projects
   <br>
  <br>
  
![image](https://github.com/user-attachments/assets/cfb42719-30ba-45fe-ad01-18fa02a06c02)

 <br>
  <br>
  2.  enter a directory.
   <br>
  <br>
  
  ![image](https://github.com/user-attachments/assets/5bbe2aba-abe4-4af4-be6d-79179aa95417)
  
<br>
<br>

3.  create subdirectories
   <br>
  <br>

![image](https://github.com/user-attachments/assets/8f2ba7a2-0b81-4a69-b9d5-1c251bcb407f)
<br>
<br>

4.  Within Case_01
 *  Enter the directory using `cd`.
 *  Use `mkdir` to create directories inside it.
 *  Use the `ls` command to list the contents of the directory.
   <br>
  <br>

![image](https://github.com/user-attachments/assets/b3063dc1-921b-4793-8efc-97eaade30ec6)

<br>
<br>

5.  Within Case_02
 * Go back to the previous directory using the command `cd ..`.
 *  Enter the directory using `cd`.
 *  Use `mkdir` to create directories inside it.
 *  Use the `ls` command to list the contents of the directory.
   <br>
  <br>

![image](https://github.com/user-attachments/assets/79438126-4e95-4ebe-a6b2-89b82350cc82)

<br>
<br>

6.  Within Case_03
 * Go back to the previous directory using the command `cd ..`.
 *  Enter the directory using `cd`.
 *  Use `mkdir` to create directories inside it.
 *  Use the `ls` command to list the contents of the directory.
   <br>
  <br>

![image](https://github.com/user-attachments/assets/ac837ab2-238d-4fb1-8976-5843320f3653)

### 10. Tool Installation Screenshots
- Screenshot of the terminal during the Sleuth Kit installation process.
  <br>
<br>

1- Clone the repository:
<br>
<br>

![image](https://github.com/user-attachments/assets/eecb201f-480c-4a34-a52d-fe01570c77a6)


<br>
<br>

2- Navigate to the project folder:
<br>
<br>

![image](https://github.com/user-attachments/assets/a8179b03-438a-475d-a9b5-9bb8cc62e7f6)

<br>
<br>
3- Run the setup script:
<br>
<br>

![image](https://github.com/user-attachments/assets/93ea6bd1-59e9-4027-8757-fd4084b94a5e)


<br>
<br>
4- Configure the project:
<br>
<br>

![image](https://github.com/user-attachments/assets/fa33fe14-e3ae-46e3-901e-18dd3ffb4916)


<br>
<br>

5- Build the project:

<br>
<br>

![image](https://github.com/user-attachments/assets/f653178a-8874-4a02-aa8c-1cbb1951e3dd)


<br>
<br>
![image](https://github.com/user-attachments/assets/e1e6d576-0550-44b2-911b-ef3c117b61b3)

<br>
<br>

6- Install the project:

<br>
<br>

![image](https://github.com/user-attachments/assets/56725073-029f-4696-ab04-95bd96813242)

<br>
<br>

![image](https://github.com/user-attachments/assets/485987b9-7323-46dc-bbf3-d32e9025b744)

<br>
<br>

- Screenshot of the terminal during the EWF installation process.

