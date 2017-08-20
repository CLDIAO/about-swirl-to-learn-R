matrices和data frames都是通过行列来存储表格式数据的数据类型。主要区别是matrices只能存储一种数据类型，而data frames可以包含多种数据类型。

创建一个数据集时，使用":"或者"c()"

length（） 可以表示向量的长度

dim（）  可以告诉我们事物的维度，可以获得或者定义维度（行，列）。向量是没有维度的，

attributes（）  可以查看事物的属性

定义维度后的向量就变成了matrices

class()  可以查看事物的属性

matrix(data = NA, nrow = 1, ncol = 1, byrow = FALSE,dimnames = NULL)  可以创建matrix

# read.table
Reads a file in table format and creates a data frame from it, with cases corresponding to lines and variables to fields in the file.

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

merge(x, y, by = intersect(names(x), names(y)),
      by.x = by, by.y = by, all = FALSE, all.x = all, all.y = all,
      sort = TRUE, suffixes = c(".x",".y"),
      incomparables = NULL, ...)
* x, y:	
data frames, or objects to be coerced to one.
* by, by.x, by.y:	
specifications of the columns used for merging. 
* all:	
logical; all = L is shorthand for all.x = L and all.y = L, where L is either TRUE or FALSE.
* all.x:	
logical; if TRUE, then extra rows will be added to the output, one for each row in x that has no matching row in y. These rows will have NAs in those columns that are usually filled with values from y. The default is FALSE, so that only rows with data from both x and y are included in the output.
* all.y:	
logical; analogous to all.x.
* sort:	
logical. Should the result be sorted on the by columns?
* suffixes	:
a character vector of length 2 specifying the suffixes to be used for making unique the names of columns in the result which are not used for merging (appearing in by etc).
* incomparables:	
values which cannot be matched. See match. This is intended to be used for merging on one column, so these are incomparable values of that column.
* ...:	
arguments to be passed to or from methods.

# dim()

Retrieve or set the dimension of an object

dim(x) <- value

* x:	
an R object, for example a matrix, array or data frame.
* value:
For the default method, either NULL or a numeric vector, which is coerced to integer (by truncation).

# data.frame()
The function data.frame() creates data frames, tightly coupled collections of variables which share many of the properties of matrices and of lists, used as the fundamental data structure by most of R's modeling software.

data.frame(..., row.names = NULL, check.rows = FALSE,
           check.names = TRUE, fix.empty.names = TRUE,
           stringsAsFactors = default.stringsAsFactors())
           
* ...:	
these arguments are of either the form value or tag = value. Component names are created based on the tag (if present) or the deparsed argument itself.
* row.names:	
NULL or a single integer or character string specifying a column to be used as row names, or a character or integer vector giving the row names for the data frame.
* check.rows:	
if TRUE then the rows are checked for consistency of length and names.
* check.names:	
logical. If TRUE then the names of the variables in the data frame are checked to ensure that they are syntactically valid variable names and are not duplicated. If necessary they are adjusted (by make.names) so that they are.
* fix.empty.names:	
logical indicating if arguments which are “unnamed” (in the sense of not being formally called as someName = arg) get an automatically constructed name or rather name "". Needs to be set to FALSE even when check.names is false if "" names should be kept.
* stringsAsFactors:	
logical: should character vectors be converted to factors? The ‘factory-fresh’ default is TRUE, but this can be changed by setting options(stringsAsFactors = FALSE).

# cbind()
Take a sequence of vector, matrix or data-frame arguments and combine by columns or rows, respectively. These are generic functions with methods for other R classes.

# row/colnames()
Retrieve or set the row or column names of a matrix-like object.

rownames(x, do.NULL = TRUE, prefix = "row")
rownames(x) <- value

colnames(x, do.NULL = TRUE, prefix = "col")
colnames(x) <- value

* x:	
a matrix-like R object, with at least two dimensions for colnames.
* do.NULL:	
logical. If FALSE and names are NULL, names are created.
* prefix：	
for created names.
* value：	
a valid value for that component of dimnames(x). For a matrix or array this is either NULL or a character vector of non-zero length equal to the appropriate dimension.

# gsub
'grep, grepl, regexpr, gregexpr and regexec 'search for matches to argument pattern within each element of a character vector: they differ in the format of and amount of detail in the results.

sub and gsub perform replacement of the first and all matches respectively.

gsub(pattern, replacement, x, ignore.case = FALSE, perl = FALSE,
     fixed = FALSE, useBytes = FALSE)
