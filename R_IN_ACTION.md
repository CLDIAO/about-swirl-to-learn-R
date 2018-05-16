# 介绍 

## 工作空间 （workspace）
 
  工作空间是当前R的工作环境，是R用来读取文件和保存结果的默认目录。使用函数getwd()
来查看当前的工作目录，或使用函数setwd()设定当前的工作目录。调用不再当前工作目录下
的文件时，需要写明完整的路径，并使用引号闭合目录和文件名。

注意路径中使用正斜杠。反斜杠作为转义符。
注意函数setwd()不会创建一个不存在的目录，需要时使用函数dir.create()来创建新目录再指向。
## 输入输出

### 输入
  
  函数source("")可以运行当前工作目录中的一个脚本。
  
### 输出
 
  函数sink("")将输出文件。默认覆盖重复的内容。使用append=TRUE可以将文本追加的文件后，而不是覆盖它。参数split=TRUE可将输出同时发送到屏幕和输出文件中。不加参数的话仅向屏幕返回输出结果。

### 图形输出

pdf("filename.pdf")  PDF文件

win.metafile("filename.wmf")  Windows图元文件

png("filename.png")  PBG文件

jpeg("filename.jpg") JPEG文件

bmp("filename.bmp")  BMP文件

postscript("filename.ps")  PostScript文件

最后使用dev.off()将输出返回到终端。

## 包

### 定义

  包是R函数、数据、预编译代码以一种定义完善的格式组成的集合。计算机上储存包的目录称为库（library）。
函数.libPaths() 能够显示库所在的位置，函数library()可以显示库中有哪些包。命令search()可以告诉哪些包已经加载并可用。
 
### 包的安装

   使用命令install.packages("")来下下载安装包。使用命令update.packages()更新已安装的包。使用命令installed.packages()
将列出安装的包，及它们的版本号、依赖关系等。

### 包的载入

  命令library()即可。

### 包的使用方法
 
  命令help(package=" ")可以输出某个包的简短描述。常见错误有：错误的大小写、引号的使用、函数的括号、错用
转义符、包的载入等。

#### 常见错误

①错误的大小写

②忘记必要的引号

③条用函数忘记使用括号

④路径名中使用\

⑥使用尚未载入的包中的函数

## 批处理
 
  多数情况下，我们交互式使用R：提示符后输入命令，等待输出结果。偶尔，我们想要以一种重复的、标准化的、无人值守的
方式执行某个R程序，例如每月生成一次相同的报告，这是可以在R中编写程序，在批处理模式下执行。
  
  在windows，使用：
  
  "C:\Program Files\R\R-2.13.0\bin\R.exe" CMD BATCH --vanilla --slave "c:\my projects\myscript.R" 
  
  将路径调整为R.exe所在的相应的位置和脚本文件所在的位置。
  
 ## 输出用为输入————结果的重用
 
 T中分析的输出结果可保存并作为进一步分析的输入使用。例如：
 
 lmfit <- lm(mpg~wt, data = mtcars)#在一个对象中保存结果
 
 summary(lmfit)#可查看分析的统计概要
 
 plot(lmfit)#可生成图形
 
## 使用一个新包，代码

help.start()

install.package("vcd")#安装包
 
help(package="vcd")#获取包中可用的函数和数据集

library(vcd)#载入包

help(Arthritis)#数据集的描述

Arthritis#显示数据集的内容

example(Athritis)#运行数据集的示例

q()退出









































+
