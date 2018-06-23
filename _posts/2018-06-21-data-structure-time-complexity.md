---
layout: post
title:  "数据结构之时间复杂度例子"
date:   2018-06-21 23:14:54
categories: Notes
tags: C 数据结构
---

* content
{:toc}


## 常见时间复杂度
O(1)、O(n)、O(logn)、O(nlogn)、O(n2)  




### O(1)：
用哈希表的查找,详见 数据结构之哈希表
### O(n)：
while（-_-）
### O(logn)：
二分查找算法以2为底，三分以3为底。
二分查找是在排序后才用的，通过取元素集中最中间的值来与要查找的value比较大小，判断在中间值的左右，然后重复上述步骤。
二分法可以分几类问题 [参考资料](https://www.cnblogs.com/luoxn28/p/5767571.html)
* 没有重复数据时
```c
    while(left <= right) {
        int mid = (left + right) / 2;
        if(array[mid] == key) {
            return mid;
        }
        else if(array[mid] < key) {
            left = mid + 1;
            }else {
                right = mid - 1;
            }
    }
```
* 有重复的数据查第一个
```c
    while (left <= right) {
        int mid = (left + right) / 2;
        if (array[mid] >= key) {
            right = mid - 1;
        }else {
            left = mid + 1;
        }
    }
    if (left < array.length && array[left] == key) {
        return left;
    }
```
* 有重复的数据查最后一个
 ```c
    while (left <= right) {
        int mid = (left + right) / 2;
        if (array[mid] <= key) {
            left = mid + 1;
        }
        else {
            right = mid - 1;
        }
    }
    if (right >= 0 && array[right] == key) {
          return right;
    }
```

### O(nlogn)：
while{二分查找}
### O(n2)：
while{while{ }}

