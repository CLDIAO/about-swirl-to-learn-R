matrices和data frames都是通过行列来存储表格式数据的数据类型。主要区别是matrices只能存储一种数据类型，而data frames可以包含多种数据类型。

创建一个数据集时，使用":"或者"c()"

length（） 可以表示向量的长度

dim（）  可以告诉我们事物的维度，可以获得或者定义维度（行，列）。向量是没有维度的，

attributes（）  可以查看事物的属性

定义维度后的向量就变成了matrices

class()  可以查看事物的属性

matrix(data = NA, nrow = 1, ncol = 1, byrow = FALSE,dimnames = NULL)  可以创建matrix

# read.table
read.table(file, header = FALSE, sep = "", quote = "\"'",
           dec = ".", numerals = c("allow.loss", "warn.loss", "no.loss"),
           row.names, col.names, as.is = !stringsAsFactors,
           na.strings = "NA", colClasses = NA, nrows = -1,
           skip = 0, check.names = TRUE, fill = !blank.lines.skip,
           strip.white = FALSE, blank.lines.skip = TRUE,
           comment.char = "#",
           allowEscapes = FALSE, flush = FALSE,
           stringsAsFactors = default.stringsAsFactors(),
           fileEncoding = "", encoding = "unknown", text, skipNul = FALSE)
* file: the name of the file which the data are to be read from.If it does not contain an absolute path, the file name is relative to the current working directory, getwd().
* header: a logical value indicating whether the file contains the names of the variables as its first line.
* sep: the field separator character. Values on each line of the file are separated by this character. If sep = "" (the default for read.table) the separator is ‘white space’, that is one or more spaces, tabs, newlines or carriage returns.
* row.names: a vector of row names.
* col.names: a vector of optional names for the variables.

# merge
Merge two data frames by common columns or row names, or do other versions of database join operations.

merge(x, y, ...)
* x, y	
data frames, or objects to be coerced to one.
* by, by.x, by.y	
specifications of the columns used for merging. See ‘Details’.
* all	
logical; all = L is shorthand for all.x = L and all.y = L, where L is either TRUE or FALSE.
* all.x	
logical; if TRUE, then extra rows will be added to the output, one for each row in x that has no matching row in y. These rows will have NAs in those columns that are usually filled with values from y. The default is FALSE, so that only rows with data from both x and y are included in the output.
* all.y	
logical; analogous to all.x.
* sort	
logical. Should the result be sorted on the by columns?
* suffixes	
a character vector of length 2 specifying the suffixes to be used for making unique the names of columns in the result which are not used for merging (appearing in by etc).
* incomparables	
values which cannot be matched. See match. This is intended to be used for merging on one column, so these are incomparable values of that column.
* ...	
arguments to be passed to or from methods.

