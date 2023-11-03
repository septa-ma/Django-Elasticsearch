# Django-Elasticsearch

# 1- What is Elasticsearch?
*** Elasticsearch is a distributed, free and open search and analytics engine for all types of data, including textual, numerical, geospatial, structured, and unstructured. Elasticsearch is the central component of the ELK Stack. ***
*** Its use cases include: ***
- Site search and application search
- Monitoring and visualizing your system metrics
- Security and business analytics
- Logging and log analysis

# 2- What is Elasticsearch used for?
*** Elasticsearch allows you to store, search, and analyze huge volumes of data quickly and in near real-time and give back answers in milliseconds. It’s able to achieve fast search responses because instead of searching the text directly, it searches an index. ***

# 3- Elasticsearch Structure and Concepts:
- Cluster -> is a collection of one or more nodes.
- Node is a single server instance that runs Elasticsearch. While communicating with the cluster, it:
    - Stores and indexes your data
    - Provides search

- Index -> An index is a collection of documents that have somewhat similar characteristics. For example, you can have an index for customer data, another index for a product catalog, and yet another index for order data. An index is identified by a name (that must be all lowercase) and this name is used to refer to the index when performing indexing, search, update, and delete operations against the documents in it.

- Type/Mapping -> a collection of documents sharing a set of common fields present in the same index. For example, an index contains data of a social networking application; there can be a specific type for user profile data, another type for messaging data, and yet another one for comments data.

- Shard -> An index can potentially store a large amount of data that can exceed the hardware limits of a single node. For example, a single index of a billion documents taking up 1TB of disk space may not fit on the disk of a single node or may be too slow to serve search requests from a single node alone. To solve this problem, Elasticsearch provides the ability to subdivide your index into multiple pieces called shards. When you create an index, you can simply define the number of shards that you want. Each shard is in itself a fully-functional and independent "index" that can be hosted on any node in the cluster.
**more info: https://www.techtarget.com/searchoracle/definition/sharding**

- Replica -> is a fail-safe mechanism and basically a copy of your index's shard.

- Document -> a collection of fields defined in the JSON format in a specific manner. Every document belongs to a type and resides inside an index. Every document is associated with a unique identifier, called the UID.

- Field -> Elasticsearch fields can include multiple values of the same type (essentially a list). In SQL, on the other hand, a column can contain exactly one value of the said type.



*** sources: ***
- https://testdriven.io/blog/django-drf-elasticsearch/
- https://medium.com/geekculture/how-to-use-elasticsearch-with-django-ff49fe02b58d
- https://www.elastic.co/guide/en/elasticsearch/reference/6.2/_basic_concepts.html#getting-started-shards-and-replicas
- https://sunscrapers.com/blog/how-to-use-elasticsearch-with-django/
