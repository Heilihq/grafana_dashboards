# Elasticsearch Dashboard
Display Elasticsearch monitoring graph based on Influxdb/Telegraf collector stored in Elasticsearch

## Node stats used
Below is list of rows in the dashboard and configuration required by the graphs in the row:
##### Node Variable
 - `node_stats: os`

###### Cluster
 - `cluster_health: indices`

###### Shards
 - `cluster_health: indices`

###### System
 - `node_stats: os`
 - `node_stats: fs`

###### Network
 - `node_stats: process`
 - `node_stats: http`
 - `node_stats: transport`

###### Documents and Latencies
 - `node_stats: indices`

###### Caches
 - `node_stats: indices`

###### Throttling
 - `node_stats: indices`

###### JVM
 - `node_stats: jvm`

## Sample configuration
```
[[inputs.elasticsearch]]
servers = ["http://elasticsearch:9200"]
http_timeout = "5s"
local = false

cluster_health = true
cluster_health_level = "indices"

cluster_stats = false
node_stats = ["indices", "os", "jvm", "http", "fs", "process", "transport"]
```
