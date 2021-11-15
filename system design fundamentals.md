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
 - Caching acts as short term memory storage that has limited space but faster to access as compared to original data source. It works better with static data. 
 - **Types of Cache**
   - **Write-Through Cache:** In this cache, whenever there is page-miss, the server gonna fetch/update the database and cache  before sending the response to the client.
   - **Write-Back Cache:** In this cache, when there is an edit in the database, the server only updates the cache and not the db. Db synchronization cache happens asynchronously. This method has a drawback of losing data if cache eviction happens before updating the db.
     - **Eviction Policies:** Least recently used, Least frequently, Last In First Out (queue).

### ***Peer to Peer Network***
  - In this network, every computer acts as peer/server to other nodes in the network.
  - **Types of P2P**
    - **Unstructured P2P:** Work load is shared equally, nodes are connected randomly, difficult to find data, easily built.
    - **Structured P2P:** Data is accessed easily, difficult to set up due to creation of virtual layer.
    - **Hybrid P2P:** Combination of P2P and client-server architecture. This network has a central server and each node can work independently as well.

### ***Proxies***
  - Proxy are servers which acts as bridge between the clients and servers. **Proxy chaining** involves forwarding traffic from one proxy to another.
  - There are two types of proxy servers.
    - **Forward proxy:** Proxy server is at client side. 
    - **Reverse proxy:** Proxy server is at server side.
  - **Purpose of Proxy Server:**
    - Gain admittance to blocked/unallowed assets
    - Improved security
    - Improved Data transfer speed
    - Privacy Benefits
<br>

- **NOTES:**
  - **Block Size is the unit of data exchange between cache and main memory.**
  - **Data and Instructions that are being used frequently are stored in Block.**