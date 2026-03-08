# Data Structure ,Databases and Einstein

# By Sachin Dixit

![](img%5CData%20Structure%20%2CDatabases%20and%20Einstein_0.jpg)

# What is Data ?

![](img%5CData%20Structure%20%2CDatabases%20and%20Einstein_1.png)

# Data Structures



* Why would we differentiate between primitives vs DSs ?
* Famous DSs
  * Array : 1D\,2D\,3D so on …
  * Stack :
  * Sets :
  * Maps
  * Queue : Simple \, circular \, priority
  * List :SLL\,DLL\,SCLL\,DCLL
  * Tree: bTree \,
  * Graph :directed \, undirected\,simple\,weighted\,connected
* Tables ? RDDs ? dataframe ?
* Advanced DS we don't talk about
* Is Date a DS ? why ? whynot ?


# Taking a grip on DS



* What gives rise to O notation ?
* Benefits vs limitations
  * time  _vs\._  space
  * performance  _vs\._  elegance
  * generality  _vs\. _ simplicity
  * one operation’s performance  _vs\._  another’s
* Choices made by language runtime \!
* The cast system :D
* Type system ? what about them ?
* Objects ? don't get me started …\. :P


# What about “other than text”

Images

Voice

Vidoes

Geospatial

Many more

What do we mean by unstructured data ?

Are these DS ?

Skipping data storage formats : perquet \,ORC \,avro \,protobuff \.Also yaml

# Data Transfer

Tab vs common vs pipe vs something separated : Loose and easy

XML is great ? why ?

JSOn is great ? why ?

Is schema necessary ? where and how it will impact ?

The Document model inspiration of the www \!

Aside : Namespacing and RSS/SOAP/ATOM

What happens to your DS in these transfer formats ?

# Xml  intuition

![](img%5CData%20Structure%20%2CDatabases%20and%20Einstein_2.png)

__<__  <span style="color:#f3975f">BOOKS</span>  __>__

__<__  <span style="color:#f3975f">book id=“123” loc=“library”</span>  __>__

__   <__  <span style="color:#f3975f">author</span>  __>Hull<__  <span style="color:#f3975f">/author</span>  __>__

__   <__  <span style="color:#f3975f">title</span>  __>California<__  <span style="color:#f3975f">/title</span>  __>__

__   <__  <span style="color:#f3975f">year</span>  __> 1995 <__  <span style="color:#f3975f">/year</span>  __>__

__<__  <span style="color:#f3975f">/book</span>  __>__

__<__  <span style="color:#f3975f">article</span>  __ id=“555” ref=“123”>__

__   <__  <span style="color:#f3975f">author</span>  __>Su<__  <span style="color:#f3975f">/author</span>  __>__

__   <__  <span style="color:#f3975f">title</span>  __> Purdue<__  <span style="color:#f3975f">/title</span>  __>__

__<__  <span style="color:#f3975f">/article</span>  __>__

__<__  <span style="color:#f3975f">/BOOKS</span>  __>__

__Credit :https://goldberg\.berkeley\.edu/courses/F04/215/XML\-215\-presentation\.ppt__

# JSON

•JSON is not a document format\.

•JSON is not a markup language\.

•JSON is not a general serialization format\.

No cyclical/recurring structures\.

No invisible structures\.

No functions

JSON has no validator

_Credit : Crockford _

•JSON's simple values are the same as used in programming languages\.

•No restructuring is required: JSON's structures look like conventional programming language structures\.

•JSON's object is record\, struct\, object\, dictionary\, hash\, associate array\.\.\.

•JSON's array is array\, vector\, sequence\, list…

Language independent data interchange

# JSON is not XML

•objects

•arrays

•strings

•numbers

•booleans

• __null__

_Credit : Crockford _

element

attribute

attribute string

content

__\<\!\[CDATA\[ \]\]>__

entities

declarations

schema

stylesheets

comments

version

namespace

# Data meet the DataBase

What happens to your DS in database ?

Issues of fitment and loss of detail

Internal DS used by db \(for  academic interest \)

Different DB/Storage types ?

# Database types or Data organization styles ?

RDBMS : oracle\,mysql\,postgres

Key Value stores : Redis \,Memcache

Document Store :MongoDB\, DynamoDB

Wide Column : Hbase \, Cassandra

Graph DB : Neo4j

General features for NOSql family

Semi structured data

Non relational flexible schema

Looser transaction guarantees

What about CMS ?

What about big data ?

Problems of scale for DBs: a CAP for you

# NSQL Intuition

