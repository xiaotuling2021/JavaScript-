# DOM基础整理

## 1.节点之间的导航

```
var htmlEl = document.documentElement;
var bodyEl = document.body;
var headEl = document.head;
var doctype = document.doctype;
console.log(htmlEl, bodyEl, headEl, doctype);

// 1.获取节点的导航
var bodyEl = document.body;
// 1.1获取body所有的子节点
console.log(bodyEl.childNodes);
// 1.2.前一个节点 previousSibling
// 1.3.后一个节点 nextSibling
// 1.4.节点的父节点 parentNode
// 1.5. 所有的子节点 childNodes
// 1.6. 第一个子节点 firstChild
// 1.7. 最后一个子节点 lastChild
```

## 2.元素之间的导航

```
// 父元素：parentElement
// 前兄弟元素：previousElementSibling
// 后兄弟元素：nextElementSibling
// 子节点元素：children
// 第一个子元素：firstElementChild
// 最后一个子元素：lastElementChild
```

### 3.table元素之间的导航

```
var tableEl = document.body.firstElementChild;

// 通过table元素获取内部的后代元素
console.log(tableEl.tHead, tableEl.tBodies, tableEl.tFoot);
console.log(tableEl.rows);

// 拿到一行元素
var rowEl = tableEl.row[2];
console.log(rowEl.cells[0]);
console.log(rowEl.sectionRowIndex);
console.log(rowEl.rowIndex);
```

## 4.form元素之间的导航

```
// 1.获取form
// var formEl = document.body.firstElementChild;
var formEl = document.forms[0];

// 2.获取form中的子元素
var inputEl1 = formEl.elements[0];
var inputEl2 = formEl.elements.account;

setTimeout(function() {
	console.log(inputEl1.value);
	console.log(inputEl2.value);
}, 5000)
```

