### History of AWS
* Concept in 2003
* SQS launched 2004
* Full Service Launched in 2006
* Has over 180k developers in 2007
* All amazon.com move over to AWS
* First Re-Invent Conference 2012
* Certifications Launched 2013
* 2015 $6B revennue, grow 90% year over year
Computing power: 90% AWS, MSFT 5%, rest combine for the 5% in May 2015

```
Only need to know a few of service to pass exam, but good to know the name and what they do for other services
```

### Global infrastruture
* 11 regions, 30 availability zones - 2015
* 5 more regions, 10 more availability zones - 2016
* Region is geographical areas - contain many zones
* Zone (data center), can opearate independently without failure
* Edge Locations for content delivery, more location than zones


### Networking
* VPC - virtual private cloud
* Direct Connect
* Route53 - highly scalable DNS

### Compute
* EC2
* EC2 container service (not in exam, run instance with container, ie Docker)
* Elastic Beanstalk( AWS for beginner, cover a lot in devOp pro exam)
* Lambda (run code without provisioning or managing service, paid for compute time)

### Storage
* S3 (object base storage) - Big in exam
* Cloud Front - CDN service, Edge locatin in the world
* Glacier - low cost, long term back up, long access time
* EFS - elastic file service (preview not feature a lot on exam yet)
* Snowball (good for move large data to AWS without internet, rentable device, not exam topic)
* Storage Gateway - Hot exam topic

### Database
* RDS - relational DB
* DynamoDB - most important, nonSQL DB
* Elasticache - cached query
* Redshift - data warehousing service
* DMS - DB mirgration service (not on exam yet)

### Analytics
* EMR
* Data Pipeline (on pro)
* Elastic Search
* Kinesis - strearming on AWS (no in exam)
* Machine learning
* Quick Sight - biz intellegent (no in exam)

### Sercurity & Identiry
* IAM 
* Diector service
* Inspector (not in exam)
* WAF (not in exam)
* Cloud HSM (not associate)
* KMS

### Managerment Tools (more on devOps, developer need to know)
* Cloud Watch (performance monnitoring)
* Cloud Formation
* Cloud Trail (history recording)
* Opsworks (come in a bit)
* Config (not in exam)
* Service Catalog
* Trusted Advisor (in exam, has lab) - advice on how to optimize all your AWS service

### Applicairon Service
* API gateway (not in exam)
* App Stream (ZenApp in AWS, not on exam)
* CloudSearch (not in exam)
* Elastic Transcoder (convert media code)
* SES - simple email service
* SQS - (in exam a lot)
* SWF - need to know the difference between SQS and SWF

### Developer Tools (know what service it, not in exam, ead FAQ)  
* CodeCommit - private repo
* CodeDeploy - deploy on any instance
* CodePipeline - continue depolyment

### Mobile Services
* Mobile Hub
* Cognito
* Device Farm
* Mobile Analytic
* SNS (big topics) - Simple notification service

### Enterprise Application
* WorkSpaces - virtual desktop on cloud
* WordDocs - drop box for enterprise, to store and share file on AWS
* WorkMail

### Internet of things
  Internet of Things

```
Know a few service inside out
```