| Data Model | <span style="color:#010000">relations </span>  <span style="color:#010000">tuples   </span>  <span style="color:#010000">attributes  </span>  <span style="color:#010000">domains</span>  <span style="color:#010000">normalization</span> | <span style="color:#010000">documents</span>  <span style="color:#010000">graphs</span>  <span style="color:#010000">key/values</span>  <span style="color:#010000">   </span> |
| :-: | :-: | :-: |
| Query Model | <span style="color:#010000">relational algebra</span>  <span style="color:#010000">tuple calculus</span> | <span style="color:#010000">graph traversal</span>  <span style="color:#010000">text search</span>  <span style="color:#010000">map/reduce</span> |
| Implementation | <span style="color:#010000">rigid schemas</span>  <span style="color:#010000">ACID compliance</span> | <span style="color:#010000">flexible schemas </span>  <span style="color:#010000">BASE</span> |

![](img%5CData%20Structure%20%2CDatabases%20and%20Einstein_3.png)

_Image source :kdnuggets  _

![](img%5CData%20Structure%20%2CDatabases%20and%20Einstein_4.png)

# CAP Theorem

__Consistency__  \- A read is guaranteed to return the most recent write for a given client\.

__Availability__  \- A non\-failing node will return a reasonable response within a reasonable amount of time \(no error or timeout\)\.

__Partition Tolerance__  \- The system will continue to function when network partitions occur\.

_credits_  _robertgreiner_  <span style="color:#101820"> _https://robertgreiner\.com/cap\-theorem\-revisited _ </span>  _ _

![](img%5CData%20Structure%20%2CDatabases%20and%20Einstein_5.png)

# CAP vs BASE

Must read on BASE

