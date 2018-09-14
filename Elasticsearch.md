# Elasticsearch 

Communication with elasticsearch is done by issuing HTTP Requests against the REST API. 
Elasticsearch is started by default in port 9200. To access, you can use whatever tool that best fits your expertise, 
but the examples below is with Postman API development environment. 

To confirm that Elasticsearch is started navigate to [localhost](http://localhost:9200)
```javascript
{
    "name": "t9mGYu5",
    "cluster_name": "elasticsearch",
    "cluster_uuid": "xq-6d4QpSDa-kiNE4Ph-Cg",
    "version": {
        "number": "5.5.0",
        "build_hash": "260387d",
        "build_date": "2017-06-30T23:16:05.735Z",
        "build_snapshot": false,
        "lucene_version": "6.6.0"
    },
    "tagline": "You Know, for Search"
}
```