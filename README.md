# Hosting Nginx docker image on Amazon EC2

This repository contains a set of Packer scripts and CloudFormation templates to build and deploy an EC2 instance which runs the Nginx Docker image with it. The Nginx server is securely exposed for public access.

First, create the Base AMI using the Packer scirpts.
Once the AMI is created, create the CloudFormation stack with the AMI ID to create the EC2 instance.

Refer to the README file of each sub directory for more details.