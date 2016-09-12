 # shortcut
 
 ##1、打开多个窗口

横向切割窗口
:new+窗口名(保存后就是文件名) 
:split+窗口名，也可以简写为:sp+窗口名

纵向切割窗口名
:vsplit+窗口名，也可以简写为：vsp+窗口名
 
    vim -o file1 file2 ...  #水平打开多窗口，
    vim -O file1 file2 ...  #垂直打开多窗口,
    vim -d file1 file2 ...  #垂直打开多窗口,并且进行比较
    vimdiff file1 file2 ..  #等同于上一句
 
##2、关闭多窗口
可以用：q!，也可以使用：close，最后一个窗口不能使用close关闭。使用close只是暂时关闭窗口，其内容还在缓存中，只有使用q!、w!或x才能真能退出。
 关闭窗口
     q  或 close   #关闭当前窗口
     only          #保留当前窗口，关闭其它所有窗口
     qall(qa)          #退出所有窗口
     wall          #保存所有窗口

##3、窗口切换
:ctrl+w+j/k，通过j/k可以上下切换，或者:ctrl+w加上下左右键，还可以通过快速双击ctrl+w依次切换窗口。

##4、窗口大小调整
纵向调整
:ctrl+w + 纵向扩大（行数增加）
:ctrl+w - 纵向缩小 （行数减少）
:res(ize) num  例如：:res 5，显示行数调整为5行
:res(ize)+num 把当前窗口高度增加num行
:res(ize)-num 把当前窗口高度减少num行
横向调整
:vertical res(ize) num 指定当前窗口为num列
:vertical res(ize)+num 把当前窗口增加num列
:vertical res(ize)-num 把当前窗口减少num列

##5、给窗口重命名
:f file

##6、vi打开多文件
vi a b c
:n 跳至下一个文件，也可以直接指定要跳的文件，如:n c，可以直接跳到c文件
:e# 回到刚才编辑的文件

##7、文件浏览
:Ex 开启目录浏览器，可以浏览当前目录下的所有文件，并可以选择
:Sex 水平分割当前窗口，并在一个窗口中开启目录浏览器
:ls 显示当前buffer情况

##8、vi与shell切换
:shell 可以在不关闭vi的情况下切换到shell命令行
:exit 从shell回到vi

##9. 多标签
直接在编辑的时候输入：
vim -p 要编辑的文件名
如vim -p * 就是编辑当前目录的所有文件
多个标签间进行切换时向右切换gt，向左切换用gT
在编辑的时候想增加一个标签就可以:tabnew filename
:tabc       关闭当前的tab
:tabo       关闭所有其他的tab
:tabs       查看所有打开的tab
:tabp      前一个
:tabn      后一个
