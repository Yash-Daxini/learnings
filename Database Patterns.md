### Data Management concepts:

1. **Partitioning**

      It devides datasets to smaller more manageable segments. There are two fundamental approaches to   data partitioning. 
    1. **Vertical partitioning:** It splits tables by columns. This approach is useful when different applications or users access different columns of a table, allowing for more efficient queries and reduced data transfer.

    2. **Horizontal partitioning:** It splits a tables by rows. This approach is useful for distributing large datasets across multiple storage locations or servers, improving query performance and scalability.

2. **Database sharding:** It extends horizontal partitioning to distribute data across multiple independent database instances. Partitioning typical happens in single database while sharding uses mutlple databases often on separate physical machines. 

3. **DB Indexing:** 
   It is a data structure that improves the speed of data retrieval operations on a database table at the cost of additional space and slower writes. It increases write overhead.

4. **Replication:** Create replication of your primary database on different servers for scaling the  reads.

5. **Caching:** Store frequently accessed data in rapid access storage tears to reduce latency and backend load.
6. **CDN (Content Delivery Network)**
7. **Scalability**
