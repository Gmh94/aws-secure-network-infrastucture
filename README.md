# Secure AWS Network Infrastructure

## Project Overview

Designed, deployed, and tested a secure AWS network environment using Amazon VPC, EC2, IAM, Linux, and Apache HTTP Server.

This hands-on project demonstrates foundational cloud engineering skills, including network segmentation, security group configuration, IAM-based server management, and web server deployment.

## Technologies Used

- Amazon Web Services (AWS)
- Amazon VPC
- Amazon EC2
- AWS Identity and Access Management (IAM)
- AWS Systems Manager Session Manager
- Amazon Linux 2023
- Apache HTTP Server
- Linux CLI

## Network Architecture

| Component | Configuration |
|---|---|
| VPC | 10.0.0.0/16 |
| Public Subnet | 10.0.1.0/24 |
| Private Subnet | 10.0.2.0/24 |
| Internet Gateway | Attached to VPC |
| Public Route Table | Default route to Internet Gateway |
| Public Security Group | HTTP port 80 allowed |
| Private Security Group | No inbound or outbound rules |
| EC2 Instance | Amazon Linux 2023 |
| Server Management | AWS Systems Manager Session Manager |

## Implementation

1. Created a custom AWS VPC with public and private subnets.
2. Configured an Internet Gateway and public route table.
3. Implemented security groups for public and private resources.
4. Launched an Amazon Linux EC2 instance in the public subnet.
5. Configured an IAM instance role for Systems Manager.
6. Installed and configured Apache HTTP Server.
7. Created and deployed a custom HTML webpage.
8. Verified local and public HTTP connectivity.

## Security Considerations

- Used separate public and private subnets for network segmentation.
- Restricted public inbound access to HTTP port 80.
- Used Session Manager rather than exposing SSH port 22.
- Configured an IAM role with Systems Manager permissions.
- Created a private security group with no inbound or outbound access.
- Used HTTP for temporary demonstration purposes; production deployment would require HTTPS.

## Troubleshooting

During deployment, the website was accessible locally but initially timed out when accessed through a browser.

Investigated:

- EC2 security group inbound rules
- Internet Gateway routing
- Public subnet associations
- Network ACL inbound and outbound rules
- Browser HTTP versus HTTPS behavior

Successfully accessed the deployed website using HTTP on port 80.

## Results

Successfully deployed a publicly accessible Apache webpage hosted on Amazon EC2 inside a custom AWS VPC.

Validated cloud networking, Linux administration, IAM-based access, and basic infrastructure troubleshooting.

## Future Improvements

- Automate infrastructure deployment using Terraform.
- Implement HTTPS using a valid TLS certificate.
- Add monitoring and centralized logging.
- Expand infrastructure across multiple Availability Zones.
- Implement automated deployment pipelines.
