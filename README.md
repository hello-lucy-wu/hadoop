### Commands
- Send file from local to hadoop: `scp -i ~/spark-cluster.pem ./sparkify_log_small.json hadoop@ec2-54-242-50-219.compute-1.amazonaws.com:~/`

- Login hadoop: `ssh -i ~/spark-cluster.pem hadoop@ec2-54-242-50-219.compute-1.amazonaws.com`


- Find where is spark: which spark-submit
- Submit job to spark cluster: /usr/bin/spark-submit --master yarn ./sparkify_log_small.json
