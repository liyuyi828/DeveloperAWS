### EC2
Amazon Elastic Compute Cloud(EC2) is a web service that provides resizable compute capacity in the cloud. Amazon EC2 reduce the time required to obtain and boot new server instances to minutes, allowing you to quickly scale capacity, both up and down, as your computing requirement changes.

Amazon EC2 changes the economic of computing by allowing you to pay only for the capacity you actually use. Amazon EC2 provides developers the tools to build failure resillient applicaitons and isolate themseleves from common failure scenarios. 

```
EC2 is the backbone is AWS
```

### Options (Pricing Model)
* On Demand - pay for fixed rate by the hours
* Reserved - provide capacity reservation, offer significant discount on the hourly change for an instance. Usually 1 year to 3 year terms. 
* Spot - enable you to bit whatever price you want for instance capacity, providing even greater saving if your applicaiton have flexible start and end time. Note: if AWS terminate your "spot" instance, you don't need to pay anything, but you need to pay if you terminate the instance on your own. (Price in different region are different)

### On Demand
* Low Cost and flexibilyt of Amazon EC2 without any up-front payment or long-term commitment
* Applicaiton with short term, spiky, or unpredictable workloads that cannot be interupted
* Application being developer or tested on Amazon EC2 for the first time

### Reserved
* Application with Steady state or preditable usage
* Applicaiton that required reserved capacity
* Users able to make upfront payments to reduce their total computing cost even further

### Spot
* Application have flexible start and end time
* Application are only feasible at very low compute prices
* Users with urgent computing needs for large amounts of additional capacity

### Instance Types
* T2: Low cost, general purpose - web server / small DBs
* M4: General purpose - Applicaiton server
* M3: General purpose - Application server
* C4: Computed Optimized - CPU intensive apps/ DBs
* C3: Computed Optimized - CPU Intensive apps / DBs
* R3: Memory optimized - Memory Intensive Apps / DBs
* G2: Graphics / General Purpose GPU - Video encoding / Machine Learning / 3D Applicaiton Streaming
* I2: High Speed Storage  - NoSQL DBs, Data Warehousing etc
* D2: Dense Storage - Filesevers / Data Warehousing / Hadoop

### Quick Reference
* D: Density
* I: IOPs
* R: RAM
* T: cheap general purpose
* M: main choice for general purpose
* C: Compute
* G: Graphics

### EBS
* Elastic Block Storage - disk on the cloud
* Attach EBS to EC2, but one EBS can only attached to one EC2, one EC2 can have multiple EBS
* SSD (GP2)
  * 99.999% availability
  * 3 IOPS per GB with up to 10,000 IOPS 
* Provisional IOPS SSD (IO1)
  * I/O intense application, use if you need more than 10,000 IOPS
* Magnetic(Standard)
  * Lowset cost per gigabyte of all EBS volume

### Exam Tips: 
#### Know the difference between: 
* On Demand
* Spot
* Reserved
#### Remember with spot instances:
* if you terminate the instance, you pay for the hours
* if AWS terminate the instance (for example, price goes up),you the the hours it was terminated in for free
#### EBS consists of:
* General Puspose SSD - GP2 - (Up to 10000 IOPS)
* Provisional IOPS SSD - IO1 - (more than 10000 IOPS)
* Magnetic - Cheap, infrequently accesss storage
* YOu can not mounted 1 EBS to multipley EC2 instance, instead use EFS. 


## Lab Note:
### Using key and access key
* ```ssh -i ec2-user@<ip2> -i your.pem``` command from course did not work, I have do use the ssh command ```ssh -i your.pem ec2-user@publicDNS```from AWS doc <http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html>, then enter "yes"
* enter ```sudo su``` back to root directory
* enter ```aws configure```, use secret ID and access key to configure credential, choose whichever service region that is convinient for you
* aws s3 mb s3://myverylongtestingbucket
* cd /
* cd ~
* cd .aws
* nano to check config file

### Using Roles
Using secret id and secret key is not the best way to access files; try to use role if possible. To use role, just apply role when launching the EC2 instance
* You can also run a "shell" script when launching the instance
* The course use the following script for PHP: 
```
#!/bin/bash
yum update -y
yum install httpd24 php56 git -y
service httpd start
chkconfig httpd on
cd /var/www/html
echo "<?php phpinfo();?>" > test.php
git clone https://github.com/acloudguru/s3
```
go to "var/www/html" directory, which is where our file is located, run 
```

```
to install aws-sdk with "composer", which is recommended by AWS. 

Always require "autoload.php" in "/var/www/html/vendor" directory in order to connect to AWS-sdk. 

```http://169.254.169.254/latest/meta-data``` to get meta data


