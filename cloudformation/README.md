# CloudFromation Stack

This directory contains the CloudFormation templates to provision the required AWS infrastructiore to run the application deployment.
<br>

## Parameters:
<br>

Upload the templates to an S3 bucket first. Then the stack needs to be created using the S3 URL to the "main.yaml"

The parameters need to be set correctly in the "main.yaml" before creating the stack

| Variable | Definition |
| ------ | ------ |
|CfnBucketUrl| The S3 bucket URL where the templates are uploaded|
|VpcBlock| CIDR block for the VPC|
|PublicSubnet01Block| CIDR block for the Public Subnet|
|BaseAmi| The base AMI ID which is built with the provided Packer scripts|
|InstanceType| The EC2 instance type|
|SshKeyName| SSH Key pair name to be attached with the EC2 instance. This has to be pre-created|

<br>

## Create Stack:

<br>

Once the parameters are set, use the AWS CLI or the AWS Console to:
- Upload the templates to the S3 bucket
- Create / Update the stack
    