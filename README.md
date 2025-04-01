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
