# JS 对象的基本用法

什么是对象？<br>
&emsp;&emsp;简单说，对象就是一组“键值对”（key-value）的集合，是一种无序的复合数据集合。
## 一. 声明对象的两种用法
方法1.
```JavaScript
let obj = {
    'name': 'Kevon',
    'age': 18
}             // 简单写法
```
方法2.
```JavaScript
let obj = new Object({
    'name': 'Kevon',
    'age': 18
})            // 正规写法
```

## 二. 如何删除对象的属性
&emsp;&emsp;使用`delete obj.xxx`或`delete obj['xxx']`即可删除 obj 中的 xxx 属性
## 三. 如何查看对象的属性
```Js
1. Object.keys(obj)               //查看自身所有属性
2. Object.values(obj)             //查看自身所有属性的值
3. Object.entries(obj)            //查看自身所有属性+属性值
4. console.dir(obj)               //查看自身+共有属性
5. obj.hasOwnProperty(obj)        //判断一个属性是自身属性还是共有属性
```

## 四. 如何修改或增加对象的属性
1.直接赋值
```js
let obj = {
    name: 'Kevon'
}                                             //声明 obj 对象
obj.name = 'frank' 或 obj['name'] = 'frank'   //修改 obj 对象中 'name' 的属性值
```
2.批量赋值
```js
let obj = {
    name: 'Kevon'
}                                             //声明 obj 对象
Object.assign(obj, {
    name: 'frank',
    age: 23,
    gender: 'man'
    })                                        //修改 obj 中 'name' 的属性值，并增加 'age' 和 'gender' 属性 
```
## 五. 如何区分 'name' in obj 和 obj.hasOwnProperty('name') 的区别
&emsp;&emsp;`'xxx' in obj` 用于查看对象里面是否有属性名 `'xxx'`<br>
&emsp;&emsp;`obj.hasOwnProperty('xxx')` 只是判断`'xxx'` 是对象 obj 的自身属性还是共有属性
```js
let obj = {
    name: 'Kevon'
}                                             //声明 obj 对象
'name' in obj   ==> true
obj.hasOwnProperty('name')   ==> true
let common = {
    name: 'frank'
}
obj.__proto__ = common
delete obj.name
'name' in obj   ==> true                      //对象 obj 中存在 'name' 属性名，但不确定是 自身属性 还是 共有属性 。
obj.hasOwnProperty('name')   ==>false         //结果返回 false ，所以能断定 'name' 是共有属性
```
