## Introduction

- ***Relational Databases*** are used for updating.
- ***Data warehouses*** (fewer tables, more records) are used for reporting.
- Flat files and excel sheets are alternatives to databases but lack scalability.

## Data Modelling Process

- Data modelling is the process of analysis data and creating design.
- Data Model Types: Conceptual (Table names), Logical (Table's Column names), Physical (Table schema).
- Goals of the database helps to identify the fields of the database.
- Best way to identify entities in tables is to look for Nouns in the requirements. While creating tables for the entities the best practise is to keep singular entities as table name.
- Properties of the entities are the best attributes i.e column names for the table.

## Database Design

- ***Normalisation:*** Process of converting a database design into a standard format i.e ***Normal Form (standard of designing a database)***
- Advantages of Normalisation : eliminate inconsistencies, remove duplicates and improve performance.
- ***Types of relationships:*** one to one , one to many, many to many and self.
- ***Relational Databases can't have many to many relationships. So have to convert many to many into two one to many relationship by introducting a new table in the middle.***
- 1 ***many to many*** relationship can be converted to 2 ***one to many*** relatioship, for better performance in the database.
- self relationships exists where records of a table has relationship with other records of the same table. E.g Employee Managers relationship where Managers are also an employee.
- ***It's best practise to maintain single source of truth for column values i.e updation of a particular column value should be performed at only one table.***
- Normalisation helps to make insert, update and delete operations easier.

## Normal Forms

- ***First Normal Form : 1NF***
  - Make the rows uniquely identifyable i.e add primary keys. 
- ***Second Normal Form : 2NF***
  - Must be in ***1NF***.
  - ***Each non-key attribute(non primary-key) must be functionally dependent on the primary key***.
  - The columns which are not dependent on primary key of the table has to be moved to some other table with foreign key relationship in the current table.
  - Usually the foreign key will be added into the table which will have many relationship with the current table e.g ***category*** has mutiple ***subject*** so ***category_id*** will added to ***subject*** table as foreign key.
- ***Third Normal Form : 3NF***
  - Must be in ****1NF**** and ***2NF***.
  - ***There must be no transitive functional dependency (TFD)***
  - ***TFD:*** Every non-key attribute must be dependent on the primary key only. i.e ***(A -> B -> C)***

## References

- [Lucid Chart](https://www.lucidchart.com/) - Drawing tool.