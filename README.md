# 🛠️ Deploying WordPress with AWS CloudFormation

## 📌 Project Overview

This project uses **AWS CloudFormation** to provision and deploy a fully functional **WordPress blog** on an Amazon EC2 instance. The infrastructure is defined as **Infrastructure as Code (IaC)** using a single YAML CloudFormation template that automates everything—from server provisioning to WordPress installation.

> ✅ Ideal for:  
> - Freelancers building personal blogs or portfolios  
> - Developers testing WordPress before production  
> - Agencies deploying reusable blog infrastructure for clients  

---

## 🚀 What’s Deployed?

- ✅ Amazon EC2 instance (Free Tier–eligible t2.micro)
- ✅ LAMP Stack (Linux, Apache, MySQL/MariaDB, PHP)
- ✅ WordPress CMS
- ✅ Secure MySQL database setup
- ✅ Public IP or Elastic IP for internet access
- ✅ SSH Access via KeyPair

---

## 💡 Use Case Example: Freelance Web Designer

**Scenario**: Ada, a freelance web designer, wants to deploy a portfolio blog without using shared hosting. With this template, she:

1. Uploads the template to AWS CloudFormation
2. Enters basic parameters (KeyPair, DB credentials)
3. Waits a few minutes for AWS to provision and configure everything
4. Logs into WordPress and starts blogging 🚀

---

## 📝 Getting Started

Deploy the Template
Option 1: Via AWS Console
Open AWS CloudFormation

Create a new stack

Upload the wordpress-ec2.yaml file

Fill in the parameter fields

Option 2: AWS CLI
aws cloudformation create-stack \
--stack-name WordPressBlog \
--template-body file://wordpress-ec2.yaml \
--parameters ParameterKey=KeyName,ParameterValue=YourKeyPairName \
             ParameterKey=DBName,ParameterValue=wordpressdb \
             ParameterKey=DBUser,ParameterValue=admin \
             ParameterKey=DBPassword,ParameterValue=StrongPass123 \
             ParameterKey=DBRootPassword,ParameterValue=RootStrongPass123 \
--capabilities CAPABILITY_IAM

---

### 🔐 𝐏𝐚𝐫𝐚𝐦𝐞𝐭𝐞𝐫𝐬⁣

Parameter Description⁣⁣
⁣⁣
1. KeyName: Name of your existing EC2 Key Pair⁣⁣
2. DBName: WordPress database name⁣⁣
3. DBUser: WordPress database user⁣⁣
4. DBPassword: Password for the WordPress DB user⁣⁣
5. DBRootPassword: Root password for the MySQL DB⁣⁣
⁣⁣
⁣
---

### 🧰 𝐓𝐨𝐨𝐥𝐬 𝐔𝐬𝐞𝐝⁣
1. AWS CloudFormation⁣
2. Amazon EC2⁣
3. Amazon Linux 2⁣
4. Apache⁣
5. MariaDB (MySQL)⁣
6. PHP⁣
7. WordPress⁣

---
⁣
### ✅ 𝐁𝐞𝐧𝐞𝐟𝐢𝐭𝐬⁣
1. Full control of your infrastructure⁣
2. One-click deployment via template⁣
3. No manual setup⁣
4. Reusable and scalable⁣
5. Compatible with AWS Free Tier⁣

---
⁣
### 🧪 𝐅𝐮𝐭𝐮𝐫𝐞 𝐈𝐦𝐩𝐫𝐨𝐯𝐞𝐦𝐞𝐧𝐭𝐬⁣
1. Add HTTPS support with ACM + ALB⁣
2. Automatically configure Elastic IP⁣
3. Parameterize WordPress version⁣
4. Integrate with Amazon RDS for managed DB⁣

---
⁣
### 📎 𝐑𝐞𝐥𝐚𝐭𝐞𝐝 𝐋𝐢𝐧𝐤𝐬⁣⁣
- [AWS CloudFormation Documentation](https://docs.aws.amazon.com/cloudformation/)
- [WordPress on EC2 Guide](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/hosting-wordpress.html)
- [Amazon Linux 2 AMI Docs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/amazon-linux-2.html)
- [RDS MySQL Best Practices](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_BestPractices.html)
- [AWS Security Best Practices](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)
⁣
### 👩🏽‍💻 𝐀𝐮𝐭𝐡𝐨𝐫⁣
Patience Sonia Ogbeba ~~~⁣
AWS Certified Solutions Architect⁣
⁣
### 📄 𝐋𝐢𝐜𝐞𝐧𝐬𝐞⁣
This project is licensed under the MIT License.
