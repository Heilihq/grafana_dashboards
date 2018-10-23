# RabbitMQ Dashboard
Display RabbitMQ monitoring graph based on Influxdb/Telegraf collector stored in Elasticsearch

## Node stats used
Below is list of rows in the dashboard and measurements and fields required by the graphs in the row:
##### Variables
 - `rabbitmq_node`
 - `rabbitmq_queue`
 - `rabbitmq_exchange`

###### Cluster Overview
 - `rabbitmq_node`
 - `rabbitmq_overview`

###### Exchange
 - `rabbitmq_exchange`

###### Queue
 - `rabbitmq_queue`

###### Nodes
 - `rabbitmq_node`

## Sample configuration
```
[[inputs.rabbitmq]]
url = "https://rabbitmq:15672"
username = "$RABBITMQ_USER"
password = "$RABBITMQ_PASSWORD"
```
