# Upload Jar And Run Job


## Upload Jar


- use UI
![image](./image/011_submit_new_job_page.png)

- use curl
```
curl -X POST -H "Expect:" -F "jarfile=@"${jar file path}" http://${vm External IP address}:8081/jars/upload
```

- use postman

![image](./image/012_upload_jar_by_postman.png)

- use scp into VM, check flink-web- full dictionary name first
```
scp -i ${ssh private key path} ${jar file path} ${metadata-username}@${vm External IP address}:/tmp/flink-web-${full dictionary name}/flink-web-upload
```

- in VM, cd to dictionary and rename
```
cd /tmp/flink-web-${full dictionary name}/flink-web-upload
mv ${jar name} ${uuid_v4}_${jar name}
```


## Run Job

```
JAR_ID: ${uuid_v4}_${jar name}
programArgsList: (if you have setting yaml)
```
![image](./image/013_run_job_by_postman.png)



## See Running Jobs

![image](./image/014_running_job.png)
