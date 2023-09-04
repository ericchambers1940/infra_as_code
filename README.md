# infra_as_code
Repository containing infrastructure provisioning code and configuration.

# Lab Goals
## Phase 1 - Development Environment Setup
1. Create AWS Free Tier Account with billing alarms, budgets, MFA, and a user account. This user account will be used with the AWS CLI and Terraform so ensure you set it up appropriately. 
2. Download Virtual Box and create a VM with Ubuntu installed. We recommend 4GB RAM, 2vCPUs and 40GB storage.
3. Install on the VM the latest Python, Ansible, Terraform, Packer, Git, Microsoft VSCode and AWS CLI.
4. Clone this GIT repo and create a folder called "phase_1". Inside, have folders called "ansible", "terraform", and "packer".
5. In ansible/ write a simple Ansible playbook that installs an Apache web server, enable SSH access and install the package "curl".
6. In packer/ write machine image configuration using the above Ansible playbook as a configurator. 
7. In terraform/ write a Terraform .tf file that spins up an EC2 instance with the newly created AMI/machine image and an Elastic IP address.
8. Commit and push the changes made in the last 3 steps to this repo in a new branch using GIT.
9. Generate an Ubuntu machine image using the Ansible Playbook and make it available for use in AWS.
10. Run the appropriate terraform commands against your TF configuration to "plan" and deploy your EC2 instance with the newly created AMI.
11. Login to your EC2 instance using SSH. Use the curl utility to download the contents of Apache's sample web page. If no errors come up, then proceed to the next step. Otherwise, troubleshoot and fix your issue.
12. Destroy the EC2 instance using Terraform.

## Phase 2 - Load Balancers and EC2 Scaling Groups.
tbd...

## Phase 3 - Repeat using GitHub Actions
tbd...
    

# Tools Used
- [Hashicorp Terraform Community Edition](https://spacelift.io/blog/terraform-ec2-instance) - provisions our infrastructure as code. This includes any AWS resources.
- [Hashicorp Packer](https://computingforgeeks.com/build-aws-ec2-machine-images-with-packer-and-ansible/?expand_article=1) - used to generate an AMI/machine image automatically.
- [Ansible](https://spacelift.io/blog/ansible-tutorial) - used to configure the AMI to our needs.
- [GitHub Actions](https://www.pluralsight.com/resources/blog/cloud/how-to-use-github-actions-to-automate-terraform) - CI/CD tool for automatically performing each step in this lab.
- [Git](https://www.w3schools.com/git/git_intro.asp?remote=github) - used for managing and versioning source code collaboratively.
- [VirtualBox](https://www.geeksforgeeks.org/how-to-install-ubuntu-on-virtualbox/) - A type 2 virtualization hypervisor. Used for creating simple virtual machines.
- [AWS EC2, ALB, Scaling Groups, IAM](https://docs.aws.amazon.com/index.html) - common AWS services we will use for this lab.
