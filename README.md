# AWS-CICD-project
This project specially shows you how you're going to  integrate AWS different services to create a CI CD  project completely on AWS by using all AWS services.  
## Beanstalk
It's a platform as a service.for running application workload very easily.You can run your application on Beanstalk.You don't need to set up EC2 instances, load, load, balancer, monitoring andstuff, not even Auto scaling group.AWS Beanstalk is onof the very famous DevOps service on AWS and it's also very popular among

First you need to create a beanstalk application

### RDS & App Setup on Beanstalk

So let's set up RDS instance.

I will say create database standard, create MySQL template 

RDS security group We have to say traffic from this

security group is allowed on 43306 from Beanstalk security group

Then login in to beanstalk server 
ssh -i Downloads/key.pem EC2-user@ip 
sudo -i
yum install git &mysql -y
clone the source code  git clone url 
cd vprofile rep
git checkout VP-rem
ls src/main/resources/db-backup.sql

mysql -h endpoint -u admin -p password accounts

logout

cd tmp

 mkdir bean app

git clone url

cd vprofile
 
git checkout Vp-rem

vim src/main/resources/application .properties

puth the end point of RDS
and password

mvn install

ls target/Vprofile_v2.war

Cp target /vprofile-v2.war .~besktop

after this wee need to upload our own version in beanstalk 

then deploy that in  to the environment 

now your beanstank and RDS is ready.

We also tested it

###  Code Commit
Now it's time to set up the CI CD pipeline for it.
So first we're going to see code commit service.

That's where we store our source code.So to understand AWS code commit quickly think of just a replacement of GitHub.So instead of using GitHub, we're going to use AWS code commit.So again it's a version control service and it is hosted by AWS and you get all the AWS security and power and also integration with other aws services 

So first we'll create a code commit repository, then we'll move or switch or transition from GitHub to code commit.So we're going to also moveall the histories commit everything from GitHub repository to code commit repository.So let's see how that can be done.


Create a repository in code committ

Create a IAM user with Codecommit full acess

then wee need  ssh public key

ssh -keygen.exe

cd .ssh

we can see the private key and public key

cat the public key then copy that the upload the public key in IAm user 

then create a config filr vim config file 

host git codecommit-*-awscodecommit

user :ssh key ID

identityfile :public ssh file name


then login in to code commit  git ssh code commit link 

cd /tmp

shh git clone code commit linnk

then cd f

git clone url 

cd v profile

checkout CI aws

remote  repository -cat .git/config

git checkout -a

git branch -a |grep -v HEAD |cat -l'/' -f3 |grep -v master >/tmp/branches

cat /tmp/branches

for i in /tmp/branches,do

git checkout $i

done;

for i in /tmp/branches,do

echo  $i

done;

git  branch -a 

git fetch --tags

git remote rm origin

git  remote add origin codecommit URL

cat  .git/config

git push origin  --all

git push tags 


