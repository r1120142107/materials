## 登录
```
mongo ${host} --username ${name} --password ${password}
```
## 基本信息
进入 mongodb shell 之后，首先打印出的信息中包含版本
```
MongoDB shell version v3.4.10
connecting to: mongodb://127.0.0.1/27017
MongoDB server version: 3.4.10
```
在 shell 中查看版本
```
db.version()
```

## db

### 创建
```
use ${dbName}
use mydb
```
如果 mydb 不存在，则创建 mydb。然后切换为当前 db。 **use** 命令也常用于切换 db。

### 查看
```
show dbs
```
**mongodb 默认不显示空db**。
### 删除
删除 mydb
```
use mydb
db.dropDatabase()
```

## Collection & Document

mongodb 中没有表这个概念，取而代之的 collection，集合。按照语义来解释，表是一种有数据规范(schema)的概念，而集合中的每个元素，则各有不同。这也是 NOSQL 宣称 schemaless 的由来。

### 创建和删除 collection
创建 collection，仅仅需要指定名称和几个可选参数。并不需要指定类似 rdbms(oracle, mysql) 必须的主键，列名，数据类型，等等。
```
db.createCollection(${name}, ${options})
```

```
db.createCollection('user', { })
db.createCollection('car')
```

options 是可选参数。可用的属性有以下几个：

| Field   | Type | Description |
| ---------|------------|---------|
| capped  | Boolean  | 默认为 false， 设置为 true 时， 必须同时设置 size 字段。表示 collection 的最大容量。如果超出容量，新数据会覆盖老数据|
| autoIndexId  | Boolean  | 默认为 false，设置为 true 时，为每一条数据添加 _id 字段|
| size  | number  | 设置 collection 最大容量（byte）|
| max  | number  | 设置数据最大条数，当设置 capped 为 true 时才能生效|

删除 collection
```javascript
db.collectionName.drop()
```
比如
```javascript
db.user.drop()
db.car.drop()
```

### 插入数据

collection 中的每条数据，称为 document，文档。 document 是一个 javascript 对象，可以使用 javascript 的数据类型作为自己的 property。

```javascript
{
   insert: <collection>,
   documents: [ <document>, <document>, <document>, ... ],
   ordered: <boolean>,
   writeConcern: { <write concern> },
   bypassDocumentValidation: <boolean>
}
```

```javascript
db.runCommand({insert: 'stores', 
  documents:[
    {  
      _id: 1,
      student: "Maya",
      homework: [ 10, 5, 10 ],
      quiz: [ 10, 8 ],
      extraCredit: 0
    },
    {  
      _id: 2,
      student: "Ryan",
      homework: [ 5, 6, 5 ],
      quiz: [ 8, 8 ],
      extraCredit: 8
    }
  ]
 }
)
```

[mongodb insert](https://docs.mongodb.com/manual/reference/command/insert/index.html)

## 导出和导入
### 导出数据
```
mongodump -h ${host} --port ${port} --username ${username} --password ${password} -d ${db name} -o ${export path}
```
collection 的 metadata 保存为 json 文件， document 信息保存为 bson 文件。
### 导入数据
```
mongorestore -d ${db name} ${data path}
```
如果目标 db，collection 不存在，则会自动创建。

# 参考文档
* https://ianlondon.github.io/blog/mongodb-auth/
