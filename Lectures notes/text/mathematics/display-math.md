## Bài học: 

Viết toán học ở một dòng riêng biệt, thay vì phải ở chung với đoạn văn bản thông thường, còn được gọi là **display math**. 

Để có thể viết toán học ở chế độ **display math**, ta có thể sử dụng một trong hai lệnh là

+ `$$...$$` 
+ `\[...\]`

Ví dụ về việc viết toán học ở chế độ **inline math** với công thức về mối liên hệ cạnh huyền và hai cạnh kề trong tam giác vuông: 

1. Sử dụng kí hiệu `$$...$$`: 

```tex
\documentclass{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình định lý Pythagoras: 
$$x^2 + y^2 =z^2$$

\end{document}
```

2. Sử dụng kí hiệu \(\): 

```tex
\documentclass{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình định lý Pythagoras: 
\[x^2 + y^2 =z^2\]

\end{document}
```

Hai cách viết ở trên cho ta một phương trình được nằm ở một dòng riêng biệt mà không được đánh số thứ tự bên cạnh. Để có thể thêm số thứ tự bên cạnh phương trình khi nằm ở một dòng riêng biệt, ta sẽ sử dụng môi trường **display math**: 

```tex
\documentclass{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình định lý Pythagoras: 
\begin{displaymath}
x^2 + y^2 = z^2
\end{displaymath}

\end{document}
```

Kết quả hiển thị: 

$$
x^2 + y^2 = z^2
$$

Việc thêm số thứ tự bên cạnh phương trình toán học rất có ích trong việc [tham chiếu chéo phương trình](). 