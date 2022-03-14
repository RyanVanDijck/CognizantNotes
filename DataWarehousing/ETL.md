# ETL
* Used mostly for traditional data warehousing. 
* Two main Varieties of ETL: 
	1. Initial 
	2. Incremental
## Extract
* Quickly pull data from source appliation. 
* Traditionally done in batches.
* Raw Data.
* Moves to the staging layer.

## Transform 

* Data needs to be normalised to allow apples to apples comparison.
* It needs to be prepared so that it can be accessed for usage.
* Can be <u>very</u> complex.

## Load
* Final stop in data pathway.
* Store data in user access layer.

## Challenges with Traditional ETL
* Significant buidness analysis before storing data.
* Significant data modeling before storing data. 

## ELT
* Blasting data into big data environment.
* Raw form in Hadoop HDFS. AWS S3, etc. 
* Use big data environment computing power to tranform when needed. 
* "Schema on read" vs "Schema on Write".
*  Not Really used for traditional data warehousing.
*  More used for data lakes and data warehouse hybrids. 

## Initial Load ETL 
* Normally one time only.
* Happens right before the data warehouse goes live.
* All relevent data necessary for analytics.
* May be redone of something happenes to the warehouse.
* Irrelevant data is not added. 

### What data is added
* Data needed for analytics. 
* Data probably needed for analytics. 
* Historical data. 

## Incremental ETL 
* Incrementally refreshes the data warehouse.
* Introduce new data. 
* Change modified data.
* Handle deleted data. Not necessarily deleted. 

### Four major Patterns
1. Append.
2. In-place update.
3. Complete Replacement.
4. Rolling append.

## Common Transformation models
* Data value unification
* Data type and size unification
* De-duplication
* Dropping columns(Vertical slicing)
* Value-based row filtering(horizontal slicing)
* Correcting known errors 