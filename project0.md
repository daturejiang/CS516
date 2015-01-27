#Project 0-Data management platform comparison
#### He Jiang(hj58)

Mongo DB
Reference: http://halls-of-valhalla.org/beta/articles/the-pros-and-cons-of-mongodb,45/  
Pros: Easy to transfer across Database by storing in JSON format, easy to usee
Cons: Because it is not relational database, it is hard to do join for different tables.

1010data
Reference: https://www.1010data.com/products https://www.trustradius.com/reviews/1010data-2014-12-12-00-27-32 
Pros: Cloud-based, good for data sharing, big amount of data management and analysis.
Cons: Too complex when the data is relatively small and simple.

Accumulo
Reference: https://accumulo.apache.org/notable_features.html http://en.wikipedia.org/wiki/Apache_Accumulo 
Similar with HBase
Pros: server-side programming mechanisms. Cell-level access labels. Sorted data. Based on BigTable technology from Google. Fault-tolerant operations. Timestamps never go backwards.
Cons: complexity of using. 

HBase:
Reference: http://sqrrl.com/product/nosql/ http://apache-accumulo.1065345.n5.nabble.com/How-does-Accumulo-compare-to-HBase-td10464.html http://hbase.apache.org/ http://www.cyanny.com/2014/03/13/hbase-architecture-analysis-part-3-pros-cons/ 
Pros: cell-level security and access labels. Similar with Accumulo, Based on BigTable technology from Google. Wide column store, scalability and flexibility. Prevent data lose. Good integration with other projects. Random, realtime read/write access. Failover between region servers. Good for sparse table. 
Cons: complexity, not good for large clusters. As master slave architecture design, it has single point of failure problem. Index only on key, sorted by key. No Joins.

Cassandra
Reference: http://sqrrl.com/product/nosql/ http://cassandra.apache.org/ http://en.wikipedia.org/wiki/Apache_Cassandra http://www.ibm.com/developerworks/library/os-apache-cassandra/ 
Pros: NoSQL, Wide column store, linear scalability and flexibility, fault-tolerance on hardware and cloud. Column indexes. As it is decentralized, No single point of failure. Focus on prevent losing data. Elastic. Handle large amounts of data across many commodity servers.
Cons: complexity, Not good for query, no ACID transactions and Joins. No foreign keys, immutable and unique keys. Failed operations might change the data.

Redis:
Reference: http://sqrrl.com/product/nosql/ http://redis.io/topics/introduction http://www.slideshare.net/TitPetric/redislessons-learned http://mvcbloggers.blogspot.com/2013/05/redis-vs-memcached.html 
Pros: Key-value cache and store, good for simple data. Scalability. Atomic operatios. In-memory dataset. Support master-slave asynchronous replication. Automatic failover. Easy to install, works in most POSIX without external dependencies. Keys could expires. LRU eviction of keys. Scaling reads and writes.
Cons: Querying is simple, lack advanced features, no key segmentation and grouping. Persistence and data integrity

Memcached
Reference: http://memcached.org/  http://www.slideshare.net/TitPetric/redislessons-learned http://mvcbloggers.blogspot.com/2013/05/redis-vs-memcached.html 
Pros: key-value store. Simplicity, stability, performance. Simple text protocol design, so it is easy to use. All the data stored in memory
Cons: cannot query on the value part. Does not support high availability features. Binary is complex to use, persistence, replication, key eviction based on slab allocation not LRU.

Couchbase
Reference: http://www.couchbase.com/nosql-databases/couchbase-server http://sqrrl.com/product/nosql/ http://www.datasciencecentral.com/forum/topics/hbase-cassandra-mongo-db-couchbase https://community.dynamics.com/crm/b/isvlabs/archive/2013/10/27/nosql-couchbase-review.aspx 
Pros: master-master replication, document store, key value store, scalable and low latency access. Integrated admin console with cluster wide monitoring. Interactive web and mobile application. Integration with map reduce products for streaming data to storm for real time analysis. Large numbers of concurrent users support. 
Cons: scalability, no transactions. Confusing re-reduce in map/reduce views. Limited query options. No modification during rebalance

CouchDB
Reference: http://couchdb.apache.org/  http://nosql.findthebest-sw.com/ http://kkovacs.eu/cassandra-vs-mongodb-vs-couchdb-vs-redis http://www.quora.com/What-are-the-pros-and-cons-of-CouchDB 
Pros: For interactive web and mobile application via HTTP and javascript. document store, high availability, partition tolerance, persistence. On-the-fly document transformation and real time change notifications. Distributed scaling. Good for accumulating and occasionally changing data. Bi-directional replication. Master-master replication.
Cons: expensive arbitrary queries. Extra space overhead. Poor error logging and reporting

