## LIST OF NOSQL DATABASE MANAGEMENT SYSTEMS [currently >225]
- Wide Column Store / Column Families
```markdown
  Hadoop / HBase
  Cassandra
  Apache Flink
```  
- Document Store
```markdown
  MongoDB
  CouchDB
```
- Key Value / Tuple Store
- Graph Database Management Systems
- Multimodel Database Management Systems
- Object Database Management Systems »
- Grid & Cloud Database Management Solutions
- XML Database Management Systems
- Multidimensional Database Management Systems
- Multivalue Database Management Systems
- Event Sourcing
- Time Series / Streaming Database Management Systems
- Other NoSQL related database management systems
- Scientific and Specialized Database Management Systems
- unresolved and uncategorized

```markdown

- Wide Column Store / Column Families
Hadoop / HBase

API: Java / any writer, Protocol: any write call, Query Method: MapReduce Java / any exec, Replication: HDFS Replication, Written in: Java, Concurrency: ?, Misc: Links: 3 Books [1, 2, 3], Guru99 Article >>
MapR, Hortonworks, Cloudera

Hadoop Distributions and professional services.
Cassandra

massively scalable, partitioned row store, masterless architecture, linear scale performance, no single points of failure, read/write support across multiple data centers & cloud availability zones. API / Query Method: CQL and Thrift, replication: peer-to-peer, written in: Java, Concurrency: tunable consistency, Misc: built-in data compression, MapReduce support, primary/secondary indexes, security features. Links: Documentation, PlanetC*, Company.
Scylla

Cassandra-compatible column store, with consistent low latency and more transactions per second. Designed with a thread-per-core model to maximize performance on modern multicore hardware. Predictable scaling. No garbage collection pauses, and faster compaction.
Hypertable

API: Thrift (Java, PHP, Perl, Python, Ruby, etc.), Protocol: Thrift, Query Method: HQL, native Thrift API, Replication: HDFS Replication, Concurrency: MVCC, Consistency Model: Fully consistent Misc: High performance C++ implementation of Google's Bigtable. » Commercial support
Accumulo

Accumulo is based on BigTable and is built on top of Hadoop, Zookeeper, and Thrift. It features improvements on the BigTable design in the form of cell-based access control, improved compression, and a server-side programming mechanism that can modify key/value pairs at various points in the data management process.
Amazon SimpleDB

Misc: not open source / part of AWS, Book (will be outperformed by DynamoDB!)
Cloudata

Google's Big table clone like HBase. » Article
MonetDB

Column Store pioneer since 2002.
HPCC

from LexisNexis, info, article
Apache Flink

(formerly known as Stratosphere) massively parallel & flexible data analytics platform, API: Java, Scala, Query Method: expressive data flows (extended M/R, rich UDFs, iteration support), Data Store: independent (e.g., HDFS, S3, MongoDB), Written in: Java, License: Apache License V2.0, Misc: good integration with Hadoop stack (HDFS, YARN), source code on Github
IBM Informix

horizontally and vertically scalable, relational, partitioned row store, document store API / Query Method: SQL (native, DRDA, JDBC, ODBC), MongoDB wire listener, mixed mode, replication: master / slave, peer-to-peer, sharding, grid operations, written in: C, Concurrency: row, page, table, db locking, Misc: ACID, built-in data compression, scheduler, automatic cyclic storage management, extensible, in memory acceleration, native ports from ARM v6 up Links: Documentation, IIUG, Company.
Splice Machine

Splice Machine is an RDBMS built on Hadoop, HBase and Derby. Scale real-time applications using commodity hardware without application rewrites, Features: ACID transactions, ANSI SQL support, ODBC/JDBC, distributed computing
eXtremeDB Financial Edition

massively scalable in-memory and persistent storage DBMS for analytics on market data (and other time series data). APIs: C/C++, Java Native Interface (JNI), C#/.NET), Python, SQL (native, ODBC, JDBC), Data layout: row, columnar, hybrid, Written in: C, Replication: master/slave, cluster, sharding, Concurrency: Optimistic (MVCC) and pessimistic (locking)
ConcourseDB

a distributed self-tuning DBMS with automatic indexing, version control and ACID transactions. Written In: Java. API/Protocol: Thrift (many languages). Concurrency: serializable transactions with just-in-time locking. Misc: uses a buffered storage system to commit all data to disk immediately while perform rich indexing in the background.
Druid

open-source analytics data store for business intelligence (OLAP) queries on event data. Low latency (real-time) data ingestion, flexible data exploration, fast data aggregation. Scaled to trillions of events & petabytes. Most commonly used to power user-facing analytic applications. API: JSON over HTTP, APIs: Python, R, Javascript, Node, Clojure, Ruby, Typescript + support SQL queries Written in: Java License: Apache 2.0 Replication: Master/Slave
KUDU

Apache Kudu (incubating) completes Hadoop's storage layer to enable fast analytics on fast data.
Elassandra

Elassandra is a fork of Elasticsearch modified to run on top of Apache Cassandra in a scalable and resilient peer-to-peer architecture. Elasticsearch code is embedded in Cassandra nodes providing advanced search features on Cassandra tables and Cassandra serve as an Elasticsearch data and configuration store.
[OpenNeptune, Qbase, KDI]
Document Store
No SQL Encryption (Oracle)

Oracle NoSQL Database can be configured securely with the proper technical guides.  Network communications between NoSQL clients, utilities, and NoSQL server components can and should be encrypted. This original document is curated and maintained by Ludovic Rembert. He has additional guides on his website about the best VPNs.
Elastic

 API: REST and many languages, Protocol: REST, Query Method: via JSON, Replication + Sharding: automatic and configurable, written in: Java, Misc: schema mapping, multi tenancy with arbitrary indexes, » Company and Support, » Article
ArangoDB, FaunaDB, OrientDB, gunDB

(Doc Store & GraphDB & Key-Value. More details in Category Multimodel DBMS)
MongoDB

API: BSON, Protocol: C, Query Method: dynamic object-based language & MapReduce, Replication: Master Slave & Auto-Sharding, Written in: C++,Concurrency: Update in Place. Misc: Indexing, GridFS, Freeware + Commercial License Links: » Talk, » Notes, » Company
Cloud Datastore

 A fully managed Document store with multi-master replication across data centers. Originally part of Google App Engine, it also has REST and gRPC APIs. Now Firestore?!
Azure DocumentDB

is a fully managed, globally distributed NoSQL DBMS perfect for the massive scale and low latency needs of modern applications. Guarantees: 99.99% availability, 99% of reads at <10ms and 99% of writes at <15ms. Scale to handle 10s-100s of millions of requests/sec and replicate globally with the click of a button. APIs: .NET, .NET Core, Java, Node.js, Python, REST. Query: SQL. Links: » Service, » Pricing, » Playground, » Documentation
RethinkDB

API: protobuf-based, Query Method: unified chainable query language (incl. JOINs, sub-queries, MapReduce, GroupedMapReduce); Replication: Sync and Async Master Slave with per-table acknowledgements, Sharding: guided range-based, Written in: C++, Concurrency: MVCC. Misc: log-structured storage engine with concurrent incremental garbage compactor
Couchbase Server

API: Memcached API+protocol (binary and ASCII) , most languages, Protocol: Memcached REST interface for cluster conf + management, Written in: C/C++ + Erlang (clustering), Replication: Peer to Peer, fully consistent, Misc: Transparent topology changes during operation, provides memcached-compatible caching buckets, commercially supported version available, Links: » Wiki, » Article
CouchDB

API: JSON, Protocol: REST, Query Method: MapReduceR of JavaScript Funcs, Replication: Master Master, Written in: Erlang, Concurrency: MVCC, Misc:
Links: » 3 CouchDB books 

, » Couch Lounge (partitioning / clustering), » Dr. Dobbs
ToroDB

API: MongoDB API and SQL, Protocol: MongoDB Wire Protocol / MongoDB compatible, Query Method: dynamic object-based language & SQL, Replication: RDBMS Backends' Replication System & Support for replication from MongoDB's Replica Set, Written in: Java, Concurrency: MVCC. Misc: Open Source NoSQL and SQL DBMS. The agileness of a doc DB with the reliability and the native SQL capabilities of PostgreSQL. Links: » Company
SequoiaDB

API: BSON, Protocol: C, Query Method: dynamic object-based language, Replication: Master Slave & Auto-Sharding, Written in: C++, Misc: Indexing, Large Object Store, Transaction, Free + Commercial License, Benchmark, Code
NosDB

 a 100% native .NET Open Source NoSQL Document DBMS (Apache 2.0 License). It also supports SQL querying over JSON Documents. Data can also be accessed through LINQ & ADO.NET. NosDB also provides strong server-side and client-side caching features by integrating NCache.
RavenDB

RavenDB is an Open Source NoSQL DBMS. Multi-Model: Document, Key-Value, Graph, Distributed Counters, Attachments. Fully Transactional (ACID) across database and throughout the cluster. Multiplatform: C#, Node.js, Java, Python, Ruby, Go. Multisystem: Windows, Linux, Mac OS, Docker, Raspberry Pi. Native GUI, MapReduce, full text search, memory management.
UnQlite

UnQLite is an embedded NoSQL (Key/Value store and Document-store) DBMS. Similar to MongoDB, Redis, CouchDB etc. as well a standard Key/Value store similar to BerkeleyDB, LevelDB, etc. It's a in-process software library which implements a self-contained, serverless, zero-configuration, transactional NoSQL DBMS. Open source, distributed under the 2-Clause BSD license.
MarkLogic Server

(developer+commercial) API: JSON, XML, Java Protocols: HTTP, REST Query Method: Full Text Search and Structured Query, XPath, XQuery, Range, Geospatial, Bitemporal Written in: C++ Concurrency: Shared-nothing cluster, MVCC Misc: Petabyte-scalable and elastic (on premise in the cloud), ACID + XA transactions, auto-sharding, failover, master slave replication (clusters), replication (within cluster), high availability, disaster recovery, full and incremental backups, government grade security at the doc level, developer community »
Clusterpoint Server

(freeware+commercial) API: XML, PHP, Java, .NET Protocols: HTTP, REST, native TCP/IP Query Method: full text search, XML, range and Xpath queries; Written in C++ Concurrency: ACID-compliant, transactional, multi-master cluster Misc: Petabyte-scalable document store and full text search engine. Information ranking. Replication. Cloudable.
JSON ODM

Object Document Mapper for JSON-Documents written in pure JavaScript. It queries the collections with a gremlin-like DSL that uses MongoDB's API methods, but also provides joining. The collections extend the native array objects, which gives the overall ODM a good performance. Queries 500.000 elements in less then a second.
NeDB

NoSQL DBMS for Node.js in pure javascript. It implements the most commonly used subset of MongoDB's API and is quite fast (about 25,000 reads/s on a 10,000 documents collection with indexing).
Terrastore

API: Java & http, Protocol: http, Language: Java, Querying: Range queries, Predicates, Replication: Partitioned with consistent hashing, Consistency: Per-record strict consistency, Misc: Based on Terracotta
AmisaDB:

Architected to unify the best of search engine, NoSQL and NewSQL DB technologies. API: REST and many languages. Query method: SQL. Written in C++. Concurrency: MVCC. Misc: ACID transactions, data distribution via consistent hashing, static and dynamic schema support, in-memory processing. Freeware + Commercial License
JasDB

Lightweight open source document DBMS written in Java for high performance, runs in-memory, supports Android. API: JSON, Java Query Method: REST OData Style Query language, Java fluent Query API Concurrency: Atomic document writes Indexes: eventually consistent indexes
RaptorDB

JSON based, Document store DBMS with compiled .net map functions and automatic hybrid bitmap indexing and LINQ query filters
djondb

jonDB API: BSON, Protocol: C++, Query Method: dynamic queries and map/reduce, Drivers: Java, C++, PHP Misc: ACID compliant, Full shell console over google v8 engine, djondb requirements are submitted by users, not market. License: GPL and commercial
EJDB

Embeddable JSON DBMS engine. API: C/C++, Protocol: Native, HTTP, Websockets Written in: C11, Query language: XPath like query language (JQL), Concurrency: RW locking, Misc: Single file database, Indexing, License: MIT
densodb

DensoDB is a new NoSQL document DBMS. Written for .Net environment in c# language. It’s simple, fast and reliable. Source
SisoDB

 A Document Store on top of SQL-Server.
SDB

 For small online databases, PHP / JSON interface, implemented in PHP.
NoSQL embedded db

 Node.js asynchronous NoSQL embedded DBMS for small websites or projects. DBMS supports: insert, update, remove, drop and supports views (create, drop, read). Written in JavaScript, no dependencies, implements small concurrency model.
[CloudKit, Perservere,Jackrabbit]
ThruDB

(please help provide more facts!) Uses Apache Thrift to integrate multiple backend DBMS as BerkeleyDB, Disk, MySQL, S3.
iBoxDB

Transactional embedded DBMS, it can embed into mobile, desktop and web applications, supports on-disk and in-memory storages. API: Java,C# (Android, Mono, Xamarin, Unity3D). Query Method: SQL-like and KeyValue. Written In: Java, C#. Replication: MasterSlave, MasterMaster.
BergDB

API: Java/.NET. Written in: Java. Replication: Master/Slave. License: AGLP. Historical queries. ACID. Schemaless. Concurrency: STM and persistent data structure. Append-only storage. Encrypted storage. Flexible durability control. Secondary & composite indexes. Transparently serializes Java/.NET objects.
ReasonDB

100% JavaScript automatically synchronizing multi-model DBMS with a SQL like syntax (JOQULAR) and swappable persistence stores. It supports joins, nested matches, projections or live object result sets, asynchronous cursors, streaming analytics, 18 built-in predicates, in-line predicates, predicate extensibility, indexable computed values, fully indexed Dates and Arrays, built in statistical sampling. Persistence engines include files, Redis, LocalStorage, block storage, and more.
IBM Cloudant

Cloud based, open-source, zero-config. Based on CouchDB and BigCouch.
BagriDB

API: XQJ/XDM, REST, OpenAPI, Protocols: Java, HTTP, Query Method: distributed XQuery + server-side XQuery/Java extensions, Written in: Java, Concurrency: MVCC, Document format: XML, JSON, POJO, Avro, Protobuf, etc. Misc: in-memory Data and Computation Grid, transparent replication and fail-over, true horizontal scalability, ACID transactions, rich indexeng and trigger capabilities, pluggable persistent store, pluggable data formats. GitHub
Key Value / Tuple Store
DynamoDB

Automatic ultra scalable NoSQL DB based on fast SSDs. Multiple Availability Zones. Elastic MapReduce Integration. Backup to S3 and much more...
Azure Table Storage

Collections of free form entities (row key, partition key, timestamp). Blob and Queue Storage available, 3 times redundant. Accessible via REST or ATOM.
Riak

API: tons of languages, JSON, Protocol: REST, Query Method: MapReduce term matching , Scaling: Multiple Masters; Written in: Erlang, Concurrency: eventually consistent (stronger then MVCC via Vector Clocks)
Redis

API: Tons of languages, Written in: C, Concurrency: in memory and saves asynchronous disk after a defined time. Append only mode available. Different kinds of fsync policies. Replication: Master / Slave, Misc: also lists, sets, sorted sets, hashes, queues. Cheat-Sheet: », great slides » Admin UI » From the Ground up »
Aerospike

Fast and web-scale DBMS. RAM or SSD. Predictable performance; achieves 2.5 M TPS (reads and writes), 99% under 1 ms. Tunable consistency. Replicated, zero configuration, zero downtime, auto-clustering, rolling upgrades, Cross Datacenter Replication (XDR). Written in: C. APIs: C, C#, Erlang, Go, Java, Libevent, Node, Perl, PHP, Python, Ruby. Links: Community, Development, Slides, 2.5M TPS on 1 node at Intel, 1M TPS on AmazonWS, 1M TPS w/ SSDs on 1 Server, Combating Memory Fragmentation
LevelDB

Fast & Batch updates. DB from Google. Written in C++. Blog », hot Benchmark », Article » (in German). Java access. C# (for Universal Windows Platform) access.
RocksDB

API: C++. Written in C++. Facebook`s improvements to Google`s LevelDB to speed throughput for datasets larger than RAM. Embedded solution.
Berkeley DB

API: Many languages, Written in: C, Replication: Master / Slave, Concurrency: MVCC, License: Sleepycat, Berkeley DB Java Edition: API: Java, Written in: Java, Replication: Master / Slave, Concurrency: serializable transaction isolation, License: Sleepycat
Helium

API: C, C++, Java, Python, NodeJS. Written in C. Key-value store aimed at high throughput and low latency (usecs) applications. Designed to run on many-core systems with fast storage such as SSDs and NVMs. Low and predictable memory footprint, low write amplification. License: proprietary Mode: embedded, single serverLinks Multi million ops/sec on GCP, Real-time low latency KV with Helium and Samsung Z-SSD
KeyDB

API: Multiple languages (Redis Compatible) Replication: Master / Master - A multithreaded fork of Redis with a ton of extra features such as Active Replication, AWS S3 integration, and significantly lower latency.
GenieDB

Immediate consistency sharded KV store with an eventually consistent AP store bringing eventual consistency issues down to the theoretical minimum. It features efficient record coalescing. GenieDB speaks SQL and co-exists / do intertable joins with SQL RDBMs.
BangDB

API: Get,Put,Delete, Protocol: Native, HTTP, Flavor: Embedded, Network, Elastic Cache, Replication: P2P based Network Overlay, Written in: C++, Concurrency: ?, Misc: robust, crash proof, Elastic, throw machines to scale linearly, Btree/Ehash
Chordless

API: Java & simple RPC to vals, Protocol: internal, Query Method: M/R inside value objects, Scaling: every node is master for its slice of namespace, Written in: Java, Concurrency: serializable transaction isolation,
Scalaris

(please help provide more facts!) Written in: Erlang, Replication: Strong consistency over replicas, Concurrency: non blocking Paxos.
Tokyo Cabinet / Tyrant

Links: nice talk », slides », Misc: Kyoto Cabinet »
Scalien

API / Protocol: http (text, html, JSON), C, C++, Python, Java, Ruby, PHP,Perl. Concurrency: Paxos.
Voldemort

Open-Source implementation of Amazons Dynamo Key-Value Store.
Dynomite

Open-Source implementation of Amazons Dynamo Key-Value Store. written in Erlang. With "data partitioning, versioning, and read repair, and user-provided storage engines provide persistence and query processing".
KAI

Open Source Amazon Dynamo implementation, Misc: slides
MemcacheDB

API: Memcache protocol (get, set, add, replace, etc.), Written in: C, Data Model: Blob, Misc: Is Memcached writing to BerkleyDB.
Faircom C-Tree

 API: C, C++, C#, Java, PHP, Perl, Written in: C,C++. Misc: Transaction logging. Client/server. Embedded. SQL wrapper (not core). Been around since 1979.
LSM

Key-Value DBMS that was written as part of SQLite4, They claim it is faster then LevelDB. Instead of supporting custom comparators, they have a recommended data encoding for keys that allows various data types to be sorted.
KitaroDB

 : A fast, efficient on-disk data store for Windows Phone 8, Windows RT, Win32 (x86 & x64) and .NET. Provides for key-value and multiple segmented key access. APIs for C#, VB, C++, C and HTML5/JavaScript. Written in pure C for high performance and low footprint. Supports async and synchronous operations with 2GB max record size.
upscaledb

 : (embedded solution) API: C, C++, .NET, Java, Erlang. Written in C,C++. Fast key/value store with a parameterized B+-tree. Keys are "typed" (i.e. 32bit integers, floats, variable length or fixed length binary data). Has built-in analytical functions like SUM, AVERAGE etc.
STSdb

API: C#, Written in C#, embedded solution, generic XTable<TKey,TRecord> implementation, ACID transactions, snapshots, table versions, shared records, vertical data compression, custom compression, composite & custom primary keys, available backend file system layer, works over multiple volumes, petabyte scalability, LINQ.
Tarantool/Box

 API: C, Perl, PHP, Python, Java and Ruby. Written in: Objective C ,Protocol: asynchronous binary, memcached, text (Lua console). Data model: collections of dimensionless tuples, indexed using primary + secondary keys. Concurrency: lock-free in memory, consistent with disk (write ahead log). Replication: master/slave, configurable. Other: call Lua stored procedures.
Chronicle Map

 In-memory (opt. persistence via mmap), highly concurrent, low-latency key-value store. API: Java. Written in: Java. Protocol: in-process Java, remote via Chronicle Engine + Wire: binary, text, Java, C# bindnings. Concurrency: in-memory lock striping, read-write locks. Replication: multi-master, eventually consistent.
Maxtable

 API: C, Query Method: MQL, native API, Replication: DFS Replication, Consistency: strict consistency Written in: C.
Pincaster

For geolocalized apps. Concurrency: in-memory with asynchronous disk writes. API: HTTP/JSON. Written in: C. License: BSD.
RaptorDB

A pure key value store with optimized b+tree and murmur hashing. (In the near future it will be a JSON document DBMS much like mongodb and couchdb.)
TIBCO Active Spaces

peer-to-peer distributed in-memory (with persistence) datagrid that implements and expands on the concept of the Tuple Space. Has SQL Queries and ACID (=> NewSQL).
allegro-C

Key-Value concept. Variable number of keys per record. Multiple key values, Hierarchic records. Relationships. Diff. record types in same DB. Indexing: B*-Tree. All aspects configurable. Full scripting language. Multi-user ACID. Web interfaces (PHP, Perl, ActionScript) plus Windows client.
nessDB

 A fast key-value DBMS (using LSM-Tree storage engine), API: Redis protocol (SET,MSET,GET,MGET,DEL etc.), Written in: ANSI C
HyperDex

Distributed searchable key-value store. Fast (latency & throughput), scalable, consistent, fault tolerance, using hyperspace hashing. APIs for C, C++ and Python.
SharedHashFile

 Fast, open source, shared memory (using memory mapped files e.g. in /dev/shm or on SSD), multi process, hash table, e.g. on an 8 core i7-3720QM CPU @ 2.60GHz using /dev/shm, 8 processes combined have a 12.2 million / 2.5 to 5.9 million TPS read/write using small binary keys to a hash file containing 50 million keys. Uses sharding internally to mitigate lock contention. Written in C.
Symas LMDB

 Ultra-fast, ultra-compact key-value embedded data store developed by Symas for the OpenLDAP Project. It uses memory-mapped files, so it has the read performance of a pure in-memory DBMS while still offering the persistence of standard disk-based DBMS, and is only limited to the size of the virtual address space, (it is not limited to the size of physical RAM)
Sophia

 Sophia is a modern embeddable key-value DBMS designed for a high load environment. It has unique architecture that was created as a result of research and rethinking of primary algorithmic constraints, associated with a getting popular Log-file based data structures, such as LSM-tree. Implemented as a small C-written, BSD-licensed library.
NCache

 .NET Open Source Distributed Cache. Written in C#. API .NET & Java. Query Parallel SQL Query, LINQ & Tags. Misc: Linear Scalability, High Availability, WAN Replication, GUI based Administration & Monitoring Tools, Messaging, Runtime Data Sharing, Cache & Item Level Events, Continuous Query & Custom Events, DB Dependencies & Expirations
TayzGrid

 Open Source In-Memory JCache compliant Data Grid. Written in Java. API Java, JCache JSR 107 & .NET. Query SQL & DB Synchronization. Misc: Linear Scalability, High Availability, WAN Replication, GUI based Administration & Monitoring Tools, Distributed Messaging, MapReduce, Entry Processor and Aggregator
PickleDB

 Redis inspired K/V store for Python object serialization.
Mnesia

 (ErlangDB »)
LightCloud

 (based on Tokyo Tyrant)
Hibari

 Hibari is a highly available, strongly consistent, durable, distributed key-value data store
OpenLDAP

 Key-value store, B+tree. Lightning fast reads+fast bulk loads. Memory-mapped files for persistent storage with all the speed of an in-memory DBMS. No tuning conf required. Full ACID support. MVCC, readers run lockless. Tiny code, written in C, compiles to under 32KB of x86-64 object code. Modeled after the BerkeleyDB API for easy migration from Berkeley-based code. Benchmarks against LevelDB, Kyoto Cabinet, SQLite3, and BerkeleyDB are available, plus full paper and presentation slides.
Genomu

 High availability, concurrency-oriented event-based K/V DBMS with transactions and causal consistency. Protocol: MsgPack, API: Erlang, Elixir, Node.js. Written in: Elixir, Github-Repo.
BinaryRage

 BinaryRage is designed to be a lightweight ultra fast key/value store for .NET with no dependencies. Tested with more than 200,000 complex objects written to disk per second on a crappy laptop 🙂 No configuration, no strange driver/connector, no server, no setup - simply reference the dll and start using it in less than a minute.
Elliptics

 Github Page »
DBreeze

 Professional, open-source, NoSql (embedded Key/Value storage), transactional, ACID-compliant, multi-threaded, object DBMS management system for .NET 3.0> MONO. Written in C#.
TreodeDB

 API: Scala. Written in Scala. Replication: Replicas vote on writes and reads. Sharding: Hashes keys onto array of replica cohorts. Concurrency: Optimistic + Multiversion Concurrency Control. Provides multirow atomic writes. Exposes optimistic concurrency through API to support HTTP Etags. Embedded solution.
BoltDB

 Key/Value DB written in Go.
Serenity

 Serenity DBMS implements basic Redis commands and extends them with support of Consistent Cursors, ACID transactions, Stored procedures, etc. The DBMS is designed to store data bigger then available RAM.
Cachelot

 API: Memcached. Written in C++. In-memory LRU cache with very small memory footprint. Works within fixed amount of memory. Cachelot has a C++ cache library and stand-alone server on top of it.
filejson

 Use a JSON encoded file to automatically save a JavaScript value to disk whenever that value changes. A value can be a Javascript: string, number, boolean, null, object, or an array. The value can be structured in an array or an object to allow for more complex data stores. These structures can also be nested. As a result, you can use this module as a simple document store for storing semistructured data.
InfinityDB

 InfinityDB is an all-Java embedded DBMS with access like java.util.concurrent.ConcurrentNavigableMap over a tuple space, enhanced for nested Maps, LOBs, huge sparse arrays, wide tables with no size constraints. Transactions, compression, multi-core concurrency, easy schema evolution. Avoid the text/binary trap: strongly-typed, fine-grained access to big structures. 1M ops/sec. Commercial, closed source, patented.
KeyVast

 Key Value Store with scripting language. Data types include list, dictionary and set. Hierarchical keys. API: TCP/IP, Protocol: Query language, Written in: Delphi, License: MIT, Links: Github
SCR Siemens Common Repository

 In-Memory, scale-by-cell division (under load), multi-tiered scalability (transactions, entries, indicies), read=write, geo-redundancy, redundancy per datatype, LDAP, API, bulkload facility for VNF state resiliency, VNF-M integratable, self-[re-]balancing, Backend for Mobile Network Functions
IOWOW

 The C/C++ persistent key/value storage engine based on skip list data structure. API: C/C++. Protocol: Native. Written in: C11, Concurrency: RW locking. License: MIT
BBoxDB

 A distributed data store for multi-dimensional data. BBoxDB enhances the key-value data model by a bounding box, which describes the location of a value in an n-dimensional space. Data can be efficiently retrieved using hyper-rectangle queries. Spatial joins and dynamic data redistribution are also supported. API: Java, Protocol: asynchronous binary, Data model: Key-bounding-box-value, Scaling: Auto-Sharding, Replication, Written in: Java, Concurrency: eventually consistent / RW locking
NuSTER

 A HTTP based, user facing, RESTful NoSQL cache server based on HAProxy. It can be used as an internal NoSQL cache sits between your application and DBMS like Memcached or Redis as well as a user facing NoSQL cache that sits between end user and your application. It supports headers, cookies, so you can store per-user data to same endpoint. Protocol: HTTP. Written in: C.
JDX

 A lightweight in-memory document-oriented DBMS written with JavaScript. Includes Single Page Application API, node serialization, tree browsing and CRUD operations on document tuples through web GUI. Integrate with server-side noSQL DBMS instance into a transaction-synchronous cluster, create SPA content or browse and serialize document tuples with HTML interface.
Antidote

 Geo-replicated; multi-master; both reads & writes have local latency; sharded. Available under Partition (AP) with a high consistency (CP); MVCC; transactions; causal consistency (no ordering anomalies). API: CRDTs (= concurrent update, convergence). Protocol buffers, Erlang, JavaScript, Java, Go, REST. Ongoing work: same guarantees at edge; SQL-like language; static analysis; strong consistency on demand. Open source; written in Erlang. Publication: Cure
[Scality », KaTree » TomP2P », Kumofs » , TreapDB », Wallet » , NoSQLz », NMDB, luxio, actord, keyspace, flare, schema-free, RAMCloud]
[SubRecord, Mo8onDb, Dovetaildb]
Graph Database Management Systems
Neo4J

 API: lots of langs, Protocol: Java embedded / REST, Query Method: Cypher, nativeJavaAPI, JRuby, Replication: typical MySQL style master/slave, Written in: Java, Concurrency: non-block reads, writes locks involved nodes/relationships until commit, Misc: ACID possible, Links: Video », Blog »
ArangoDB, FaunaDB, OrientDB, gunDB

 (Doc Store & GraphDB & Key-Value. More details in Category Multimodel Database Management Systems)
Infinite Graph

 (by Objectivity) API: Java, Protocol: Direct Language Binding, Query Method: Graph Navigation API, Predicate Language Qualification, Written in: Java (Core C++), Data Model: Labeled Directed Multi Graph, Concurrency: Update locking on subgraphs, concurrent non-blocking ingest, Misc: Free for Qualified Startups.
Sparksee

(former DEX): API: Java, .NET, C++, Python, Objective-C, Blueprints Interface Protocol: Embedded, Query Method: as above + Gremlin (via Blueprints), Written in: C++, Data Model: Labeled Directed Attributed Multigraph, Concurrency: yes, Misc: ACID possible, Free community edition up to 1 Mio objects, Links: Intro », Technical Overview »
TITAN

 : API: Java, Blueprints, Gremlin, Python, Clojure Protocol: Thrift, RexPro(Binary), Rexster (HTTP/REST) Query Method: Gremlin, SPARQL Written In: Java Data Model: labeled Property Graph, directed, multi-graph adjacency list Concurrency: ACID Tunable C Replication: Multi-Master License: Apache 2 Pluggable backends: Cassandra, HBase, MapR M7 Tables, BDB, Persistit, Hazelcast Links: Titan User Group
InfoGrid

API: Java, http/REST, Protocol: as API + XPRISO, OpenID, RSS, Atom, JSON, Java embedded, Query Method: Web user interface with html, RSS, Atom, JSON output, Java native, Replication: peer-to-peer, Written in: Java, Concurrency: concurrent reads, write lock within one MeshBase, Misc: Presentation »
HyperGraphDB

 API: Java (and Java Langs), Written in:Java, Query Method: Java or P2P, Replication: P2P, Concurrency: STM, Misc: Open-Source, Especially for AI and Semantic Web.
GraphBase

Sub-graph-based API, query language, tools & transactions. Embedded Java, remote-proxy Java or REST. Distributed storage & processing. Read/write all Nodes. Permissions & Constraints frameworks. Object storage, vertex-embedded agents. Supports multiple graph models. Written in Java
Trinity

 API: C#, Protocol: C# Language Binding, Query Method: Graph Navigation API, Replication: P2P with Master Node, Written in: C#, Concurrency: Yes (Transactional update in online query mode, Non-blocking read in Batch Mode) Misc: distributed in-memory storage, parallel graph computation platform (Microsoft Research Project)
AllegroGraph

API: Java, Python, Ruby, C#, Perl, Clojure, Lisp Protocol: REST, Query Method: SPARQL and Prolog, Libraries: Social Networking Analytics & GeoSpatial, Written in: Common Lisp, Links: Learning Center », Videos »
BrightstarDB

 A native, .NET, semantic web DBMS with code first Entity Framework, LINQ and OData support. API: C#, Protocol: SPARQL HTTP, C#, Query Method: LINQ, SPARQL, Written in: C#
Bigdata

 API: Java, Jini service discovery, Concurrency: very high (MVCC), Written in: Java, Misc: GPL + commercial, Data: RDF data with inference, dynamic key-range sharding of indices, Misc: Blog » (parallel DBMS, high-availability architecture, immortal DBMS with historical views)
Meronymy

 RDF enterprise database management system. It is cross-platform and can be used with most programming languages. Main features: high performance, guarantee database transactions with ACID, secure with ACL's, SPARQL & SPARUL, ODBC & JDBC drivers, RDF & RDFS. »
WhiteDB

WhiteDB is a fast lightweight graph/N-tuples shared memory DBMS library written in C with focus on speed, portability and ease of use. Both for Linux and Windows, dual licensed with GPLv3 and a free nonrestrictive royalty-free commercial licence.
Onyx DBMS

 Graph/ORM high throughput DBMS built in Java supports embedded, in-memory, and remote. Horizontal scalability through sharding, partitioning, replication, and disaster recovery API: Java, REST via (Objective C, Android, etc...), Protocol: Java embedded/Binary Socket/REST, Query Method: Persistence Manager/ORM, Replication: Multicast, Written in: Java, Concurrency: Re-entrant read/write, Misc: Free and Open Source. Commercial licensing available Tutorials
OpenLink Virtuoso

 a/k/a Virtuoso Universal Server Multi-model (hybrid) DBMS supporting SQL/Tabular Relational (SQL), RDF/Graph Relational (SPARQL), XML (XPath, XQuery), Text/Document/Object, and more, available in Community (Open Source) and Enterprise (Commercial) Editions.
API: ODBC, JDBC, OLE DB, ADO.NET, JSON, RDF4J/Sesame, Redland, SPARQL, others;
Protocol: ODBC, JDBC, OLE DB, ADO.NET, HTTP, SPARQL, NNTP, IMAP, POP, LDP, others;
Query Method: SQL, SPARQL, SPARQL-in-SQL (SPASQL), SQL-in-SPARQL (via SQL/PSM), XPath, XQuery, others;
Replication (Enterprise Edition only): Star, Chain, and/or Bi-Directional Replication Clusters, as well as Shared-Nothing Elastic Clusters;
Written in: C/C++; extensible via C/C++, Java, Perl, Python, PHP, others;
Concurrency: ACID;
Misc: Role-Based Access Control (RBAC), Attribute-Based Access Control (ABAC)
Links: Virtuoso manual, Evolving Documentation. Open Source Project
VertexDB
FlockDB

 by twitter » »
weaver

scalable, fast, consistent
BrightstarDB
Execom IOG
Fallen 8

Github »
[Java Universal Network / Graph Framework, OpenRDF / Sesame, Filament, OWLim, NetworkX, iGraph, Jena]
List of SPARQL implementations can be found here
Multimodel Database Management Systems
ArangoDB

API: REST, Graph Blueprints, C#, D, Ruby, Python, Java, PHP, Go, Python, etc. Data Model: Documents, Graphs and Key/Values. Protocol: HTTP using JSON. Query Method: declarative query language (AQL), query by example. Replication: master-slave (m-m to follow), Sharding: automatic and configurable Written in: C/C++/Javascript (V8 integrated), Concurrency: MVCC, tunable Misc: ACID transactions, microservices framework "Foxx" (Javascript), many indices as secondary, fulltext, geo, hash, Skip-list, capped collections
OpenLink Virtuoso

a/k/a Virtuoso Universal Server Multi-model (hybrid) DBMS supporting SQL/Tabular Relational (SQL), RDF/Graph Relational (SPARQL), XML (XPath, XQuery), Text/Document/Object, and more, available in Community (Open Source) and Enterprise (Commercial) Editions.
API: ODBC, JDBC, OLE DB, ADO.NET, JSON, RDF4J/Sesame, Redland, SPARQL, others;
Protocol: ODBC, JDBC, OLE DB, ADO.NET, HTTP, SPARQL, NNTP, IMAP, POP, LDP, others;
Query  Method: SQL, SPARQL, SPARQL-in-SQL (SPASQL), SQL-in-SPARQL (via SQL/PSM), XPath, XQuery, others;
Replication (Enterprise Edition only): Star, Chain, and/or Bi-Directional Replication Clusters, as well as Shared-Nothing Elastic Clusters;
Written in: C/C++; extensible via C/C++, Java, Perl, Python, PHP, others;
Concurrency: ACID; Misc: Role-Based Access Control (RBAC), Attribute-Based Access Control (ABAC)
Links: Virtuoso manual, Evolving Documentation. Open Source Project
OrientDB

API: REST, Binary Protocol, Java, Node.js, Tinkerpop Blueprints, Python, PHP, Go, Elixir, etc., Schema: Has features of an Object DBMS, Document DBMS, Graph DBMS, and Key-Value DBMS, Written in: Java, Query Method: SQL, Gremlin, SparQL, Concurrency: MVCC, tunable, Indexing: Primary, Secondary, Composite indexes with support for Full-Text and Spatial, Replication: Master-Master + sharding, Misc: Really fast, Lightweight, ACID with recovery.
FaunaDB

Packaging: Fully managed serverless cloud, or on-premise enterprise packages. API: HTTP, JavaScript, C#, Java, Ruby, Python, Swift, Android, Go, Python, Scala. Data Model: Documents, Graphs and Key/Values. Query Method: Fauna Query Language is optimized for expressing business transactions including precondition checks and control flow. Replication: active/active with global ACID transactions, Sharding: automatic Written in: Scala Concurrency: MVCC with configurable snapshot retention, all transactions are consistent. Misc: Multi-region ACID transactions, indexes, joins, and object level security.
FoundationDB

Bought by Apple Inc. Closed and reopened for public access.
Datomic

API: Many jvm languages, Protocol: Native + REST, Query Method: Datalog + custom extensions, Scaling: elastic via underlying DB (in-mem, DynamoDB, Riak, CouchBase, Infinispan, more to come), Written in: Clojure, Concurrency: ACID MISC: smart caching, unlimited read scalability, full-text search, cardinality, bi-directional refs 4 graph traversal, loves Clojure + Storm.
gunDB

API: JavaScript Schema: Has features of an Object DBMS, Document DBMS, Graph DBMS, and Key-Value DBMS Written in: JavaScript Query Method: JavaScript Concurrency: Eventual consistency with hybrid vector/timestamp/lexical conflict resolution Indexing: O(1) key/value, supports multiple indices per record Replication: Multi-Master/Master; browser peer-to-peer (P2P) enabled Misc: Open source, realtime sync, offline-first, distributed/decentralized, graph-oriented, and fault-tolerant
CortexDB

CortexDB is a dynamic schema-less multi-model data base providing nearly all advantages of up to now known NoSQL data base types (key-value store, document store, graph DB, multi-value DB, column DB) with dynamic re-organization during continuous operations, managing analytical and transaction data for agile software configuration,change requests on the fly, self service and low footprint.
Oracle NOSQL Database

Oracle NoSQL Database is a distributed key-value DBMS with support for JSON docs. It is designed to provide highly reliable, scalable and available data storage across a configurable set of systems that function as storage nodes. NoSQL and the Enterprise Data is stored as key-value pairs, which are written to particular storage node(s), based on the hashed value of the primary key. Storage nodes are replicated to ensure high availability, rapid failover in the event of a node failure and optimal load balancing of queries. API: Java/C, Python, NodeJs, C#.
AlchemyDB

GraphDB + RDBMS + KV Store + Document Store. Alchemy Database is a low-latency high-TPS NewSQL RDBMS embedded in the NOSQL datastore redis. Extensive datastore-side-scripting is provided via deeply embedded Lua. Bought and integrated with Aerospike.
WonderDB

API:JDBC,SQL; WonderDB is fully transactional, distributed NewSQL DBMS implemented in java based on relational architectures. So you can get best of both worlds, sql, joins and ease of use from SQL and distribution, replication and sharding from NoSQL movement. Tested performance is over 60K per node with Amazon m3.xlarge VM.
RockallDB

A new concept to ‘NoSQL’ DBMS where a memory allocator and a transactional DBMS are melted together into an almost seamless whole. The programming model uses variants of well-known memory allocation calls like ‘new’ and ‘delete’ to manage the database. The result is very fast, natural to use, reliable and scalable. It is especially good in Big Data, data collection, embedded, high performance, Internet of Things (IoT) or mobile type applications.
ZZZ Base

GraphDB + KV Store + Document Store + Object + TimeSeries. ZZZ base is a knowledge base embedded in a single executable ZZZ server. Currently, a base can store up to 8,000,000 terabytes of information. A ZZZ server can access an unlimited number of knowledge bases on the computer on which it is installed or on the Internet by linking to an unlimited number of other ZZZ servers.

The following section contains Soft NoSQL Systems

[Mostly NOT originated out of a Web 2.0 need but worth a look for great non relational solutions]
Object Database Management Systems »
Versant

API: Languages/Protocol: Java, C#, C++, Python. Schema: language class model (easy changeable). Modes: always consistent and eventually consistent Replication: synchronous fault tolerant and peer to peer asynchronous. Concurrency: optimistic and object based locks. Scaling: can add physical nodes on fly for scale out/in and migrate objects between nodes without impact to application code. Misc: MapReduce via parallel SQL like query across logical database groupings.
db4o

API: Java, C#, .Net Langs, Protocol: language, Query Method: QBE (by Example), Soda, Native Queries, LINQ (.NET), Replication: db4o2db4o & dRS to relational, Written in: Java, Concurrency: ACID serialized, Misc: embedded lib, Links: DZone Refcard #53 », Book »,
Objectivity

API: Languages: Java, C#, C++, Python, Smalltalk, SQL access through ODBC. Schema: native language class model, direct support for references, interoperable across all language bindings. 64 bit unique object ID (OID) supports multi exa-byte. Platforms: 32 and 64 bit Windows, Linux, Mac OSX, *Unix. Modes: always consistent (ACID). Concurrency: locks at cluster of objects (container) level. Scaling: unique distributed architecture, dynamic addition/removal of clients & servers, cloud environment ready. Replication: synchronous with quorum fault tolerant across peer to peer partitions.
GemStone/S

API: Java, C, C++, Smalltalk Schema: language class model Platforms: Linux, AIX, Solaris, Mac OSX, Windows clients Modes: always consistent (ACID) Replication: shared page cache per node, hot standby failover Concurrency: optimistic and object based locks Scaling: arbitrarily large number of nodes Misc: SQL via GemConnect
Starcounter

API: C# (.NET languages), Schema: Native language class model, Query method: SQL, Concurrency: Fully ACID compliant, Storage: In-memory with transactions secured on disk, Reliability: Full checkpoint recovery, Misc: VMDBMS - Integrating the DBMS with the virtual machine for maximal performance and ease of use.
Perst

API: Java,Java ME,C#,Mono. Query method: OO via Perst collections, QBE, Native Queries, LINQ, native full-text search, JSQL Replication: Async+sync (master-slave) Written in: Java, C#. Caching: Object cache (LRU, weak, strong), page pool, in-memory DBMS Concurrency: Pessimistic+optimistic (MVCC) + async or sync (ACID) Index types: Many tree models + Time Series. Misc: Embedded lib., encryption, automatic recovery, native full text search, on-line or off-line backup.
VelocityDB

Written in100% pure C#, Concurrency: ACID/transactional, pessimistic/optimistic locking, Misc: compact data, B-tree indexes, LINQ queries, 64bit object identifiers (Oid) supporting multi millions of databases and high performance. Deploy with a single DLL of around 400KB.
HSS Database

Written in: 100% C#, The HSS DB v3.0 (HighSpeed-Solutions Database), is a client based, zero-configuration, auto schema evolution, acid/transactional, LINQ Query, DBMS for Microsoft .NET 4/4.5, Windows 8 (Windows Runtime), Windows Phone 7.5/8, Silverlight 5, MonoTouch for iPhone and Mono for Android
ZODB

API: Python, Protocol: Internal, ZEO, Query Method: Direct object access, zope.catalog, gocept.objectquery, Replication: ZEO, ZEORAID, RelStorage Written in: Python, C Concurrency: MVCC, License: Zope Public License (OSI approved) Misc: Used in production since 1998
Newt DB

Newt DB leverages the pluggable storage layer of ZODB to use RelStorage to store data in Postgres. Newt adds conversion of data from the native serialization used by ZODB to JSON, stored in a Postgres JSONB column. The JSON data supplements the native data to support indexing, search, and access from non-Python applications. It adds a search API for searching the Postgres JSON data and returning persistent objects. Query Method: Postgres SQL, ZODB API, Replication: Postgres, ZEO, ZEORAID, RelStorage, Written in: Python, Concurrency: MVCC, License: MIT
NEO

API: Python - ZODB "Storage" interface, Protocol: native, Query Method: transactional key-value, Replication: native, Written in: Python, Concurrency: MVCC (internally), License: GPL "v2 or later", Misc: Load balancing, fault tolerant, hot-extensible.
Magma

Smalltalk DB, optimistic locking, Transactions, etc.
siaqodb

An object DBMS engine that currently runs on .NET, Mono, Silverlight,Windows Phone 7, MonoTouch, MonoAndroid, CompactFramework; It has implemented a Sync Framework Provider and can be synchronized with MS SQLServer; Query method:LINQ;
JADE

Programming Language with an Object DBMS build in. Around since 1996.
Sterling

is a lightweight object-oriented DBMS for .NET with support for Silverlight and Windows Phone 7. It features in-memory keys and indexes, triggers, and support for compressing and encrypting the underlying data.
MarcelloDB

An embedded object DBMS designed for mobile apps targeting .net and Mono runtimes. Supports .net/mono, Xamarin (iOS and Android), Windows 8.1/10, Windows Phone 8.1. Simple API, built on top of json.net and has a simple but effective indexing mechanism. Development is focussed on being lightweight and developer friendly. Has transaction support. Open-source and free to use.
Morantex

Stores .NET classes in a datapool. Build for speed. SQL Server integration. LINQ support.
EyeDB

EyeDB is an LGPL OODBMS, provides an advanced object model (inheritance, collections, arrays, methods, triggers, constraints, reflexivity), an object definition language based on ODMG ODL, an object query and manipulation language based on ODMG OQL. Programming interfaces for C++ and Java.
FramerD

Object-Oriented DBMS designed to support the maintenance and sharing of knowledge bases. Optimized for pointer-intensive data structures used by semantic networks, frame systems, and many intelligent agent applications. Written in: ANSI C.
Ninja Database Pro

Ninja Database Pro is a .NET ACID compliant relational object DBMS that supports transactions, indexes, encryption, and compression. It currently runs on .NET Desktop Applications, Silverlight Applications, and Windows Phone 7 Applications.
NDatabase

API: C#, .Net, Mono, Windows Phone 7, Silverlight, Protocol: language, Query Method: Soda, LINQ (.NET), Written in: C#, Misc: embedded lib, indexes, triggers, handle circular ref, LinqPad support, Northwind sample, refactoring, in-memory DBMS, Transactions Support (ACID) and more, Documentation: »
PicoLisp

Language and Object DBMS, can be viewed as a DBMS Development Framework. Schema: native language class model with relations + various indexes. Queries: language build in + a small Prolog like DSL Pilog. Concurrency: synchronization + locks. Replication, distribution and fault tolerance is not implemented per default but can be implemented with native functionality. Written in C (32bit) or assembly (64bit).
acid-state

API: Haskell, Query Method: Functional programming, Written in: Haskell, Concurrency: ACID, GHC concurrent runtime, Misc: In-memory with disk-based log, supports remote access Links: Wiki », Docs »
ObjectDB

API: Java (JPA / JDO) Query method: JPA JPQL, JDO JDOQL Replication: Master-slave Written in: 100% Pure Java Caching: Object cache, Data cache, Page cache, Query Result cache, Query program cache Concurrency: Object level locking (pessimistic + optimistic) Index types: BTree, single, path, collection Misc: Used in production since 2004, Embedded mode, Client Server mode, automatic recovery, on-line backup.
CoreObject

CoreObject: Version-controlled OODB, that supports powerful undo, semantic merging, and real-time collaborative editing. MIT-licensed, API: ObjC, Schema: EMOF-like, Concurrency: ACID, Replication: differential sync, Misc: DVCS based on object graph diffs, selective undo, refs across versioned docs, tagging, temporal indexing, integrity checking.
[ StupidDB », KiokuDB » (Perl solution), Durus »]
Grid & Cloud Database Management Solutions
GridGain

In-Memory Computing Platform built on Apache® Ignite™ to provide high-speed transactions with ACID guarantees, real-time streaming, and fast analytics in a single, comprehensive data access and processing layer. The distributed in-memory key value store is ANSI SQL-99 compliant with support for SQL and DML via JDBC or ODBC. API: Java, .NET, and C++. Minimal or no modifications to the application or database layers for architectures built on all popular RDBMS, NoSQL or Apache™ Hadoop® DBMS.
Crate Data

A shared nothing, document-oriented cluster data store. Accessed via SQL and has builtin BLOB support. Uses the cluster state implementation and node discovery of Elasticsearch. License: Apache 2.0, Query Method: SQL, Clients: HTTP (REST), Python, Java (JDBC or native), Ruby, JS, Erlang, Replication + Sharding: automatic and configurable, written in: Java, » Crate Data GitHub Project, » Documentation.
Oracle Coherence

Oracle Coherence offers distributed, replicated, multi-datacenter, tiered (off-heap/SSD) and near (client) caching. It provides distributed processing, querying, eventing, and map/reduce, session management, and propagation of database updates to caches. Operational support provided by a Grid Archive deployment model.
GigaSpaces

Popular SpaceBased Grid Solution.
GemFire

GemFire offers in-memory globally distributed data management with dynamic scalability, very high performance and granular control supporting the most demanding applications. Well integrated with the Spring Framework, developers can quickly and easily provide sophisticated data management for applications. With simple horizontal scale-out, data latency caused by network roundtrips and disk I/O can be avoided even as applications grow.
Infinispan

scalable, highly available data grid platform, open source, written in Java.
Queplix

NOSQL Data Integration Environment, can integrate relational, object, BigData – NOSQL easily and without any SQL.
Hazelcast

Hazelcast is a in-memory data grid that offers distributed data in Java with dynamic scalability under the Apache 2 open source license. It provides distributed data structures in Java in a single Jar file including hashmaps, queues, locks, topics and an execution service that allows you to simply program these data structures as pure java objects, while benefitting from symmetric multiprocessing and cross-cluster shared elastic memory of very high ingest data streams and very high transactional loads.
ScaleOut Software, Galaxy, Joafip, Coherence, eXtremeScale]
XML Database Management Systems
EMC Documentum xDB

(commercial system) API: Java, XQuery, Protocol: WebDAV, web services, Query method: XQuery, XPath, XPointer, Replication: lazy primary copy replication (master/replicas), Written in: Java, Concurrency: concurrent reads, writes with lock; transaction isolation, Misc: Fully transactional persistent DOM; versioning; multiple index types; metadata and non-XML data support; unlimited horizontal scaling. Developer Network »
eXist

API: XQuery, XML:DB API, DOM, SAX, Protocols: HTTP/REST, WebDAV, SOAP, XML-RPC, Atom, Query Method: XQuery, Written in: Java (open source), Concurrency: Concurrent reads, lock on write; Misc: Entire web applications can be written in XQuery, using XSLT, XHTML, CSS, and Javascript (for AJAX functionality). (1.4) adds a new full text search index based on Apache Lucene, a lightweight URL rewriting and MVC framework, and support for XProc.
Sedna

Misc: ACID transactions, security, indices, hot backup. Flexible XML processing facilities include W3C XQuery implementation, tight integration of XQuery with full-text search facilities and a node-level update language.
BaseX

BaseX is a fast, powerful, lightweight XML DBMS and XPath/XQuery processor with highly conformant support for the latest W3C Update and Full Text Recommendations. Client/Server architecture, ACID transaction support, user management, logging, Open Source, BSD-license, written in Java, runs out of the box.
Qizx

commercial and open source version, API: Java, Protocols: HTTP, REST, Query Method: XQuery, XQuery Full-Text, XQuery Update, Written in: Java, full source can be purchased, Concurrency: Concurrent reads & writes, isolation, Misc: Terabyte scalable, emphasizes query speed.
Berkeley DB XML

API: Many languages, Written in: C++, Query Method: XQuery, Replication: Master / Slave, Concurrency: MVCC, License: Sleepycat
JEntigrator

API: Java. The application and database management system in one. Collects data as multiple XML files on the disk. Implements facet-oriented data model. Each data object is considered as an universal facet container. The end-user can design and evolve data objects individually through the GUI without any coding by adding/removing facets to/from it.
[ Xindice, Tamino, ]
Multidimensional Database Management Systems
Globals:

by Intersystems, multidimensional array.Node.js API, array based APIs (Java / .NET), and a Java based document API.
Intersystems Cache

Post-relational System. Multidimensional array APIs, Object APIs, Relational Support (Fully SQL capable JDBC, ODBC, etc.) and Document APIs are new in the upcoming 2012.2.x versions. Available for Windows, Linux and OpenVMS.
GT.M

API: M, C, Python, Perl, Protocol: native, inprocess C, Misc: Wrappers: M/DB for SimpleDB compatible HTTP », MDB:X for XML », PIP for mapping to tables for SQL », Features: Small footprint (17MB), Terabyte Scalability, Unicode support, Database encryption, Secure, ACID transactions (single node), eventual consistency (replication), License: AGPL v3 on x86 GNU/Linux, Links: Slides »

Huge thanks to my buddy Ludovic Rembert from Privacy Canada for reminding me to include GT.M to this list. His website touches on many privacy issues, mainly focusing on the best VPNs for Canadians and preserving digital anonymity.
SciDB

Array Data Model for Scientists, » paper, » poster, » HiScaBlog
MiniM DB

: Multidimensional arrays, API: M, C, Pascal, Perl, .NET, ActiveX, Java, WEB. Available for Windows and Linux.
rasdaman

: Short description: Rasdaman is a scientific DBMS that allows to store and retrieve multi-dimensional raster data (arrays) of unlimited size through an SQL-style query language. API: C++/Java, Written in C++, Query method: SQL-like query language rasql, as well as via OGC standards WCPS, WCS, WPS link2
DaggerDB

: is a new Realtime analytics DBMS written in .NET C#. ACID compliant. fluent .NET query API, Client / server or in-process. In-memory and persistent mode.
[ YottaDB: Fast fork of GT.M, EGTM: GT.M for Erlang, "IODB: EGTM-powered ObjectDB for Erlang ]
Multivalue Database Management Systems
U2

(UniVerse, UniData): MultiValue Databases, Data Structure: MultiValued, Supports nested entities, Virtual Metadata, API: BASIC, InterCall, Socket, .NET and Java API's, IDE: Native, Record Oriented, Scalability: automatic table space allocation, Protocol: Client Server, SOA, Terminal Line, X-OFF/X-ON, Written in: C, Query Method: Native mvQuery, (Retrieve/UniQuery) and SQL, Replication: yes, Hot standby, Concurrency: Record and File Locking (Fine and Coarse Granularity)
OpenInsight

API: Basic+, .Net, COM, Socket, ODBC, Protocol: TCP/IP, Named Pipes, Telnet, VT100. HTTP/S Query Method: RList, SQL & XPath Written in: Native 4GL, C, C++, Basic+, .Net, Java Replication: Hot Standby Concurrency: table &/or row locking, optionally transaction based & commit & rollback Data structure: Relational &/or MultiValue, supports nested entities Scalability: rows and tables size dynamically
TigerLogic PICK

(D3, mvBase, mvEnterprise) Data Structure: Dynamic multidimensional PICK data model, multi-valued, dictionary-driven, API: NET, Java, PHP, C++, Protocol: C/S, Written In: C, Query Method: AQL, SQL, ODBC, Pick/BASIC, Replication: Hot Backup, FFR, Transaction Logging + real-time replication, Concurrency: Row Level Locking, Connectivity: OSFI, ODBC, Web-Services, Web-enabled, Security: File level AES-128 encryption
Reality

(Reality NPS): The original MultiValue dataset DBMS, virtual machine, enquiry and rapid development environment. Delivers ultra efficiency, scalability and resilience while extended for the web and with built-in auto sizing, failsafe and more. Interoperability includes Web Services - Java Classes, RESTful, XML, ActiveX, Sockets, .NetLanguages, C and, for those interoperate with the world of SQL, ODBC/JDBC with two-way transparent SQL data access.
OpenQM

Supports nested data. Fully automated table space allocation. Concurrency control via task locks, file locks & shareable/exclusive record locks. Case insensitivity option. Secondary key indices. Integrated data replication. QMBasic programming language for rapid development. OO programming integrated into QMBasic. QMClient connectivity from Visual Basic, PowerBasic, Delphi, PureBasic, ASP, PHP, C and more. Extended multivalue query language.
Model 204 Database

A high performance dbms that runs on IBM mainframes (IBM z/OS, z/VM, zVSE), +SQL interface with nested entity support API: native 4GL (SOUL + o-o support), SQL, Host Language (COBOL, Assembler, PL1) API, ODBC, JDBC, .net, Websphere MQ, Sockets Scalability: automatic table space allocation, 64-bit support Written in: IBM assembler, C Query method: SOUL, SQL, RCL ( invocation of native language from client ) Concurrency: record and file level locking Connectivity: TN3270, Telnet, Http
Tieto TRIP

Hybrid DBMS / search engine system with characteristics of multi-value, document, relational, XML, and graph DBMS. Used in production since 1985 for high-performance search and retrieve solutions. Full-text search, text classification, similarity search, results ranking, real time facets, Unicode, Chinese word segmentation, and more. Platforms: Windows, Linux, AIX and Solaris. API: .NET, Java and C/C++. Query methods: native (CCL), SQL subset, XPath. Commercial.
ESENT

(by Microsoft) ISAM storage technology. Access using index or cursor navigation. Denormalized schemas, wide tables with sparse columns, multi-valued columns, and sparse and rich indexes. C# and Delphi drivers available. Backend for a number of MS Products as Exchange.
jBASE

jBASE is an application platform and DBMS that allows normal MultiValue (MV) applications to become native Windows, Unix or Linux programs. Traditional MV features are supported, including BASIC, Proc, Paragraph, Query and Dictionaries. jBASE jEDI Architecture, allows you to store data in any DBMS, such as Microsoft SQL, Oracle and DB2. jBASE jAgent supports BASIC, C, C++, .NET, Java and REST APIs. Additional features include dynamic objects, encryption, case insensitivity, audit logging and transaction journaling for online backup and disaster recovery.
Event Sourcing
Event Store
Eventsourcing for Java (es4j)

Key features: Clean, succinct Command/Event model, Compact data storage layout, Disruptor for fast message processing, CQengine for fast indexing and querying, In-memory and on-disk storage, Causality-preserving Hybrid Logical Clocks, Locking synchronization primitive, OSGi support
Time Series / Streaming Database Management Systems
Axibase

Distributed DB designed to store and analyze high-frequency time-series data at scale. Includes a large set of built-in features: Rule Engine, Visualization, Data Forecasting, Data Mining. API: RESTful API, Network API, Data API, Meta API, SQL API Clients: R, Java, Ruby, Python, PHP, Node.js Replication: Master Slave Major protocol & format support: CSV, nmon, pickle, StatsD, collectd, tcollector, scollector, JMX, JDBC, SNMP, JSON, ICMP, OVPM, SOAP.
kdb+

time-series DBMS optimized for Big Data analytics.
quasardb

very high-performance time series DBMS. Highly scalable. API: C, C++, Java, Python and (limited) RESTful Protocol: binary Query method: API/SQL-like, Replication: Distributed, Written in: C++ 11/Assembly, Concurrency: ACID, Misc: built-in data compression, native support for FreeBSD, Linux and Windows. License: Commercial.
Riak TS

Enterprise-grade NoSQL time series DBMS optimized specifically for IoT and Time Series data. It ingests, transforms, stores, and analyzes massive amounts of time series data. Riak TS is engineered to be faster than Cassandra.
Informix Time Series Solution , influxdata , pipelinedb
http://btrdb.io/

The Berkeley Tree DataBase BTrDB provides very fast storage of scalar-valued timeseries data. Stores data with nanosecond-precision timestamps. Boasts 16.7 million writes per second and 19.8 million reads per second on a single Intel Xeon E5-2680v2 based cloud server with 60GB of RAM (EC2 c3.8xlarge).
eXtremeDB

(listed also under other NoSQL related DBMS)
Akumuli

Akumuli is a column-oriented time-series DBMS. It uses novel data-structures and compression algorithms designed with time-series data in mind. It can take full advantage of modern SSD and NVMe drives. Akumuli integrates with Grafana, Prometheus, Collectd, and other monitoring systems.
Other NoSQL related database management systems
IBM Lotus/Domino

Type: Document Store, API: Java, HTTP, IIOP, C API, REST Web Services, DXL, Languages: Java, JavaScript, LotusScript, C, @Formulas, Protocol: HTTP, NRPC, Replication: Master/Master, Written in: C, Concurrency: Eventually Consistent, Scaling: Replication Clusters
eXtremeDB

Type: Hybrid In-Memory and/or Persistent DBMS DBMS Written in: C; API: C/C++, SQL, JNI, C#(.NET), JDBC; Replication: Async+sync (master-slave), Cluster; Scalability: 64-bit and MVCC
RDM Embedded

APIs: C++, Navigational C. Embedded Solution that is ACID Compliant with Multi-Core, On-Disk & In-Memory Support. Distributed Capabilities, Hot Online Backup, supports all Main Platforms. Supported B Tree & Hash Indexing. Replication: Master/Slave, Concurrency: MVCC. Client/Server: In-process/Built-in.
ISIS Family

(semistructured databases) »
Moonshadow

NoSql, in-memory, flat-file, cloud-based. API interfaces. Small data footprint and very fast data retrieval. Stores 200 million records with 200 attributes in just 10GB. Retrieves 150 million records per second per CPU core. Often used to visualize big data on maps. Written in C.
VaultDB

Next-gen NoSQL encrypted document store. Multi-recipient / group encryption. Features: concurrency, indices, ACID transactions, replication and PKI management. Supports PHP and many others. Written in C++. Commercial but has a free version. API: JSON
Vyhodb

Service oriented, schema-less, network data model DBMS. Client application invokes methods of vyhodb services, which are written in Java and deployed inside vyhodb. Vyhodb services reads and modifies storage data. API: Java, Protocol: RSI - Remote service invocation, Written in: Java, ACID: fully supported, Replication: async master slave, Misc: online backup, License: proprietary
Applied Calculus

Applied Calculus implements persistent AVL Trees / AVL DBMS. 14 different types of DBMS - represented as classes in both C# and Java. These DBMS perform transaction logging on the node file to ensure that failed transactions are backed out. Very fast on solid state storage (ca. 1780 transactions/second. AVL Trees considerably outperform B+ Trees on solid state. Very natural language interface. Each DBMS is represented as a collection class that strongly resembles the corresponding class in Pure Calculus.
Prevayler

Java RAM Data structure journalling.
Yserial

Python wrapper over sqlite3
SpreadsheetDB

A DBMS as a service that can be queried with a spreadsheet through an HTTP API.
chaozzDB

A full-featured, easy-to-use flatfile (noSQL) DBMS. Download from Github >>
Scientific and Specialized Database Management Systems
BayesDB

BayesDB, a Bayesian database table, lets users query the probable implications of their tabular data as easily as an SQL DBMS lets them query the data itself. Using the built-in Bayesian Query Language (BQL), users with no statistics training can solve basic data science problems, such as detecting predictive relationships between variables, inferring missing values, simulating probable observations, and identifying statistically similar database entries.
GPUdb

A distributed DBMS for many core devices. GPUdb leverages many core devices such as NVIDIA GPUs to provide an un-parallelled parallel DBMS experience. GPUdb is a scalable, distributed DBMS with SQL-style query capability, capable of storing Big Data. Developers using the GPUdb API add data, and query the data with operations like select, group by, and join. GPUdb includes many operations not available in other "cloud DBMS" offerings.
unresolved and uncategorized
Web Hosting Canada Reviews

- Live up time tracking and testing on over 20 of the most popular hosting solutions. Hosting speeds compared across 3 different CMS configurations.
Btrieve

(by Pervasive Software) key/index/tuple DB. Using Pages. » (faq »)
KirbyBase

Written in: Ruby. github: »
Tokutek:
Recutils:

GNU Tool for text files containing records and fields. Manual »
FileDB:

Mainly targeted to Silverlight/Windows Phone developers but its also great for any .NET application where a simple local DBMS is required, extremely Lightweight - less than 50K, stores one table per file, including index, compiled versions for Windows Phone 7, Silverlight and .NET, fast, free to use in your applications
MentDB:

A digital brain, based on the language of thought (Mentalese), to manage relations and strategies (with thoughts/words/symbols) into a cognitive cerebral structure. Programing language: MQL (Mentalese Query Language) for mental processes, ACID transaction, API: REST and web socket, Thoughts Performance: READ: 18035/s; WRITE: 416/s; Asynchronous Full JAVA
D2000:

Realtime application server with an in-memory realtime DBMS with object level events and optional persistence of data of selected objects. Subscribe/publish mechanism of objects changes distribution. API / Query Method: SQL(ODBC), C, Java, multiple industrial communication protocols. Support for timeseries. Multiplatform (Windows/Linux/ARM/HP-UX/OpenVMS). Replication: async (master-slaves). Proprietary code. Written in: ADA
CodernityDB

illuminate Correlation Database », FluidDB (Column Oriented DB) », Fleet DB », Btrieve, Twisted Storage », Java-Chronicle », Ringo, Sherpa, tin, Dryad, SkyNet, Disco Possibly the oldest NoSQL DB (together with MUMPS and IBMs IMS & IDMS [1968,1964]): » Adabas VSAM by IBM is also a good candidate.



```