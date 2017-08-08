# Promise-Mongodb

使用 Promise 封装的一个 Node 下的 MongoDB 操作模块

使用方法举例：

```
var mongodb = require('./mongo');
mongodb.init('mongodb://localhost:27017/test');

mongodb.insert('user', {username: "嘿嘿嘿354435243", password: "123456"}).then((data) => {
    console.log(data)
}, (err) => {
    console.log(err)
});

mongodb.update('user', {username: "嘿嘿嘿354435243"}, {$set: {username: "我改了", password: "123456"}}).then((data) => {
    console.log(data)
}, (err) => {
    console.log(err)
});

mongodb.find('user', {username: "嘿嘿嘿"}).then((data) => {
    console.log(data)
}, (err) => {
    console.log(err)
});

mongodb.remove('user', {username: "嘿嘿嘿22222"}).then((data) => {
    console.log(data)
}, (err) => {
    console.log(err)
});
```

