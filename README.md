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
