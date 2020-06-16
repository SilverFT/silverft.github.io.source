---
title: Node.js
copyright: true
date: 2019-08-13 23:46:28
tags: 后端
---

# 基础知识





# TIPS

## NodeJS访问数据库

### mysqljs

```javascript
var mysql = require('mysql');
var connection = mysql.createConnection(mysqlConfig);

connection.connect();

connection.query('SELECT 1 + 1 AS solution',function(error,results,fields){
    if(error)throw error;
    console.log('The solution is:',results[0].solution);
});
connection.end();
```

### egg-mysql

```javascript
const results = yield app.mysql.select('posts',{
    where:{status:'draft'},
    orders:[['create_at','desc'],['id','desc']],
    limit:10,
    offset:0
});
```

### 写SQL实现一个服务端分页

```javascript
// 拼接各种条件
let whereSql = 'where online_version is not null and state <> 1';
if (scope == 'only') {
  whereSql += ' and use_scope like "%' + query.use_scope + '%"';
}
whereSql += handleIn(query) + handleEqual(query) + handleLike(query);

// 取得全部数据条数
const sqlTotal = 'select count(*) as total from component' + whereSql;
const resultTotal = yield this.app.mysql.query(sqlTotal, values);

// 取得当前页数据
let sqlSelect = 'select * from component'
sqlSelect += whereSql;
sqlSelect += ' order by modified_time desc, id desc limit ';
sqlSelect += (pageIndex - 1) * pageSize + ',' + pageSize;
const resultList = yield this.app.mysql.query(sqlSelect, values);

// 返回分页结果
const result = {
  list: resultList,
  total: resultTotal[0].total,
};
return result;
```

那有没有更简洁的方法去操作数据库呢，答案是肯定的社区有很多优秀的orm或sql builder的类库比如objection、sequelize、knexjs、squel等。



## 同步太多容易造成异步回调黑洞

# 面试题

* nodejs导出导入原理

  * ？？

* 

