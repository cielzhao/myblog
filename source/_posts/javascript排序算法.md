---
title: javascript排序算法
date: 2018-05-03 23:53:00
tags:
 - javascript
---
- 冒泡排序
``` bash
function bubbleSort(arr) {
	for(var i = 0; i < arr.length - 1; i++) {
		for(var j = 0; j < arr.length - 1 - i; j++) {
			if(arr[j] > arr[j+1]) {
				var temp = arr[j];
				arr[j] = arr[j+1];
				arr[j+1] = temp;
			}
		}
	}
	return arr;
}
var arr = [4, 67, 23, 55, 1];
var a = bubbleSort(arr);
console.log(a);
```
- 快速排序
``` bash
function quickSort(arr) {
	if(arr.length <= 1) {
		return arr;
	}
	var pivotIndex = Math.floor(arr.length / 2);
	var pivot = arr.splice(pivotIndex, 1)[0];
	var leftArr = [];
	var rightArr = [];
	for(var i = 0; i < arr.length; i++) {
		if(arr[i] < arr[pivotIndex]) {
			leftArr.push(arr[i]);
		} else {
			rightArr.push(arr[i]);
		}
	}
	return quickSort(leftArr).concat([pivot], quickSort(rightArr));
}
var arr = [4, 67, 23, 55, 1];
var a = quickSort(arr);
console.log(a);
```
- 选择排序
``` bash
function selectSort(arr) {
	var len = arr.length;
	var minIndex, temp;
	for(var i = 0; i < len; i++) {
		minIndex = i;
		for(var j = i + 1; j < len; j++) {
			if(arr[j] < arr[minIndex]) {
				minIndex = j;
			}
		}
		temp = arr[i];
		arr[i] = arr[minIndex];
		arr[minIndex] = temp;
	}
	return arr;
}
var arr = [4, 67, 23, 55, 1];
var a = selectSort(arr);
console.log(a);
```
- 插入排序
``` bash
function insertSort(arr) {
    for (var i = 1; i < arr.length; i++) {
      var temp = arr[i];
      var j = i - 1;
      while (j >= 0 && arr[j] > temp) {
        arr[j + 1] = arr[j];
         j--;
      }
      arr[j + 1] = temp;
    }
    return arr;
}
var arr = [4, 67, 23, 55, 1];
var a = insertSort(arr);
console.log(a);
```
