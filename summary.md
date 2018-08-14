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
* ALTER – ALTER TABLE tablename ADD/DROP/MODIFY columnname datatype; ALTER TABLE tablename MODIFY columnname datatype NOT NULL;
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
![test level](https://user-images.githubusercontent.com/42009214/43596548-99a1f560-964d-11e8-93ad-2a3455d2be03.png)

### SDLC/STLC
![sdlc](https://user-images.githubusercontent.com/42009214/43596553-9bf6301a-964d-11e8-942b-eeadda7aa3d2.jpg)
Test strategy vs test planning
test strategy – high level (PM)
### Test plan (test lead or test manager)
scope, approach, schedule and resource
define roles and responsibilities; schedule; environment prepar4, risks and acceptance criteria
* test plan identifier
* introduction
* test item
* **IN/OUT scope**
* approach
* **entry/exit criteria**
entry criteria: business environment, requirement finalized; unit test pass
exit criteria: no severity 1 and severity 2 defect
* test deliverables
* testing task
* environment needs
* responsibilities
* staffing and training
* schedule
* risk
* approval
### Test case 
* **test case ID**
* test scenario
* test case description
* **test actions**
* prerequisite
* **expected result**
* test parameters
* **actually results**
* environment information
* comment
### Defect management
* priority
* severity
### DLC
* new
* assigned
* test
* verified
* closed
* reopened
* deferred
* rejected
### Dimesion vs Fact table
![dimension fact table](https://user-images.githubusercontent.com/42009214/43650817-c6524a94-970e-11e8-94ad-4989e361e854.jpeg)

### OLTP vs OLAP
#### OLTP (on line transaction processing)
* relatively standardized and simple query, fast 
* multi-access
* normalized with many table; joins
* operational data
* short and fast insert and updates
#### OLAP (on line analytical processing)
* aggregated, historical data
* multi-demensional schemas  
  * star schema - denormalized dimension tables to describe data aggregated in a fact table.
  * snow flake schema - normalized dimension tables to describe data aggregated in a fact table
* integrated different sources (OLTP)
* denormalized
* periodic long-running batch jobs
* complex query involving aggregations
![star snow flake schema](https://user-images.githubusercontent.com/42009214/43649955-7ff07dca-970c-11e8-9703-a76a17277e1c.jpg)
## ETL
Data is extracted from OLTP database, or non-OLTP system, transformed to match the data warehouse schema and loaded into data warehouse database
### Extraction
#### Source: how to verify source files 
* Business
  * mortgate
  * credit card information
  * CIF (customer information)
  and so on
* IT 
  * flat file: 
    * file name validation (name convention), also size of the file:
      * header information: meaning of field (business)
      * Trailer information: filename|transaction date|total count of records|schema change Y/N -- count validation
      * "bcr" -- control file, a small binary file that is part of an Oracle database. The control file is used to keep             track of the database's status and physical structure.
    * how to find the file (ls, cd, find, locate, grep, pwd, cat, >, >>)
    * column length, data type
    * extract attrubutes
        * frequency -- daily, monthly, bi-weekly
        * delta/full: delta -- update/new data compared to the previous data; full snapshot-- all historical data
     * delimiter ","-csv or "pipe", or tab . command: cut -d" " -f 1 file.txt; cut -c 1-7 file.txt; cut -b 1,2,5 file.txt 
        // sed -n '2p' file.txt; sed -n '10,33p' file.txt
     * fixed length
     * null -- left join
     * duplicate -- group by,having
     * constrain -- PK, FK
  
  * json -- javascript object notation
    * notepad++ json plugin
    * object: {key1: value, key2: value}
    * array: [value, value]
  * xml -- extensible markup language
    * <string> ...</string>
    * notepad++ plugin -- by providing .xsd, the schema of xml can be validated
  * ebcidic -- Extended Binary Coded Decimal Interchange Code
    * cobol copybook, record editor
    * mainly used on IBM mainframe
  * RDBMS
    * fields; data type
    * duplicate: group by , having
    * left join: check NULL
    * union; union all
    * constrains: PK, FK, NULL
  ### Data warehouse
  * subject oriented -- modelling and analysis
  * integrated -- heterogeneous sources
  * time variant -- time period
  * non-volatile -- historical data
  ### ETL testing five stages
  * identifying data source
  * data acquisition
  * implement business logics and dimensional modelling
  * build and populate data -- run ETL process
  * build reports
  
