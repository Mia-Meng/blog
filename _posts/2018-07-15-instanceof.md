---
layout:     post
title:      instanceof
subtitle:   基础及进阶
date:       2018-07-15
author:     Mia
catalog: true
tags:
    - js
    - 原创
---
## 五、instanceof
[toc]
### 1. instanceof是如何判断的?
 * **表达式**: A instanceof B
  * 如果B函数的显式原型对象在A对象的原型链上, 返回true, 否则返回false
 ```javascript
 function Foo() {  }
  var f1 = new Foo()
  console.log(f1 instanceof Foo) // true
  console.log(f1 instanceof Object) // true
  ```
  ![](./images/8.png)
### 2. Function是通过new自己产生的实例
 ```javascript
 console.log(Object instanceof Function) // true
  console.log(Object instanceof Object) // true
  console.log(Function instanceof Function) // true
  console.log(Function instanceof Object) // true
  
  function Foo() {}
  console.log(Object instanceof  Foo) // false
```
### 3. 终极版图解（重点）（记住此图即可）
![最终图，记住此图即可](./images/9.png)