# JIRA Service Desk Virtual Lab Setup Guide

## Table of Contents
1. [Virtual Environment Setup](#virtual-environment-setup)
2. [JIRA Installation](#jira-installation)
3. [Database Configuration](#database-configuration)
4. [JIRA Configuration](#jira-configuration)
5. [Email Integration Setup](#email-integration-setup)

## Virtual Environment Setup
1. Download and install VirtualBox 
2. Create a new VM with the following specifications:
   - Name: JIRA-ServiceDesk-Lab
   - Type: Linux
   - Version: Ubuntu (64-bit)
   - Memory: 4096 MB
   - Hard Disk: Create a virtual hard disk now
   - Hard disk file type: VDI
   - Storage on physical hard disk: Dynamically allocated
   - File location and size: 50 GB
3. Download Ubuntu Server 20.04 LTS ISO
4. Start the VM and install Ubuntu Server

## JIRA Installation
1. Update Ubuntu: sudo apt update && sudo apt upgrade
2. Install Java: sudo apt install openjdk-11-jdk -y
3. Download JIRA Service Desk
4. Install JIRA

## Database Configuration
1. Install MySQL: sudo apt install mysql-server -y
2. Secure MySQL installation: sudo mysql_secure_installation
3. Create JIRA Db --- sudo mysql -u root -p
CREATE DATABASE jiradb CHARACTER SET utf8mb4 COLLATE utf8mb4_bin;
CREATE USER jirauser@localhost IDENTIFIED BY your_password;
GRANT ALL PRIVILEGES ON jiradb.* TO jirauser@localhost;
FLUSH PRIVILEGES;
EXIT

## JIRA Configuration

1. Access JIRA setup wizard through your web browser: http://your_server_ip:8080
2. Choose "I'll set it up myself"
3. Configure your database:
- Database type: MySQL
- Hostname: localhost
- Port: 3306
- Database: jiradb
- Username: jirauser
- Password: your_password
4. Set up application properties:
- Application Title: [Your Company] IT Support
- Mode: Private
- Base URL: http://your_server_ip:8080
5. Set up administrator account
6. Set up email notifications (we'll use Postfix in the next section)
7. Finish setup and log in to JIRA

## Email Integration Setup
1. Install Postfix:
2. 2. Configure Postfix as a local SMTP server
3. In JIRA, go to Administration > System > Mail Server
4. Configure with the following settings:
- Name: Local Postfix
- From address: jira@your_domain.com
- Email Prefix: [JIRA]
- Protocol: SMTP
- Host Name: localhost
- SMTP Port: 25
5. Test the email configuration

## Service Desk Project Setup

1. Go to Projects > Create Project
2. Choose "IT Service Management" as the project template
3. Name your project "IT Support"
4. Configure request types:
- Hardware Issue
- Software Problem
- Network Access
- General Inquiry
5. Set up SLAs for each request type
6. Configure the customer portal

## Security and Performance Tuning

1. Enable HTTPS:
- Install Certbot: sudo apt install certbot python3-certbot-apache -y
- Obtain SSL certificate: sudo certbot --apache -d your_domain.com
2. Adjust Java heap settings in setenv.sh
3. Optimize database connection pool in dbconfig.xml
4. Set up regular backups:

