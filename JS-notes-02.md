# JavaScript 的基本语法

## 一.  表达式和语句
   1. 表达式<br>
  &emsp;&emsp;JavaScript 中表达式和语句的主要区别在于一条语句执行一个动作，一个表达式产生一个值。意思是一个表达式执行后一定会生成一个值，而语句不一定会产生值。语句主要是用来执行动作，程序就是由一系列语句组成。表达式分为基本的表达式（包括基本关键字），还有左值表达式以及运算符。
  ```JavaScript
  // 表达式
  name
  1 + x
  getNames()
  
  // 语句
  var name = 'Fang';
  function getNames() {}
  var foo = getNames() {};
  ```
  2. 语句<br>
   &emsp;&emsp;语句分为声明语句、流程控制语句和其他语句。其中，流程控制语句分为基本流程控制语句、迭代语句、跳转语句和条件语句。
   ```JavaScript
   var a;
   var a = 2;
   var a = 2, b = 3; // 多个变量的初始化
   ```
   * 表达式一般都有值，语句可能有也可能没有
   * 语句一般会改变环境（声明、赋值）
   * 以上两条不是绝对的
   * 注意大小写
***
## 二. 标识符的规则
&emsp;&emsp;标识符（Identifier） 就是名称的专业术语。 JavaScript 标识符包括变量名、函数名、参数名和属性名。 第一个字符必须是字母、下划线（_）或美元符号（$）。 除了第一个字符外，其他位置可以使用 Unicode 字符。 一般建议仅使用 ASCII 编码的字母，不建议使用双字节的字符。 不能与 JavaScript 关键字、保留字重名。
```JavaScript
<script type="text/javascript">
	/*
	标识符
	- 在js中所有可以让我们自由命名的为标识符
	- 例如：变量名、函数名、属性名都标识符
	- 命名一个标识符时需要遵守如下规则：
		1.标识符中可以含有字母、数下划线、$
		2.标识符不能以数字开头
		3.标识符不能是Es中的关键字留字
		4.驼峰命名法
			-首字母小写，每个单词大写，其余小写
			helloWorld
				
	- JS底层保存标识符实际上是utf-8的
	*/		   
</script>
```
***
## 三. if else 语句
### &emsp;&emsp;通常在写代码时，总是需要为不同的决定来执行不同的动作。我们可以在代码中使用条件语句来完成该任务。

&emsp;&emsp;在 JavaScript 中，我们可使用以下条件语句：

* if 语句 - 只有当指定条件为 true 时，使用该语句来执行代码
* if...else 语句 - 当条件为 true 时执行代码，当条件为 false 时执行其他代码
* JavaScript三目运算 - 当条件为true 时执行代码，当条件为 false 时执行其他代码
* if...else if....else 语句- 使用该语句来选择多个代码块之一来执行<br>
## 标准写法：
```JavaScript
if (表达式){
    语句
}else if (表达式) {
    语句
}else {
    语句
}
```
## 次标准写法:
```JavaScript
function (fn) {
    if (表达式) {
        return 表达式
    }
    if (表达式) {
        return 表达式
    }
    return 表达式
}
```
* `{}`在语句中只有一句的时候可以省略，不过不建议这样做
***
## 四. while for 循环语句
### 1. while 循环
```JavaScript
while（表达式）{
    要循环的内容；
    条件控制语句；（如i++等）
}
```
&emsp;&emsp;判断表达式的真假，当表达式为真时，执行完再判断表达式的真假；当表达式为假时，执行后面的语句。
### 2. for 循环
```JavaScript
for (语句 1; 表达式 2; 语句 3)
   {
   循环体
   }
```
1） 先执行语句1<br>
2） 然后判断表达式2<br>
3） 如果为真，执行循环体，然后执行语句3<br>
4） 如果为假，直接退出循环，执行后面的语句<br>
***
## 五. break continue
### 1. break
&emsp;&emsp;用来终止循环，让循环不再往下继续：
```JavaScript
<script>
for(var i = 0; i<=5; i++){
   console.log(i); //输出012345
   if(i === 5){
       break;
       }
}
</script>
```
### 2. continue
&emsp;&emsp;continue 语句用来跳过本次循环，执行下次循环。当遇到 continue 语句时，程序会立即重新检测条件表达式，如果表达式结果为真则开始下次循环，如果表达式结果为假则退出循环。
```JavaScript
for (var i = 0; i < 10; i++) {
    if(i % 2 == 0) {//输出13579
        continue;
    }
    document.write(i + "&nbsp;");
}
```
***
## 六. label
JavaScript 语言允许，语句的前面有标签（label），相当于定位符，用于跳转到程序的任意位置.
```
label:
  语句
```
标签可以是任意的标识符，但不能是保留字，语句部分可以是任意语句。

标签通常与break语句和continue语句配合使用，跳出特定的循环。
```JavaScript
top:
  for (var i = 0; i < 3; i++){
    for (var j = 0; j < 3; j++){
      if (i === 1 && j === 1) break top;
      console.log('i=' + i + ', j=' + j);
    }
  }
// i=0, j=0
// i=0, j=1
// i=0, j=2
// i=1, j=0
```
标签也可以用于跳出代码块.
```JavaScript
foo: {
  console.log(1);
  break foo;
  console.log('本行不会输出');
}
console.log(2);
// 1
// 2
```
上面代码执行到break foo，就会跳出区块。

continue语句也可以与标签配合使用。
```JavaScript
top:
  for (var i = 0; i < 3; i++){
    for (var j = 0; j < 3; j++){
      if (i === 1 && j === 1) continue top;
      console.log('i=' + i + ', j=' + j);
    }
  }
// i=0, j=0
// i=0, j=1
// i=0, j=2
// i=1, j=0
// i=2, j=0
// i=2, j=1
// i=2, j=2
```
&emsp;&emsp;上面代码中，continue命令后面有一个标签名，满足条件时，会跳过当前循环，直接进入下一轮外层循环。如果continue语句后面不使用标签，则只能进入下一轮的内层循环。