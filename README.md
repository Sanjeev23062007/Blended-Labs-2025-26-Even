# Blended-Labs
# Lab 1 - Introduction to AWS Identity and Access Management (IAM)

## Title
Introduction to AWS Identity and Access Management (IAM)


## Objective
The objective of this lab is to understand how AWS Identity and Access Management (IAM) controls authentication and authorization in AWS. The lab focuses on exploring IAM users and groups, analyzing attached policies, assigning users to appropriate groups based on organizational roles, and validating permissions by testing service access.


## Prerequisites
- Basic understanding of cloud computing concepts  
- AWS Academy Lab access  
- Web browser with internet connectivity  


## Tools Used
- AWS Management Console  
- AWS Identity and Access Management (IAM)  
- Amazon EC2  
- Amazon S3  


## Tasks Performed

### Task 1: Explore IAM Users and Groups
- Reviewed pre-created IAM users: user-1, user-2, user-3  
- Explored IAM groups: EC2-Admin, EC2-Support, S3-Support  
- Inspected managed and inline policies attached to groups  
**Screenshot:**  
<img width="1912" height="836" alt="Screenshot 2026-10-29 130335" src="https://github.com/user-attachments/assets/30f163ff-5453-479e-8f61-89028b1fc187" />



### Task 2: Add Users to Groups
- Added user-1 to the S3-Support group  
- Added user-2 to the EC2-Support group  
- Added user-3 to the EC2-Admin group  
**Screenshot:**  
<img width="1917" height="1136" alt="Screenshot 2026-10-29 132721" src="https://github.com/user-attachments/assets/9db2e6c9-f7c8-4edd-a770-bf6590acd1f5" />


### Task 3: Test IAM User Permissions
- Logged in using IAM sign-in URL  
- Verified S3 access for user-1  
- Verified EC2 read-only access for user-2  
- Verified EC2 administrative access for user-3  
**Screenshot:**  
<img width="1917" height="1198" alt="Screenshot 2026-10-29 133205" src="https://github.com/user-attachments/assets/b4ef55c7-13cf-4aa3-a9e2-f47e6610bf88" />



## Workflow
1. Accessed IAM console and reviewed users and groups.  
2. Inspected policy permissions attached to groups.  
3. Assigned users to groups based on their roles.  
4. Logged in as each IAM user using the sign-in URL.  
5. Validated permissions by accessing AWS services.  


## Learning Outcomes
- Understood the role of IAM in AWS security.  
- Learned how IAM users, groups, and policies interact.  
- Gained practical experience implementing role-based access control.  
- Verified permission enforcement through real-time service testing.  


## Conclusion
This lab provided hands-on experience with AWS IAM by demonstrating how organizations manage secure access to cloud resources. Assigning users to groups with predefined policies simplified permission management and ensured role-based access control across AWS services.


## Author
**Name:** Sanjeev A and (212224230246)
**Course:** Introduction to Cloud Computing  


# Ex. 2 Build your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: Sanjeev A
* **Register Number**: 212224230246
* **Date of Submission**: 29.10.2026
---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

1.A Virtual Private Cloud (VPC) was designed and created with the CIDR block 10.0.0.0/16 to establish a secure and isolated network environment within AWS.

2.A public subnet was configured within the VPC with the CIDR range 10.0.1.0/24, and auto-assign public IPv4 addresses was enabled to allow internet connectivity for instances.

3.An Internet Gateway was created and attached to the VPC, followed by the setup of a route table with a default route (0.0.0.0/0) pointing to the gateway, and the route table was associated with the public subnet.

4.A security group was established to permit inbound SSH (port 22) and HTTP (port 80) traffic, and an EC2 instance was launched using the Amazon Linux 2 AMI, associated with the security group and a key pair.

5.The Apache HTTPD web server was installed and started on the EC2 instance, a simple HTML webpage was created, and its accessibility was verified through the public IP address of the instance via a web browser.


---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details


<img width="1247" height="606" alt="687753120-ad01a1bf-085b-4758-96da-25ca51ad033f" src="https://github.com/user-attachments/assets/86e82c08-9734-4eca-bbba-06f9552b82a4" />

---

### Screenshot 2: EC2 Instance Running

<img width="1255" height="634" alt="687753360-5b8c84d5-ebdd-4e34-b97b-44b33476206d" src="https://github.com/user-attachments/assets/482c290d-bc8c-407f-bcf5-fbe16ddcebfe" />
---

### Screenshot 3: Web Server Output in Browser

<img width="1170" height="710" alt="687753705-c53b8670-2271-4ac2-99a6-6aa6270b1be9" src="https://github.com/user-attachments/assets/a70e1c65-9e83-411d-9e26-bff4f6d1a6a5" />

---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.


# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

Name: Sanjeev A

Register Number: 21222420246

Date of Submission: 20.11.2026

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

- Basic understanding of cloud computing concepts
- AWS account or AWS Academy Lab access
- Web browser with internet connectivity
- Basic knowledge of Linux commands (optional)

---

## Tools Used

- AWS Management Console
- Amazon EC2
- Key Pair
- Security Group
- SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

- SSH (Port 22) from your IP address
- HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

ssh -i "keyname.pem" ec2-user@<Public-IP>

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

- Stop the instance
- Start the instance
- Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Output Screenshots

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1230" height="595" alt="image" src="https://github.com/user-attachments/assets/0e515995-cb0f-4f7a-a8bc-814bdc56ca10" />

