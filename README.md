## aws-efs-benchmark

This ansible role can be used to benchmark EFS file systems.

The process happens in five phases.

- 
- 
-
-
-
-

----

## Prerequisites

- Ansible version 2.3 or higher
- boto and boto3

----

## Installation

Clone the project using git:

```bash
$ sudo pip install boto boto3
$ mkdir -p ~/ansible/roles/; cd $_
$ git clone ssh://git.amazon.com/pkg/Aws-efs-benchmark
```

----

## Configuration

All variables are set in vars/vars.yml:

```yaml
# AWS Credentials
aws_access_key: "xxxxx"
aws_secret_key: "xxxxx"
aws_region:     "eu-west-1"

# VPC Information
vpc_name:       "aws-efs-benchmark"
vpc_cidr_block: "10.0.0.0/16"

# For Security Group Rule
my_ip:          "0.0.0.0"

# Subnets
public_subnet_1_cidr:  "10.0.1.0/24"

# key_name:
ssh_key_name: "id_rsa"

# AMI Name:
ami_id: "ami-d7b9a2b1"
#ami_id: "ami-061b1560"
# Instance Type
type: "t2.micro"

# Instance Count
count_number: "1"

#Public Adrees
yon: "yes"

ec2_tag_Name: "aws_efs_benchmarky"
ec2_tag_Type: "benchmark"
ec2_tag_Environment: "load_generator"
```

----

## Running

Run this role using the ansible-playbook command:

```bash
$ ansible-playbook /etc/ansible/roles/aws-efs-benchmark/role.yml
```

----

## Licence

This project is licensed under the Apache license. See included LICENSE.md.