# [js] 简要描述下什么是回调函数并写一个例子出来
## 说法1
- 回调函数
任何一个函数都可以是回调函数，他单纯的就是一个函数

- 高阶函数
有很多说法都是，把函数作为参数传入另一个函数就是回调函数，其实这是错误的，这个应该叫做高阶函数

因为平时见到的大部分回调函数的应用，都是通过高阶函数来完成的

- 回调函数的应用
在jQuery中，回调函数被广泛应用，比如：
```
$("#btn_1").click(function() {
  alert("Btn 1 Clicked");
});
```
### 理解
简单理解，就是满足某个条件的时候去调用一个函数，这个被调用的就是回调函数

## 说法2
- 回调函数是作为其他函数的参数的函数

```
function loggle(msg, cb) {
    setTimeout(function () {
      // cb 是 print 回调函数的引用
      cb(msg);
    }, 1000)
  }

 // 我就是回调函数
  function print (msg) {
    console.log(msg); // Hello
  }

  // 一秒后打印 message
  loggle('Hello', print);
 ```
