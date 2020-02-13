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
### Reruning kafka-producer-job
1. Change values file kafka-producer/values.yaml if needed. (value "messages" is stands for number of messages)
3. helm upgrade kafka-producer kafka-producer/ --force
