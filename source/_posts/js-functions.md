---
title: JS 新特性中那些常用的方法。

date: 2016-12-8 10:53:00

categories:
- 前端

tags:
- JavaScript

toc: true
thumbnail: /images/blogecmascript6.png
banner: /images/blogecmascript6.png

---

ES6,ES7 真的很强，你是时候去学习这些强大的函数了

<!-- more -->

> ES5，ES6中新增的好函数

## Array

### forEach

`forEach` 是Array新方法中最基本的一个，就是遍历，循环。

```js
[1, 2 ,3, 4].forEach(console.log);

//结果
// 1, 0, [1, 2, 3, 4]
// 2, 1, [1, 2, 3, 4]
// 3, 2, [1, 2, 3, 4]
// 4, 3, [1, 2, 3, 4]

```
显而易见，forEach回调支持三个参数 1.遍历的内容。2.数组的索引。 3.这个数组本身

`forEach`除了接受一个回调函数，还可以接受一个可选上下文函数参数（改变回调里的this指向）

`array.forEach(callback,[ thisObject]);`

*使用场景*

1. 数组求和

2. 数组调用某些方法




### map

`map` 映射，使用方法和forEach类似 参数也类似，但是map的callback需要一个返回值，根据返回值会返回一个新的数组

`array.map(callback,[ thisObject]);`

```js

var data = [1, 2, 3, 4];

var arrayOfSquares = data.map(function (item) {
  return item * item;
});

alert(arrayOfSquares); // 1, 4, 9, 16

```
*使用场景*

1. 利用map方法方便获得对象数组中的特定属性值。


### filter

`filter`中文过滤，与map基本相似，callback需要返回一个布尔型值，且只需弱 `==true/false` 。

`array.filter(callback,[ thisObject]);`

*使用场景*

1. 筛选数据时。

### some,every

`some` 意指“某些”，指是否“某些项”合乎条件。与之对应的则是`every`

```js

array.some(callback,[ thisObject]);//只需要数组中有一个值能让callback返回true则some返回true


array.every(callback,[ thisObject]);//数组中有所有值能让callback返回true才能使every返回true

```

*使用场景*

1. 对一些数组进行验证


### indexOf,lastIndexOf

`indexOf`方法在字符串中自古就有，`string.indexOf(searchString, position)`。数组这里的indexOf方法与之类似。

`lastIndexOf` 与indexOf也类似。

```js

array.indexOf(searchElement[, fromIndex])
//返回整数索引值，如果没有匹配（严格匹配），返回-1. fromIndex可选，表示从这个位置开始搜索，若缺省或格式不合要求，使用默认值0
var data = [2, 5, 7, 3, 5];

console.log(data.indexOf(5, "x")); // 1 ("x"被忽略)
console.log(data.indexOf(5, "3")); // 4 (从3号位开始搜索)

console.log(data.indexOf(4)); // -1 (未找到)
console.log(data.indexOf("5")); // -1 (未找到，因为5 !== "5")


array.lastIndexOf(searchElement[, fromIndex])
//lastIndexOf是从字符串的末尾开始查找，而不是从开头。还有一个不同就是fromIndex的默认值是array.length - 1而不是0

```


### reduce，reduceRight

这个函数的意义接近于“迭代”、“递归(recursion)”

```js

array.reduce(callback[, initialValue])

//callback函数接受4个参数：之前值、当前值、索引值以及数组本身。
//initialValue参数可选，表示初始值。
//若指定，则当作最初使用的previous值；
//如果缺省，则使用数组的第一个元素作为previous初始值，同时current往后排一位，相比有initialValue值少一次迭代。

var sum = [1, 2, 3, 4].reduce(function (previous, current, index, array) {
  return previous + current;
});

console.log(sum); // 10


array.reduceRight(callback[, initialValue])

//使用方式和reduce方法相同，区别在于此方法从数组尾部开始。
```

*使用场景*

1. 数组求和

2. 二维数组扁平化
