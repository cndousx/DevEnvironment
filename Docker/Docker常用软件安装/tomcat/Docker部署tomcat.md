# Docker 部署 tomcat

## 1. 部署

```shell
docker run -d -p 18080:8080 --name tomcat tomcat:9.0.87-jdk8-corretto-al2
```

## 2.修改 webapps

```shell
cd /usr/local/tomcat/
```

```shell
rm webapps -r
```

```shell
mv webapps.dist/ webapps
```

## 2. 修改时区

```shell
# 进入容器
docker exec -it tomcat /bin/bash
```

```shell
# 在容器内执行
ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

echo "Asia/Shanghai" > /etc/timezone

# 退出容器
exit
```

```shell
# 重启容器
docker restart tomcat

```
