# AWS ENVIRONMENT WITH TERRAFORM
Create Infra in AWS using Terraform template. It creates Ec2, DB, ELB, public & private subnets etc.


Steps to login instance:
cd directory
Note:- "directory" where your pem file exists

ssh -i "******.pem" ec2-user@**.**.**.**
Note:- Change your pem file name and ipaddress of the instance

***Install Terraform***
$ curl -O https://releases.hashicorp.com/terraform/0.8.2/terraform_0.8.2_linux_amd64.zip
$ unzip terraform_*
$ mv terraform /usr/local/bin/
$ rm -rf terraform_*
=>>Access terraform using the below command:-
$ /usr/local/bin/terraform command_name
Note:- command_name includes "apply", "destroy", "plan" etc


****Clone the Terraform automation template repo****
$ yum update -y
$ yum install git -y
$ git clone https://github.com/pavank1933/terraform_aws_test.git
$ cd terraform_aws_test/


Error Workouts:-
To get instances in ELB to inservice, have replaced the port of httpd.conf file parameter value from Listen 80 to 8081.
Then do:- $ service httpd restart
Changed the ELB health configuration and listener port information as per the screenshots available in this repo.