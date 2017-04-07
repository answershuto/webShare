在body上绑定一个touchstart事件的空函数即可触发:active状态。

```javascript
document.body.addEventListener('touchstart', function () { });  
```