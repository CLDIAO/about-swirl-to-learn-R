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
函数.libPaths() 能够显示库所在的位置，函数library()可以显示库中有哪些包。函数search()可以告诉哪些包已经加载并可用。
 
### 包的安装









































+