Neo4j
Reference: http://neo4j.com/product/  http://sqrrl.com/product/nosql/ http://kkovacs.eu/cassandra-vs-mongodb-vs-couchdb-vs-redis 
Pros: graph store, complex data relationships and queries. Full ACID conformity. Indexing nodes and relationships. Good for more read less writes situation. Powerful query language. Easy to import from other database
Cons: flexibility. No sharding, hard to store data across servers. Need to carefully design the data storage

YarcData
Reference: http://sqrrl.com/product/nosql/ 
Pros: graph store, graph joins
Cons: flexibility

OrientDB
Reference: http://www.orientechnologies.com/orientdb/  http://kkovacs.eu/cassandra-vs-mongodb-vs-couchdb-vs-redis 
Pros: Full ACID conformity. Fast. Support schema-less, schema-full and schema-mixed modes. Could be both document and graph database. Multi-master architecture. Supports relationships between documents via pointers. SQL-like query language. Support sharding. Low total cost of ownership
Cons: no joins. When the data grows bigger, performance drops quickly

Infinite Graph
Reference: http://www.objectivity.com/infinitegraph#.VMVuZCvF9-s  http://sqrrl.com/product/nosql/ http://en.wikipedia.org/wiki/InfiniteGraph 
Pros: graph store, graph joins. Graph-Focused Java API Optimized for data relationships. Flexible graph visualization tools. Multi-threaded processing.  Powerful query methods, traverser and graph navigation API, predicate language qualification, path pattern matching.
Cons: flexibility, no sharding

Sqrrl Enterprise
Reference: http://sqrrl.com/product/sqrrl-enterprise/  http://sqrrl.com/product/nosql/ http://db-engines.com/en/system/Elasticsearch%3BSolr%3BSqrrl 
Pros: combined the different type of NoSQL database. Based on accumulo. Use JSON format. Streaming or bulk data ingest from any source. Encryption and labeling of data with fine-grained access controls. Automatically organize data and extract information about the entities and relationships you care about. Web-based dashboarding and visual, contextual navigation of the data and relationships in the system. Immediate consistency.
Cons: only support schema-free. No server-side scripting. 

Lucene/Solr
Reference: http://lucene.apache.org/solr/features.html  http://db-engines.com/en/system/Elasticsearch%3BSolr%3BSqrrl 
Pros: Enterprise search Engine. Full text search capabilities. Optimized for high volume traffic. Highly scalable and fault tolerant. Support sharding. Cloud/distributed master-slave replication. Dynamic fields enable on-the-fly addition of new fields. Customizable data types. Automatically and near real-time indexing. 
Cons: limited query time joins

Elasticsearch
Reference: http://www.elasticsearch.org/  http://db-engines.com/en/system/Elasticsearch%3BSolr%3BSqrrl 
Pros: enterprise real time search and analytics engine. High availability. Good for complex document store. Conflict management. Full text search. Reliability and scalability. Use json structures. Automatically and multi indexed. Support sharding and replication. Configurable consistency. Per-operation persistence
Cons: only schema-free. No server-side scripts. No transaction. No foreign keys. 

Riak
Reference: http://basho.com/riak/  http://sqrrl.com/product/nosql/  http://www.slideshare.net/cscyphers/big-data-platforms-an-overview 
Pros: Key value pair stores, simplicity, low-latency, fault-tolerance, availability. Near-linear performance increase as capacity added. Lighter on memory requirements. No single point of failure.
Cons: lack advanced querying. Not designed for small discrete and numerous data. Not good for export. Security. Conflict resolution can bubble up. Erlang is not widely used.

Voldemort
Reference: http://www.project-voldemort.com/voldemort/  http://www.slideshare.net/cscyphers/big-data-platforms-an-overview 
Pros: key value pair store, in-memory database. Fast reads, low latency. Highly customizable. Automatically replicated over multiple servers. Sharding. Tunable consistency. No single point failure. Support for pluggable data placement strategies. 
Cons: no complex query filter. No foreign key constraints. No support. Use lots of space as versioning. No range queries.

FatDB
Reference: http://www.componentsource.com/products/fatcloud-fatdb/index.html  http://nosql.findthebest-sw.com/ http://www.infoq.com/articles/fatdb 
Pros: key value document store, rapid development process. Consistency. Partition tolerance. All the application is plumbing.  Unified API. Tightly integrated with sql server. Scalability. Indexing for range queries. Efficient memory-based cache with expiry window. 

Hypertable
Reference: http://hypertable.org/  http://kkovacs.eu/cassandra-vs-mongodb-vs-couchdb-vs-redis http://www.databaseskill.com/1950359/ 
Pros: based on BigTable design. Run on hadoop’s HDFS. Low latency. Immediate consistency, not eventually. SQL like language, easier to use. Query by key, by cell. Search could be limited to key/column ranges. Versioning. Tables are in namespaces. Scalability. Cost savings in performance and efficiency. Don’t sharding to avoid imbalance. concurrency
Cons: No associated query. Single query response may not as good as traditional database. because it runs on Hadoop, server might fail. 

