# Visualise-a-Relational-Database

## Overview

This project demonstrates how to set up a **Relational Database** using **Amazon RDS**, populate it with data using **MySQL Workbench**, and securely integrate it with **Amazon QuickSight** for data visualization. The aim of this project is to showcase the ability to manage a relational database in the cloud, perform basic SQL operations, and build secure data pipelines to visualize and analyze data using AWS services.

## Table of Contents

1. [Project Description](#project-description)
2. [Prerequisites](#prerequisites)
3. [Setup Guide](#setup-guide)
   - [Creating the RDS Database](#creating-the-rds-database)
   - [Connecting MySQL Workbench](#connecting-mysql-workbench)
   - [Connecting RDS to QuickSight](#connecting-rds-to-quicksight)
4. [Security Configuration](#security-configuration)
5. [Data Visualization](#data-visualization)
6. [Conclusion](#conclusion)
7. [License](#license)

---

## Project Description

In this project, we explore how to use **Amazon RDS (Relational Database Service)** for hosting a relational database, specifically **MySQL**, and how to use **Amazon QuickSight** for business intelligence (BI) and data visualization. The database is created and populated with SQL queries using **MySQL Workbench**, while QuickSight is used to generate dashboards and charts based on the data stored in RDS.

Key elements of this project:
- **Amazon RDS** for creating, managing, and scaling relational databases in the cloud.
- **MySQL Workbench** for interacting with and populating the RDS database.
- **Amazon QuickSight** for building interactive data visualizations and dashboards.

---

## Prerequisites

Before starting this project, you will need the following:
- An **AWS account** (to use Amazon RDS, QuickSight, and other services).
- **MySQL Workbench** installed on your local machine.
- Basic knowledge of **SQL**, **AWS services**, and **cloud security best practices**.

---

## Setup Guide

### Creating the RDS Database

1. **Log into AWS Console**: Navigate to the **RDS Dashboard**.
2. **Create a Database**:
   - Click on **Databases** > **Create Database**.
   - Select **MySQL** as the engine.
   - Choose instance settings (e.g., instance type, storage, etc.).
   - Enable public accessibility to allow external connections (optional, but required for testing).
3. **Configure Security**:
   - Set up a **Security Group** to control which IPs can access the database.
   - Ensure that your database is accessible only by trusted sources, like QuickSight and your application.

### Connecting MySQL Workbench

1. **Open MySQL Workbench**: Use the **RDS endpoint** (publicly accessible or private) to configure a new connection.
2. **Create Schema**: Once connected, create a schema (database) in MySQL.
3. **Create Tables and Insert Data**: Use **SQL queries** in MySQL Workbench to create tables and populate the database with sample data.

### Connecting RDS to QuickSight

1. **Log into Amazon QuickSight**: Navigate to **Datasets** > **New Dataset**.
2. **Select RDS** as the data source.
3. **Configure RDS Connection**: Provide the necessary details (database endpoint, security credentials, etc.) and validate the connection.
4. **Create Data Source**: Once the connection is validated, create the data source for QuickSight.

---

## Security Configuration

To ensure secure connections between services, I configured the following security measures:
1. **Security Groups**: 
   - Created security groups for both RDS and QuickSight.
   - Allowed inbound traffic from QuickSight’s IP range or VPC to the RDS instance.
2. **Encryption**: 
   - Used **SSL/TLS encryption** to secure data transmission between MySQL Workbench, RDS, and QuickSight.
3. **Restricted Access**:
   - Initially, the RDS instance was publicly accessible for testing purposes. However, after completing the setup, I made the RDS instance **private** and configured necessary inbound and outbound rules to restrict access.

---

## Data Visualization

1. **Data Transformation**: Once QuickSight was connected to the RDS data source, I started creating various **visualizations** such as:
   - **Bar charts**, **line graphs**, and **pie charts** to represent business metrics.
   - **Dashboards** for a comprehensive view of the data.
2. **Interactive Insights**: The data visualizations were interactive, enabling detailed analysis and reporting based on real-time data from the RDS instance.

---

## Conclusion

In this project, we set up a **fully managed MySQL relational database** on **Amazon RDS**, populated it with data, and integrated it with **Amazon QuickSight** for data analysis and visualization. We also ensured the security of the database by configuring **security groups** and **encrypted connections**. This project demonstrates the power of combining cloud database management, business intelligence, and security best practices on AWS.

---
