### Hadoop Commands
- Send file from local to hadoop: `scp -i ~/spark-cluster.pem ./sparkify_log_small.json hadoop@ec2-54-242-50-219.compute-1.amazonaws.com:~/`
### Spark Commands
- Login spark cluster: `ssh -i ~/spark-cluster.pem hadoop@ec2-54-242-50-219.compute-1.amazonaws.com`
- Find where is spark-submit: which spark-submit
- Submit job to spark cluster: /usr/bin/spark-submit --master yarn ./sparkify_log_small.json
- Convert date time in string to timestamp, 01/Jul/1995:00:00:09 -0400 -> 1995-07-01 04:00:09
```
from pyspark.sql.functions import to_timestamp
from pyspark.sql.types import TimestampType

dfCleanTyped = dfClean.withColumn("timestamp", to_timestamp("date_time", "dd/MMM/yyyy:HH:mm:ssZ").cast(TimestampType()))
```
