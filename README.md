forked from [kiwenlau/hadoop-cluster-docker](https://github.com/kiwenlau/hadoop-cluster-docker)

####修改了:
```
master.xxxx.xx -> master
slave[x].xxx.xx -> slave[x]
以及使用hadoop2.7.0编译
```

添加了hadoop-spark

```
  build时添加
  scala-2.11.7.tgz 以及spark-1.4.1-bin-hadoop2.6.tgz 到 hadoop-spark/files
```

####使用方法
```
  spark-shell --master yarn
```
