### Cloud-Native Node.js API on Google Cloud Platform using IaC

This project focuses on a user management system with a robust backend to efficiently create, update, and delete user accounts while ensuring scalability through cloud technology. The system supports CRUD operations, making it dynamic and user-friendly. By integrating with GCP, it offers secure account verification along with automated email notifications to update users on their account status.

### About this Repository

This repository contains the code for developing a cloud-native web application. It explains how to create a machine image, configure the Google Cloud Ops Agent, and set up the web application to launch automatically using Systemd on a VM instance. Additionally, it covers implementing GitHub Actions workflows for integration testing and CI/CD processes in a production environment.

### Tech Stack

| **Category**               | **Technology/Tool**                                      |
|----------------------------|---------------------------------------------------------|
| **Programming Language**   | JavaScript (Node.js)                                    |
| **Database**               | MySQL                                                  |
| **Cloud Services**         | GCP (Compute Engine, SQL, VPC Network, IAM & Admin, Network Services, Cloud Functions, Cloud Storage) |
| **Infrastructure as Code** | Terraform                                              |
| **Image Creation**         | Packer (Custom Machine Images)                         |
| **Version Control**        | Git                                                    |
| **CI/CD**                  | GitHub Actions                                         |
| **Other Tools**            | Mailgun                                                |

### Setting Up Applications, Infrastructure as Code, and Serverless Repositories

1. **Clone the repositories:**
   - Clone the **webapp repository** (set up as per its documentation).
   - Clone the **tf-gcp-infra repository** and follow the instructions in `terraform.md`.
   - Clone the **serverless repository** and follow the guidance in `serverless.md`.

2. **How these repositories work together:**
   - Clone all three repositories and ensure that Terraform prerequisites are installed locally.
   - Set up everything according to `terraform.md`.
   - Prepare your system with:
     - Terraform
     - Google Cloud CLI
   - Navigate to the `tf-gcp-infra` repository folder, copy the zip file from the `serverless repository`, and rename it to `function-source.zip`.
   - Run the `terraform apply` command from the folder containing the Terraform code to set up your infrastructure.

3. **Deployment Workflow:**
   - Once the infrastructure is set up, pushing changes to the **webapp repository** and merging a pull request will trigger a GitHub Actions workflow. This will automatically build a new machine image for you.



**Serverless Repo:** https://github.com/smank7/serverless
**Terraform repo:** https://github.com/smank7/Terraform-Infra
