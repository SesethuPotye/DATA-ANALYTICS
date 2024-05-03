
# Chapter 3


Exploring Databases

 Different database options to choose from when an organization needs to store data.

1. Relational: A relational database is a type of database designed to store and manage data in a structured way, using tables with rows and columns.
(all these tables connect to each other)

* Each table revolves around an entity
* when sing relational database you can encrypt tabales, hide information,making sure that the right people have access to data

* sturactured way to store data, it is stored in a table that is why is called relational sinsince there table has got  a relationship

  
3. Nonrelational:  Store data differently than relational databases. They offer more flexibility in structure and data types, making them a good choice for big data, rapid development, and specific performance needs.
# types f nonerational

* Key values: this shows data as a key and a value, one key that tise to a value and another value that tise to a key(and you can retrive these value by pluggig the keys and getting the information back

* column store: stores values in seperate column and is optimised in seperate columns

* graph database: this shows different entities in the data base and how they connect to each other in a graphical way

* Document sore database: so this data base sotores data in a document or a group of documents which is called a collection you can retrive information as it relats to a single information

A document database is indeed similar to a key-value store with enforced structure.

* Key-Value Similarities: Both document and key-value databases store data using key-value pairs for retrieval.
  
* Structured Values: A key difference is in the value. Key-value databases allow for any type of data in the value field. Document databases constrain the value to a specific format, often JSON. This structure makes documents more complex than raw values but enables richer queries.

#  Structured Flexibility:

Document databases share similarities with key-value stores, using key-value pairs for data retrieval.
However, document databases add a layer of structure. The value (data) adheres to a defined format, often JSON.
# Benefits of Structure:

* This structure unlocks greater flexibility compared to key-value stores.
* While retrieving data by document key is the fastest method, document databases allow you to search within the document itself.
# Example: Social Network Profiles

* Imagine storing social media profiles
where the key is the username and the value is a JSON document containing profile details (like Figure 3.6).
* With a document database, you can efficiently search for profiles based on specific fields within the document, like finding all profiles in a particular zip code.
# Core Advantage:

* The key advantage is the ability to search and query data based on its internal structure, making it powerful for scenarios where you need to find information within documents.


# ERD line endings
![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/87d8fb2d-1107-4c37-bd4f-2a03ce702cd7)


# Unary relationship
A unary relationship is when an entity has a connection with itself.
![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/5862f6c1-ded7-40a0-8b50-1c14bb9ddfb9)

# Entity relationship diagram

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/3005294a-d0ac-4d85-b639-e0e323e4a5a2)

Relational databases translate your ERD (Entity-Relationship Diagram) into a functioning system. Here's the breakdown:

1. ERD to Reality: An ERD blueprint is transformed into a physical database design.
   
2. Tables and Columns: ERD entities become database tables, and entity attributes become columns within those tables.

3. Column Order Flexibility: The order of columns within a table doesn't inherently matter. You can specify the order when retrieving data.

4.  Data Types: Each column is assigned a data type to define the kind of information it can store (e.g., text, numbers, dates).
   
6. Schema: The Big Picture: The final product, containing all this information, is called a schema. It's essentially a detailed ERD ready for database creation.


# Database schema
![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/9f9e91aa-9601-45c6-9650-21e34b92a1e5)


# Person Data

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/12285f8d-2fe7-4ac0-8e7a-99e354b71778)





Referential integrity

Referential integrity in data analytics ensures consistency across linked tables in a relational database. It's like a set of rules that maintains data accuracy and avoids confusion. Here's the gist:

* Foreign Keys and Primary Keys: The magic relies on primary keys (unique identifiers in one table) and foreign keys (which reference those primary keys in another table).
  
* Data Consistency: Referential integrity prevents rows existing in a table if the referenced data (identified by the foreign key) doesn't exist in the linked table.

*   Imagine an "Orders" table referencing a "Customers" table by customer ID. Referential integrity stops orders from being placed for non-existent customers.
  
* Avoiding Broken Links: By enforcing these rules, referential integrity helps avoid "orphaned" data - entries with meaningless foreign key references. This keeps your data analysis accurate and reliable.
  
In short, referential integrity acts like a data guardian, ensuring relationships between tables are valid and your analysis reflects a clean, consistent picture.

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/e7219491-4130-41dd-b407-33320d279aa6)

example:

customer ERD

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/d95f8e85-f57e-4754-961f-466c7733889a)


