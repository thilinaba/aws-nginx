# Building the EC2 base image

Set the values in "variables.json" accoirding to your AWS account

| Variable | Definition |
| ------ | ------ |
| profile | The AWS CLI Profile which you use to run Packer with. Refer to the  "Setup AWS CLI" section of the [Blog Post](https://medium.com/cloud-life/building-a-cis-hardened-ami-on-aws-for-free-87b482b52ccb) more info  |
| region | The region in which the AMI to be built |
| source_ami | The respective Ubuntu 22.04 base AMI ID for your region. Refer to "Building the AMI" section of the [Blog Post](https://medium.com/cloud-life/building-a-cis-hardened-ami-on-aws-for-free-87b482b52ccb) more info |
| vpc_id | The VPC ID in which the resources to be created |
| subnet_id | A Public subnet which Packer can create the temporary resources for the build |
| instance_type | Packer will use an EC2 instance with the type mentioned here to build the AMIs. However, you can use the resulting AMI with any type of instance later. Keep the default “t3.micro” to stay within the Free tear, unless there is a specific requirement. |
| ami_name_prefix | The resulting AMI will be named with this prefix and a timestamp. You can change this to a preferred name or keep it as default. |

<br>

## More info:

This packer script will build a security hardened Ubuntu base image and install Docker engine on top of it.
Please refer to my [Original Repository](https://github.com/thilinaba/aws-cis-ami) and the [Blog Post](https://medium.com/cloud-life/building-a-cis-hardened-ami-on-aws-for-free-87b482b52ccb) for a detailed guideline of how to customize and use this template.

Please note that in the [Original Repository](https://github.com/thilinaba/aws-cis-ami), this Packer script was created to build Amazon Linnux 2 AMIs and it is not fully tested on Ubunut 22.04 yet. Feel free to contribute if you see any issues. 