# docker-mongodb

```docker pull mongo:4.2.9```

```sh

docker run --name mongo-d1 -v D:\bin\mongodb\data\d1:/etc/mongo -p 27017:27017 -d mongo:4.2.9 --config /etc/mongo/mongod.conf

docker run --name mongo-d1 -it -v /home/taketoto.cn/db/mongo-d1:/data/db -p 27017:27017 -d mongo:4.2.9 --config /etc/mongo/mongod.conf

docker run --name mongo-d1  -p 27017:27017 -v /home/taketoto.cn/db/mongo-d1:/data/db  -d mongo:4.2.9 

$ docker exec -it mongo-d1 mongo admin
# 创建一个名为 admin，密码为 123456 的用户。
>  db.createUser({ user:'admin5jkl',pwd:'kemhl3beq8kaxcea8nbr5c80zod6ypob',roles:[ { role:'userAdminAnyDatabase', db: 'admin'}]});
# 尝试使用上面创建的用户信息进行连接。
> db.auth('admin5jkl', 'kemhl3beq8kaxcea8nbr5c80zod6ypob')


> db.createUser({ user:'gggjs',pwd:'cp06u2tqmyet41yvzj4mugsywkqqj1um',roles:[ { role:'readWrite', db: 'shop1'}]});
> db.auth('gggjs', 'cp06u2tqmyet41yvzj4mugsywkqqj1um')
```



