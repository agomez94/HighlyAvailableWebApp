# Deploying a Highly Available Company Intranet on AWS
As a DevOps Engineer, it's essential to gain hands-on experience with various AWS services. In this tutorial, we will walk through the process of deploying a highly available company intranet web portal on AWS. We will utilize EC2 instances, an autoscaling group, an Application Load Balancer (ALB), S3 buckets, CloudWatch, and more. By following this tutorial, you will gain experience with AWS CLI, scripting, and creating a secure and scalable deployment.


Step 1: Set Up the Environment
Create an S3 Bucket:

**Ensure no public access to the bucket.
Upload the provided index.html file to the bucket.

**Create an IAM Role:**

This role will be assigned to the EC2 instances.
Grant the role read-only access to the S3 bucket.

Step 2: Deploy the Autoscaling Group (ASG) and Load Balancer
Create an Application Load Balancer (ALB):

Configure the ALB to distribute traffic to the EC2 instances.
Assign a security group to the ALB for inbound and outbound traffic.

Set Up Availability Zones (AZs):

Choose two AZs for high availability.

Create the Autoscaling Group:

Configure the ASG to use the created IAM role and the desired AZs.
Set the scaling policies based on EC2 CPU usage.

Step 3: Configure DNS (Optional)
Purchase a Domain Name:

Choose a domain name for your intranet web portal (e.g., .click).

Create a DNS Record:

Configure a record type to route traffic from your domain to the ALB.

Step 4: Deploy EC2 Instances and Bootstrap Script
Write an AWS CLI Command for EC2 Instance Deployment:

Define the instance type, key pair, security group, and subnet.

Create a Bootstrap Script:

The script will run on EC2 instances during initialization.
Use the script to download the website files from the S3 bucket.
Install and configure the required software (e.g., httpd).
Retrieve the EC2 instance's instanceID from the metadata endpoint.
Update the web page to display the instanceID.

Step 5: Configure Security Groups and Custom CloudWatch Metrics
Set Up Security Groups:

Configure inbound and outbound rules to allow necessary traffic.

Configure Custom CloudWatch Metrics:

Define metrics to monitor RAM usage, TCP connections, etc.
Use CloudWatch to set up alarms and notifications (SNS) for autoscaling events.

Conclusion: By following this step-by-step tutorial, you have successfully deployed a highly available company intranet web portal on AWS. You gained experience with AWS CLI, scripting, and deploying resources in a secure and scalable manner. This project demonstrates your knowledge of bootstrap scripts, autoscaling groups, ALBs, S3 buckets, IAM roles, and CloudWatch. Continue exploring AWS services and building upon this foundation to further enhance your cloud practitioner skills.
