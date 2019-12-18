# Pi-Spark

* The application launching spark on k8s must have a .kube/config file with the authentication



https://github.com/apache/spark/blob/master/docs/running-on-kubernetes.md



```
/opt/spark-3.0.0-preview-bin-hadoop2.7/bin/spark-submit     --master k8s://https://192.168.0.80:6443    --deploy-mode cluster     --name spark-pi     --class org.apache.spark.examples.SparkPi     --conf spark.executor.instances=2     --conf spark.kubernetes.container.image=spark:spark-rpi  --executor-memory 1g --driver-memory 1g  local:///opt/spark/examples/jars/spark-examples_2.12-3.0.0.jar 

```