# jre-with-docker


## build docker image

```bash
docker build . -t scdf
```

## start docker container
Dockerfileのenv変数と異なる場合、下記のようにカスタマイズできる。

```Dockerfile 
docker run --name=spring-cloud-data-flow -d -p 9393:9393 \
-e spring_datasource_url='jdbc:postgresql://xxx.xxx.xxx.xxx:5432/dbname?currentSchema=xxx' \
-e spring_datasource_username='xxx' \
-e spring_datasource_password='xxx' \
scdf
```
