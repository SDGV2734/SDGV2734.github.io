---
Title: DBS101 Flipped Class 7 (Guided session)
categories: [DBS101, Flipped_Class_7]
tags: [DBS101]
---

### Topic: Storage and buffer management 

In todays guided session of practical 7 we learned about creating virtual representations of disk storage units, setting up RAID setups for redundancy and performance, and managing temporary data storage in memory buffers efficiently.

In the first task, which was about Disk Block implementation we were introdued to methods initializing the disk, allocating blocks for data, and managing the allocation of blocks. This simulation was useful for understanding the principles of disk storage and file system management, including how data is stored and retrieved in blocks, and how space is allocated and managed within these blocks.

In the second task, which was about implementation of simulating different RAID levels (0, 1, and 5) using a fixed block size and a configurable number of disks. And it demonstrates how data is written and read across different RAID configurations, including how data is distributed (striped) and protected (mirrored or with parity). It also shows how a RAID array can be rebuilt after a disk failure, specifically for RAID 1 and RAID 5 configurations. This simulation was useful for understanding the principles of RAID technology, including its benefits and limitations. RAID configurations like RAID 0 offer high performance but no redundancy, RAID 1 provides redundancy at the cost of storage space, and RAID 5 combines performance and redundancy. However, RAID is not a complete backup solution and can still lose data if the RAID controller or all disks fail simultaneously.

in the final task, we were given with simulation of buffer pool with a fixed size, designed to manage pages of data. The buffer pool used the Least Recently Used (LRU) strategy to manage its contents, ensuring that the least recently accessed pages are removed when the buffer is full and a new page needs to be added. This implementation of an LRU cache strategy, which is commonly a caching technique used to improve the performance of applications by keeping the most frequently accessed data in a cache. 

---

### Exercise

In todays exercise we were given a task to learn and research how a database is build from scratch and the procedures to create a database. In this exercise I learned the fundamentals of database and from where and how to start building a database. The key concept that I learned during the process were:

- Defining the data requirements and understanding the data and how we want to store the data in our database. 

- Choosing the correct database model that best suits our needs.

- Designing the database schema with logical data models by defining tables, columns, datatype, primary keys, and foreign key.

- Setting up database environment and configuring it according to the requirements.

- Implementing data validation and security measures  to prevent SQL attacks.

- Maintaining proper documentation for the database design, schema, and code for future maintenance.