Brewer :  _[https://ieeexplore\.ieee\.org/document/6133253](https://ieeexplore.ieee.org/document/6133253)_  or  _[https://www\.infoq\.com/articles/cap\-twelve\-years\-later\-how\-the\-rules\-have\-changed/](https://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed/)_

Coda hale :  _[https://codahale\.com/you\-cant\-sacrifice\-partition\-tolerance/](https://codahale.com/you-cant-sacrifice-partition-tolerance/)_

Klepmenn :  _[https://martin\.kleppmann\.com/2015/05/11/please\-stop\-calling\-databases\-cp\-or\-ap\.html](https://martin.kleppmann.com/2015/05/11/please-stop-calling-databases-cp-or-ap.html)_

Greiner :  _[https://robertgreiner\.com/cap\-theorem\-revisited](https://robertgreiner.com/cap-theorem-revisited)_  <span style="color:#101820">  </span>

# Different Definition

A as in CAP ie A with network partition of Data vs 9’s “a” implied by cloud vendors

C as in CAP vs C as in ACID vs C as in DB engine consistency models

Image :  _[https://jepsen\.io/consistency](https://jepsen.io/consistency)_

Read more :  _[https://www\.alexdebrie\.com/posts/database\-consistency/](https://www.alexdebrie.com/posts/database-consistency/)_

_[https://www\.alexdebrie\.com/posts/when\-does\-cap\-theorem\-apply/](https://www.alexdebrie.com/posts/when-does-cap-theorem-apply/)_

![](img%5CData%20Structure%20%2CDatabases%20and%20Einstein_6.png)

# Aviability



* Server availability vs Data availability \( as in CAP theorem\)
* __Data availability __ wins over consistency \.Partition tolerance no more a choice
* Replication in DB:
  * Master Slave replication
  * Master Master replication \( conflicts \,load balancing \,extra resources \)
* Sharding : Data partitioning on some basis in separate servers /nodes \.Adds to complexity
* Denormalization :Duplicate less critical data for read performance \. Now called NoSQL
* Cache : Benefit from local copy for slow chanings data \, leads to refresh/staleness problems
  * DB Cache : Queries \,Rows \,Frequent data
* Sync/Real Time vs Async storage
* Queueing within Dbs \(hidden from us \)


# Consistency



* Every read receives the most recent write or an error
* Weak Consistency : typical network based services eg phone calls \,video cals \, cable tv
* Eventual Consistency : Think facebook updates
  * BASE Theorem
    * Basically available \- the system guarantees availability\.
    * Soft state \- the state of the system may change over time\, even without input\.
    * Eventual consistency \- the system will become consistent over a period of time\,
  * 2 phase commit
* Strong Consistency : ACID as in RDBMS
* Problem of consensus and leader election: PAXOS \,RAft
* Fault Tolerance : Byzantine
* Task Distribution : Zookeeper and Yarn
* Computational consistency : Time clocks
* Read  _[https://cloud\.google\.com/spanner/docs/true\-time\-external\-consistency](https://cloud.google.com/spanner/docs/true-time-external-consistency)_


# Partition Tolerance

The system continues to operate despite network partitions

Coda Hale\, Yammer software engineer:

“Of the CAP theorem’s Consistency\, Availability\, and Partition Tolerance\,  __Partition Tolerance is mandatory in distributed systems__ \. You cannot not choose it\.”

Different data may require different consistency and availability

keep related data close together to assure better performance

No partition ⇒ Latency or consistency loss

# DataModelling

RDBMS

_[https://www\.seas\.upenn\.edu/~zives/03f/cis550/codd\.pdf](https://www.seas.upenn.edu/~zives/03f/cis550/codd.pdf)_

Cassandra

_[https://www\.oreilly\.com/content/cassandra\-data\-modeling/](https://www.oreilly.com/content/cassandra-data-modeling/)_

_[https://tech\.ebayinc\.com/engineering/cassandra\-data\-modeling\-best\-practices\-part\-1/](https://tech.ebayinc.com/engineering/cassandra-data-modeling-best-practices-part-1/)_

Mongo db :

_[https://docs\.mongodb\.com/manual/data\-modeling/](https://docs.mongodb.com/manual/data-modeling/)_

Overall : This one has lots of sublinks

_[https://www\.kdnuggets\.com/2016/07/seven\-steps\-understanding\-nosql\-databases\.html](https://www.kdnuggets.com/2016/07/seven-steps-understanding-nosql-databases.html)_

Credit : stack exchange

![](img%5CData%20Structure%20%2CDatabases%20and%20Einstein_7.png)

# Usage Scenario:Cassandra

Distributed data \{enough partition key\}\{sparse\-wide column\}

Scale linearly \(peer to peer gossip\,It AP of CAP\)

Restricted by keys \(no query by columns like RDBMS\,sec index are for optimizations and not to be confused for where clause facility \)

No ACID \, locks \,transactions

No Joins\-groupby please \( data Model can take care of it in some part\)

Write oriented \(for a reason \!\,time sensitivity \)

Updates are rare \(and are idempotent \)

Lifetime is key feature

Faster reads for primary keys \( remember OLAP\-DW \)\(keys are the gist\)\(columnar storage \)

Counters \(but not that imp \)

Replicated to 3 nodes \, <span style="color:#242729"> triple \(R\,W\,N from dynamo paper \. Vector clocks \.</span>

Hence : Logging \,time series data \,tracking data\,Telemetry

# Usage Scenario:MongoDB



* Document \(json like \) nature
  * Few relations in data hence no joins \!
  * key based search that are faster
  * Aggregated views concept\-embedded data models
  * liberal with data duplication but focused on ref keys \( 1\-1 \,1\-many etc \)
* Retrieval is schema free so less queries are direct and hence fast to process
* Almost ACID \,via 4\.0 transactional guarantees apply
* Rapid changes in table ie collection structure \,flexible schema \,TTL =yes
* Index yes \,but don't rely on too many secondary index
* Sharding\(shard key\)\, replica set   \(primary\-write and secondary\-read\)
* Ootb aggregation \(map\-reduce\,distinct \)
* Larger variery of index \(\_id\,geospatial\,multikey\,hased\,ttl \)
* Raft like \, leader election
* Full text search


![](img%5CData%20Structure%20%2CDatabases%20and%20Einstein_8.png)

# Meet Einstein

Mutable or not ?

What is state ?

Time sensitivity \!

Batch vs Streaming

Eventtime vs process time vs windowing

AWS style data centers

![](img%5CData%20Structure%20%2CDatabases%20and%20Einstein_9.png)

__React : h__  _[ttps://medium\.com/better\-programming/react\-state\-of\-the\-state\-e30e98abdb01](https://medium.com/better-programming/react-state-of-the-state-e30e98abdb01)_  __\,__

__microsevics :__  _[https://garysmicroservices\.wordpress\.com/2016/01/06/event\-logs\-state\-flows\-microservices\-how\-do\-these\-relate/](https://garysmicroservices.wordpress.com/2016/01/06/event-logs-state-flows-microservices-how-do-these-relate/)_  __ __

__ __  _[https://www\.youtube\.com/watch?v=F6I5zquEUsw](https://www.youtube.com/watch?v=F6I5zquEUsw)_  __  __  _[https://www\.youtube\.com/watch?v=6bWBEJBMNG0](https://www.youtube.com/watch?v=6bWBEJBMNG0)_

_[https://www\.oreilly\.com/radar/the\-world\-beyond\-batch\-streaming\-102/](https://www.oreilly.com/radar/the-world-beyond-batch-streaming-102/)_  __  __

Brewer :  _[https://ieeexplore\.ieee\.org/document/6133253](https://ieeexplore.ieee.org/document/6133253)_  or  _[https://www\.infoq\.com/articles/cap\-twelve\-years\-later\-how\-the\-rules\-have\-changed/](https://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed/)_

Greiner :  _[https://robertgreiner\.com/cap\-theorem\-revisited/](https://robertgreiner.com/cap-theorem-revisited/)_

Coda hale :  _[https://codahale\.com/you\-cant\-sacrifice\-partition\-tolerance/](https://codahale.com/you-cant-sacrifice-partition-tolerance/)_

Klepmenn :  _[https://martin\.kleppmann\.com/2015/05/11/please\-stop\-calling\-databases\-cp\-or\-ap\.html](https://martin.kleppmann.com/2015/05/11/please-stop-calling-databases-cp-or-ap.html)_

Debrie :   _[https://www\.alexdebrie\.com/posts/database\-consistency/](https://www.alexdebrie.com/posts/database-consistency/)_   _[https://www\.alexdebrie\.com/posts/when\-does\-cap\-theorem\-apply/](https://www.alexdebrie.com/posts/when-does-cap-theorem-apply/)_

# Further Viewing

_[https://www\.youtube\.com/watch?v=Y6Ev8GIlbxc](https://www.youtube.com/watch?v=Y6Ev8GIlbxc)_

_[https://www\.youtube\.com/watch?v=tpspO9K28PM](https://www.youtube.com/watch?v=tpspO9K28PM)_

_[https://www\.youtube\.com/watch?v=d7nAGI\_NZPk](https://www.youtube.com/watch?v=d7nAGI_NZPk)_

_[https://www\.youtube\.com/watch?v=LAqyTyNUYSY](https://www.youtube.com/watch?v=LAqyTyNUYSY)_

_[http://thesecretlivesofdata\.com/raft/](http://thesecretlivesofdata.com/raft/)_  __ __

_[http://harry\.me/blog/2014/12/27/neat\-algorithms\-paxos/](http://harry.me/blog/2014/12/27/neat-algorithms-paxos/)_  __ or __  _[https://lamport\.azurewebsites\.net/pubs/paxos\-simple\.pdf](https://lamport.azurewebsites.net/pubs/paxos-simple.pdf)_  __  __

_[https://www\.youtube\.com/watch?v=q3ja\_07MFr8](https://www.youtube.com/watch?v=q3ja_07MFr8)_  __ __

_[http://www\.scs\.stanford\.edu/17au\-cs244b](http://www.scs.stanford.edu/17au-cs244b/)_

__https://pdos\.csail\.mit\.edu/6\.824/schedule\.html__  _[/](http://www.scs.stanford.edu/17au-cs244b/)_  __  __

# Further reading

_[https://en\.wikipedia\.org/wiki/Multiversion\_concurrency\_control](https://en.wikipedia.org/wiki/Multiversion_concurrency_control)_

_[https://medium\.com/@rakyll/things\-i\-wished\-more\-developers\-knew\-about\-databases\-2d0178464f78](https://medium.com/@rakyll/things-i-wished-more-developers-knew-about-databases-2d0178464f78)_

_[https://www\.techempower\.com/benchmarks/\#section=data\-r19&hw=ph&test=json](https://www.techempower.com/benchmarks/#section=data-r19&hw=ph&test=json)_

_[https://eng\.uber\.com/postgres\-to\-mysql\-migration](https://eng.uber.com/postgres-to-mysql-migration)_

_[https://guides\.library\.oregonstate\.edu/research\-data\-services/data\-management\-types\-formats](https://guides.library.oregonstate.edu/research-data-services/data-management-types-formats)_

_[https://www\.w3schools\.com/xml/](https://www.w3schools.com/xml/)_    _[https://www\.json\.org/json\-en\.html](https://www.json.org/json-en.html)_

_[https://db\-engines\.com/en/ranking\_categories](https://db-engines.com/en/ranking_categories)_

_[https://www\.kdnuggets\.com/2016/07/seven\-steps\-understanding\-nosql\-databases\.html](https://www.kdnuggets.com/2016/07/seven-steps-understanding-nosql-databases.html)_

_[https://robertgreiner\.com/cap\-theorem\-revisited/](https://robertgreiner.com/cap-theorem-revisited/)_

_[https://web\.mit\.edu/6\.005/www/fa15/classes/09\-immutability/](https://web.mit.edu/6.005/www/fa15/classes/09-immutability/)_

