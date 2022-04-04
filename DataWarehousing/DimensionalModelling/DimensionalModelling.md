# Dimensional Modelling
## Foundational Concepts
### Dimension Tables
* Key data warehousing subject areas.
* Subject areas that provide context to measurements. 
* All (or most) meaningful information.
* "One stop shopping" for that dimensional context. 
### Heirarchical vs "flat" dimensions 
![Diagram showing difference between hierarchical and flat dimensions](HeirFlat.png)

* Faculty members are part of a department, each department belongs to college. 
* These are examples of Heirarchical dimensions. 

* Student is not part of any Heirarchy. 
* So it is an example of a flat dimension. 

## Four types of fact table

1. Transaction fact tables 
2. Periodic snapshot fact tables
3. Accumulating snapshot fact tables
4. Factless fact tables

|Fact Table Type|Usage|
|---|---|
|Transaction|Record facts from transactions|
|Periodic Snapshot|Track a given measurement at regular intervals|
|Accumulating Snapshot|Track the progress of a business process through formally defined stages|
|Factless|1. Record Occurrence of a transaction that has no measurements </br> 2. Record coverage or eligibility relationships|


## Transaction fact table

* Formally transaction-grained fact tables. 
* Heart of dimensional models. 
* Where facts from transactions are stored. 
* There are rules to say how many facts should be in a fact table. 



Two or more facts can be stored in a table if both of the following rules apply: 

1. Facts available at same grain (level of detail). 
2. Facts occur simulataneously. 

Why not violate the rules? 

* Complicates data analysis
* Requires SQL workarounds
* Facts can be conceptually different. 


## Primary and Foreign keys

### Primary key of fact tables
* The combination of all foreign keys relating back to dimension tables. 
* Even if it has a natural key. 
* 



