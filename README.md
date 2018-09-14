# ELK Stack Configuration

## Elasticsearch

Search and Analytics Engine

1. [Download](https://www.elastic.co/downloads/elasticsearch) Elasticsearch
2. Extract the content of the folder 
3. Open command prompt (cmd) as administrator 
4. Navigate to _/elasticsearch-6.4.0/bin_
5. Start elasticsteach with the following command `elasticsearch`

## Kibana

Server-side data processing pipeline that ingests data from multiple sources

1. [Download](https://www.elastic.co/downloads/kibana) Kibana
2. Extract the content of the folder 
3. Open command prompt (cmd) as administrator 
4. Navigate to _/kibana-6.4.0-windows-x86/bin_
5. Start Kibana with the following command `kibana`
6. Navigate to [localhost](http://localhost:5601)


## Logstash

1. [Download](https://www.elastic.co/downloads/logstash) Logstash
2. Extract the content of the folder 
3. Open command prompt (cmd) as administrator 
4. Prepare logstash.config file
5. Navigate to _/logstash-6.4.0/bin_
6. Run the following command `logstash -f logstash.conf`





