# Pi-Spark

* The application launching spark on k8s must have a .kube/config file with the authentication



https://github.com/apache/spark/blob/master/docs/running-on-kubernetes.md


```
/opt/apache-spark/bin/spark-submit \
    --master k8s://https://192.168.0.80:6443\
    --deploy-mode cluster \
    --name spark-pi \
    --class org.apache.spark.examples.SparkPi \
    --conf spark.executor.instances=5 \
    --conf spark.kubernetes.container.image=spark \
    local:///opt/apache-spark/examples/jars/spark-examples_2.11-2.4.4.jar
    
```