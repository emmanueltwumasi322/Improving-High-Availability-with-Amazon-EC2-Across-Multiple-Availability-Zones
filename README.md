# Improving-High-Availability-with-Amazon-EC2-Across-Multiple-Availability-Zones
<h1>Improving High Availability with Amazon EC2 Across Multiple Availability Zones</h1>

<h2>Description</h2>
This project demonstrates how I improved the reliability and availability of a critical application by deploying Amazon EC2 instances across multiple Availability Zones (AZs). The solution replaces a single on-premises server with cloud-based infrastructure, ensuring that if one Availability Zone experiences an outage, the application can continue operating from another AZ. The project also demonstrates launching EC2 instances, configuring user data scripts, attaching Amazon EBS storage, and accessing the application through its public DNS name.<br />

<h2>Technologies Used</h2>

- <b>Amazon EC2</b>
- <b>Amazon EBS</b>
- <b>AWS Management Console</b>
- <b>Amazon VPC</b>
- <b>Security Groups</b>
- <b>Amazon Linux</b>

<h2>Environments Used</h2>

- <b>AWS Cloud (US East - N. Virginia / us-east-1)</b>
- <b>Windows 10</b> (21H2)

<h2>Project Scenario</h2>

A critical stabilization system was running on a single physical server whose hard drive was beginning to fail. Waiting for replacement hardware would result in downtime and service disruption. To improve reliability, the system was migrated to Amazon EC2 by deploying multiple instances in separate Availability Zones within the same AWS Region. This design increases fault tolerance and reduces the risk of a single point of failure.

<h2>Walk-through:</h2>

<p align="center">
Step 1: Set the AWS Region to <b>US East (N. Virginia) - us-east-1</b> and downloaded the user data script that would automatically configure the EC2 instance during launch.<br/>
<img src="YOUR_IMAGE_LINK_1" height="80%" width="80%" alt="AWS Region"/>
<br />
<br />

Step 2: Launched the first Amazon EC2 instance (<b>veeserver01</b>) using the Amazon Linux AMI, selected the <b>t3.micro</b> instance type, configured an 8 GiB gp3 EBS volume, selected the appropriate VPC, subnet, and security group, and uploaded the user data script.<br/>
<img src="YOUR_IMAGE_LINK_2" height="80%" width="80%" alt="Launch EC2"/>
<br />
<br />

Step 3: Launched a second EC2 instance (<b>veeserver02</b>) in a different Availability Zone (<b>us-east-1a</b> and a second AZ) to improve application availability and eliminate a single point of failure.<br/>
<img src="YOUR_IMAGE_LINK_3" height="80%" width="80%" alt="Multiple Availability Zones"/>
<br />
<br />

Step 4: Verified that the user data script executed successfully by accessing the instance through its public DNS name. The script automatically generated a webpage displaying the EC2 instance details.<br/>
<img src="YOUR_IMAGE_LINK_4" height="80%" width="80%" alt="User Data Output"/>
<br />
<br />

Step 5: Confirmed that the application was accessible using the EC2 instance's public DNS address and validated that the security group allowed the required inbound traffic. The deployment demonstrates how AWS infrastructure can provide greater reliability than a single on-premises server.<br/>
<img src="YOUR_IMAGE_LINK_5" height="80%" width="80%" alt="Final Result"/>
<br />
<br />

<h2>Key Concepts Demonstrated</h2>

- Deploying Amazon EC2 instances
- Configuring Amazon EBS block storage
- Using User Data scripts for automated server configuration
- Deploying resources across multiple Availability Zones
- Configuring VPC networking and Security Groups
- Accessing EC2 instances using Public DNS
- Improving application availability and fault tolerance using AWS infrastructure

<!--
```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
-->
