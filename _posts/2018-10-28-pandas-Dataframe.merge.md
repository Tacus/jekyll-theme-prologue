---
title: pandas.DataFrame.merge
date: 2018-10-28 00:00:00 Z
author: tacus
layout: post
---

[官方文档] [1]

>
DataFrame.merge(right, how='inner', on=None, left_on=None, right_on=None, left_index=False, right_index=False, sort=False, suffixes=('_x', '_y'), copy=True, indicator=False, validate=None)[source]
Merge DataFrame objects by performing a database-style join operation by columns or indexes.
If joining columns on columns, the DataFrame indexes will be ignored. Otherwise if joining indexes on indexes or indexes on a column or columns, the index will be passed on.

合并两个dataframe
默认不指定合并列，则会使用二者列的交集,如果不存在会产生异常，如果有，则合并后的DataFrame的列为二者所有列并集除去相同的

1. on：指定dataframe合并的列，需要left、right都含有此列，如果没有则会空。如果要合并的列在left和right中列名不同，则可以分别用left_on和right_on来指定



* 两个dataframe所有的columns都不相同
* 两个dataframe的columns相同，值不同
* 使用on时，其中某个dataframe缺失该column


使用方法:
```
>>> A              >>> B
    lkey value         rkey value
0   foo  1         0   foo  5
1   bar  2         1   bar  6
2   baz  3         2   qux  7
3   foo  4         3   bar  8

A.merge(B, left_on='lkey', right_on='rkey', how='outer')

   lkey  value_x  rkey  value_y
0  foo   1        foo   5
1  foo   4        foo   5
2  bar   2        bar   6
3  bar   2        bar   8
4  baz   3        NaN   NaN
5  NaN   NaN      qux   7
```



[1]: http://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.merge.html  "官方文档"