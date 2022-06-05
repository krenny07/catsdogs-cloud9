Pre-requisites: 

1.	Generate SSH key with filename Assignment1-dev
2.	Update the following repository secrets: 
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_SESSION_TOKEN
Repo_Name = clo835-assignment1

Deployment steps:

1.	Clone catsdogs-cloud9 application to local environment.

2.	From local environment, cd to /catsdogs-cloud9/terraform/ec2 and deploy the terraform code with the following commands:
 terraform init, terraform validate, terraform plan and terraform apply
 
3.	Push the code to dev branch on Github and create a pull request to merge to master branch. Upon merge, GitHub actions workflow will build our docker images and push them to Amazon ECR!

4.	From local environment, run $ aws configure and enter your AWS Access Key ID and AWS Secret Access Key.

5.	Run $ aws ecr get-login --region us-east-1 and copy the output starting docker login and make sure to remove the -e none near the end

6.	SSH to EC2 and paste the output of step#5

7.	Pull both images from AWS ECR.
  
8.	Run cats container on port 8080 and dogs container on port 8081.
  
9.	Demonstrate both applications are accessible via the Internet.
  
10.	Demonstrate that cats and dogs container can ping each other.
  
11.	Update the application code in GitHub and repeat steps 3 to 9.
  
