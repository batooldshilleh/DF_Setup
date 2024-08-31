
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
  - Manual installation with partitions: `swap`, `/`, `/boot`, `/home`

- **Directory Structure:**
  - Main directory: `Forensics_Projects`
  - Subdirectories: `Case_01`, `Case_02`, `Case_03`
  - Further subdirectories: `Evidence`, `Reports`, `Scripts`

- **Tool Installation:**
  - Sleuth Kit
  - EWF (use `ewfacquire`)

## System Setup

### 1. Ubuntu Installation

*Note: My device runs on Ubuntu Linux. I don't use any VM tools; it's the system on the physical device.*

To check the partitions and the space each one occupies on the hard drive in an Ubuntu system, use the following command in the terminal:

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

**Note 1: Why use `sudo`?**  
We use the `sudo` command to execute commands with superuser privileges, allowing us to perform administrative tasks like installing or updating software. It temporarily elevates our user privileges to those of the root user, which is necessary for system-level operations.

**Note 2: Why enter the password?**  
Typically, when using `sudo`, we would be prompted to enter our user password as a security measure. However, since we're working in the same terminal session, we weren't asked to enter the password again.

**Additional Note:**  
If you'd like to clear the previous commands from the terminal screen, use the `clear` command.

## Directory Structure

### 3. Creating Directories

You can create the necessary directory structure using the following command:

```bash
mkdir -p ~/Forensics_Projects/{Case_01/{Evidence,Reports,Scripts},Case_02/{Evidence,Reports,Scripts},Case_03/{Evidence,Reports,Scripts}}
```

Alternatively, you can create the directories manually:

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

<p align="center">
  <img src="https://github.com/user-attachments/assets/5059955c-bfcb-4bfb-bbe0-a844cb43b21a" alt="Partitions">
</p>

### 8. System Update and Upgrade Screenshots

- Screenshot after running `sudo apt-get update` and `sudo apt-get upgrade`.

<p align="center">
  <img src="https://github.com/user-attachments/assets/40d7cde0-3dd1-4fc1-babf-6f1fc42ce263" alt="Update">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f2dda66c-ae16-4ec1-b9c8-2312efd17f9c" alt="Upgrade">
</p>

### 9. Directory Structure Screenshots

- Screenshot of the directory structure for `Forensics_Projects`, showing all subdirectories.

1. Create the main directory `Forensics_Projects`.

<p align="center">
  <img src="https://github.com/user-attachments/assets/cfb42719-30ba-45fe-ad01-18fa02a06c02" alt="Main Directory">
</p>

2. Enter a directory.

<p align="center">
  <img src="https://github.com/user-attachments/assets/5bbe2aba-abe4-4af4-be6d-79179aa95417" alt="Enter Directory">
</p>

3. Create subdirectories.

<p align="center">
  <img src="https://github.com/user-attachments/assets/8f2ba7a2-0b81-4a69-b9d5-1c251bcb407f" alt="Subdirectories">
</p>

4. Within `Case_01`, use `cd`, `mkdir`, and `ls` commands to manage directories.

<p align="center">
  <img src="https://github.com/user-attachments/assets/b3063dc1-921b-4793-8efc-97eaade30ec6" alt="Case_01">
</p>

5. Within `Case_02`, navigate and manage directories similarly.

<p align="center">
  <img src="https://github.com/user-attachments/assets/79438126-4e95-4ebe-a6b2-89b82350cc82" alt="Case_02">
</p>

6. Within `Case_03`, navigate and manage directories similarly.

<p align="center">
  <img src="https://github.com/user-attachments/assets/ac837ab2-238d-4fb1-8976-5843320f3653" alt="Case_03">
</p>

### 10. Tool Installation Screenshots

- Screenshot of the terminal during the Sleuth Kit installation process.

1. Clone the repository.

<p align="center">
  <img src="https://github.com/user-attachments/assets/eecb201f-480c-4a34-a52d-fe01570c77a6" alt="Sleuth Kit Clone">
</p>

2. Navigate to the project folder.

<p align="center">
  <img src="https://github.com/user-attachments/assets/a8179b03-438a-475d-a9b5-9bb8cc62e7f6" alt="Navigate Folder">
</p>

3. Run the setup script.

<p align="center">
  <img src="https://github.com/user-attachments/assets/93ea6bd1-59e9-4027-8757-fd4084b94a5e" alt="Setup Script">
</p>

4. Configure the project.

<p align="center">
  <img src="https://github.com/user-attachments/assets/fa33fe14-e3ae-46e3-901e-18dd3ffb4916" alt="Configure Project">
</p>

5. Build the project.

<p align="center">
  <img src="https://github.com/user-attachments/assets/f653178a-8874-4a02-aa8c-1cbb1951e3dd" alt="Build Project">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/e1e6d576-0550-44b2-911b-ef3c117b61b3" alt="Build Project">
</p>

6. Install the project.

<p align="center">
  <img src="https://github.com/user-attachments/assets/56725073-029f-4696-ab04-95bd96813242" alt="Install Project">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/485987b9-7323-46dc-bbf3-d32e9025b744" alt="Install Project">
</p>

- Screenshot of the terminal during the EWF installation process.

1. Clone the repository.

<p align="center">
  <img src="https://github.com/user-attachments/assets/58aea29a-16a0-4e65-9f59-72b3b7659b01" alt="EWF Clone">
</p>

2. Navigate to the project folder.

<p align="center">
  <img src="https://github.com/user-attachments/assets/6a595682-d7d7-47d5-b0eb-43026c620838" alt="Navigate EWF Folder">

3. Synchronize the required libraries.

<p align="center">
  <img src="https://github.com/user-attachments/assets/843a8a81-ab09-41a2-9b48-13a6aa9deccc" alt="Sync Libraries">
</p>

4. Generate configuration files.

<p align="center">
  <img src="https://github.com/user-attachments/assets/f6d7aa32-5b5b-4946-b71c-794d4c271ba0" alt="Generate Config Files">
</p>

5. Configure the build environment.

<p align="center">
  <img src="https://github.com/user-attachments/assets/64e8429b-e09d-4ab7-925a-0bdb5b6eedba" alt="Configure Build Environment">
</p>

6. Compile the code.

<p align="center">
  <img src="https://github.com/user-attachments/assets/04e32dd1-4305-4b9d-b812-04acb23f1237" alt="Compile Code">
</p>

7. Install the compiled tools.

<p align="center">
  <img src="https://github.com/user-attachments/assets/02f09f72-a6c2-4cd1-bbc4-79b450ca97d4" alt="Install Tools">
</p>

8. Update the shared library cache.

<p align="center">
  <img src="https://github.com/user-attachments/assets/1a79bd08-98c9-42fc-aa22-09f1bb8d7e51" alt="Update Library Cache">
</p>

9. Use `ewfacquire`.

<p align="center">
  <img src="https://github.com/user-attachments/assets/c4bf61ec-cbae-4ed2-a2c4-bd7ccbf1910e" alt="ewfacquire">
</p>
