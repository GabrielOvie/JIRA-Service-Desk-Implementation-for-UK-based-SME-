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

## Email Integration Setup
