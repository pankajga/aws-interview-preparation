## 01. What is DynamoDB?
DynamoDB is a fully managed NoSQL database service. It is backed by AWS and provides exciting features like seamless scalability, fast performance, and high reliability over data. DynamoDB supports both key-value and document data structures. In addition, this service comes with different pricing tiers to suit varying user requirements.

DynamoDB is quite effective at data storing and retrieval in all traffic levels and allows the users to create tables for the database.

## 02. What are NoSQL databases?
NoSQL or non-relational databases focus on different data storing models rather than a tabular structure. There are four types of NoSQL databases:

* Key-value stores
* Document stores
* Graph store
* Colum stores
* DynamoDB supports both document and key-value structures.

## 03. What are the key features of DynamoDB?
* Highly Scalable without any intervention from the user.
* It has a latency of microseconds.
* Serverless and enterprise-ready.
* Encryption at Rest.
* On-demand backup and restore.
* Point-in-time recovery.

## 04. What are the advantages of using DynamoDB?
* We can store any amount of data with the unlimited storage provided by the DynamoDB service.
* The data we store replicates over many availability regions. It allows to easily cope with global-scale applications and make sensitive information highly available.
* It is highly cost-effective, and the users have to pay only for what they use.
* Easy administration and the user doesn't have to worry about software patching, setup, and configuration because AWS fully manages DynamoDB.
* DynamoDB has an advanced system for reporting and highly secured user authentication mechanisms to provide maximum security over sensitive data.

## 05. What are the disadvantages of DynamoDB?
* No triggers and lack server-side scripts.
* No table joins possible.
* Data querying is highly limited.
* The cost can be unpredictable with spikes in usage.

## 07. What is DynamoDBMapper?
The DynamoDBMapper class is an entry point that allows access to DynamoDB endpoints, enabling users to handle the database. Users can perform CRUD operations, run queries, and scan against tables. And this class is only available for Java.

## 08. What is meant by Partition Key in DynamoDB?
A partition key is a primary key composed of only a single attribute. In DynamoDB, the value of the partition key work as the input for internal hash functions. The resulting output from that function helps determine the partition to store the item in question.

## 09. How does DynamoDB Query functionality work?
DynamoDB provides 2 options to fetch data from collections as Query and Scan. When using Scan, DynamoDB will look through the complete table for records with matching criteria, while Query uses key constraints to perform a direct lookup for a particular data set.

In addition to the primary key, DynamoDB uses global secondary key, local secondary key, and partition primary key to help improve flexibility and improve the read/ write operation speed.

As a result, it is fast and time effective compared to the DynamoDB Scan operation and is recommended for most data fetching scenarios.

## 10. What are the key differences between Amazon DynamoDB and Amazon Aurora?
* DynamoDB is NoSQL, whereas Aurora is a relational database service.
* Aurora uses SQL for data manipulation and fetching, whereas DynamoDB uses a specialized syntax.
* Aurora uses horizontal partitioning, whereas DynamoDB uses sharding as the partitioning method.
* DynamoDB implements key-value and document models where Aurora operates with relational DBMS.
* Aurora supports server-side scripting, but DynamoDB does not.

## 11. List 5 ways to fetch data from DynamoDB
* GetItem
* Query
* Scan
* BatchGet
* TransactRead

## Database Sharding
* Involves dividing a database into smaller, autonomous units (shards), typically distributed across multiple servers
* Each shard contains a subset of the data and is responsible for specific data ranges or attributes
* Often employed in distributed systems to improve scalability and performance
* Requires a mechanism to route queries and transactions to the appropriate shard

## Database Partitioning
* Divides a database into smaller logical units, but these units are not necessarily autonomous like shards
* Partitions can be located on the same server or within a single database
* Aims to organize data for better manageability and performance, often based on attributes like date, region, or key ranges
* Does not involve distributing partitions across multiple servers as a fundamental requirement but that is often done to preserve data in case of the loss of individual nodes
* In summary, while both Sharding and Partitioning aim to organize data, Sharding specifically focuses on distribution across multiple servers for scalability though partitioning often does the same thing.

## 12. What are DynamoDB Projections?
As its name suggests, the attributes in a table projected to the index are the projections. (Similar to the GROUP BY operation in SQL). Projections can exclude all the unnecessary items and reduce the overall size of the payload returned by the API.

We have to define the projected attributes each time we create a local secondary index. Each index must have minimally three attributes: table partition key, index sort key, and table sort key.

## 13. How does DynamoDB prevent data loss?
There is long-term storage and a two-tier backup system in DynamoDB to keep data loss at a minimal level. There are three nodes for each participant, and each node contains the same data from the partition. In addition, there is a B tree for data location and a replication log to track the changes in each node. DynamoDB stores snapshots of these and stores them in another AWS database for a month for data restoration when necessary.

