---
layout: post
title:  "pandas处理csv数据"
date:   2018-06-23 22:14:54
categories: Notes
tags: Python pandas
---

* content
{:toc}

本文记录了使用pandas处理的过程，及出现的问题




## 1、准备数据
如果你没有数据，可以从tushare获得一个股票、电影票房数据练手（关于[tushare](http://tushare.org/)）
```python     
    import tushare as ts    #导入tushare
    data = ts.get_stock_basics()    #获得所有股票包括股票代码、名字等基本数据
    data.to_csv("stock_basics.csv")    #保存到csv
```
csv中的每列数据为code，name， industry， area......
csv数据结构类似{code:[1000,10001,1002], name:[腾讯,阿里,百度]}
## 2、pandas的使用
### [1]取A第n个数据
```python
    import pandas as pd    #导入pandas
    df = pd.read_csv("stock_basics.csv",sep=",")    #读取csv文件，得到一个表
    print(df["A"][n])    #取A列第n个数据
```
### [2]取A列第n个数据对应的C列的数据

### [3]取A列叫 name的数据