---

### Screenshot 2: SSH Connection to Instance

<img width="1187" height="637" alt="image" src="https://github.com/user-attachments/assets/24f36212-0505-4c0e-ae30-830ee77696bf" />


<img width="1920" height="1200" alt="565000924-1ba4796f-c26e-4088-ac80-31795160b9cc" src="https://github.com/user-attachments/assets/9357b9a2-d043-4c5f-8ab9-33122e34c868" />


---

### Screenshot 3: Instance Monitoring / Status

<img width="1231" height="612" alt="Screenshot 2026-11-18 181031" src="https://github.com/user-attachments/assets/99d4ff80-cbfd-4c64-b24f-b567e277f7d3" />

---

## Result

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.

# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: Sanjeev A
* **Register Number**: 21222420246
* **Date of Submission**: 20.11.2026

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

1. Create a 1 GiB gp2 EBS volume in the AWS EC2 console.
2. Attach the EBS volume to the running EC2 instance as /dev/sdb.
3. Connect to the EC2 instance using AWS Systems Manager Session Manager.
4. Format the attached volume using the ext3 filesystem.
5. Create the /mnt/data-store directory and mount the EBS volume.
6. Configure /etc/fstab for persistent mounting of the EBS volume.
7. Verify the mounted volume using the df -h command.
8. Create a test file in /mnt/data-store and verify its contents.
9. Verify that the data remains available after remounting/rebooting the instance.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="1920" height="1200" alt="Screenshot 2026-11-03 115313" src="https://github.com/user-attachments/assets/46ea6730-e165-48fc-a95c-32aef38fc1d2" />

---

### Screenshot 2: EBS Volume Attached to EC2

<img width="1920" height="1200" alt="Screenshot 2026-11-03 120040" src="https://github.com/user-attachments/assets/12068d23-49f2-46f3-b694-dd71047f4cac" />

---

### Screenshot 3: Mounted Volume with Data

<img width="1920" height="1200" alt="Screenshot 2026-11-03 121343" src="https://github.com/user-attachments/assets/7fd6b215-e7e8-4cf3-8739-b2303da34184" />
<img width="1920" height="1139" alt="Screenshot 2026-11-03 122455" src="https://github.com/user-attachments/assets/7c845a4a-a036-4062-a8cf-227577ecdac7" />


---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.


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

This experiment demonstrated how to create and configure a MySQL database using Amazon RDS. The database was connected to a web application, and sample data was successfully stored and displayed.

# Lab 6 – Scale and Load Balance Your Architecture

## Author

* **Name**: Sanjeev A
* **Register Number**: 212224230246
* **Date of Submission**: 22.11.2026

---

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow (To be filled by Student)
1. Created an Amazon Machine Image (AMI) named WebServerAMI from the existing Web Server 1 instance.
2. Created a target group named LabGroup and configured it to use the Lab VPC.
3. Created an Application Load Balancer named LabELB using the two public subnets and Web Security Group.
4. Created a launch template named LabConfig using WebServerAMI, t2.micro, vockey key pair, and Web Security Group.
5. Created an Auto Scaling Group named Lab Auto Scaling Group with a desired capacity of 2, minimum of 2, and maximum of 6 instances.
6. Attached the Auto Scaling Group to the LabGroup target group and configured target tracking based on average CPU utilization of 60%.
7. Verified that two Lab Instance instances were launched and became healthy in the target group.
8. Accessed the web application through the Load Balancer DNS name to verify load balancing.
9. Used CloudWatch to monitor CPU utilization and triggered a load test.
10. Verified that Auto Scaling automatically launched additional instances when CPU utilization increased.
11. Terminated the original Web Server 1 instance after completing the test.
12. Submitted the lab and checked the final result.

---

## Output Screenshots 
<img width="1920" height="1200" alt="Screenshot 2026-11-22 152704" src="https://github.com/user-attachments/assets/67f2d220-95ee-4c33-b5be-4b58a32368e7" />
<img width="1920" height="1084" alt="Screenshot 2026-11-22 160701" src="https://github.com/user-attachments/assets/5402a5d6-6096-4209-8638-3253b748f3ee" />
<img width="1920" height="1200" alt="Screenshot 2026-11-22 161533" src="https://github.com/user-attachments/assets/afc6f23f-726a-4bc2-aaf1-0c4b7075d802" />
<img width="1920" height="1200" alt="Screenshot 2026-11-22 161904" src="https://github.com/user-attachments/assets/ce15560d-5a34-4b8f-bb21-9bbe1cdb15fa" />
<img width="1920" height="1145" alt="Screenshot 2026-11-22 164458" src="https://github.com/user-attachments/assets/ef4c2e56-0f93-40b4-95d2-4f24868d0522" />
<img width="1920" height="1145" alt="Screenshot 2026-11-22 164458" src="https://github.com/user-attachments/assets/6880a37a-0663-4d7f-9fa8-3d74a15f4f9e" />
<img width="1920" height="1146" alt="Screenshot 2026-11-22 164621" src="https://github.com/user-attachments/assets/b0ecf81d-0bd9-4ded-a33a-cdfa6774f801" />
<img width="1920" height="1145" alt="Screenshot 2026-11-22 165745" src="https://github.com/user-attachments/assets/3ab2a243-c83b-4ef4-a841-aca8b36eb71c" />



---


## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
