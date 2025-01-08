# project-prometheus
Setup Instructions
Create EC2 Ubuntu Instance and assign a role to make sure your Instance has access to EC2 and VPC resources or create access and secret keys and run:
export AWS_ACCESS_KEY_ID="your_acces_key"
export AWS_SECRET_ACCESS_KEY="your_secret_acces_key"
Generate key pair
Create terraform.tfvars file in terraform folder
region = "us-east-2"
vpc_cidr = "10.0.0.0/16"
subnet1_cidr = "10.0.1.0/24"
subnet2_cidr = "10.0.2.0/24"
subnet3_cidr = "10.0.3.0/24"
ip_on_launch = true
instance_type = "t2.micro"
Run ./script.sh