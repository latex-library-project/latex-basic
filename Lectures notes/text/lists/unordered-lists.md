## Bài học: 

Để tạo danh sách không có thứ tự trong LaTeX, ta sẽ sử dụng môi trường `itemize`. 

Bên trong môi trường `itemize`, ta sẽ sử dụng thêm lệnh `item` để liệt kê. 


Ví dụ: (sẽ thay bằng một ví dụ mới sau) 

```tex
\documentclass{article}

\usepackage[utf8]{vietnam}

\begin{document}

Danh sách các danh sách trong \LaTeX : 

\begin{itemize}
    \item Danh sách không có thứ tự . 
    \item Danh sách có thứ tự . 
\end{itemize}

\end{document}
```

Kết quả hiển thị: 

Danh sách các danh sách trong LaTeX : 

+ Danh sách không có thứ tự. 
+ Danh sách có thứ tự. 