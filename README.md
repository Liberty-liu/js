<!--### ECMASCRIPT5.1

文章链接        |     文章内容       | 创建日期     |
--------------------|------------------|-----------------------|
 | 对象   |  2018-03-17   |-->
 
## <p align="center">你需要深入了解一下对象</p>
日常开发中，object接触的很多很多，{}，这个都不陌生，对象是一种复合值，它将很多值聚合在了一起，对象除了自有的属性，还会从一个原型（prototype）对象继承属性，对它的常见的用法有创建（create）、设置（set）、查找(query)、删除（delete）、检测（test）、枚举（enumerate）

##1.创建对象
```
1. var obj = {}  //对象直接量
2. var obj1 = new Object() //调用new
3. var obj2 = Object.create(Object.prototype)//创建一个有继承Object.prototype的空对象
```
<h4>1.Object.create(param1, param2)</h4>
<p>该方法会创建一个新的对象,第一个参数是这个对象要继承的原型，第二个可选参数是propertiesObject（）</p>

<br/>

```
var o1 = Object.create({x:1, y:2})//o1继承了属性x和y
```
<img width="200px" src="./img/WX20180317-212132@2x.png">

以上是创建一个名为o1的对象，同时给它的原型上面继承了{x:1, y:2}，这些属性不在对象自身上面。

<br/>

```
var o2 = Object.create(null)//o2不继承任何属性和方法，以及toString()
```
<img width="200px" src="./img/WX20180317-212819@2x.png">

以上是创建一个名为o2的对象，传递null，o2对象不具备任何属性和方法