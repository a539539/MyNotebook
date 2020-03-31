# MyNotebook
查看数据库版本：未登录前：mysql --version 或 mysql -V（大写的V） 登录后：select version();
登录MySQL：mysql -u 用户名 -p
启动MySQL：net start mysql
关闭MySQL：net stop mysql
database：数据库	table：数据表

DDL（数据定义语言）：create（创建数据库和表）、drop（删除数据库和表）、alter（修改数据库和表结构）

DML（数据操作语言）：insert（向表中插数据）、delete（删除表数据）、select（查询表数据）、update（修改表数据）

DCL（数据控制语言）：commit（确认数据变更）、rollback（取消对数据变更）、crant（赋予用户操作权限）

数据库：
创建数据库：create database databasename;（数据库名）
查看数据库数量：show databases;
导入数据（执行sql脚本）：source 文件路径（直接拖进命令行）

连接数据库：use databasename（数据库名）
查看当前的使用的数据库：select database();
中止正在运行的sql语句：\c或（Ctrl+c）

查看数据库表数量：show tables; 
删除数据库：drop database databasename;（数据库名）


数据表查询：
查看表结构：desc tablesname;（表名）
查看表数据：select * from tablesname;（表名）
查看其他数据库的表：show tables from databasename;（其他数据库名）

查看表创建的语句：show create table tablename;（表名）
查询表中单个字段：select 字段名 from 表名;
查询表中多个字段：select 字段名,字段名 from 表名;
查询同时重命名字段名：select 字段名 as 重命名的字段名 from 表名;

查询单条件语句：select 字段名 from 表名 where 条件;
查询多条件语句1：select 字段名 from 表名 where 条件 and（or） 条件;
查询多条件语句2：select 字段名 from 表名 where 字段名+between+范围;

 _代表占位，%代表任意字段
模糊查询：select 字段名 from 表名 where 表名 like 需要模糊查询的条件（_A% ）;

升序：asc  降序：desc
升序查询：select 字段名 from 表名 order by 需要排序的字段名 asc;
降序查询：select 字段名 from 表名 order by 需要排序的字段名 desc; 
多字段查询：select 字段名1,字段名2 from 表名 order by 需要排序的字段名1 asc, 需要排序的字段名2 asc;（顺序在前先执行）

lower：小写  upper：大写
查询字段并将字段转换为小写（不改变底层数据）：select lower(字段名) from  表名
查询字段并将字段转换为大写（不改变底层数据）：select upper(字段名) from  表名
查询字段数据长度：select length(字段名) from 表名;

生成随机数：select rand();
max：最大值	min：最小值	sum：总和	avg：平均值
查询最大（小）值：select max或min (字段名) from 表名;
查询总和、平均值：select sum或avg (字段名) from 表名;
统计字段中的数据：select count(字段名) from 表名;

去除重复：select distinct 字段名 from 表名;
