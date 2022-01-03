Deploying Services
=========

By running this role you will be deploying a Virtual Private Cloud with two subnets and an Internet Gateway also a RDS subnet group for your rds db instance which will also be created on your AWS cloud.

Requirements
------------
Install boto, botocore and boto 3 to run this role

Role Variables
--------------
aws_access_key: "your aws creds"
aws_secret_key: "your aws creds"
region: "e.g. us-east-1"
vpc_cidr: 
vpc_name: ""
igw_name: "Traffic IGW"
securitygroup_name: "Ansible Security Group"
ec2_tag: "WebServer"
#The local path to which we would save our EC2 Private Key
ec2_key_directory: "/home/ansible/roles/aws-vpc/"
keypair_name: "ec2_key_pair

Example Playbook
----------------
[playbook.yaml]

    - hosts: localhost or target
      roles:
         - aws-deploy



