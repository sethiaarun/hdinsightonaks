## Orchestrate Apache Spark Job on HDInsight on AKS Using Azure Logic App

The sample workflow to submit Apache Spark job on HDinsight on AKS:

<img src="workflow.png">

The input payload to trigger the workflow schema will be as following:
```
{
    "type": "object",
    "properties": {
        "cluster_dns_name": {
            "type": "string"
        },
       "tenantId": {
            "type": "string"
        },
        "spark_submit_payload": {
            "type": "object",
            "properties": {}
        }
    }
}
```
The sample payload is as following:

```
{
  "cluster_dns_name":"<<cluster dns>>.hdinsightaks.net",
  "tenantId":"<<tenantId>>",
  "spark_submit_payload":{
	"className": "org.apache.spark.examples.SparkPi",
        "args": [10],
	  "name": "testjob",
	  "file": "abfs://<<container>>@<<storage account>>.dfs.core.windows.net/spark-examples_2.12-3.3.3.jar"
   }
}
```
