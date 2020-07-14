命令参数: 
-d 后台运行 -p 映射端口 外:内 -e 传递参数 -v 映射目录
```shell script
docker run -d -p 6379:6379 --name=redis redis --requirepass "123456"
docker exec -it redis redis-cli -h localhost -p 6379

docker run -d -p 3306:3306 --name=mysql -e MYSQL_ROOT_PASSWORD="123456" mysql:5.7.20

docker run -it -v /Users/admin/wayne/gopath:/tmp --name=tmp redis /bin/bash
```