# docker-MySQL

```docker pull mysql:5.7```

```sh
docker run \
  --name=mysql5.7 \
  --env=MYSQL_ROOT_PASSWORD=123456 \
  -p 3357:3306 \
  -d \
  mysql:5.7

docker exec -it mysql5.7 bash
cd /etc/mysql/conf.d
```

Replace ```___YOUR_MYSQL_DIR___``` to loc dir eg:/Users/ggg/db/mysql/t5.7_1

```sh
docker run \
  --name=mysql5.7 \
  --env=MYSQL_ROOT_PASSWORD=123456 \
  -d \
  mysql:5.7

docker cp mysql5.7:/etc/mysql/mysql.cnf ___YOUR_MYSQL_DIR___/my.cnf
docker cp mysql5.7:/etc/mysql/conf.d ___YOUR_MYSQL_DIR___/conf.d
docker cp mysql5.7:/etc/mysql/mysql.conf.d ___YOUR_MYSQL_DIR___/mysql.conf.d
mkdir ___YOUR_MYSQL_DIR___/log
echo '' >> ___YOUR_MYSQL_DIR___/log/error.log

docker rm -f mysql5.7


# edit log-error at ___YOUR_MYSQL_DIR___/mysql.conf.d/mysqld.cnf


docker run \
  --name=mysql5.7 \
  --env=MYSQL_ROOT_PASSWORD=123456 \
  -v ___YOUR_MYSQL_DIR___/data:/var/lib/mysql \
  -v ___YOUR_MYSQL_DIR___/log:/var/log/mysql \
  -v ___YOUR_MYSQL_DIR___/my.cnf:/etc/mysql/my.cnf \
  -v ___YOUR_MYSQL_DIR___/mysql.conf.d:/etc/mysql/mysql.conf.d \
  -v ___YOUR_MYSQL_DIR___/conf.d:/etc/mysql/conf.d \
  -p 3357:3306 \
  -d \
  mysql:5.7

```



