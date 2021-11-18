### ***Scalability***
- **Types of load**
  - **Web Server:** Requests per second
  - **Database:** Ratio of reads : writes
  - **Chat Room:** Number of active users

### ***Sharding***

*Sharding is a type of database partitioning that separates very large database into smaller parts, more easily managed parts are called data shards.*

   - **Types of sharding**
     - **Key-Based Sharding:** It is also known as alogrithmic sharding as it relies on hash function to identify the shard for the record. Hash funcion needs to be changed when data is increased and new shard has to be added.
     - **Range-Based Sharding:** It is useful when the data has to be sharded based on some deifinte range like month wise dates or quarted wise dates.
     - **Directory-Based Sharding:** It is also known as dynamic sharding. It is used when any one of the columns have fixed values like countries, states, zones etc. The column with fixed has separated shard for each data and value is mapped to a shard in a lookup table.

### ***Caching***
*Caching acts as short term memory storage that has limited space but faster to access as compared to original data source. It works better with static data.* 
 - **Types of Cache**
   - **Write-Through Cache:** In this cache, whenever there is page-miss, the server gonna fetch/update the database and cache  before sending the response to the client.
   - **Write-Back Cache:** In this cache, when there is an edit in the database, the server only updates the cache and not the db. Db synchronization cache happens asynchronously. This method has a drawback of losing data if cache eviction happens before updating the db.
     - **Eviction Policies:** Least recently used, Least frequently, Last In First Out (queue).

### ***Peer to Peer Network***
*In this network, every computer acts as peer/server to other nodes in the network.*
  - **Types of P2P**
    - **Unstructured P2P:** Work load is shared equally, nodes are connected randomly, difficult to find data, easily built.
    - **Structured P2P:** Data is accessed easily, difficult to set up due to creation of virtual layer.
    - **Hybrid P2P:** Combination of P2P and client-server architecture. This network has a central server and each node can work independently as well.

### ***Proxies***
*Proxy are servers which acts as bridge between the clients and servers. **Proxy chaining** involves forwarding traffic from one proxy to another.*
  - There are two types of proxy servers.
    - **Forward proxy:** Proxy server is at client side. 
    - **Reverse proxy:** Proxy server is at server side.
  - **Purpose of Proxy Server:**
    - Gain admittance to blocked/unallowed assets
    - Improved security
    - Improved Data transfer speed
    - Privacy Benefits

### ***Replication and Redudancy***
**Replication:** *It is the technique of creating duplicate copies of the primary DB as the standby DB, which will be used when the main DB goes down. Both synchronous and asynchronous update happens on the db based on the use case.*

**Redudancy:** *It is the duplication of critical components of the system with the intention of increasing reliability of the system, usually in the form of backup or to improve system performance.*
  - **Model of Redudancy:**
    - **Standby/Backup Redudancy:** In this model a secondary system is present to take over the primary system in case of failure.
       - **Types of standby:**
         - **Hot standby:** Not in sync, will take time to bring everything online.
         - **Cold Standy:** In sync and always ready which shortens downtime.
    - **N Modular/Parallel Redudancy:** In this model multiple units are running in parallel and are in sync. It has a quick switchover time as compared to Hot standby.
      - **Types of N modular redudancy;**
        - **Double Modular Redudancy(DMR):** Uses 2 identical units
        - **Triple Modular Redudancy(TMR):** Uses 3 identical units
        - **Quadruple Modular Redudancy(QMR):** Uses 4 identical units
    - **1:N Redudancy Technique:** It is the most efficient redudancy technique since the cost is much lower as compared to other designs. It has only single backup which serves as backup for other systems. The disadvantag of this methodolgy are the additional complexities of choosing when to switch framework.

### ***Indexes***
*Indexes can defined as a data structure in any DB that points to the location where actual DB is present. It is used to retrive data faster.*
*Indexing is done by 2 methods. 
**Ordered Indexing:** Indexes are stored either increasing or decreasing order 
**Hash indexing:** Indexes are calculated using hash function*
  - **Types of Indexing:**
    - **Primary Indexing:** It is done with ordered data file having primary key and ordered key field having fixed length. It specifies 1-1 relationship.
    - **Secondary Indexing/ Non Clustering Index:** In this indexing data is not found directly, instead it has multilevel virtual reference which points to the location of the data and data is present in leaf nodes.
    - **Clustering Index:** In this indexing data is present in the same table having indexes. Records with similar characteristics are grouped together and indexes are created for these groups.
    - **B-Tree Index:** This multilevel indexing is present in the form of balanced binary search tree. All nodes in B-Tree are pointer to some other node or data. This is the fastest indexing technique.
<br>

- **NOTES:**
  - **Block Size is the unit of data exchange between cache and main memory.**
  - **Data and Instructions that are being used frequently are stored in Block.**
  - **Partition is not allowed in any indexed based data.**
  - **Indexing needs a primary key on the table with a unique value.**