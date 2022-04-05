# Cloud Economics and Billing

## AWS Pricing Model 

### Three Fundamental Drivers of cost with AWS 
#### <span style = "color:blue">Compute</span> 
* Charged per hour/second(Linux Only).
* Varies by instance type.
#### <span style = "color:teal">Storage</span>
* Charged Typically per GB 
#### <span style = "color:magenta"> Data Transfer</span>
* Outbound is aggregated and charged. 
* Inbound had no charge(With some exceptions). 
* Charged Typically per GB. 
* Data transfer between services in the same region is free. 
1. For outbound data services, it is aggregated across services, and charged at the outbound data transfer rate. 
2. This charge appears on the monthly statement as AWS data transfer out.

### How do you pay for AWS. 
* Pay for what you use. 
* Pay less when you reserve. 
* Pay less when you use more and as AWS grows. 
1. Pay only for the services that you consume. 
2. No Large Upfront expenses.

### Pay less by using more
* <span style = "color:purple">Savings</span> as usage increases. 
1. <span style = "color:purple">Tiered Pricing</span> for services like Amazon S3, EBS or EFS.
2. The more you use, the less you pay per GB.
*  Multiple storage services deliver <span style = "color:purple">lower</span> storage costs based on needs. 

#### As AWS grows:
* AWS focuses on lowering cost of doing business.
* This practice results in AWS passing savings from economies of scale to you.
* Since 2006, AWS has <span style = "color:purple">Lowered pricing 75</span> times (as of September 2019). 
* Future higher-performing resources replace current resources for no extra charge. 

### Custom pricing

* Meet varying needs through custom pricing. 
* Available for high-volume projects with unique requirements. 

### AWS Free Tier
* Enables you to gain free hands on experience with the AWS platform, products and services. 
* You can run a <span style = "color:purple">free EC2 T2</span> microinstance for a year. 

1. Sign up for an AWS account.
2. Learn with 10 minute tutorials.
3. Start building with AWS. 

### Services with no charge. 
* Amazon VPC
* Elastic Beanstalk**
* Auto Scalling**
* AWS CloudFormation**
* AWS Identity and Access Management (IAM)

** Charges accociated with other AWS services that are used with these services. 


## Total Cost of Ownership
### On-premises vs Cloud
|Traditional Infrastructure|Cloud|
|---|---|
|Equipment|No Upfront Expense|
|Resources and administration|Improve time to market and agility|
|Contracts|Scale Up and Down|
|Cost|Self-service infrastructure|

#### Capital Expenses
1. Capital expenses are fixed costs.
2. Include facilities, hardware, licenses and maintenance staff.   

* Scaling up can be expensive and time consuming. 


### What is Total Cost of Ownership

``` TCO is the financial estimate to help identify direct and indirect costs of a system```

#### Why use TCO ?

* To compare the costs of running an <span style = "color:purple"> entire infrastructure environment or specific workload </span> on premises versus on aws. 
* To budget and <span style = "color:purple">build the business case </span> for moving to the cloud. 

### TCO Considerations
1. Server Costs 
2. Storage Costs
3. Network Costs 
4. IT Labor Costs

### AWS Pricing Calculator
Use the <span style = "color:purple">  AWS Pricing Calcluator </span> to:
* Estimate monthly costs.
* Identify opportunities to reduce monthly costs.
* Model your solutions before building them. 
* Explore price points and calculations behind your estimate. 
* Find the available instance types and contract terms that meet your needs. 
* Name your estimate and name groups of services. 

#### Estimate
* The estimate is broken into 12 months total, total upfront and total monthly. 
### Additional Benefit Considerations
|Hard Benefits|Soft Benefits|
|---|---|
|Reduced spending on compute, storage, networking and security.|Reuse of service and applications that enable you to define and redefine solutions using the same cloud service.|
|Reductions in hardware and software purchases.|Increased developer productivity.|
|Reductions in operational costs, backup, and disaster recovery.|Increased customer satisfaction.|
|Reduction in operations personnel|Agile Business processes that can quickly respond to new and emerging oppertunities.|
||Increase in global reach|


## AWS Organizations
1. Can sometimes be better to assign separate AWS accounts in business to each department or team.
2. Depends on the size of the department. 
3. Allows the spending for each department/team to have a clear and defined report. 
4. When this happens, we need to tie the accounts for a single organisation together. 
5. AWS organizations is used for consolidated billing of multiple. accounts. 
6. This services splits branches into an organisational tree. 

### Key Features and benefits. 

* Policy Based account management. 
* Group Based account management. 
* Application programming interfaces that automate account management. 
* Consolidated billing. 

### Security
* You can control access with AWS identity and Access management(IAM). 
* IAM policies allow you the approve or deny access to AWS services for users, groups and roles. 

### Setup
1. Create Organisation. 
2. Create organisational users. 
3. Create service control policies. 
4. Test restrictions. 

## AWS Billing &  Cost Management
 AWS Billing and Cost Management is a service that you use to: 
 *  Pay your AWS bill.   
 *  Monitor usage.
 *  Budget Expenses.

### Functionality 
* Billing and Cost Management enables you to forecast and obtain a better idea of what your costs might be in the future.
* Can set a time period. 
* Can view in a monthly or daily level of granularity. 
* Grouping and filtering. 
* AWS cost and usage report tool helps you understand your cost and usage data trends.  

### Monthly Bills 
* Lists costs incurred over the past month for each AWS service. 
* Further breakdown by AWS region and linked account. 










