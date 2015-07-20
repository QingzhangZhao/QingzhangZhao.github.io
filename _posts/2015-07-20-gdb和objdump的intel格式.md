---
layout: post
category: disassembly
title: gdb和objdump设置Intel格式
tags: [disassembly，linux]
---
由于我看不习惯ATT（其实我不会），就转换到了Intel

<!--more-->

最近在学习（打发时间）逆向方面的知识

##Objdump支持Intel格式很简单

    $objdump -M intel -d xxx

##gdb中设置Intel
gdb要disassemb必须要在gcc的时候加入`-g`选项。
gdb中设置intel格式

	(gdb)set disassembly-flavor intel

不过上面只对本次运行生效，下次又要再输入一遍很麻烦，机智（偷懒）的我在家目录中的.gdbinit中（没有就自己建一个）加入了以下代码就方便多了。
{% highlight bash%}
set disassembly-flavor intel
{% endhighlight %}


--------------------

	

