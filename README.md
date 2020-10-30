# ValtixLabs AWS

This AWS CloudFormation template creates a demo environment for use with Valtix gateway deployments.  This template deploys: 
- 1 VPC
- 2 Public Subnets & 2 Private Subnets
- 1 Public SG & 1 Private SG
- Bastion EC2 instance
- 1 App instance per Availability Zone running web server with simple hello world html
- private key is injected into jump instances to ssh to the backend instances

*(Note) The private subnet route table has a default route for the internet gateway in order to download updates and install apache.  After deployment, please delete this default route on each private subnet*

## How to use:
Download the quickstart.yml template file and open CloudFormation in AWS console and upload the file and deploy the stack<br>
In order to connect to the App instances from the Bastion instance, create the SSH private key for your keypair to the Bastion instance.  

### Deploy Valtix gateways
You can now deploy the Valtix gateways to secure the applications in this VPC.  Please refer to the following tutorial here for reference:
https://prod1-dashboard.vtxsecurityservices.com

## Resulting diagram
<img src="https://raw.githubusercontent.com/valtix-security/valtixlabs-aws/master/ValtixLabs-AWS.png">

