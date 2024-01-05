## 路由
onLoad 函数参数为 options，其中是页面跳转的 query
```js
// page A
uni.navigateTo({
  url: '/pages/index?foo=aaa&bar=bbb'
})

// page B
onLoad((options) => {
  // options is { foo: 'aaa', bar: 'bbb' }

  // 另一种取法
  const page = getCurrentPages()[0]
  const query = page.$vm.$route.query
  // query is { foo: 'aaa', bar: 'bbb' }
})
```
值都是string类型，建议仅在路由中使用 query 的方式传递少量固定的信息。


npx @dcloudio/uvm@latest