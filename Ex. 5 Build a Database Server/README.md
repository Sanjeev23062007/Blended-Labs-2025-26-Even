# Lab 5 – Build a Database Server (AWS)

## Author

* **Name**: Sanjeev A
* **Register Number**: 212224230246
* **Date of Submission**: 21.11.2026

---

## Objective

The objective of this experiment is to understand how to deploy and configure a database server in AWS. This lab focuses on launching an EC2 instance, installing a database management system (DBMS), configuring basic database settings, creating a sample database, and validating connectivity to the database server.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing VPC and EC2 knowledge (from previous labs)
* Basic knowledge of Linux commands and SQL

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Security Groups
* SSH Client (Terminal / PuTTY)
* MySQL / MariaDB / PostgreSQL (any one)

---

## Tasks Performed

### Task 1: Launch EC2 Instance for Database Server

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type and configure key pair and security group.

---

### Task 2: Configure Security Group for Database Access

Modify the security group to allow:

* SSH (Port 22) for remote access
* Database port (e.g., MySQL – 3306 or PostgreSQL – 5432)

---

### Task 3: Connect to EC2 Instance

Connect to the EC2 instance using SSH from your local machine.

---

### Task 4: Install Database Server

Install a database server software such as MySQL, MariaDB, or PostgreSQL on the EC2 instance using package manager commands.

---

### Task 5: Start and Configure Database Service

Start the database service and configure basic settings such as root password and user privileges.

---

### Task 6: Create a Sample Database

Create a sample database and a table inside it. Insert a few records into the table.

---

### Task 7: Test Database Connectivity

Test the database server by connecting to it locally or remotely and performing basic SQL queries.

---

## ## Workflow (Student Explanation)

1. Created a security group for the RDS database and configured MySQL/Aurora access on port 3306 from the Web Security Group.

2. Created a DB subnet group using the Lab VPC and selected subnets from two Availability Zones for the database.

3. Created a MySQL Amazon RDS instance named `lab-db` with the required database, username, password, storage, instance class, VPC, and security group settings.

4. Waited for the RDS instance to become available and obtained its endpoint and connectivity details from the RDS console.

5. Opened the provided WebServer application, selected the RDS option, entered the database endpoint and credentials, and connected to the database to display and interact with the Address Book data.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Instance for Database Server

<img width="1920" height="1200" alt="Screenshot 2026-11-21 083909" src="https://github.com/user-attachments/assets/73fe962e-6a44-4947-a7bf-beffdba7ed48" />


---

### Screenshot 2: Database Service Running

<img width="1920" height="1200" alt="Screenshot 2026-11-21 083919" src="https://github.com/user-attachments/assets/9f38d506-9831-4ac7-a7aa-6b727c300834" />


---

### Screenshot 3: Sample Database and Table

<img width="1920" height="1200" alt="Screenshot 2026-11-21 084739" src="https://github.com/user-attachments/assets/26f60db1-897c-494f-8a2c-c911e917253b" />


---

## Result

This experiment demonstrated how to build a database server in AWS using an EC2 instance. By installing and configuring a DBMS, creating a sample database, and testing connectivity, the fundamentals of hosting and managing a cloud-based database server were underst
