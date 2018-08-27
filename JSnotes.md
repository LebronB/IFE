# JS高程笔记
## 引用类型
### 1.Array类型：

 #### 创建:  
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

#### 检测数组：Array.isArray()方法

#### 转换方法：Array.toString() Array.valueOf()

#### 栈方法：
```javascript
var names = ["Elena","Stefan","Damon"];
var count = names.push("Caroline");
alert(count); //返回栈长度3
var item = names.pop();
alert(item); //返回弹出项内容：Caroline
```

#### 队列方法：
```javascript
var names = ["Elena","Stefan","Damon"];
var count = names.push("Caroline");
alert(count); //返回栈长度3
var item = names.shift();
alert(item); //返回弹出项内容：Elena，长度减一
```

#### 重排序方法
```javascript
var values = [0,1,5,10,15];
values.sort(compare); //sort参数必须为比较函数
alert(values); //升序排列

function compare(a,b) {
  return a-b; //升序
}
```

#### 操作方法
concat方法--末尾拼接  
slice方法--Array.slice(1) //从下标为1处开始截取后面部分  
Array.slice(1,4) //从1开始到4结束  

splice方法
```javascript
var names = ["Elena","Stefan","Damon"];
var removed = names.splice(0,2); //删除前两项
removed = names.splice(1,2,"Bonnie","Caroline"); //起始位置，要删除项数，添加的项
```

#### 位置方法
indexof(a,b) //a为要查找的项，b为查找起点位置

#### 归并方法
可用作求和，返回值作为第一个参数传递给下一项
``` javascript
var values = [1,2,3,4,5];
var sum = values.reduce(function(prev,cur,index,array){
  return prev + cur;
});
alert(sum); //15
```