* In this ERD you understant that A specific customer can have many addresses, while a particular address belongs to a single customer.
  
* A specific address has a single address type, while a particular address type can apply to many different addresses.
  
* A specific address has a single state, while a particular state can exist in many different addresses. 

* Implementing the relationships from an ERD enforces data constraints
*  For example, Figure the above customer ERD shows that an individual address must have a relationship with a state
* You use foreign keys to implement data constraints in a database, like the relationship connecting Address with State.

# Foreign key data constraint

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/e41d77b7-a5a5-41d6-934d-1558d600cda7)

# Relational Database Providers: 

* Oracle: A veteran player, established in 1979, offering a mature and proven database platform.
  
* Microsoft SQL Server: Developed by Microsoft as a competitor to Oracle in the relational database market..
  
* Open Source Options: MySQL, MariaDB, and PostgreSQL are open-source relational database options, known for their flexibility and community support.
  
* AWS Aurora: A cloud-based relational database service by Amazon Web Services, compatible with MySQL and PostgreSQL. It leverages the scalability of the AWS cloud platform.


The passage emphasizes that these are just a few examples, and choosing the right provider depends on your specific needs. It then lays the groundwork for a comparison between relational and non-relational databases.


# Database Use Cases

Different business needs require different database designs. While all databases store data, the database's structure needs to match its intended purpose. Business requirements impact the design of individual tables and how they are interconnected. Transactional and reporting systems need different implementation approaches to serve the people who use them efficiently. Databases tend to support two major categories of data processing: Online Transactional Processing (OLTP) and Online Analytical Processing (OLAP).


# Online Transactional Processing

A vet clinic transactional schema is the blueprint for a database that tracks activity at the clinic. It uses interconnected tables to represent different aspects, like clients, pets, appointments, and procedures.


Tables: Clients, Pets, Appointments, Procedures, Treatments (linking procedures to appointments), Medications (potentially linking to Treatments).
Relationships:
* Clients can have many Pets (one-to-many).
* Appointments are for one Pet belonging to one Client (many-to-one with both tables).
* Treatments link Appointments to Procedures (many-to-one with both).
* Medications might be linked to Treatments (many-to-many).
Customization: The schema can be extended with Staff and Invoices tables, and specific details (attributes) are chosen for each table.

This structure allows the clinic to efficiently manage pet care, appointments, billing, and potentially inventory.

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/fb19458e-4a78-45db-998e-1d01518a4832)

# Normalization
Normalization is a process for structuring a database in a way that minimizes duplication of data.

# First normal form
* (1NF) is when every row in a table is unique and every column contains a unique value.
 ![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/5a8413c2-9451-48dc-b1ca-a6ec17681303)


# Second normal form 

* (2NF) starts where 1NF leaves off. In addition to each row being unique, 2NF applies an additional rule stating that all nonprimary key values must depend on the entire primary key. 
![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/d69d4d9b-d299-42de-98a4-7f1ebe923c4d)



# Third normal form

* (3NF) builds upon 2NF by adding a rule stating all columns must depend on only the primary key. 


![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/ed3122e4-1eb1-4770-a92d-f0a99a0c464e)

# Online Analytical Processing

Online Analytical Processing (OLAP) is all about crunching data for insights, and its database design reflects that goal. Here's a summary:

* Focus on Analysis: OLAP systems prioritize data analysis for organizations.
  
* Different Structures: While OLAP and OLTP (Online Transactional Processing) can use relational databases, their structures differ fundamentally.
  
* OLTP for Transactions: OLTP databases balance read/write performance for frequent transactions, leading to a highly normalized design (3NF - Third Normal Form) to minimize data redundancy.
  
* OLAP for Big Picture: OLAP databases favor a denormalized approach. Data is spread wider within tables (compared to OLTP) to optimize complex analytical queries that read large amounts of data at once. Joining multiple normalized tables can be slow for analysis.
  
Example: Imagine analyzing a family's pet history (Figure 3.18). The normalized OLTP schema (Figure 3.14) requires joining data from five separate tables, making the query complex and slow.

In essence, OLAP prioritizes speed and ease of complex data analysis over strict data normalization practices found in OLTP systems.

# Schema Concepts

* The design of a database schema depends on the purpose it serves. Transactional systems require highly normalized databases, whereas a denormalized design is more appropriate for analytical systems.
* A data warehouse is a database that aggregates data from many transactional systems for analytical purposes. 
* Transactional data may come from systems that power the human resources, sales, marketing, and product divisions.

