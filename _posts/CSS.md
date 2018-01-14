---
layout:     post                    # 使用的布局（不需要改）
title:      CSS RECORD # 标题 
subtitle:   Record what I learn                         #副标题
date:       2018-1-14              # 时间
author:     Zehua Wang                      # 作者
header-img: img/post-bg-2015.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - CSS
---

## CSS 
>This is a record of CSS.

2.2
CSS选择符

上下文选择符 基于祖先或者同胞元素选择一个元素
ID和类选择符 基于id和class属性的值选择元素
属性选择符号 基于属性的有无和特征选择元素

上下文选择符

上下文选择符又叫做后代组合式选择符-选择作为指定祖先元素后代的标签

article p{font-weight:bold;} /*只有article后代的P元素才会应用后面的样式 */

特殊的上下文选择符号

<section>
  <h2>An H2 Heading</h2>
  <p>This is paragraph</p>
  <p>Paragraph 2 has a link</p>
  <a href="#>Link</a>
</section>
子选择符> 标签 1 > 标签 2 section > h2 {font-style:italic;}

紧邻同胞选择符 标签 1 + 标签 2 (标签2必须紧跟在其同胞标签1的后面.) h2 + p{font-variant:small-caps;} 选中第一个P

一般同胞选择符 标签1 ~ 标签2 标签2不一定跟在其同胞标签1的后面 h2 ~ a {color:red;}  最后一个a被选中

通用选择符 * 匹配任何元素 *{color:green;} 导致所有元素 包括文本和边框都会变成绿色 可以构成非子选择符 section * a {font-size:1.3em;} 

section * a{font-size:1.3em;} 任何是section的孙子元素而非子元素的a标签都会被选中 第一个a标签被选中了

ID和类选择符号

类属性

是HTML的class属性,body标签中包含的任何HTML元素都可以添加这个属性. 

<h1 class="specialtext">XXX</h1>
<p>This tag has no class.</p>
<p class="specialtext> </p>

类选择符

.类名 .specialtext {font-style:italic;}

标签带类选择符 

p.specialtext{color:red;} 只选择带specialtext类的段落 p.specialtext span {font-weight:bold;} p.specialtext中间没空格

多类选择符 可以给元素添加多各类

<p class="specialtext featured">Here the span tag <span> may or may not </span> be styled.</p>

选择同时存在这两个类名的元素 .specialtext.featured {font-size:120%;}

ID属性

ID与类的写法类似. 而且表示ID -> #

<p id="specialtext">This is a text.</p>

对应的ID选择符 #specialtext {CSS样式生命}

ID属性也可以用在页内导航的ID

ID也可以用在页内导航链接中 <a href="#bio>Biography</a> 表示链接的目标在当前的页面中 因为不会触发浏览器和加载页面

<h3 id="bio">Biography</h3>

<p>I was born ...</p>

作为目标的ID值前面是没有#的, 就是一个普通的ID值

如果链接的href属性只有一个# 那么点击链接会页面顶部

<a href="">Back to Top</a>

什么时候有用ID,什么时候用类

ID的用途是在页面中唯一的标识一个元素. 

类的目的是标识一组具有相同特征的元素 


属性选择符

属性名选择符- 标签名[属性名]

img[title] {border:2px solid blue;} 会选择下面的带有title属性的HTML img元素 title属性有什么值,无关紧要,只要有这个属性就行.

<img src="XX.jpg" title="yellow" alt="yellow"/>

属性值选择符

标签名[属性名="属性值"] 

img[title="red flower"] {border:4px solid green;}

在图片的title属性为 red flower的情况下, 才会为图片添加边框. 

<img src="img.jpg" title="red flower" alt="red flower" />

伪类

UI 伪类





Author：Zehua Wang
