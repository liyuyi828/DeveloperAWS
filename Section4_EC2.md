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
* Provisional IOPS SSD
  * I/O intense application, use if you need more than 10,000 IOPS
* Magnetic(Standard)
  * Lowset cost per gigabyte of all EBS volume