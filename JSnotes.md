# JS高程笔记
## 引用类型
 1.Array类型：

 创建:  
 方法1
 ```javascript
  var colors = new Array(3); //一个包含三项的数组
  var names = Array('Lance');
  //可省略new，也可直接创建所包含内容的数组
 ```
 方法2: 字面量表示法
 ```javascript
 var colors = ["red","blue","green"];
 ```
Array并非只读，利用length属性可以添加新项，对于中间未定义的项，将返回undefined。（数组最多可包含42949672995个项  - -）  

检测数组：Array.isArray()方法

转换方法：Array.toString() Array.valueOf()
