# DP-900-Azure-Data-Fundamentals-Study-Guide
Comprehensive study guide for Azure Dta Fundamentals (DP-900) certification

## Welcome to the Azure Data Fundamentals (DP-900) Study Guide!

This repository contains comprehensive notes, practice tests, and resources to help you prepare for the DP-900 certification exam.

## Table of Contents
1. Introduction
2. Study Notes
3. Practice Tests
4. Additional Resources

## Introduction

This guide is designed to help you understand the key concepts and prepare effectively for the DP-900 exam. It covers the following topics:
- Describe core data concepts
- Explain how to work with relational data on Azure
- Explain how to work with non-relational data on Azure
- Explore modern data warehouse analytics in Azure

## Study Notes

# Describe Core Data Concepts

## What is a Database?
- A database is an organized collection of structured information or data, typically stored electronically in a computer system. Its primary functions include storing, retrieving, and managing data efficiently.
- **Types of Databases:**
  - Relational Databases (e.g., SQL Server, MySQL, PostgreSQL)
  - Non-Relational Databases (e.g., MongoDB, Azure Cosmos DB)
  - Object-Oriented Databases
  - Graph Databases

## What is a Data Warehouse?
- A data warehouse is a large, centralized repository of integrated data from multiple sources, designed for query and analysis. Unlike traditional databases optimized for transaction processing, data warehouses are optimized for analytical processing, handling large volumes of historical data efficiently.

## ETL Process
- ETL stands for Extract, Transform, Load:
  - **Extract:** Retrieving data from various source systems.
  - **Transform:** Converting the extracted data from its source format into the required target format.
  - **Load:** Inserting the transformed data into the target system (e.g., data warehouse).

## File Formats Supported in Azure
- **CSV:** Used for tabular data and delimited data.
- **JSON:** For semi-structured data.
- **Avro:** For big data processing; a row-based data format.
- **Parquet:** For analytics workloads; a columnar data format.
- **ORC:** For optimizing read and write operations in Hive; a columnar data format.

## Types of Data in Azure
- **Structured Data:** e.g., SQL databases.
- **Semi-Structured Data:** e.g., JSON, XML.
- **Unstructured Data:** e.g., images, videos.

## Transactions and ACID Properties
- **Transactions:** A sequence of database operations treated as a single unit of work, ensuring data integrity.
- **ACID Properties:**
  - **Atomicity:** All operations in a transaction succeed or they all fail.
  - **Consistency:** A transaction brings the database from one valid state to another.
  - **Isolation:** Concurrent execution of transactions results in a state that would be obtained if transactions were executed sequentially.
  - **Durability:** Once a transaction has been committed, it will remain so.

## Data Roles and Responsibilities
- **Database Administrator:** Manages data security, implements backup and recovery plans, and monitors the performance of database solutions.
- **Data Engineer:** Manages data privacy, monitoring data stores and data pipelines.
- **Data Analyst:** Responsible for building data models, cleaning and transforming data, and finding hidden data patterns.
- **Database Users:** Use a database.

# Identify Considerations for Relational Data on Azure

## Relational Data
- Relational data is structured data that adheres to a schema and is stored in tables with relationships between them.

## Azure Services for Relational Data
- **Azure SQL Database:** A serverless platform as a service (PaaS) SQL instance used to store relational data. It is the best option for create, read, update, and delete (CRUD) operations and uses the least amount of storage space. It is used to persist processed results in a database table for querying and analysis.
- **Azure Database for MySQL:** A fully managed MySQL database service.
- **Azure Database for PostgreSQL:** A fully managed PostgreSQL database service.

## SQL Managed Instance
- A PaaS service where databases are maintained in the same SQL Managed Instance cluster. Allows migration of an entire SQL server to the cloud without requiring infrastructure management after migration.

## SQL Server on Azure Virtual Machines
- Running Windows or Linux, these are not serverless options and require full management of SQL Server.

