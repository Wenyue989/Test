# Standard operating procedure for Setup a Virtual Linux Server for Web Application Testing

## Company name
NSA-W25 Ltd.
## Company street address 
130 Henlow Bay, Winnipeg, MB, Canada
## Company or department phone number
204-XXX-XXXX
## Reversion info: 
Version: 1.0 

Last Updated: 2025-11-19

## Approved Table: 
| __Version__ | **Date** | __Name__ | **Designation** |
|:---------|------:|:------:|:-------------|
| 1.0 | 2025-11-19 | Wenyue | Submitter |

### Purpose
This SOP provides instructions for setting up a virtual Linux server for web app testing using Ubuntu Server and VMware Worlstation. The goal is to create a repeatable test environment.

### Scope
This SOP applies to IT students, or junior technicians who are responsible for building and configuring a Linux-based test environment using virtualization technology.

This procedure will demo how to install the OS, configure essential services, and prepare a functional testing environment supporting web apps.

### Accountability Matrix
| **Role** | __Responsibility__ |
|------|---------------|
| Technician | Perform installation and configuration tasks |
| Supervisor / Admin | Verify completion and accuracy (if applicable) |

### Definitions
| **Term** | **Meaning** |
|------|--------|
| VM | A virtual computer running inside another computer. |
| LAMP Stack | A setup that includes Linux, Apache, MySQL, and PHP for web applications. |
| NAT | A network mode that allows the VM to access the internet using the host computer. |
| SSH | A secure way to remotely access and control a server. |

### Procedure steps

**Step 1:** Download Ubuntu Server  
- Navigate to: https://ubuntu.com/download/server  
- Download ISO image file for Ubuntu Server 22.04 LTS.

__Step 2:__ Create Virtual Machine in VMware 
- Open VMware Workstation 
- Click **Create a New Virtual Machine**  
- Select **Installer Disk Image File (ISO)**
- Browse and select your downloaded Ubuntu Server ISO image file
- Click __Next__
- Set a name for the VM: __`Linux-Testserver`__
- Select the folder for VM storage (optional)

**Step 3:** Configure System Resources  
- Assign CPU: 2 cores  >Note: Enough for testing server 
- RAM: 2GB
  >Note: Stable performance
- Disk: 20GB (Store as a single file recommended)  
- Set networking mode to **NAT**
- Firmware: BIOS (default)
  >Note: Do not change unless needed

__Step 4:__ Install Ubuntu Server  
- Click __Play Virtual Machine__ 
- Follow the installer prompts  
- Enable **OpenSSH Server**  
- Set hostname to __`Linux-testserver`__

**Step 5:** Update System Packages  
Run the following command in the terminal:
```
sudo apt update && sudo apt upgrade -y
```

__Step 6:__ Install LAMP Stack  
Install the required packages by running:
```
sudo apt install apache2 mysql-server php php-mysql -y
```

**Step 7:** Verify Apache Web Service  
Check Apache status using:
```
systemctl status apache2
```

>Open a browser and enter:\(http://localhost)

**Step 8:** Create and Test PHP Info Page 

Run the command:
```
echo '<?php echo "PHP is working!"; ?>' | sudo tee /var/www/html/info.php
```

>Verify output by visiting:\(http://localhost/info.php)

### Reference or Related Documents

- Ubuntu Server Documentation: https://ubuntu.com/server/docs  
- Apache HTTP Server Guide: https://httpd.apache.org/  
- PHP Documentation: https://www.php.net/manual/en  
