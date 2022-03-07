# Concepts
## Four Rules
* Created by Bill Inmon

1. Data Warehouse is an integrated envrionment.
2. Data Warehouse is subject oriented.
3. Data Warehouse contains Historical data as well as current data.
4. Data Warehouse remains stable during refreshes.

* Data Warehouse is restructured and reorganised to make it more useful for analysis. 
* These rules support data driven decision making. 

## Reasons to Build Data Warehouse
### Decision making
* Support making decisions in a data driven manner.
* Reduces reliance on experience and intuition. 


### One Stop Shopping
* Required data is in one location.
* Useful for making data driven decisions. 
<br>
* Before Data Warehousing, data was often scattered all over the place.
* Decisions that needed the use of data were costly and time consuming. 
* One stop shopping provides the opportunity to concentrate on data analysis. 

### Making Data Driven Decisions
Need knowledge of the:
* Past
* Present
* Future
* Unknown

Buisness Intelligence is the representation of theses factors as one. 

### Business Intelligence
* Works well with Data Warehousing

## Data Warehouse vs Data Lakes
* Lines Blurring between two factors. 

### Data Warehouse

* Often built on Relational Databases. 
* Can be built on a cube(multidimensional database). 
* Most compaines retain robust Data Warehouse technology, even with the introduction of Data Lakes. 


### Data Lakes
* Built on a big data environment (instead of RDBMS). 
* Handles extremely large volumes of data
* The three Vs:
	1.   #### Volume
	2.  #### Velocity
	3.  #### Variety

### Data Virtualisation 
* A read only distributed database. 
* Data is not copied into a seperate database. 
* Particularly useful in data with:
	* Simple Transfomations
	* Smaller Number of Data Sources
	* Relaxed response time

## Data Warehouse Envrionment
* Data wherehouse is built by pulling data from other applications and sources. 
* In between the sources and the warehouse, ETL can be performed.
* Somes times data will be pooled and copied into smaller environments (data marts).  

### ETL
* #### Extract 
* #### Transform 
* #### Load
<br> 












