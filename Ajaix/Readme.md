虽然 AJAX 是经典的前端数据交互方式，但现在它逐渐被以下技术替代：

## Fetch API（现代的异步请求方式，浏览器原生支持）：

fetch("https://api.example.com/data")
.then(response => response.json())
.then(data => console.log(data))
.catch(error => console.error("Error:", error));

## 前端框架的内置功能（如 React、Vue、Angular）：

这些框架提供了更高级的数据请求和状态管理方式，减少了直接使用 AJAX 的复杂性。
