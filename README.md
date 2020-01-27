### Hadoop Commands
- Send file from local to hadoop: `scp -i ~/spark-cluster.pem ./sparkify_log_small.json hadoop@ec2-54-242-50-219.compute-1.amazonaws.com:~/`
### Spark Commands
- Login spark cluster: `ssh -i ~/spark-cluster.pem hadoop@ec2-54-242-50-219.compute-1.amazonaws.com`
- Find where is spark-submit: which spark-submit
- Submit job to spark cluster: /usr/bin/spark-submit --master yarn ./sparkify_log_small.json
