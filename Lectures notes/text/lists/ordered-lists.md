## Bài học: 

Để tạo danh sách có thứ tự trong LaTeX, ta sẽ sử dụng môi trường `enumerate`. 

Bên trong môi trường `enumerate`, ta cũng sẽ sử dụng thêm lệnh `item` như bên môi trường `itemize` để liệt kê. 

Ví dụ: (sẽ thay bằng một ví dụ mới sau) 

```tex
\documentclass{article}

\usepackage[utf8]{vietnam}

\begin{document}

Danh sách các danh sách trong \LaTeX : 

\begin{enumerate}
    \item Danh sách không có thứ tự . 
    \item Danh sách có thứ tự . 
\end{enumerate}

\end{document}
```

Kết quả hiển thị: 

Danh sách các danh sách trong LaTeX : 

1. Danh sách không có thứ tự. 
2. Danh sách có thứ tự. 