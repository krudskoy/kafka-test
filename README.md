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
1. Delete the job
2. Change values file kafka-producer/values.yaml if needed.
3. helm upgrade kafka-producer kafka-producer/
