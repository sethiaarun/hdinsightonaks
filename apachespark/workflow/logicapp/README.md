The input payload to trigger the workflow:

```
{
  "cluster_dns_name":"<<cluster dns>>.hdinsightaks.net",
  "spark_submit_payload":{
	"className": "org.apache.spark.examples.SparkPi",
        "args": [10],
	  "name": "testjob",
	  "file": "abfs://<<container>>@<<storage account>>.dfs.core.windows.net/spark-examples_2.12-3.3.3.jar"
   }
}
```
