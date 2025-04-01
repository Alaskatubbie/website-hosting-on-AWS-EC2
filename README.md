# website-hosting-on-AWS-EC2
Just a step by step documentation on hosting a static website on EC2 Instance
## Set up an EC2 Instance
Sign in to the AWS Management Console and navigate to the EC2 dashboard, Click "launch Instance"
![image](https://github.com/user-attachments/assets/0a4e29e0-92d7-41f0-b970-d9acd0046fbe)
Give Instance a name and Choose an Amazon Machine Image (AMI)
![image](https://github.com/user-attachments/assets/7638c4a8-a2e8-4f16-b693-67d6c964c4d0)
Select an instance type and Create or select a key pair for SSH access
![image](https://github.com/user-attachments/assets/c3391e01-f916-47fd-b6a9-c046846cda7d)
Configure security group rules to allow SSH (port 22) and HTTP (port 80) or HTTPS (port 443) traffic
![image](https://github.com/user-attachments/assets/2a026b8c-d2c6-437c-a0f1-35f829bcc1ad)
Click "launch Instance" =, Instance will show up after clicking "Instances" in the left pane
![image](https://github.com/user-attachments/assets/a6beee53-2bd5-47b8-82b7-4064ef543957)
Use an SSH client to connect to the instance using the public IP, your key pair, and the appropriate username
![image](https://github.com/user-attachments/assets/5e0aa810-18dc-4e32-8bd9-e095e9953758)
## Install and Configure a Web Server
Switch user to root(sudo -i) and Update the Instance(sudo yum update -y) 
![image](https://github.com/user-attachments/assets/40a1f5c6-d076-4314-9802-ea851957ae05)
Install Apache Web Server(sudo yum install httpd -y)
![image](https://github.com/user-attachments/assets/21cdca9b-c070-423e-ae98-e64dbd711217)
Start the Apache web server service and enable it (sudo systemctl start httpd && sudo systemctl enable httpd)
![image](https://github.com/user-attachments/assets/84968f86-3aab-4c76-94e8-60af26af168b)
check if the apache web server service is running (sudo systemctl status httpd)
![image](https://github.com/user-attachments/assets/aacbb399-1329-48ab-a208-d73130243a87)
make a temp directory (mkdir temp) and change to the "temp" directory
![image](https://github.com/user-attachments/assets/bd5f6f3a-f3ab-4a2e-b8e5-3029b79a90bd)
using wget command download the free css template directly to your web server instance
![image](https://github.com/user-attachments/assets/a913d71b-a43b-41f1-9765-7b7caeaf8394)
unzip file with unzip command (unzip neogym.zip)
![image](https://github.com/user-attachments/assets/fd098c02-8e5a-411b-a319-66f917205f5b)
  
change directory to the neogym.html file and move content of file to /var/www/html
![image](https://github.com/user-attachments/assets/ef68234b-37e7-4005-9861-7fa14c0b7c81)

## Access Your Website
Open your web browser and navigate to the public IP address of your EC2 instance
![image](https://github.com/user-attachments/assets/426a86f5-ee0d-48b6-bc30-69f48dd0b0e7)

