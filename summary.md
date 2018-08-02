![os](https://user-images.githubusercontent.com/42009214/43595100-d1db2a2c-9649-11e8-813c-e126eae76377.jpg)
  
Shell – CLI (command line interface) & GUI (graphical user interface)

![shell](https://user-images.githubusercontent.com/42009214/43595186-09829988-964a-11e8-90a7-42faf691547a.jpg)
### File system:
* Directory – Make dir; rename dir; delete dir; check content; check dir property
* File – create new; edit; rename; delete;  check property
Linux – open source; commonly used in server; multi-threading; Hierachical file system; security
//server usually UTC time zone (coonrdinated universal time), 4 hrs ahead of eastern
Everything in UNIX is either a file or a process
### Database
* Primary key: unique, not null, index
* Foreign key: point to PK, nul
* Candidate key: can be primary key, but is not
* Natural kay/business key: unique, real, (SIN, driver licence#)
* Surrogate key: technical key, unique, not real
NULL cannot be compared
Index: divided data into buckets. Good performance
### DDL (data definition language) – define database struction or table
* CREATE – CREATE DATABASE databasename; CREATE TABLE tablename (column1 datatype, column2 datatype, ...columnN datatype, PRIMARY KEY (columnname));
* ALTER – AlTER TABLE tablename ADD/DROP/MODIFY columnname datatype; ALTER TABLE tablename MODIFY columnname datatype NOT NULL;
* DROP – DROP TABLE tablename
* TRUNCATE – delete table space
* RENAME
### DML (date manipulation language)
* SELECT
* INSERT – INSERT INTO tablename (column1, ..columnN) VALUES (value1, ...valueN)
* UPDATE
* DELETE – DELETE FROM tablename WHERE condition;
### SQL
![sql join](https://user-images.githubusercontent.com/42009214/43595190-0c1617b0-964a-11e8-9312-4230a9561127.jpg)
### QA concept
#### TEST level:
* Unit testing
* Sanity testing
* Feature testing –positive, negative, boundary
* Regression testing
* Integration testing – Big-Bang; Top-down; Bottom-Up
* System testing
* Acceptance testing
#### Test type:
* Functional testing
Sanity testing
Feature testing
Regression testing
SIT
UAT
* Non functional testing
Performance testing – scalability, reliability; load tesing; stress testing
GUI testing
Compatility testing
Installation testing
Usability testing
Security testing
