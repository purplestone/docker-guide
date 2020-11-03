# docker-mongodb

```docker pull mongo:4.2.9```

```sh

docker run --name mongo-d1 -v D:\bin\mongodb\data\d1:/etc/mongo -p 27017:27017 -d mongo:4.2.9 mongod --config /etc/mongo/mongod.conf

docker run --name mongo-d1 -it -v /home/yourdir/db/mongo-d1:/data/db -p 27017:27017 -d mongo:4.2.9 mongod --config /etc/mongo/mongod.conf

docker run --name mongo-d1-n  -p 27017:27017 -v /home/yourdir/db/mongo-d1:/data/db  -d mongo:4.2.9 mongod --auth
docker run --name mongo-d1  -p 27017:27017 -v /home/yourdir/db/mongo-d1:/data/db  -d mongo:4.2.9 

$ docker exec -it mongo-d1 mongo admin

> db.createUser({ user:'adminssiiggnn',pwd:'xxxxxxxxxxxxxxxxxxx',roles:[ { role:'userAdminAnyDatabase', db: 'admin'}]});
> db.auth('adminssiiggnn', 'xxxxxxxxxxxxxxxxxxx')

> use shop1
> db.createUser({ user:'gggjs',pwd:'xxxxxxxxxxxxxxxxxxx',roles:[ { role:'readWrite', db: 'shop1'}]});
> db.auth('gggjs', 'xxxxxxxxxxxxxxxxxxx')

/usr/local/mongodb/bin/mongodump -u uusseernaammee -p xxxxxxxxxxxxxxxxxxx -h 127.0.0.1:27017 -d shop1 --out ./bak/shop1_v1


```



