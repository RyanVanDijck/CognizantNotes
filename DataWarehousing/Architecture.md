# Architecture

There are various approaches to data warehousing:

* Building a centralised warehouse (one central database). 
* Using data marts, smaller scale and more focused warehouses. 

## Centralised Data Warehouse

* One centralised data store is ideal 
* All sources will filter into one database. 
* Often very difficult to achieve. 

Some difficulties have been: 
*   Limits of technology.
*   Work processes.
*   Organisational and human factors.
<br>
* We now have techology that is able to handle this task. 
* Work Processes have now been improved in many businesses. 

## Data Warehouses vs Data Marts 

### Data Marts
* Like "Data Retailers". 
#### Dependant Data Marts
* Dependent data marts require a data warehouse.
* Dataware houses supply data to Dependant Data Marts 
* Architecturally Simple
* Uniform data across marts. 
#### Independent data marts 
* Doesn't need a data warehouse. 
* Draws data directly from source applications. 
* Data is organized dimensionally.
* Like a small scale data warehouse. 
* Little or no uniformity across marts. 
* Confusing architecture. 

### Independent Data Mart vs Data Warehouse

|Independent Data Mart|Data Warehouse|
|---|---|
|One or more Sources|Many Sources|
|ETL from sources|ETL from Sources|
|Possibly large data volumes|Possibly large data volumes|
|Dimensionally organised data|Dimensionally organised data|

## Which approach is the best fit? 
![Image of Selection Chart](./Architecture.png)






