# Independent - level III

## Elasticsearch

### What is Elasticsearch?

Elasticsearch is a distributed, open source search and analytics engine for all types of data, including textual, numerical, geospatial, structured, and unstructured. Elasticsearch is built on Apache Lucene and was first released in 2010. Known for its simple REST APIs, distributed nature, speed, and scalability. Commonly referred to as the ELK Stack (after Elasticsearch, Logstash, and Kibana).

### What is Elasticsearch used for?

The speed and scalability of Elasticsearch and its ability to index many types of content mean that it can be used for a number of use cases:

* Application search
* Website search
* Logging and log analytics
* Infrastructure metrics and container monitoring
* Application performance monitoring
* Geospatial data analysis and visualization
* Security analytics
* Business analytics

### 🎓 Learn
  - 📗 [Guide](https://www.elastic.co/guide/index.html)
  - 📙 [Videos and Webinars](https://www.elastic.co/videos)
  - 📙 [Discuss](https://discuss.elastic.co/)
  - 📗 [Mappings](https://www.youtube.com/watch?v=IGQCiAlYiuY)

> **Note:**
> So far all books look *outdated*. If you will find something useful, please let us know.

----

## 📦 Tools

You would need:

- Elasticsearch (hosted by docker or docker-compose)
- Kibana / curl / httpie or any other REST client

### 📦 Setup

```bash
$ curl https://gist.githubusercontent.com/bartlomiejdanek/2413a5f19a1471f78856772cdb5b8130/raw/2967ba039e098fdab78f98ca278158c5be84f462/docker-compose.yml
$ docker-compose up
```

Visit `http://localhost:5601` to get access to Kibana or `http://localhost:9200` to get pure ES.

----

## 📦 Elasticsearch

### 🎓 Learn

Before you start:

1. Make sure that you have a general knownledge about ES (how it works, what is the difference between index and document and so on)
2. Feel free to have a code samples for every single exercise listed below.

### 📝 Katas

- [create index](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/indices-create-index.html)
- [create document](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/docs-index_.html)
- [update document](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/docs-update.html)
- [delete document](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/docs-delete.html)
- [basic search](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/search-search.html)
- [mapping](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/mapping.html)
- [full text queries](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/full-text-queries.html)
- [from and size queries](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/search-request-body.html#request-body-search-from-size)
- [sorting](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/search-request-body.html#request-body-search-sort)
- [search after](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/search-request-body.html#request-body-search-search-after)
- [delete by query](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/docs-delete-by-query.html)
- [update by query](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/docs-update-by-query.html)
- [geo queries](https://www.elastic.co/guide/en/elasticsearch/reference/7.5/geo-queries.html)
