# Elasticsearch 

Communication with elasticsearch is done by issuing HTTP Requests against the REST API. 
Elasticsearch is started by default in port 9200. To access, you can use whatever tool that best fits your expertise, 
but the examples below is with [Postman](https://www.getpostman.com/) API development environment. 

To confirm that Elasticsearch is started navigate to [localhost](http://localhost:9200)
```javascript
{
    "name": "t9mGYu5",
    "cluster_name": "elasticsearch",
    "cluster_uuid": "xq-6d4QpSDa-kiNE4Ph-Cg",
    "version": {
        "number": "5.5.0",
        "build_hash": "260387d",
        "build_date": "2018-09-14T12:00:05.735Z",
        "build_snapshot": false,
        "lucene_version": "6.6.0"
    },
    "tagline": "You Know, for Search"
}
```

The distribution.virk.dk endpoint _/cvr-permanent/virksomhed/search_ requires authorization. 
Generate a [basic authorization](https://www.getpostman.com/docs/v6/postman/sending_api_requests/authorization) token by navigating to the Authorization tab. Select Basic Auth 
and enter username and password. 

![text](https://github.com/HakimiX/ELKconfiguration/blob/master/images/authorizationLogin.png)

You should now be authorized to make HTTP request to the distribution.virk.dk endpoint _/cvr-permanent/virksomhed/search_.
Elasticsearch provides a JSON-style domain specific language that you can use to execute queries. 
This is refered to as the [Query DSL](https://www.elastic.co/guide/en/elasticsearch/reference/6.4/query-dsl.html). 
Navigate to the Body tab in postman and enter the following query:

![text](https://github.com/HakimiX/ELKconfiguration/blob/master/images/PostRequest.png)

This query uses a company's cvr number to fetch the company's current name. 
Below is the JSON response from distribution.virk.dk endpoint _/cvr-permanent/virksomhed/search_

![text](https://github.com/HakimiX/ELKconfiguration/blob/master/images/PostResponse.png)

If there is no company that meets the search terms, you get the following response. `hits {"total": 0}`
which shows how many documents in total that meets the search terms, in this case none. 

![text](https://github.com/HakimiX/ELKconfiguration/blob/master/images/PostRequestEmpty.png)