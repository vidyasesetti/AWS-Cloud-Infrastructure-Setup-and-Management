# AWS Cloud Infrastructure Setup and Management

This repository contains the code and documentation for setting up and managing a cloud infrastructure using AWS services. This project was developed during an AWS hackathon and demonstrates the use of various AWS tools to create a scalable, secure, and highly available infrastructure.

## Project Overview

### Network Creation
- **VPC Creation**: Created a Virtual Private Cloud (VPC) with specified IP address ranges.
- **Subnet Configuration**: Set up subnets within the VPC.
- **Route Tables**: Configured route tables for directing network traffic.
- **Internet Gateway**: Created and attached an internet gateway to the VPC.
- **NAT Gateway**: Set up NAT gateways for routing traffic from private subnets.

### Project Creation
- **Elastic File System (EFS)**: Created an EFS for shared storage.
- **EC2 Instances**: Launched instances, including a jump bastion instance and a web server.
- **Load Balancer**: Created an Elastic Load Balancer for distributing traffic.
- **Launch Template**: Created a launch template for EC2 instances.
- **Auto Scaling Group**: Configured an auto-scaling group linked with the load balancer.
- **Python-Django App**: Deployed a Python-Django application using Git and GitHub, running on an EC2 instance.

### Database Connectivity
- **Jump/Bastion Instance**: Launched and connected a jump bastion instance to a database instance.
- **Security Groups**: Configured security groups for secure network traffic.
- **Database Connection**: Connected to the database instance from the jump bastion instance.

### Interacting Infrastructure
- **NACL Creation**: Created and configured Network Access Control Lists (NACLs) for subnets.
- **Subnet Associations**: Associated NACLs with subnets to control traffic.

## Repository Structure

```plaintext
(my_proj)/
|── Lib/site-packages/
|     └── various packages and dependencies
|── Scripts/
|     └── various scripts and executables for the virtual environment
|── pyvenv.cfg/
my_proj/
|── my_proj/
|     ├── __init__.py
|     ├── asgi.py
|     ├── settings.py
|     ├── urls.py
|     └── wsgi.py
|── myapp/
|     ├── __init__.py
|     ├── admin.py
|     ├── apps.py
|     ├── models.py
|     ├── tests.py
|     ├── urls.py
|     └── views.py
|── static/
|     └── static files (e.g., images)
|── templates/
|── db.sqlite3
|── manage.py
```
# Description of Key Files and Directories

- **Lib/site-packages/**: Contains the installed packages and dependencies for the Python virtual environment.
- **Scripts/**: Contains various scripts and executables for the virtual environment.
- **pyvenv.cfg**: Configuration file for the virtual environment.
- **my_proj/**: Contains the main Django project files, including settings, URLs, and WSGI configuration.
- **myapp/**: Contains the application-specific files, such as models, views, URLs, and admin configurations.
- **static/**: Contains static files such as images.
- **templates/**: Contains template files for the Django project.
- **db.sqlite3**: SQLite database file.
- **manage.py**: Django's command-line utility for administrative tasks.

# How to Run

## 1.Clone the Repository

```sh
git clone https://github.com/vidyasesetti/AWS-Cloud-Infrastructure-Setup-and-Management.git
cd AWS-Cloud-Infrastructure-Setup-and-Management
```
## 2.SetUp AWS Infrastructure
- Follow the steps to create VPC, subnets, route tables, internet gateway, and NAT gateway.
- Launch EC2 instances and configure security groups.
## 3.Deploy Python-Django Application

```sh
python manage.py runserver 0.0.0.0:8000
```
## 4.Setup Load Balancer and Auto Scaling
- Follow the steps to create a load balancer and configure auto-scaling groups.
## 5.Connect to Database
- Use a jump bastion instance to securely connect to the database instance.

# Conclusion
This project demonstrates the comprehensive setup and management of AWS cloud infrastructure, incorporating network setup, instance management, load balancing, auto-scaling, and secure database connectivity. It serves as a practical guide for deploying scalable and secure applications on AWS.