Scalaris
Reference: https://code.google.com/p/scalaris/  http://kkovacs.eu/cassandra-vs-mongodb-vs-couchdb-vs-redis 
Pros: scalable, transactional, distributed key-value store. Support ACID. The first nosql database. In-memory. Consistent, distributed write operations. 
Cons: availability

VoltDB
Reference: http://voltdb.com/  http://kkovacs.eu/cassandra-vs-mongodb-vs-couchdb-vs-redis http://highscalability.com/blog/2010/6/28/voltdb-decapitates-six-sql-urban-myths-and-delivers-internet.html 
Pros: fast, in-memory operational database. Real time analysis. Full streaming capability. Transactional consistency as RDBMS. Automation decisions in real time when collecting data. Scalability. Can export data into Hadoop. Cross-datacenter replication.
Cons: complex to use. To reach scalability, the design must follow VoltDB rules. Centralized. Not good failure handle.

Aerospike
Reference: http://www.aerospike.com/ http://kkovacs.eu/cassandra-vs-mongodb-vs-couchdb-vs-redis 
Pros: key-value store. In-memory. Flash-optimized fast access. Scalability. Reliability. Cross-datacenter replication. Support complex data types. Aggregation query model. Data could expire. Automatic failover and rebalancing. Immediate consistency for writes.
Cons: may lead to imbalance nodes. 

AWS SimpleDB
Reference: http://aws.amazon.com/simpledb/  http://nosql.findthebest-sw.com/ http://blog.cyril.me/en/2011/12/amazon-aws-simpledb-pros-cons/ 
Pros: document store. simple database solutions. Low touch. Highly available. Flexible. Simple to use. Intergrated with amazon web services. Security.
Cons: no advanced features. No complex data type support. No aggregation. Slow replication across servers.

ArangoDB
Reference: https://www.arangodb.com/  http://nosql.findthebest-sw.com/ 
Pros: consistency. Multi-model store. Suitable for multiple cases. Support joins. Transactional. Easy to learn query language. Sharding. Json format data structure.
Cons: asynchronized replication

MySQL
Reference: http://www.smartfile.com/blog/the-pros-and-cons-of-mysql/ http://www.myhostsupport.com/index.php?/News/NewsItem/View/58 
Pros: Easy to use. Support. Industry standard
Cons: stability. Scalability. Not community drive, functionality depends on addons

Exadata
Reference: https://www.oracle.com/engineered-systems/exadata/index.html http://h30499.www3.hp.com/t5/System-Administration/Should-we-consider-EXADATA/td-p/5560497#.VMb3YivF9-s 
Pros: Performance. Flash storage. Support Oracle VM for virtualization. Elastic configurations. Support all the time
Cons: need to use with Oracle machine. Vendor lock-in, hard to move to other platform. Hard to integrate other environment. Hard to monitor and backup. 

IBM PureData
Reference: http://www-01.ibm.com/software/data/puredata/ 
Pros: simplified. Built-in expertise. Integration by design. Big data and business ready. Security. Good for analytics.

SAP HANA
Reference: http://hana.sap.com/abouthana.html  http://en.wikipedia.org/wiki/SAP_HANA http://www.asugnews.com/article/gartner-the-pros-and-cons-of-saps-core-strategies 
Pros: in-memory, column-oriented RDBMS. High transaction rates. Support complex query processing. Real time transactional analytics. Reduction in bottlenecks. Data loss prevent
Cons: no HTML5 support in mobile platform. Not support open standard cloud management

SQL Server:
Reference: http://www.microsoft.com/en-us/server-cloud/products/sql-server/ 

Pros: mission critical performance. Platform on hybrid cloud. Availability and disaster recovery. Scalability. Easy to use. Graphical query analyzer.
Cons: need to learn different language. Require advanced hardware to reach the performance. Price.

Tajo
Reference: http://tajo.apache.org/ 
Pros: Fast and efficient. Scalability. Compatible with other environment. User-defined functions. Backup/restore utility. Good for big chuck of data. Incorporate map reduce. 
Cons: no aggregation. No nested data model.

Google app engine
Reference: https://cloud.google.com/appengine/docs  https://groups.google.com/forum/#!topic/google-appengine/EjQleHJzrzI http://stackoverflow.com/questions/1306279/pros-cons-of-google-app-engine 
Pros: don’t need own servers. Specified for app development. Scalability. Multi-site replication. Both RDBMS and NoSQL available. Managed VMs. Support map reduce.
Cons: vendor lock-in. limited language support. Read-only access to the file system. 

MetaScale
Reference: http://www.metascale.com/ 
Pros: Hadoop architecture. Scalability. Big data appliance. Performance. Quick response. Tool based conversion. 


