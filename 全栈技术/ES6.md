[http://es6.ruanyifeng.com/#docs/intro](http://es6.ruanyifeng.com/#docs/intro)

[http://www.cnblogs.com/huansky/tag/ES6/](http://www.cnblogs.com/huansky/tag/ES6/)

  

【import 几种引入方式】

import echarts from 'echarts'; // 引入第三方插件

import * as tools from './libs/tools'; //导入成组的方法

import {axiosfetch,post} from './util';//需要加花括号 可以一次导入多个也可以一次导入一个

import 'iview/dist/styles/iview.css';//导入 css文件

import name1 from './name1';//导入组件

  

【Es6常用函数】

Object.create(null)

Object.keys()   用于返回对象所有key组成的数组。

Object.getOwnPropertyNames()  用于返回对象所有key组成的数组。

Object.values()  用于返回对象所有value组成的数组  

Object.entries() 方法返回一个给定对象自身可枚举属性的键值对数组  

Object.assign：方法用于对象的合并，将源对象（ source ）的所有可枚举属性，复制到目标对象（ target ）  

Object.is  

Object.groupBy(items, callbackFn)  主要用来处理 分组 相关的操作  

  

Array.from(dataList,(item,i)=>{ }  数组转换

dataList.forEach((item, i) =>{ }  //遍历修改数组 forEach不能return

let key = Object.keys(record); 枚举属性名

for(var key in values){} 遍历对象

for(let item of set.keys()){} 遍历属性名

menuNavnewlist.map((obj, i)=>{ }  遍历输出结构

[...new Set(arr)]  去除数组的重复成员 http://www.cnblogs.com/huansky/p/5680410.html（es6 Set）

  

  

重要的是要理解JavaScript中只有这几个类型:number/boolean/string/undefined/null/object，

并没有什么乱七八糟的Object/Function/Array，它们都只不过是一堆object!

  

instanceof的高级用法我把它概括如下:

1.所有对象和函数 instanceof Object  //true     （因为JS万物皆对象，函数也是对象）

2.所有函数 instanceof Function  //true      （这个很好理解，包括普通函数和构造函数）

3.除Object和Function之外的构造函数 instanceof 自身  //false     （因为构造函数的原型链上只有Function.prototype和Object.prototype而没有它们自身的prototype，这一点很不容易理解！）

  

requirejs作为异步加载工具，

zepto作为简化操作的一个库（类似jquery），

backbone作为MVVM框架，将视图层与模型联系起来，

underscore作为拓展库。

requirejs+angularjs搭配。