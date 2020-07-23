# docker 使用指南

* ```docker ps -a``` <br />
显示所有容器

* ```docker attach ContainerName``` <br />
进入运行的容器

* ```docker exec -it ContainerName bash``` <br />
登录运行中的容器

* ```docker rm -f $(docker ps -f name=xxxx -q)``` <br />
强制销毁所有名字带xxxx字符的容器

* ```docker inspect --format={{.NetworkSettings.Networks.sxsh_default.IPAddress}}{{.Name}} sxsh_erpnext-worker-default_1``` <br />
显示容器参数

* ```docker-compose --project-name nnaammee up -d``` <br />
执行docker项目编排

* ```docker cp ContainerName:filePath locFilePath``` <br />
容器与宿主间复制文件

* ```docker logs ContainerName -f``` <br />
显示容器输出

* ```docker volume ls``` <br />
显示所有存储




