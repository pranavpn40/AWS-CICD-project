# AWS-CICD-Project
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

