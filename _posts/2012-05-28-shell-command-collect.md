---
layout: post
title: 常用的一些shell命令，不断增量中
categories:
- code
tags:
- shell-command
- 收集
- 常用
---
>都是些基础的小命令,但是, It works 

- 合并文本

{% highlight bash %}
cat file1 file2 >> file3
{% endhighlight %}

- 将文件以若干行分割成多个文件

{% highlight bash %}
split -l 行数 filename
{% endhighlight %}

- 当前目录中文件排序显示，ps:rn从小到大,n从大到小

{% highlight bash %}
du -h *|sort -rn 
{% endhighlight %}

- 统计当前目录中文件数目,包含子目录使用-lR

{% highlight bash %}
ls -l|grep "^-"|wc -l 
{% endhighlight %}

- 去除文件中重复行,并排序.ps:rn从小到大,n从大到小

{% highlight bash %}
sort -n file|uniq
{% endhighlight %}

- 转换图片分辨率

{% highlight bash %}
convert -scale 800x600 infile outfile 
{% endhighlight %}

