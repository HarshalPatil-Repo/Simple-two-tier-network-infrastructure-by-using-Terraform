
# Simple AWS network infrastructure by using Terraform



## Following resources are created by using above code:

- VPC
- Public and Private Subnets
- Internet Gateway
- NAT Gateway
- Main and Custom Route Tables
- Instance in public as well as private subnet
- Security Group
- Key-Pair



## This network infrastructure allows :

- Ingress SSH, HTTP, HTTPS and egress all traffic via internet gateway to EC2 instance in public subnet
- Egress traffic to internet via NAT gateway from private subnet
- Local traffic in VPC (10.10.0.0/16) via local routes

## Steps to run the code :

1. Configure IAM user using AWS CLI
2. Copy terraform code in one folder
3. Open VS Code in that folder and open terminal in VS code
4. Run command 'terraform init'
5. After that run command 'terraform plan'
6. Give key pair name
7. Run command 'terraform apply' and again enter key-pair name and give approval
8. After successful resource creation add '.pem' extenstion in key name which is saved in local
9. While connecting to instance change key permission using 'chmod 400 {key name}' if you are using Linux or MacOS
10. To change key permission for Windows, follow this youtube video:
https://www.youtube.com/watch?v=OTwEfZP1nb8


Resources will be created by following above steps


11. To clean up run command 'terraform destroy' this will delete all the created resources


    