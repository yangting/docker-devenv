# README

### docker mysql env
#### Based on https://github.com/docker-library/mysql docker image.

1. simple(单机环境)

```
$ docker login --username=aliyun_account registry.cn-hangzhou.aliyuncs.com
$ docker pull mysql:5.7.19
$ docker run -p 3306:3306 [--name vm-mysql] -it -e MYSQL_ROOT_PASSWORD=root_password -v /docker-mysql/simple/my.cnf:/etc/mysql/mysql.cnf -v /docker-mysql/simple/data:/var/lib/mysql -d mysql:5.7.19
```


2. m1s1(读写分离环境)