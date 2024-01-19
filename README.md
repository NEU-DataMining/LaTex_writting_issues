# LaTex_writting_issues
记录论文写作过程中遇到的问题及解决方案，便于查询，提高写作效率。

## 1. 版面

## 2. Table
- 表格宽度超出页面范围问题
  1. 单元格内内容过长
     将列对齐方式替换为m控制
     ```latex
     % 普通居中对齐，内容过长会导致超出页面范围
     \begin{tabular}[ccc]
     \end{tabular}
     %修改为m控制，过长部分会自动换行
     \begin{tabular}[m{0.1}m{0.2}m{0.7}]
     \end{tabular}
     ```
  2. 表格列数过多
     可以使用resizebox控制，需要注意**这种方式会将表格整体缩小，使用时应注意控制字体**
     ```latex
     \begin{table*}
     \centering
     \resizebox{\columnwidth}{!}{
       \begin{tabular}[cccccccccccccccccccccccccccccccc]
       \end{tabular}
     }
     \label{tab:resize}
     \caption{Show for resize.}
     \end{table*}
     ```
