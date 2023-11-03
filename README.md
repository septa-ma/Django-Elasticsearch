# Django-Elasticsearch

# 1- What is Elasticsearch?
*** Elasticsearch is a distributed, free and open search and analytics engine for all types of data, including textual, numerical, geospatial, structured, and unstructured. Elasticsearch is the central component of the ELK Stack. ***
*** Its use cases include: ***
- Site search and application search
- Monitoring and visualizing your system metrics
- Security and business analytics
- Logging and log analysis

# 2- Elasticsearch Structure and Concepts:
- Cluster is a collection of one or more nodes.
- Node is a single server instance that runs Elasticsearch. While communicating with the cluster, it:
    - Stores and indexes your data
    - Provides search
- Index is used to store the documents in dedicated data structures corresponding to the data type of fields (akin to a SQL database). Each index has one or more shards and replicas.
- Type is a collection of documents, which have something in common (akin to a SQL table).
- Shard is an Apache Lucene index. It's used to split indices and keep large amounts of data manageable.
- Replica is a fail-safe mechanism and basically a copy of your index's shard.
- Document is a basic unit of information that can be indexed (akin to a SQL row). It's expressed in JSON, which is a ubiquitous internet data interchange format.
- Field is the smallest individual unit of data in Elasticsearch (akin to a SQL column).


