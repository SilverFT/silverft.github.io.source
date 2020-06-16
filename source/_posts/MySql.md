---
title: MySql
copyright: true
date: 2019-07-24 22:58:11
tags: 数据库
---









# 概念

* 数据库
  * 数据库（Database）是按照数据结构来组织、存储和管理数据的仓库。
* RDBMS 即关系数据库管理系统(Relational Database Management System)的特点：
  * 1.数据以表格的形式出现
  * 2.每行为各种记录名称
  * 3.每列为记录名称所对应的数据域
  * 4.许多的行和列组成一张表单
  * 5.若干的表单组成database
* RDBMS术语
  * **数据库:** 数据库是一些关联表的集合。
  * **数据表:** 表是数据的矩阵。在一个数据库中的表看起来像一个简单的电子表格。
  * **列:** 一列(数据元素) 包含了相同类型的数据, 例如邮政编码的数据。
  * **行：**一行（=元组，或记录）是一组相关的数据，例如一条用户订阅的数据。
  * **冗余**：存储两倍数据，冗余降低了性能，但提高了数据的安全性。
  * **主键**：主键是唯一的。一个数据表中只能包含一个主键。你可以使用主键来查询数据。
  * **外键：**外键用于关联两个表。
  * **复合键**：复合键（组合键）将多个列作为一个索引键，一般用于复合索引。
  * **索引：**使用索引可快速访问数据库表中的特定信息。索引是对数据库表中一列或多列的值进行排序的一种结构。类似于书籍的目录。
  * **参照完整性:** 参照的完整性要求关系中不允许引用不存在的实体。与实体完整性是关系模型必须满足的完整性约束条件，目的是保证数据的一致性。



# MySql常用命令行

* 连接数据库格式： 
  * mysql -h主机地址 -u用户名 －p用户密码
* 查看数据库：
  * show databases;
* 选择并进入数据库
  * use databasename;
* 查看表
  * show tables;
* 查看表结构
  * desc tablename;
* 查看表数据
  * select * from tablename;	
* where条件语句
  * <!-- 获取年龄在14-18岁之间的学生 -->
    select student_age from pre_student where student_age > 14 and student_age < 18;
* in枚举查询
  * <!-- 查找文章id为1,3,5 -->
    SELECT * FROM pre_article WHERE aid IN (1, 3, 5)
* %模糊查询
  * <!-- 查找姓名里面有张的人 , 张三， 小张张, 大张伟 -->
    SELECT * FROM pre_user WHERE username like "%张%"; // 所有
    SELECT * FROM pre_user WHERE username like "%张"; // 小张张
    SELECT * FROM pre_user WHERE username like "_张%"; // 小张张 大张伟
  * %：代替一个或多个字符
  * _：代替一个字符
* limit限制
  * SELECT * FROM table LIMIT 5; // 直接查条数
  * SELECT * FROM table LIMIT （index, length）; // 以哪个下标开始，共多少条数据。
* order by排序
  * 降序：desc
  * 升序：asc
  * select * from pre_student order by student_age desc
* 插入数据
  * INSERT INTO user (username,password) VALUES ('admin','123456');
* 修改数据(必须指定条件 where，不然全部都会被修改到！)
  * UPDATE user SET username = 'admin1', passwd ='12345678'  WHERE uid = 10
* 删除数据
  * DELETE FROM user WHERE uid = 10
* 



# 配置

* **my.ini** 

  * ```mysql
    [client]
    # 设置mysql客户端默认字符集
    default-character-set=utf8
     
    [mysqld]
    # 设置3306端口
    port = 3306
    # 设置mysql的安装目录
    basedir=C:\\web\\mysql-8.0.11
    # 设置 mysql数据库的数据的存放目录，MySQL 8+ 不需要以下配置，系统自己生成即可，否则有可能报错
    # datadir=C:\\web\\sqldata
    # 允许最大连接数
    max_connections=20
    # 服务端使用的字符集默认为8比特编码的latin1字符集
    character-set-server=utf8
    # 创建新表时将使用的默认存储引擎
    default-storage-engine=INNODB
    ```