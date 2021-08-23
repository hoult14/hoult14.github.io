---
layout: article
title:  如何使用Markdown撰写博客
tag: Markdown
aside:
  toc: true
---
Jekyll生成的博客网页采用的语法为Markdown，可以类似于LaTeX一样根据代码生成布局。
<!--more-->
# 一、标题
Markdown语法下，标题通过#来标注，共分为1\~6级标题。注意：#后面需要空格。
~~~
# 这是一级标题
## 这是二级标题
### 这是三级标题
#### 这是四级标题
##### 这是五级标题
###### 这是六级标题
~~~
# 这是一级标题
## 这是二级标题
### 这是三级标题
#### 这是四级标题
##### 这是五级标题
###### 这是六级标题

# 二、正文
## 2.1 段落
文字中空一行，表示新起一个段落。
~~~
第一段
第二段

第一段

第二段
~~~
第一段
第二段

第一段

第二段
## 2.2 换行不换段落
使用\<br>或者两个空格可以起到换行的作用。
~~~
使用<br>换行。

使用(后续跟2个空格)  
换行。
~~~
使用<br>换行。

使用(后续跟2个空格)  
换行。


## 2.3 文字效果
段落的效果包括加粗、倾斜、删除线等，在需要添加效果的文字两端同时使用对应符号。
~~~
*这是倾斜的文字*
**这是加粗的文字**
***这是斜体加粗的文字***
~~这是加删除线的文字~~
~~~
*这是倾斜的文字*

**这是加粗的文字**

***这是斜体加粗的文字***

~~这是加删除线的文字~~
## 2.3 引用
使用符号>即可表示引用，多个引号可以进行嵌套使用。注意：引号后面不必有空格。
~~~
>这是一级引用
>>这是二级引用
~~~
>这是一级引用
>>这是二级引用

## 2.4 分割线

使用不少于3个的-或者\*表示分割线。注意：需要单独一行。
~~~
***
---
****
-----
~~~
***
---
****
-----

## 2.5 其他特殊效果
TeXt主题自己提供了一些特殊的文字效果，类型为success、info、warning、error。  
使用格式有2种，一种是换行后使用，可以对整段文字使用；一种是不换行使用，同时前缀用反引号括起来，该效果仅对引号内文字起作用。
同时可以嵌套使用。
~~~
这是Success!
{:.success}
这是info!
{:.info}
这是warning!
{:.warning}
这是error!
{:.error}

这是`success`{:.success} 
这是`info`{:.info} 
这是`warning`{:.warning} 
这是`error`{:.error}

这是Success!的嵌套使用：`success`{:.success} 
{:.success}
~~~
这是Success!
{:.success}
这是info!
{:.info}
这是warning!
{:.warning}
这是error!
{:.error}

这是`success`{:.success} 
这是`info`{:.info} 
这是`warning`{:.warning} 
这是`error`{:.error}

这是Success!的嵌套使用：`success`{:.success}
{:.success} 


# 三、表格






# 四、图片
## 4.1 图片引用
Markdown可以通过链接放置图片，图片的引用格式如下：
~~~
![图名](图片地址 "图片悬浮名称")

图名发现在kramdown种并没有显示。
图片悬浮名称是当鼠标移到图片上时显示的内容，可加可不加，
~~~
例如：
~~~
![Image](https://img2.baidu.com/it/u=3818893070,1837406947&fm=26&fmt=auto&gp=0.jpg "这是标题")
~~~
![Image](https://img2.baidu.com/it/u=3818893070,1837406947&fm=26&fmt=auto&gp=0.jpg "这是标题")
## 4.2 图片样式
同时TeXt内置了一些图片的样式，使用格式为：圆形{:.circle}，边框{:.border}，阴影{:.shadow}，或者将它们组合使用：{:.circle.border.shadow}
~~~
![](https://img2.baidu.com/it/u=3818893070,1837406947&fm=26&fmt=auto&gp=0.jpg "这是标题"){:.circle.border.shadow}
~~~
![](https://img2.baidu.com/it/u=3818893070,1837406947&fm=26&fmt=auto&gp=0.jpg "这是标题"){:.circle.border.shadow}

# 五、代码

	




`import re`{:.language-python}
~~~
#include<stdio.h>
int main()
{
	return 0;
}
~~~
{:.language-c}