*  A data warehouse facilitates analytics across the entire company.
* Data marts are specialized versions of data warehouses.
* Data warehouses cater to the whole company, while data marts zoom in on specific departments.
Your example of HR data for employee trends is a great illustration.

* Raw and Unstructured: Data lakes store data "as is" without forcing it into a pre-defined structure. This includes text, images, sensor readings, and anything else you might collect.
* Flexibility: This unstructured approach allows for wider data exploration and potential future uses you might not have anticipated yet.
* Complexity: Since data isn't prepped and organized, analyzing it requires more effort from data scientists who need to understand the raw format.
* Missing Structure: Unlike relational databases where data is organized and reflects business rules, data lakes lack this built-in structure.


* Design Matters: How you structure your data warehouse or data mart (schema design) affects how efficiently you can analyze it, especially for large datasets.
* Beyond Design: Thinking about the data's life cycle is just as important as the initial design. This includes:
  * Origin: Where does the data come from (different sources)?
  * Freshness: How often does the data change (daily, monthly)?
  * Retention: How long do you need to store the data (years, archives)?


# STAr


# Data Acquisition Concepts

* Data is the fuel for data analysis, and it can come from two main sources:
 * Internal Systems: Data you collect from your own software and applications.
 * External Sources: Data purchased or obtained from outside providers.
* This section dives into how to get data from both internal and external sources for your analysis

Integration 

Data from transactional systems flow into data warehouses and data marts for analysis. Recall that OLTP and OLAP databases have different internal structures. You need to retrieve, reshape, and insert data to move data between operational and analytical environments. You can use a variety of methods to transfer data efficiently and effectively.

 # methods to transfer data efficiently and effectively.


1. Extract:  In the first phase, you extract data from the source system and place it in a staging area. The goal of the extract phase is to move data from a relational database into a flat file as quickly as possible.

2. Transform:  The second phase transforms the data. The goal is to reformat the data from its transactional structure to the data warehouse's analytical design.

3. Load:  The purpose of the load phase is to ensure data gets into the analytical system as quickly as possible.

# ELT vs ETL for data warehouses:

 ELT vs ETL for data warehouses:

* ELT (Extract, Load, Transform): Loads raw data directly into the warehouse first, then transforms it later. This can be faster for big data sets.
* ETL (Extract, Transform, Load): Transforms data outside the warehouse before loading it in. This offers more control but can be slower.
* Key Difference: ETL transforms data with external tools, while ELT uses the power of the data warehouse itself (often with SQL).
* Choosing Between Them: Consider data size, processing speed needs, technical expertise, and overall data strategy.

  # ETL Vendors

  

# Data Collection Methods
![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/611e52a5-9407-4d0c-84f7-5f7ba7bea919)


 # Working With Data

Data Manipulation: When manipulating data, one of four possible actions occurs:

* Create new data.
* Read existing data.
* Update existing data.
* Delete existing data.
  
The acronym CRUD (Create, Read, Update, Delete) is a handy way to remember these four operations.

SQL uses verbs to identify the type of activity a specific statement performs. For each CRUD activity, there is a corresponding DML verb, as Table 3.8 illustrates. These verbs are known as keywords or words that are part of the SQL language itself.


# SQL Considerations: Case Sensitivity:
SQL keywords themselves are not case-sensitive (SELECT vs. Select).
However, column names and values might be case-sensitive depending on your database setup.
Formatting:
SQL queries can span multiple lines for readability, but they will produce the same result if written on one line.
Best practices for formatting depend on your organization, but should consider clarity, efficiency, and readability.


![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/d6235136-076d-4f93-83d3-b7c035633490)

# illustrates the basic structure of a SQL query that reads from a database. SELECT, FROM, and WHERE are all reserved words that have specific meanings in SQL.

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/c92e0e48-4bab-4583-80ac-a884a0ca26ab)


The SELECT clause identifies the columns from the table(s) that are retrieved. If you want to list the name and animal type from the table , the SELECT portion of the query will look like this:

SELECT Animal_Name, Breed_Name

The FROM clause in a query identifies the source of data, which is frequently a database table. Both the SELECT and FROM clauses are required for a SQL statement to return data, as follows:

SELECT Animal_Name, Breed_Name

FROM  Animal

As the queries in Figure 3.21 illustrate, it is possible to specify more than one location for data by joining tables together.
