# Build Your VPC and Launch a Web Server (AWS) 

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

## Tools Used<img width="1247" height="606" alt="687753120-ad01a1bf-085b-4758-96da-25ca51ad033f" src="https://github.com/user-attachments/assets/47bdf393-d50a-4918-a082-2f50aa70a7da" />


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
