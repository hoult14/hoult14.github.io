---
layout: article
title:  如何使用Markdown撰写博客
tag: Markdown
page:
  comment: true
aside:
  toc: true
article_header:
  type: overlay
  theme: dark
  background_color: '#203028'
  background_image:
    gradient: 'linear-gradient(135deg, rgba(34, 139, 87 , .4), rgba(139, 34, 139, .4))'
---
Jekyll生成的博客网页采用的语法为Markdown，可以类似于LaTeX一样根据代码生成布局。  
![Image](https://mdg.imgix.net/assets/images/markdown-flowchart.png?auto=format&fit=clip&q=40&w=1080 "markdown工作原理")

<!--more-->
# 一、标题
Markdown语法下，标题通过#来标注，共分为1\~6级标题。注意：#后面需要空格。
~~~markdown
指定标头ID：{#head_id}

# 这是一级标题
## 这是二级标题
### 这是三级标题
#### 这是四级标题
##### 这是五级标题
###### 这是六级标题 {#head_id}
~~~

# 这是一级标题
## 这是二级标题
### 这是三级标题
#### 这是四级标题
##### 这是五级标题
###### 这是六级标题 {#head_id}

# 二、正文
## 2.1 段落
文字中空一行，表示新起一个段落。
~~~markdown
第一段
第二段

第一段

第二段
~~~

第一段
第二段

第一段

第二段
## 2.2 换行
使用\<br>或者两个空格可以起到换行的作用。
~~~markdown
使用<br>换行。

使用(后续跟2个空格)  
换行。
~~~

使用<br>换行。

使用(后续跟2个空格)  
换行。


## 2.3 文字效果
段落的效果包括加粗、倾斜、删除线等，在需要添加效果的文字两端同时使用对应符号。
~~~markdown
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
~~~markdown
>这是一级引用
>>这是二级引用
~~~

>这是一级引用
>>这是二级引用

## 2.4 分隔符

使用不少于3个的-或者\*表示分割线。注意：需要单独一行。
~~~markdown
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
~~~markdown
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


# 三、表格及列表

## 3.1 表格
Markdown和kramdown中的表格方式均如下，第一行为表头，第二行为分隔行，用来定义每一列的对齐格式（:-表示左对齐，-:表示右对齐，:-:表示居中对齐）,从第3行开始为表格的内容部分。空格不必完全对齐，有编译器自动处理。
~~~markdown
| 表头 | 表头 |
|:----:|:---------:|
|第三行  |第三行 |
|第四行  |    第四行 |
~~~

| 表头 | 表头 |
|:----:|:---------:|
|第三行  |第三行 |
|第四行  |    第四行 |

## 3.2 列表
列表分为有序列表和无序列表，有序列表通过"1. "进行排序，注意点后跟空格；无序列表通过"\* ""+ ""- "表示，同样注意空格。  
另外，列表可以进行嵌套使用,有序列表的数字不必顺序排列。
~~~markdown
1. 列表1
	1. 子列表1
	2. 子列表2
2. 列表2
	* 子列表1
		3. 子列表3
		1. 子列表1
	+ 子列表2
3. 列表3
	* 子列表1
		- 子列表1
		+ 子列表2
	+ 子列表2
~~~
1. 列表1
	1. 子列表1
	2. 子列表2
2. 列表2
	* 子列表1
		3. 子列表3
		1. 子列表1
	+ 子列表2
3. 列表3
	* 子列表1
		- 子列表1
		+ 子列表2
	+ 子列表2


# 四、图片和超链接
## 4.1 图片引用
Markdown可以通过链接放置图片，图片的引用格式如下：
~~~markdown
![图名](图片地址 "图片悬浮名称")

图名发现在kramdown种并没有显示。
图片悬浮名称是当鼠标移到图片上时显示的内容，可加可不加，
~~~

例如：
~~~markdown
![Image](https://img2.baidu.com/it/u=3818893070,1837406947&fm=26&fmt=auto&gp=0.jpg "这是标题")
~~~

![Image](https://img2.baidu.com/it/u=3818893070,1837406947&fm=26&fmt=auto&gp=0.jpg "这是标题")

注意到此时图片并未居中，如果想要居中，可以采用如下格式：

~~~html
<div align = center>
<img src="https://img2.baidu.com/it/u=3818893070,1837406947&fm=26&fmt=auto&gp=0.jpg" />
</div>
~~~

<div align = center>
<img src="https://img2.baidu.com/it/u=3818893070,1837406947&fm=26&fmt=auto&gp=0.jpg" />
</div>

## 4.2 图片样式
同时TeXt内置了一些图片的样式，使用格式为：圆形{:.circle}，边框{:.border}，阴影{:.shadow}，或者将它们组合使用：{:.circle.border.shadow}

~~~markdown
![](https://img2.baidu.com/it/u=3818893070,1837406947&fm=26&fmt=auto&gp=0.jpg "这是标题"){:.circle.border.shadow}
~~~
{:.language-markdown}

![](https://img2.baidu.com/it/u=3818893070,1837406947&fm=26&fmt=auto&gp=0.jpg "这是标题"){:.circle.border.shadow}


## 4.3 超链接
超链接的应用格式与图片类似，但没有感叹号!，使用方法有两种：
~~~markdown
[链接名称](链接地址)
<链接地址>
~~~
例如：
~~~markdown
1. 我的[博客](http://hoult14.github.io)
2. 我的GitHub主页：<http://github.com/hoult14>
~~~
1. 我的[博客](http://hoult14.github.io)
2. 我的GitHub主页：<http://github.com/hoult14>



# 五、代码

## 5.1 单行代码
单独一行代码可以用反引号+特定语言样式，如下：

`import numpy as np`{:.language-c}

## 5.2 代码块
有2种方法可以表示代码块：（1）在代码块前使用4个空格或者<kbd>tab</kbd>键，（2）使用三个及其以上的波浪线\~或者反引号\`。  

注意：使用方法2时，要求结束符号的波浪线的数量不小于起始符号的波浪线数量。言外之意，若想在代码块中添加波浪线，需要加长起始符号的数量。
{:.warning}
~~~~~markdown
1.

    代码块1
2.1. 
```c
代码块1
```
2.2. 
~~~c
代码块2
~~~
2.3. 
~~~c
代码块3
~~~
{:.language-c}

以c语言为例
~~~~~~~~
代码块均如下所示。
~~~~
#include<stdio.h>
int main()
{
	return 0;
}
~~~~
方式1：

    #include<stdio.h>
    int main()
    {
    	return 0;
    }

方式2.1：
```c
#include<stdio.h>
int main()
{
	return 0;
}
```
方式2.2
~~~c
#include<stdio.h>
int main()
{
	return 0;
}
~~~
方式2.3
~~~
#include<stdio.h>
int main()
{
	return 0;
}
~~~
{:.language-c}

md




# 六、其他
## 6.1 缩略语 {#Abbreviations}
~~~markdown
使用：
md

定义需要放在markdown文档末尾：
*[md]: markdown
~~~
使用：
md
## 6.2 脚注
~~~
博客主页的网址.[^http]

[^http]: 木水的[博客主页](http://hoult14.github.io)
~~~
博客主页的网址.[^http]

[^http]: 木水的[博客主页](http://hoult14.github.io)



# 七、参考资料



1. [知乎专栏：kramdown基本语法](https://zhuanlan.zhihu.com/p/60838339)  
1. [kramdown语法文档](https://kramdown.gettalong.org/syntax.html)  
1. [Markdown菜鸟教程](https://www.runoob.com/markdown/md-tutorial.html)  

*[md]: markdown
