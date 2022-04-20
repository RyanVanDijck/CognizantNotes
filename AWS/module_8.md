# Databases

## Amazon Relational Database Service

* AWS solutions typically fall into one of two categories:
  * #### Managed
    * Scalling fault tolerance and availability are built into the service. 
    * Some configuration e.g setting permissions for an S3 bucket. 
    * Require less configuration. 
    
  * #### Unmanaged 
    * Scalling, fault tolerance and availability are managed by you. 
    * As the owner of the service, you manage how the service responds to changes in load, erros and situations where resources become unavailable. 
    * If you want to keep complete control of the database, you can install a RDBMS on an EC2 instance. 
    * Gives more fine tuned control. 
### Challenges of relational databases 

* Server maintenance and energy footprint. 
* Software installation and patches. 
* Database backups and high availabilty. 
* Limits on scalability. 
* Data Security. 
* Operating system installation and patches.

### Amazon RDS

* Managed Service that sets up and operated a relational database in the cloud. 
* Can be used in a VPC.
1. Can configure for high availability with Multi-AZ deployment. 
2. In this case, amazon vpc creates a Standby instance in another Availability Zone and synchronises changes between the main and standby instances.

### Read Replicas

#### Features 
* Offers asynchronous replication. 
* Can be promoted to main(master) if needed.

#### Functionalility 
* Use for read-heavy database workloads. 
* Offload read queries. 

### Use Cases
|||
|---|---|
|Web and mobile Applications|High Throughput</br>Massive Storage scalability </br>High Availability|
Ecommerce applications|Low-cost database</br>Data security</br>Fully managed solution|
|Mobile and online games|Rapidly grow capacity</br>Automatic scaling</br>Database montoring|

### When to use amazon RDS
|Use|Do not use|
|---|---|
|Complex transactions or queries|Massive read/write rates|
|Medium to high query or write rate|Sharding from high data size or throughput demands|
|Only one worker node or shard|Simple GET/PUT requests.|
|High Durability|RDBMS customization|


### Managed services resposiblities 

* Reduced Operational Workload
* Reduced Costs

#### You Manage: 
* Application Optimisation

#### AWS manages:
* OS installation and patches
* Database software installation and patches 
* Database backups 
* High availability 
* Scaling
* Power and racking and stacking servers
* Server maintenance 
  
### Instances 

* Isolated database environment. 
* Contain multiple user created databases. 
* Access database using same tools and applications with a standalone database instance. 
* Differ in performance characterstics and price. 
* There are two factors chosen when creating an instance:
  * #### Instance Class
    * CPU 
    * Memory 
    * Network performance
  * #### Instance Storage 
    * Magnetic 
    * General Purpose (SSD)
    * Provisioned IOPS
#### Engines

1. MYSQL 
2. Amazon Aurora
3. Microsoft SQL server
4. PostgreSQL
5. MariaDB
6. Oracle

## DynamoDB

* Fast and flexibile NoSQL database for any scale. 
* NoSQL database tables. 
* Virtually unlimited storage. 
* Items can have differing attributes. 
* Low-latency queries.
* Scalable read/write throughput.

### Core Components 

* Tables, items and attributes are the core DynamoDB components. 
* DynamoDB support two different kinds of primary keys: Partition key and partition and sort key. 
* Items in a table must have a key. 

## Redshift

* A fast, fully managed data warehouse. 
* Simple and cost effective. 
* Analyse data using standard SQL. 
* Use existing business intelligence tools. 
* Simple to scale. 
* Use complex analytics queries against petabytes of structured data. 
* Sophisticated query optimization.
* Columnar storage on high performance local disk. 
* Massively parallel queries. 
* Supports SQL, JDBC  and Open Database Connectivity. 

### Data warehouses

* Building data warehouses is complex and expensive. 
* Takes months to set up. 

### Architecture

* Consists of a cluster of leader and compute nodes. 
* Leader node manages communication with client programs. 

### Use Cases 

|Enterprise data warehouse|Big Data|
|---|---|
|Migrate at comfortable pace for customers|Low price point for small customers|
|Expermient without large upfront cost or commitment|Managed service for ease of deployment and maintenance|
|Respond Faster to business needs|
|Focus more on data and less on database management|

### Software as a Service

* Scale as capability grows.
* Add analyic functionalilty to applications.
* Reduce hardware and software costs. 


## Aurora

* Enterprise class relational database. 
* Compatabile with MySQL or PostgreSQL 
* Works with AWS Database Migration Service.
* Works With AWS Schema Conversion Tool. 
* Can easily move dataset into Aurora
* Automates:
    * Provisioning
    * Patching 
    * Backup 
    * Recovery
    * Failure Detection 
    * Repair