## Structured Data Concepts
- **Datatypes:** Define the type of data that can be stored in columns (e.g., integer, string).
- **Primary Key and Foreign Key:** Ensure unique identification of rows and relationships between tables.
- **Indexes:** Improve the speed of data retrieval.
- **Views:** Virtual tables based on the results of a SELECT query.
- **Stored Procedures:** Encapsulate SQL statements for reuse.
- **Functions:** Used to query a database but cannot modify or create objects.
- **SQL Commands:**
  - **SELECT - INTO:** Inserts data into a table.
  - **SELECT – OVER:** Applies a windowing function.
  - **INSERT – VALUES:** Inserts values into a single row.
  - **JOIN:** Combines data from two tables.
  - **SELECT – HAVING:** Filters data from a GROUP BY command.
  - **UPDATE and MERGE:** Modify existing data.
  - **UNION:** Combines results from two queries.
  - **INTERSECT:** Shows common values between two queries.

## Database Management Systems
- **SQL Server:** Microsoft’s relational database management system.
- **Azure Native Service:** Built for and integrated with Azure.
- **Apache Spark:** Distributed computing system for big data.
- **Databricks:** Unified analytics platform on Apache Spark.
- **Spark Pool:** Compute resources for Apache Spark jobs.
- **Scala:** Programming language for big data processing.
- **Apache Hadoop:** Framework for distributed storage and processing.
- **Pipeline:** Series of data processing elements.
- **Event:** Significant change or action triggering a response.
- **MariaDB:** Open-source relational database. MariaDB has built-in support for temporal data. It enables applications to query data as the data appeared in previous points in time.
- **MongoDB:** A popular NoSQL database that uses a document-oriented data model. It can be used in Azure through Azure Cosmos DB’s API for MongoDB.
- **HBase:** A non-relational, distributed database modeled after Google’s BigTable.

# Describe Considerations for Working with Non-Relational Data on Azure

## Non-Relational Data
- Non-relational data doesn’t adhere to a fixed schema. It can be managed in Azure using various services.

## Azure Services for Non-Relational Data
- **Azure Tables:** For structured NoSQL data.
- **Azure Blobs:** For unstructured data like documents or media files.
- **Azure Files:** For shared file storage in the cloud.
- **Azure Data Lake Storage:** Used to store data. Data Lake Storage is commonly used to ingest data for processing.
- **Azure Cosmos DB:** A globally distributed, multi-model database service that supports multiple APIs:
  - **MongoDB API:** Stores data in the BSON format.
  - **Table API:** Used for key/value pairs.
  - **Cassandra API:** Used for tabular data in a column-family storage.
  - **Gremlin API:** Used for graph databases.
  - **SQL API:** Manages data in the JSON format.

## Querying APIs
- The Cassandra API is queried by using SQL.
- The MongoDB API is queried by using MongoDB Query Language (MQL).
- The Gremlin API is queried by using Graph.
- The Table API is queried by using OData and LINQ queries.

## Types of Non-Relational Databases
- **Document Database:** Uses unstructured data like JSON.
- **Key/Value Store:** Simple lookups based on a single key.
- **Graph Database:** Stores hierarchical data.
- **Column-Family Databases:** Store tabular data comprising rows and columns.

# Describe an Analytics Workload on Azure

## Azure Synapse Analytics
- An integrated analytics service that brings together big data and data warehousing. It provides capabilities for data integration, enterprise data warehousing, and big data analytics. Use cases include real-time analytics, data exploration, and machine learning.

## Azure Data Factory
- A cloud-based ETL and data integration service. It allows you to create data-driven workflows for orchestrating data movement and transforming data at scale. It supports a wide range of data stores and compute environments.

## Data Pipelines
- A set of actions that ingest, process, and move data from various sources to storage for analysis. In Azure, services like Data Factory and Synapse Analytics can create and manage data pipelines for batch and real-time processing.

