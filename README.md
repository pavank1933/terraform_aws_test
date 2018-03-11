# AWS ENVIRONMENT WITH TERRAFORM     <br/>
Create Infra in AWS using Terraform template. It creates Ec2, DB, ELB, public & private subnets etc.  <br/>


Steps to login instance:  <br/>
cd directory   <br/>
Note:- "directory" where your pem file exists  <br/>

ssh -i "******.pem" ec2-user@**.**.**.** <br/>
Note:- Change your pem file name and ipaddress of the instance  <br/>

***Install Terraform***  <br/>
$ curl -O https://releases.hashicorp.com/terraform/0.8.2/terraform_0.8.2_linux_amd64.zip  <br/>
$ unzip terraform_*   <br/>
$ mv terraform /usr/local/bin/  <br/>
$ rm -rf terraform_*   <br/>
=>>Access terraform using the below command:-   <br/>
$ /usr/local/bin/terraform command_name         <br/>
Note:- command_name includes "apply", "destroy", "plan" etc   <br/>


****Clone the Terraform automation template repo****            <br/>
$ yum update -y           <br/>
$ yum install git -y       <br/>
$ git clone https://github.com/pavank1933/terraform_aws_test.git      <br/>
$ cd terraform_aws_test/          <br/>


Error Workouts:-          <br/>
To get instances in ELB to inservice, have replaced the port of httpd.conf file parameter value from Listen 80 to 8081.   <br/>
Then do:- $ service httpd restart          <br/>
Changed the ELB health configuration and listener port information as per the screenshots available in this repo.         <br/>