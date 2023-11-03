# Django-Elasticsearch

# 1- What is Elasticsearch?
**Elasticsearch is a distributed, free and open search and analytics engine for all types of data, including textual, numerical, geospatial, structured, and unstructured. Elasticsearch is a near real time search platform. What this means is there is a slight latency (normally one second) from the time you index a document until the time it becomes searchable. Elasticsearch is the central component of the ELK Stack. Its use cases include:**
- Site search and application search
- Monitoring and visualizing your system metrics
- Security and business analytics
- Logging and log analysis

# 2- What is Elasticsearch used for?
**Elasticsearch allows you to store, search, and analyze huge volumes of data quickly and in near real-time and give back answers in milliseconds. It’s able to achieve fast search responses because instead of searching the text directly, it searches an index.**

# 3- Elasticsearch Structure and Concepts:
- Cluster -> A cluster is a collection of one or more nodes (servers) that together holds your entire data and provides federated indexing and search capabilities across all nodes. A cluster is identified by a unique name which by default is "elasticsearch". This name is important because a node can only be part of a cluster if the node is set up to join the cluster by its name.

- Node -> A node is a single server that is part of your cluster, stores your data, and participates in the cluster’s indexing and search capabilities. Just like a cluster, a node is identified by a name which by default is a random Universally Unique IDentifier (UUID) that is assigned to the node at startup. You can define any node name you want if you do not want the default. This name is important for administration purposes where you want to identify which servers in your network correspond to which nodes in your Elasticsearch cluster.

- Index -> An index is a collection of documents that have somewhat similar characteristics. For example, you can have an index for customer data, another index for a product catalog, and yet another index for order data. An index is identified by a name (that must be all lowercase) and this name is used to refer to the index when performing indexing, search, update, and delete operations against the documents in it.

- Type/Mapping -> A type used to be a logical category/partition of your index to allow you to store different types of documents in the same index, eg one type for users, another type for blog posts. It is no longer possible to create multiple types in an index, and the whole concept of types will be removed in a later version.

- Shard -> An index can potentially store a large amount of data that can exceed the hardware limits of a single node. For example, a single index of a billion documents taking up 1TB of disk space may not fit on the disk of a single node or may be too slow to serve search requests from a single node alone. To solve this problem, Elasticsearch provides the ability to subdivide your index into multiple pieces called shards. When you create an index, you can simply define the number of shards that you want. Each shard is in itself a fully-functional and independent "index" that can be hosted on any node in the cluster.
**more info: https://www.techtarget.com/searchoracle/definition/sharding**

- Replica -> Is a fail-safe mechanism and basically a copy of your index's shard. In a network/cloud environment where failures can be expected anytime, it is very useful and highly recommended to have a failover mechanism in case a shard/node somehow goes offline or disappears for whatever reason. To this end, Elasticsearch allows you to make one or more copies of your index’s shards into what are called replica shards, or replicas for short.

- Document -> a collection of fields defined in the JSON format in a specific manner. Every document belongs to a type and resides inside an index. Every document is associated with a unique identifier, called the UID.

- Field -> Elasticsearch fields can include multiple values of the same type (essentially a list). In SQL, on the other hand, a column can contain exactly one value of the said type.





**Sources:**
- https://testdriven.io/blog/django-drf-elasticsearch/
- https://medium.com/geekculture/how-to-use-elasticsearch-with-django-ff49fe02b58d
- https://www.elastic.co/guide/en/elasticsearch/reference/6.2/_basic_concepts.html#getting-started-shards-and-replicas
- https://sunscrapers.com/blog/how-to-use-elasticsearch-with-django/
