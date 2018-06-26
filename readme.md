

# Grafana Docker 安装与配置

```
    docker pull grafana/grafana
    docker run -d -p 3000:3000 grafana/grafana
```

进入 localhost:3000 即可


# influxdb Docker 安装与配置

```
    docker pull influxdb 
    docker run -d -p   8086:8086 -v $PWD:/var/lib/influxdb  influxdb

    docker ps

    // 进入docker 虚拟机
    docker exec -it [CONTAINER ID] /bin/bash   
    
    // 进入 influxdb 
    influx -precision rfc3339

    // 查看数据库 
    show databases

    // 创建数据库
    create database <数据库名称>

    // 删除数据库
    drop datavase <数据库名>

    // 创建用户 分配权限
    create user <用户名> with password '<密码>'
    grant all privileges on <数据库名> to <用户名>

    // 操作此数据库
    use <数据库名>

    // 查看该数据库内的所有表
    show measurements

    // 查询语句
    select * from <表名>

    // 创建表插入数据
    insert <表名>,hostname=server01 value=442221834240i

    // 删除表 
    drop measurement <表名>

```