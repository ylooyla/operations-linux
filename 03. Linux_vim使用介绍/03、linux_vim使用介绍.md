Linux vim使用介绍

1、文本编辑器

​	1）建议打开终端来运行

​	2）gedit   kwrite    vim    

​	3）在终端运行如下命令(在图形界面下编辑指定的文件)

​        #gedit   /a/b.txt

​    提示：tab键使用，可以自动补齐命令或文件名

2、路径

​	1）在 Linux 中，简单的理解一个文件的路径，指的就是该文件存放的位置。

​	2）Linux 系统中所有的文件（目录）都被组织成以根目录“/”开始的倒置的树状结构

​         参考图"Linux目录路径树状图.png"



3、vim使用配置

​	1）vi和vim的区别       vim具有颜色显示，支持程序语法 

​	2）/etc/vimrc    ~/.vimrc     //配置文件 

​	3）filename 和 .filename.swp      

​		编辑时所做的修改会临时存入.swp文件，系统死机时且未保存时，

​		下次编辑时，可（R）恢复至修改过程的样子，而不是源文件

4、vi的四种模式

​	1） 一般模式（浏览模式） 

​	2）编辑模式(ESC回到一般 模式)           

​			I   INSERT  a  o  R  进入编辑模式 

​	3）命令行模式(ESC回到一般 模式)           

​			：  /     ?

​	4）可视化模式（v  V   ctrl+v）           	

​			v   字符可视化           V   行可视化           ctrl+v   块可视化



5、常见的快捷命令

​	0     光标所在行行头  

​	$     光标所在行行尾

​	G     到文件最后一行

​	nG   到文件第n行

​	gg     到文件第一行

​	nENTER   光标向下移动n行

​	/word      向下查找word字符串

​	?word     向上查找word字符串

​	n N         重复前一个搜索的动作  下/上

​	:n1,n2   s/word/new/g    n1到n2间word替换成new（无g?）

​	x, X      向后删除和向前删除

​	dd      删除整行

​	ndd   从光标位置开始删除n行    //2dd   d2d   

​	d1G   从第一行开始删除到（包括）光标行

​	d5G    只删第5行

​	dG   删除光标位置到最后一行

​	d$    删除光标位置到该行行尾

​	yy   复制光标所在行   y5y  5yy  y5G  yG  y$

​	P,p   粘贴到光标行前一行/后一行

​	:w    保存数据

​	:wq   保存退出vi

​	:wq!   强制存储后离开vi  (权限相关，强制写入)

​	u   撤消前一操作

​	.（点号）    重复前一操作

​	:w[filename]  将编辑的数据另存为filename

​	:r[filename]   读入filename内容到光标行后面