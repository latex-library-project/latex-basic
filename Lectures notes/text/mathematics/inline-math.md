## Bài học: 

Viết toán học vào trong đoạn văn bản thông thường còn được gọi là **inline math**. 

Để viết toán học ở chế độ **inline math**, ta có thể sử dụng một trong hai lệnh là

+ `$...$` 
+ `\(...\)`

hoặc một môi trường có tên là **math**.  

Ví dụ về việc viết toán học ở chế độ **inline math** với công thức về mối liên hệ cạnh huyền và hai cạnh kề trong tam giác vuông: 

1. Sử dụng kí hiệu $$: 

```tex
\documentclass{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình định lý Pythagoras: $x^2 + y^2 =z^2$

\end{document}
```

2. Sử dụng kí hiệu \(\): 

```tex
\documentclass{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình định lý Pythagoras: \(x^2 + y^2 =z^2\)

\end{document}
```

3. Sử dụng môi trường `math`: 

```tex
\documentclass{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình định lý Pythagoras: 
\begin{math}
x^2 + y^2 = z^2
\end{math}

\end{document}
```

Để có thể viết toán học ở một dòng riêng biệt, ta sẽ chuyển sang bài học [display math](/Lectures%20notes/text/mathematics/display-math.md)