### ***Scalability***
- **Types of load**
  - **Web Server:** Requests per second
  - **Database:** Ratio of reads : writes
  - **Chat Room:** Number of active users

### ***Sharding***
Sharding is a type of database partitioning that separates very large database into smaller parts, more easily managed parts are called data shards.
   - **Types of sharding**
     - **Key-Based Sharding:** It is also known as alogrithmic sharding as it relies on hash function to identify the shard for the record. Hash funcion needs to be changed when data is increased and new shard has to be added.
     - **Range-Based Sharding:** It is useful when the data has to be sharded based on some deifinte range like month wise dates or quarted wise dates.
     - **Directory-Based Sharding:** It is also known as dynamic sharding. It is used when any one of the columns have fixed values like countries, states, zones etc. The column with fixed has separated shard for each data and value is mapped to a shard in a lookup table.