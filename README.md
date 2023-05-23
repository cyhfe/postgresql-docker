# postgresql

datatype: [https://www.postgresql.org/docs/current/datatype.html](https://www.postgresql.org/docs/current/datatype.html)

```bash
# compose
docker-compose -p -d pg up
# 查看 ip
docker inspect <id> | grep IPAddress
# 运行 docker 镜像
docker run --name postgres -e POSTGRES_PASSWORD=admin -d postgres
# 进入 bash 环境
docker exec -it postgres bash
# 切换用户 进入 db server
psql -U postgres

# List of databases
\l

# create database
create database test;

# drop database
drop database tset;
drop table person;

# connect to db
\c test

# create table
create table person(
  id BIGSERIAL NOT NULL PRIMARY KEY,
  name VARCHAR(10) ,
  birth DATE,
);

# insert table
INSERT INTO person (name, birth)
VALUES ('wang', '1988-01-10')

# detail
\d person

# sql
/g

```
