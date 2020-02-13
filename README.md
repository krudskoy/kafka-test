# kafka-test
  
### Update dependencies
```shell
helm dependency update kafka-cluster/
```
  
### Install charts  
```shell
helm install --name=kafka-cluster kafka-cluster/  
helm install --name=kafka-consumer kafka-consumer/  
helm install --name=kafka-producer kafka-producer/
```
### Kafka-consumer
This deployment is used to comsume messages from the certain topic.

| Parameter                                      | Description                                                                                                                                                              | Default                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| `topic`                                               | Kafka Topic                                                                                                                                               | `TEST`                                            |
| `kafka_cluster.host`                                            | Kafka Cluster hostname                                                                                                                                                | `kafka-cluster`                                                            |
| `kafka_cluster.port`                                     | Kafka Cluster port                                                                                                                                              | `9092`                                                     |

### Kafka-producer-job
This job is responsible for producing random messages to the cluster's topic.

| Parameter                                      | Description                                                                                                                                                              | Default                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| `topic`                                               | Kafka Topic                                                                                                                                               | `TEST`                                            |
| `messages`                                            | Number of messages to produce                                                                                                                                                | `5`                                                            |
| `kafka_cluster.host`                                     | Kafka Cluster hostname                                                                                                                                              | `kafka-cluster`                                                     |
| `kafka_cluster.port`                                            | Kafka Cluster port                                                                                                                                                            | `9092`                                                                |

### Kafka-producer-job rerun
1. Change values file.  
2. Upgrade helm release:
```shell
helm upgrade kafka-producer kafka-producer/ --force
```
