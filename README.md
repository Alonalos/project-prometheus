# Project Prometheus Setup Instructions

Follow these steps to set up your environment and launch the infrastructure.

---

## **1. Create an EC2 Ubuntu Instance**

1. Launch an EC2 instance with an Ubuntu image.
2. Assign a role to the instance to ensure it has access to **EC2** and **VPC** resources.
   - Alternatively, you can create **AWS access keys** and set them up as environment variables:
     ```bash
     export AWS_ACCESS_KEY_ID="your_access_key"
     export AWS_SECRET_ACCESS_KEY="your_secret_access_key"
     ```

---

## **2. Generate a Key Pair**

- Generate an SSH key pair to use for secure access to your EC2 instance.

---

## **3. Configure Terraform Variables**

1. Navigate to the `terraform` folder.
2. Create a file named `terraform.tfvars` and populate it with the following variables:

    ```hcl
    region        = "us-east-2"
    vpc_cidr      = "10.0.0.0/16"
    subnet1_cidr  = "10.0.1.0/24"
    subnet2_cidr  = "10.0.2.0/24"
    subnet3_cidr  = "10.0.3.0/24"
    ip_on_launch  = true
    instance_type = "t2.micro"
    ```

---

## **4. Run the Script**

- Execute the setup script to provision the infrastructure:
  ```bash
  ./script.sh
