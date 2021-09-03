---
layout: article
title:  2021.08.30日记
tag: Dairy
page:
  comment: true
aside:
  toc: true
# article_header:
#   type: overlay
#   theme: dark
#   background_color: '#203028'
#   background_image:
#     gradient: 'linear-gradient(135deg, rgba(34, 139, 87 , .4), rgba(139, 34, 139, .4))'
---
**今日是今日毕**
# 今天需要学习内容
1. 手写快速选择算法
2. 手写最大堆数据结构

<!--more-->
# A. 快速选择算法
## A.1 对应问题
前k大/小数字，第k大/小数字。

## A.2 算法原理及步骤
举例：  
`输入`{:.info}对于未知顺序的数组`arr{0,2,...,n-1}`  
`输出`{:.success}第k小数字
1. 初始化`l=0`,`r=arr.length-1`,`index=k-1`
2. 对`arr[l~r]`数组进行随机划分，返回索引`q`,满足`arr[l~q-1]<=a[q]<=arr[q+1~r]`
3. 对返回值`q`进行判断：  
若`q=index`,执行步骤4  
若`q>index`,说明第k小数字在`l~q-1`中，更新`r=q-1`,重复步骤2  
若`q<index`,说明第k小数字在`q+1~r`中，更新`l=q+1`,重复步骤2  
4. 输出`arr[index]`

## A.3 伪代码
* `quickSelect()`

	`Input `{:.info}data array`arr{}`,int`left`,int`right`,int`index`  
	`Output`{:.success}data`arr[index]`  
	1. get initial: left=arr.begin, right=arr.end(), index=k // only for the first function call
	2. index_r $\leftarrow$ randomPartition(arr{},left,right)
	3. if index_r $\leq$ index,then: 
			right $\leftarrow$ index_r - 1  
      return quickSelect(arr{},left,right,index)  
	 else if index_r $\leq$ index, then  
      left $\leftarrow$ index_r + 1  
      return quickSelect(arr{},left,right,index)  
   else if index_r $=$ index, then  
      return arr[index]

* `randomPartition()`  
`输入`{:.info}数组`arr{}`,左索引`left`,右索引`right`  
`输出`{:.success}数值`arr[index]`  
* `partition()`  


## A.4 复杂度计算

期望复杂度为`O(n)`,空间复杂度`O(log(n))`



## A.5 C++代码


# B. 最大堆数据结构
## B.1 对应问题
前k大/小数字，第k大/小数字。
## B.2 算法原理及实现

## B.3 伪代码


## B.4 复杂度计算


## B.5 C++代码


