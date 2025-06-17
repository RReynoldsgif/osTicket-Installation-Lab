# 🎫 osTicket Installation Lab  (Windows 10 Local Environment)

This project documents the full installation and configuration of the **osTicket** open-source support ticket system on a Windows 10 virtual machine This lab simulated a real-world help desk environment using: **IIS**, **PHP**, and **MySQL**. Screenshots were captured throughout the process to validate installation success and system functionality.
---

## 📌 Lab Objectives

- Configure **Internet Information Services (IIS)** on Windows
- Install and configure **PHP** for IIS
- Set up **MySQL 5.5** with secure root access
- Deploy osTicket to the `wwwroot` directory
- Create and configure the **osTicket database** using HeidiSQL
- Launch the **osTicket web installer** and complete installation
- Verify successful setup via **Support Center interface**

---

## 🖥️ Environment

- **OS:** Windows 10 VM
- **Web Server:** Internet Information Services (IIS)
- **Database:** MySQL 5.5 (via MySQL Installer)
- **Database Tool:** HeidiSQL
- **PHP Version:** 7.x
- **osTicket Version:** v1.15.8
---

## 📁 Prepare Installation Files

Installation Files![image](https://github.com/user-attachments/assets/01375fb5-f888-4148-b15c-38904aa42688)


📄 **Description**: This screenshot shows the directory containing all required components for the osTicket installation, including the osTicket package, MySQL installer, PHP runtime, PHP Manager for IIS, VC redistributables, and HeidiSQL.

---

## ⚙️ Enable IIS Web Server

Enable IIS Features ![image](https://github.com/user-attachments/assets/d8c9c686-8b93-4c95-8193-9fd1df7648dd)



📄 **Description**: This image displays the Windows Features menu, where IIS and necessary modules such as CGI and common HTTP features were enabled to support PHP and web hosting for osTicket.

---

## 🌐 Verify IIS Installation

IIS Welcome Page ![image](https://github.com/user-attachments/assets/38653e9e-e220-4a2e-b859-02b088e418c9)


📄 **Description**: Navigating to `localhost` confirms that IIS is installed and running properly. This default welcome page is served from the `wwwroot` directory.

---

## 🔐 Set MySQL Root Password

MySQL Root Setup ![image](https://github.com/user-attachments/assets/fbd9d898-b7e7-47ba-835a-b36d6918de85)


📄 **Description**: This step configures the MySQL root user password during setup. The MySQL 5.5 instance was installed locally and secured with a password for later integration with osTicket.

---

## 🧠 Register PHP with IIS

Register PHP ![image](https://github.com/user-attachments/assets/af5800bc-80af-4785-8214-9038d4fd1166)


📄 **Description**: Using PHP Manager for IIS, the PHP CGI executable was registered to enable server-side processing of PHP files. This path points to the version extracted from the installation folder.

---

## 📂 Move osTicket Files to IIS Root

osTicket Upload Directory ![image](https://github.com/user-attachments/assets/b3a5dcbc-4529-43bf-96e3-ae457e01333b)


📄 **Description**: The `upload` folder from the osTicket installation package was moved into the `C:\inetpub\wwwroot` directory. This folder contains all the core web files needed to launch the web installer.

---

## 🏷️ Rename Upload Folder

Rename to osTicket ![image](https://github.com/user-attachments/assets/6db1fd10-f53a-424f-81fd-089d642844e9)


📄 **Description**: After copying, the folder was renamed from `upload` to `osTicket` for a cleaner URL and clearer identification during the installation process.

---

## ✅ Verify PHP Extensions & Prereqs

Installer Prerequisites ![image](https://github.com/user-attachments/assets/9f4ebbb1-e846-45e7-baa9-3240248ffc72)


📄 **Description**: The osTicket setup page checks PHP version and required modules. Here, it confirms that PHP 8 and MySQLi are enabled, although some optional modules are missing.

---

## 🔁 Fix Extensions & Reload Installer

All Prereqs Pass ![image](https://github.com/user-attachments/assets/6aaa7e7a-c202-485a-b210-c9db29f50a9a)


📄 **Description**: After installing or enabling missing PHP extensions, this refreshed page shows all requirements passed. The system is now ready to proceed with the installation.

---

## 🛠️ Finalize Se

Installation Confirmation ![image](https://github.com/user-attachments/assets/233fb87e-def2-4333-905a-e38b1e9924e1)


📄 **Description**: This screen confirms the installation is complete. It provides URLs to the Support Center and Staff Control Panel, and reminds users to remove write permissions on the config file for security.

---

## 🧩 Verify Database Configuration

![Database Tables in HeidiSQL](

📄 **Description**: This screenshot shows the populated `osticket` database in HeidiSQL. It includes all system tables created during setup, confirming successful MySQL integration.

---

## 🎟️ View Admin Panel

![Staff Control Panel](

📄 **Description**: The Staff Control Panel is accessible via `localhost/osTicket/scp`. It shows the default support ticket created upon installation, validating successful admin access.

---

## 👥 View Support Center

![Customer Support Portal]

📄 **Description**: The front-end user interface of osTicket is shown here, where users can submit new tickets and check ticket statuses. This verifies the help desk system is fully operational.
