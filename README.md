# Web-Based Bookstore Deployment on AWS

This repository contains the deployment scripts and configuration files for hosting a web-based bookstore system on Amazon Web Services (AWS). The system is built using React for the front end, Java (JSP/servlet) for the backend, with Tomcat as the application server, and MySQL as the database.

## Basic Deployment

The basic deployment includes setting up two EC2 instances in a VPC:
- **Web Server**: Hosts the application server (Tomcat) and has internet access to serve the bookstore website to customers.
- **Database Server**: Hosts the MySQL database but is not accessible from outside networks.

## Advanced Deployment

The advanced deployment architecture includes:
- **Public Subnet**: Hosting the application server in the public subnet.
- **Private Subnet**: Hosting the database server in the private subnet to restrict external access.
- **Internet Gateway**: For internet access from the public subnet.
- **NAT Gateway**: Allows the private subnet to access the internet for updates and patches.

## Requirements

- Only HTTP/HTTPs, SSH, and MySQL traffic is allowed into the deployment.
- HTTP access from the network to the internet is allowed.
- Database is not accessible from outside networks.
- AWS free tier services are utilized as much as possible.

## AWS Services Used

- EC2 instances (t2.micro) running Amazon Linux 2023.
- VPC with public and private subnets.
- Software stack: Tomcat (version 10), MySQL, Java (11 or later)
