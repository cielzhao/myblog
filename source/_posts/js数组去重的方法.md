---
title: js数组去重的方法
date: 2018-03-01 23:41:15
tags:
 - javascript
---
- 方法一（利用indexOf判断，有两种方案）
``` bash
//若要ie8以下浏览器支持数组的indexOf方法，先对其进行兼容。
Array.prototype.indexOf = Array.prototype.indexOf || function(val) {
	for(var i = 0; i < this.length; i++) {
		if(this[i] === val) {
			return i;
		}
	}
	return -1;
}
```
1.利用indexOf的返回值判断是否存在
``` bash
//遍历数组，创建一个新数组，利用indexOf判断新数组中是否存在该值，不存在则push到新数组中，最后返回新数组
function arrRemoveRepeat(arr) {
	var newArr = [];
	for(var i = 0; i < arr.length; i++) {
		if(newArr.indexOf(arr[i]) === -1) {
			newArr.push(arr[i]);
		}
	}
	return newArr;
}
var arr = [21, 43, 15, 21, 36]; 
console.log(arrRemoveRepeat(arr));   //[21, 43, 15, 36]
```
2.利用indexOf的返回值判断是否等于索引值
``` bash
//遍历数组，创建一个新数组，利用indexOf判断该值在数组中首次出现的位置是否等于当前索引值，相等则push到新数组中，最后返回新数组
function arrRemoveRepeat(arr) {
	var newArr = [];
	for(var i = 0; i < arr.length; i++) {
		if(arr.indexOf(arr[i]) === i) {
			newArr.push(arr[i]);
		}
	}
	return newArr;
}
var arr = [21, 43, 15, 21, 36]; 
console.log(arrRemoveRepeat(arr));   //[21, 43, 15, 36]
```
- 方法二（对象键值对法）
``` bash
//创建新的对象和数组，遍历传入数组时判断值是否为新对象的键值
function arrRemoveRepeat(arr) {
	var temp = {}, newArr = [], val, type;
	for(var i = 0; i < arr.length; i++) {
		val = arr[i];
		type = typeof val;
		if(!temp[val]) {
			temp[val] = [type];
			newArr.push(val);
		} else if(temp[val].indexOf(type) === -1) {
			temp[val].push(type);
			newArr.push(val);
		}
	}
	return newArr;
}
var arr = [21, 43, 15, 21, 36]; 
console.log(arrRemoveRepeat(arr));   //[21, 43, 15, 36]
```
- 方法三（排序相邻比较法）
``` bash
//排序数组，遍历时只push不与前一值重复的值，需要注意的是这样会改变原数组的顺序
function arrRemoveRepeat(arr) {
	arr.sort(function(a,b){
  	    return a - b;
    });

	var newArr = [arr[0]];
	for(var i = 0; i < arr.length; i++) {
		if(arr[i] !== newArr[newArr.length-1]) {
			newArr.push(arr[i]);
		}
	}
	return newArr;
}
var arr = [21, 43, 15, 21, 36]; 
console.log(arrRemoveRepeat(arr));   //[21, 43, 15, 36]
```
- 方法四（遍历数组法）
``` bash
//创建一个新数组，双层循环遍历数组，外层循环元素，内层循环比较值，若不相同则push进新数组
function arrRemoveRepeat(arr) {
	var newArr = [];
	for(var i = 0; i < arr.length; i++) {
		for(var j = i + 1; j < arr.length; j++) {
			if(arr[i] === arr[j]) {
				j = ++ i;
			}
		}
		newArr.push(arr[i]);
	}
	return newArr;
}
var arr = [21, 43, 15, 21, 36]; 
console.log(arrRemoveRepeat(arr));   //[21, 43, 15, 36]
```
- 方法五（利用ES6的set）
``` bash
//Set数据结构，它类似于数组，其成员的值都是唯一的。利用Array.from将Set结构转换成数组
function arrRemoveRepeat(arr) {
	return Array.from(new Set(arr));
}
var arr = [21, 43, 15, 21, 36]; 
console.log(arrRemoveRepeat(arr));   //[21, 43, 15, 36]
```
以上是js的几种数组去重方法，如果用的是jQuery，可以参考以下方法：
``` bash
//jQuery中的$.inArray() 函数用于在数组中查找指定值，并返回它的索引值（如果没有找到，则返回-1）
function arrRemoveRepeat(arr) {
	var newArr = [];
	$.each(arr, function(i, el){
	  if($.inArray(el, newArr) === -1) {
	  	newArr.push(el);
	  }
	});
	return newArr;
}
var arr = [21, 43, 15, 21, 36]; 
console.log(arrRemoveRepeat(arr));   //[21, 43, 15, 36]
```