# Data Warehouse Architecture
- A typical data warehouse architecture includes:
  - Data Sources
  - ETL Processes: Extract, Transform, Load
  - Data Storage: Often in a star or snowflake schema
  - Metadata Repository
  - Query and Analysis Tools
  - Data Marts: Subsets of the warehouse for specific business units

# Data Warehousing
- **Data Warehouse:** Uses fact and dimension tables in a star/snowflake schema. Cubes are generated from a data warehouse but are tables themselves.
- **Fact Table:** In a data warehouse, a table that contains quantitative data about business events or transactions. It typically contains foreign keys to dimension tables and numerical measures. Fact tables contain measures that are aggregated, not values to aggregate by.
- **Dimension Table:** In a data warehouse, a table that contains descriptive attributes used to provide context to numeric data in the fact table. Examples include date, product, or customer tables. Dimensions are used to aggregate data.
- **Relationship:** Used to tie facts to dimensions.

# Data Processing and Analytics
- **Azure Synapse Analytics:** An Azure native service built on Apache Spark, allowing near real-time analytics on operational data. Supports creating pipelines in response to events.
- **Azure Data Factory:** Allows orchestration of data flow without coding by using pipelines. Used to run ETL pipelines.
- **Databricks:** Used for processing large amounts of data, supported by multiple cloud providers.
- **HDInsight:** Used to process large amounts of data by using Hadoop.
- **Batch Processing:** Used to execute complex analysis. Batch processing handles a large amount of data at a time and is usually measured in minutes and hours.
- **Azure IoT Hub and Azure Event Hubs:** Can be used as sources for stream processing. Event Hubs is used as a source or a sink for stream processing.
- **Stream Processing:** Processes data as it arrives, executing simple analytics or writing data to a sink. Handles small chunks of data.
- **Azure Stream Analytics:** Defines streaming jobs, applies a perpetual query, and writes the results to an output. Stream Analytics can handle stream processing from Kafka to Data Lake. Stream Analytics allows you to aggregate data from a specific period before it is written to a data lake.
- **Data Explorer:** Used for the analysis of large amounts of text log data, websites, and IoT devices using a common querying language.

# Microsoft Power BI
- A business analytics service that provides interactive visualizations and business intelligence capabilities. It allows users to create reports and dashboards, share insights across an organization, and embed analytics into applications.

# Data Visualization and Analytics Tools
- **Power BI Desktop:** Used to define analytical models.
- **Power BI Phone App:** Used to view Power BI reports.
- **Power BI Service:** Used to serve data.

# Data Visualization Tools
- **Scatter Plots:** Determine relationships between numeric values.
- **Pie Charts:** Compare values as proportions.
- **Line Charts:** Examine trends over time.
- **Bar Charts and Column Charts:** Compare numeric values for discrete categories.
- **Tables:** Display multiple related values.
- **Card:** Shows a single value, useful for highlighting important metrics.
- **Matrix:** View data across multiple dimensions.
- **Dashboards:** Combine related reports for easier visibility into data.


## Practice Tests

Test your knowledge with these practice tests:
- Practice Test 1 - https://learn.microsoft.com/en-us/credentials/certifications/azure-data-fundamentals/practice/results?assessmentId=24&practice-assessment-type=certification&snapshotId=bb0a2d23-9cb6-4171-b8fd-a67a58e1ac2d
- Practice Test 2 - https://learn.microsoft.com/en-us/credentials/certifications/azure-data-fundamentals/practice/results?assessmentId=24&practice-assessment-type=certification&snapshotId=d3a17feb-6ca8-44ff-b899-ae7972a4950e

## Additional Resources

Here are some additional resources to aid your study:
- Microsoft Learn: DP-900 Learning Path - https://learn.microsoft.com/en-us/credentials/certifications/azure-data-fundamentals/?practice-assessment-type=certification#certification-prepare-for-the-exam
- YouTube Playlist: Azure Data Fundamentals - https://youtu.be/wi3PkLK_gNc?si=caWnZdBjeq3wgX3k
