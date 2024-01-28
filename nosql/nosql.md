# NoSQL

> Class notes of NoSQL taken from PWSkills by Yuvraj.

# Challenges of RDBMS

## 1. Unstructured or Dynamic Schema

**Schema**: It is a logical structure of the data

**Dynamic Schema**: The data changes/updates dynamically

**Challenges**: Due to the dynamic updating of data, RDBMS might not be the best choice. Certain complexities arises while using RDBMS in such circumstances.

## 2. Scalability

**Scalability:** The ability of a computing process to be used or produced in a range of capabilities.

**Challenges**: RDBMS is a best solution until the data is stored in a single computer, but if a single computer contains too much data then it causes scalability issues. Even if we try to scale the no. of computer systems, the queries becomes more slower because it will have to run multiple JOINS and multiple NETWORK CALLS to connect with other systems. Therefore, scaling systems is inversely proportional to performance in RDBMS

## 3. Complex

**Challenges**: RDBMS is complex in terms of data modelling, data structuring. RDBMS contains complex concepts such as Normalization, Schema, Relationships, Joins, Partitioning which makes it a bit complex database management system.

## 4. Expensive

**Challenges**: RDBMS can be a very expensive solutions for companies and organizations to store and manage database. Ex: Oracle’s Enterprise Plan costs about **₹ 179.25251**

# NoSQL

## Introduction

- NoSQL does not mean it is an ANTI-RDBMS database management system, instead it complements RDBMS.
- The functionalities which are limited in NoSQL are covered in NoSQL databases.

## Features

- Natively scalable (Because of distributed systems)
- Dynamic schema

## Categories/Types of NoSQL

1. Key Value Database
2. Document Based Database
3. Columnar Database
4. Graph Database
5. Time Series

## Distributed Systems

**Definition**: Distributed System is an organization of systems in which multiple computers are used for storing and computing data.

## Features

1. Uses multiple systems (i.e. Commodity Hardware, which means, using multiple inexpensive systems instead of a single expensive one)
2. Each machine will be connected to each other over network (aka, Cluster of Machines)
3. All the complexities should be abstracted from the end users

## Faults in Distributed Systems

1. It uses cheap/commodity hardware which are unreliable
2. It is network dependent and network is the most unreliable thing to happen

## Solutions of Faults

1. **Replication:** Storing data on multiple nodes instead of a single node, by which, even if one of the node goes down, other node will still be there to handle the situation.

## CAP Theorem

### C → Consistency

If many people at the same time are accessing the same data and the data retrieved by people, then, the system is said to be consistent. Whenever, data is updated at a particular node at time t1, then, some inconsistency arises which is eventually consistent again after sometime.

### A → Availability

Whenever user asks for data and the application provides the data to the user, then the system is called as Highly Available (i.e. it show highly availability)

### P → Partition Tolerance

Whenever a device goes down, the whole cluster of devices/machines may go down. Therefore, we use REPLICATION in order to tolerate such partitioning of machines

### Theorem:

CAP Theorem says that, any system cannot be CONSISTENT, AVAILABLE and Partition Tolerant at the same time. Hence, only 2 parameters will able to be acquired by the system and will sacrifice the 3rd parameter. [i.e. If a system chose CA then, P will be compromised; If a system chose AP, then C will be compromised; If a system chose CP, then A will be compromised].

## Types/Categories of NoSQL Databases

## 1. Key Value Database

- Data is stored in the form of keys and values (i.e. (k, v))
- Key is normally string and value can be any other type of data
  ### Use Cases -
  - Caching: Avoids multiple unnecessary calls and computations (Ex: Redis)
  - Distributed Systems: (Ex: Zookeeper)
  - Real-Time Analytics
  ### Challenges -
  - Lack of query support
  - Data modelling complexity
  - Limited data type

## 2. Document Database

- Data is stored in the form of documents (that could be JSON, BSON)
  ### Use Cases -
  - Semi-structured data
  - Flexibility
  - MongoDB uses Document Database
  - Best for RDBMS as well as NoSQL
  ### Challenges -
  - Consistency
  - Aggregation
  - Transaction Support

## 3. Graph Database

- Data is stored in the form of Graph (i.e. in the form of set of edges and vertices)
  ### Use Cases -
  - Complex Relationships
  - Recommendation System
  - Fraud Detection (Evaluates very complex relationships)
  - Ex: Neo4J is widely used Graph Database
  ### Challenges -
  - Data Modelling is complex and is still evolving
  - Less query speed in huge database
