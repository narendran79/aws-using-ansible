AWS Using Ansible
=================

## Installation Instructions

Follow these steps to set up Ansible and configure your EC2 instance:

1. **Connect to EC2 Instance**
   - Ensure that you’ve already set up a connection to your EC2 instance running Ubuntu as the base image.

2. **Update System**
   - Once connected to the EC2 instance, run the following command to update the package index:
     ```
     sudo apt update
     ```

3. **Install Ansible**
   - Ansible is not pre-installed on Ubuntu. To install it, run:
     ```
     sudo apt install ansible
     ```

4. **Verify Ansible Installation**
   - To verify that Ansible was successfully installed, check the version:
     ```
     ansible --version
     ```

5. **Install AWS Ansible Collection**
   - Install the necessary AWS libraries via Ansible Galaxy by running the following commands:
     ```
     ansible-galaxy collection install amazon.aws
     ansible-galaxy collection install community.aws
     ```

## Running the Ansible Playbook

1. **Clone the Repository**
   - Clone your repository using the following command:
     ```
     git clone your-repo-name
     ```

2. **Configure Secrets**
   - In the `secrets.yml` file, paste your AWS **access key ID** and **secret access key**.

3. **Update Variables**
   - If needed, modify any variables by editing the `vars.yml` file to meet your specific requirements.

4. **Navigate to Playbook Directory**
   - Change into the directory where your playbook is located:
     ```
     cd /home/ubuntu/your-project-name/playbook
     ```

5. **Run the Playbook**
   - Once everything is configured, execute the Ansible playbook with the following command:
     ```
     ansible-playbook your-playbook.yml
     ```
## Snapshot

Below are the snapshot after running the ansible playbook

1. After running the ansible command:
   ![instance](https://github.com/user-attachments/assets/f2a48661-3629-41a8-b535-80b7c05fce9c)

2. EC2 Instance got created successfully:
   ![ec2_using_ansible](https://github.com/user-attachments/assets/27045f58-37a9-459c-afd6-6164c2cc5b73)

4. S3 bucket created with object upload:
   ![s3_using_ansible](https://github.com/user-attachments/assets/aaae5b39-011e-414b-8403-83232c67358f)
