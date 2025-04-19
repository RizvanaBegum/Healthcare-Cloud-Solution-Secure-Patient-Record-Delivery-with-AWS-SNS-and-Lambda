# Healthcare Cloud Solution: Secure Patient Record Delivery with AWS SNS, Lambda, and VPC

## 📝 Project Overview
In the healthcare industry, safeguarding patient data and ensuring the confidentiality of medical records is paramount. This project addresses the need for secure, real-time access to patient records by leveraging AWS cloud services to build a scalable and secure platform for delivering medical reports via mobile push notifications.

The platform ensures that sensitive patient data is transmitted securely, leveraging **AWS VPC**, **SNS**, **Lambda**, and other AWS services to create a robust solution for patient record management.

## 🔐 Key Features

- ✅ **AWS CloudFormation for Infrastructure as Code**:
  - Deployed the entire infrastructure using **AWS CloudFormation**, allowing for easy replication, version control, and management of resources. The CloudFormation template provisions all necessary components for the secure delivery of medical reports.

- 🌐 **VPC Configuration for Secure Networking**:
  - Created a **VPC** (Virtual Private Cloud) with a **custom subnet**, **Internet Gateway (IGW)**, and **Route Table** to ensure secure networking. This isolated environment allows for safe communication between resources, enhancing security and reducing exposure to external threats.
  - **Security Groups**: Configured **Security Groups** for **EC2 instances** and other components, restricting access to internal communication within the VPC and SSH traffic from anywhere.

- 📩 **SNS Topics for Messaging**:
  - Configured two **SNS topics** (Simple Notification Service) to handle secure report publishing and notifications.
  - **SNS Endpoint**: Established private **VPC Endpoints** for SNS to avoid traffic exposure to the public internet, ensuring message privacy and secure delivery.

- 🖥️ **EC2 Instance for Hosting Logic**:
  - Deployed an **EC2 instance** inside the VPC, responsible for running the logic to handle medical report generation and messaging.
  - **Security Group** settings were fine-tuned to allow traffic only within the
