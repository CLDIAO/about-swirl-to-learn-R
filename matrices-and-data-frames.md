matrices和data frames都是通过行列来存储表格式数据的数据类型。主要区别是matrices只能存储一种数据类型，而data frames可以包含多种数据类型。

创建一个数据集时，使用":"或者"c()"

length（） 可以表示向量的长度

dim（）  可以告诉我们事物的维度，可以获得或者定义维度（行，列）。向量是没有维度的，

attributes（）  可以查看事物的属性

定义维度后的向量就变成了matrices

class()  可以查看事物的属性

matrix(data = NA, nrow = 1, ncol = 1, byrow = FALSE,dimnames = NULL)  可以创建matrix

