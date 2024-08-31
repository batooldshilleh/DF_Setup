# DF_Setup

This repository contains the solution for the Gaza Sky Geeks Take Home Task #1. The task involves installing Ubuntu, setting up directories for forensic projects, and downloading and converting specific tools to executables.

## Table of Contents
- [Task Overview](#task-overview)
- [System Setup](#system-setup)
- [Directory Structure](#directory-structure)
- [Tool Installation](#tool-installation)
- [Task Progress](#task-progress)
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
To check the partitions and the space each one occupies on the hard drive in an Ubuntu
system, we use the following command in the terminal:

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

