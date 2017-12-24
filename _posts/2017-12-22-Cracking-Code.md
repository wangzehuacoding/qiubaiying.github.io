---
layout:     post                    # 使用的布局（不需要改）
title:      A log to record the cracking the code interview # 标题 
subtitle:   A digest of the book                            #副标题
date:       2017-12-22              # 时间
author:     Zehua Wang                      # 作者
header-img: img/valley.png    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - 面试
---

## Interview
>A log of CC.

2017-12-22

The Interview Process

Algorithm and coding problems form the largest component of the interview process.

Skills: 1.Analytical skills - 是否需要帮助 答案是否最优化 所用时间长短 是否有所权衡
        2.Coding Skills - 能否将想法转化为可实现的代码 是否clean 代码组织是否良好 有没有潜在的错误
        3.Technical knowledge - 计算机科学的基础知识
        4.Experience: Project - important factors
        5.Culture fit/ Commuication Skills 
        
Big(O): Suppose we had an algorithm that took in an array of strings, sorted each string, and then sorted the full
array. What would the runtime be?
Many candidates will reason the following: sorting each string isO(N log N) and we have to do this for
each string,so that'sO(N*N log N).We also have to sort this array,so that's an additionalO(N log N)
work.Therefore,the total runtime isO(N2 log N + N log N),which isjust0(N2 log N).
This is completely incorrect. Did you catch the error?
The problem is that we used N in two different ways. In one case,it's the length of the string (which string?).
And in another case,it's the length of the array.
In your interviews, you can prevent this error by either not using the variable "N" at all,or by only using it
when there is no ambiguity as to what N could represent.
In fact, I wouldn't even use a and b here,or m and n. It's too easy to forget which is which and mix them up.
AnO(a2 ) runtime is completely different from anO(a*b) runtime.
Let's define new terms-and use names that are logical.
Let s be the length of the longest string.
Let a be the length of the array.
Now we can work through this in parts:
• Sorting each string is0(s log s).
• We have to do this for every string (and there are a strings),so that's 0(a*s log s).
Now we have to sort all the strings.There area strings,so you'll may be inclined to say that this takesO ( a
log a) time. This is what most candidates would say. You should also take into account that you need
to compare the strings. Each string comparison takesO(s) time.There areO(a log a) comparisons,
therefore this will take0(a*s log a) time.
If you add up these two parts,you get0(a*s (log a + log s)).
This is it.There is no way to reduce it further.



Author：Zehua Wang
