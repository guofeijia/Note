在 vs code中新建文件login.js

注意：es6语法支持不好

```javascript
var userName="xxx"
var timeStamp=Date.parse(new Date())
//var timeStamp=(new Date()).getTime()
var jsonData={
    "loginName":userName,
    "loginTime":timeStamp
}
var db=connect('log')
db.login.insert(jsonData)
```

在集成终端中执行 mongo login.js

或者mongo  =>load(login.js)

