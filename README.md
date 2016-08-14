# docker-hive
hive container

Hive uses Hadoop, so this Dockerfile uses [sequenceiq/hadoop-docker](https://github.com/sequenceiq/hadoop-docker) as Hadoop container.


## JDBC connecting test

1. Run hive container

	```
	$ docker run -d -p 10000:10000 --name hive gillax/hive
	```

1. and exec `hiveserver2`

	```
	$ docker exec -d hive hiveserver2
	```

1. run jdbc sample application

	```
	$ ./gradlew runApp
	```
