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
<img width="1920" height="1200" alt="Screenshot 2026-11-22 152704" src="https://github.com/user-attachments/assets/c2d0c7a1-8bcf-4f9b-818c-bfd3951a8312" />
<img width="1920" height="1084" alt="Screenshot 2026-11-22 160701" src="https://github.com/user-attachments/assets/bd41c8c3-a709-4f57-a73c-21bc6ec84f43" />
<img width="1920" height="1146" alt="Screenshot 2026-11-22 164621" src="https://github.com/user-attachments/assets/99d0a011-fd28-4b3d-aa6c-37194c94ee65" />
<img width="1920" height="1145" alt="Screenshot 2026-11-22 165745" src="https://github.com/user-attachments/assets/c6fb10b8-b5d0-45e7-8763-301a18341a97" />
<img width="1920" height="1145" alt="Screenshot 2026-11-22 164458" src="https://github.com/user-attachments/assets/eb7f0f93-93a2-4eb1-a528-adede50fcbec" />
<img width="1920" height="1200" alt="Screenshot 2026-11-22 161904" src="https://github.com/user-attachments/assets/b4121074-1be8-4469-a649-dc7eae8fe699" />
<img width="1920" height="1200" alt="Screenshot 2026-11-22 161533" src="https://github.com/user-attachments/assets/cf3fd115-393c-4e45-8c50-bd79c573b9a1" />



---


## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
