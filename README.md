# Using Cloudformation installed wordpress using Ansible

Setup Wordpress on ubuntu linux EC2 instance using ansible and automate this using a cloud formation template



Used CM tool such as Ansible,to automate the installation of WordPress,sample site. Automated using Cloudformation template.

Deliverable:

A cloudformation template that accepts user inputs as parameters where applicable ( for example, Admin password). This template should setup VPC, create subnets, launch a CM instance, pull the necessary code (modules, classes, recipes etc) from a GIT repo (or S3), and configure the web instance for  Wordpress setup.

Approach:

Step 1: For this assessment, I set up a test environment on VMWare Workstation to install wordpress on localhost using ansible(using a Ubuntu Linux image).

Step 2: Created a playbook for the installation of Apache, MySQL, PHP, Wordpress in the test Environment.

Step 3: After success of Step 2, I pushed this playbook to my GitHub account.

Step 4: Built a CloudFormation Template with parameters(Name.Password,.,etc;) and resources(VPC,subnets.,etc;) mentioned in the rerqurirements


Mapping between AWS Resources:


Step 5: Installed necessary packages(git, ansible, cfn-heat ...) to download the repo(mentioned in step3), run playbook, wait handle and  referencing parameters in Userdata. 


Step 6: Tested the functioning of the CFT and pushed the Repository to GitHub https://github.com/guruprasadsingirikonda/awsansible 

To Build the stack:

1. Download  this repository.

2. Create a stack using CloudFormation.json file in cloud formation.

3. Fill parameters of Stackname, DatabaseName, DBUser, DBPassword.. and choose an existing keypair for SSH connection.

4. The User parameters will give you access to corresponding mysqlDB and user on EC2 instance built.

Output:

Stack up and running, able to access EC2 instance and MySQLDB with input username and password. 
Access the wordpress using the ip address>


