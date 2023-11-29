# AWS Cloud Computing Lab: EC2 Deployment

## Overview

This repository contains the documentation and scripts for a lab exercise completed as part of the ALX AWS Cloud Computing Course. The lab, conducted in a sandbox environment, focuses on deploying a web server using Amazon Elastic Compute Cloud (EC2) instances.

## Lab Duration

Approximately 30 minutes

## Lab Tasks

### Task 1: Launch EC2 Instance

1. Access the AWS Management Console
2. Launch an EC2 instance with Amazon Linux
3. Configure network settings, security groups, and storage

### Task 2: Install Web Server

1. Connect to the EC2 instance
2. Run a script to install Apache Web Server and PHP

## Accessing the Web Server

1. Wait until the EC2 instance status shows 2/2 checks passed
2. Copy the Public IPv4 DNS from the AWS console
3. Open a web browser and paste the DNS to view the web page

## Repository Structure

- `/scripts`: Contains scripts used in the lab
- `/images`: Screenshots or diagrams related to the lab
- `/docs`: Additional documentation or insights gained during the lab

## Lab Scripts

### Install Web Server Script

```bash
#!/bin/bash
# Install Apache Web Server and PHP
dnf install -y httpd wget php mariadb105-server
# Download Lab files
wget https://aws-tc-largeobjects.s3.us-west-2.amazonaws.com/CUR-TF-100-ACCLFO-2/2-lab2-vpc/s3/lab-app.zip
unzip lab-app.zip -d /var/www/html/
# Turn on web server
chkconfig httpd on
service httpd start
```

## Resources

AWS Documentation

https://aws.amazon.com/ec2/?nc2=h_ql_prod_fs_ec2

ALX AWS Cloud Computing Course

## Lab Complete
