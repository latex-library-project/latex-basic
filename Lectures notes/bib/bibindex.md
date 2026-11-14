## Bài học: 

### Ôn tập: 

Trước khi học bài này, ta sẽ ôn lại vài kiến thức cơ bản.

Để chèn link, trước tiên ta cần sử dụng package `hyperref`:

```tex
\usepackage{hyperref}
```

Đối với chèn trực tiếp, ta sẽ sử dụng lệnh: 

```tex
\url{}
```

và bên trong dấu ngoặc nhọn đó, là nơi ta sẽ dán (paste) đường link mà ta muốn. 

Đối với chèn gián tiếp, ta sẽ sử dụng lệnh: 

```tex
\href{link}{text}
```

trong đó: 

+ link: là nơi ta sẽ chèn link
+ text: là văn bản sẽ chứa đường link đó. 

### Khởi động: 

Ví dụ cơ bản: 

```tex
\documentclass{article}

\usepackage{hyperref}

\begin{document}

\LaTeX{} \cite{lamport94} is a set of macros built atop \TeX{} \cite{texbook}.

\begin{thebibliography}{9}
\bibitem{texbook}
Donald E. Knuth (1986) \emph{The \TeX{} Book}, Addison-Wesley Professional.

\bibitem{lamport94}
Leslie Lamport (1994) \emph{\LaTeX: a document preparation system}, Addison
Wesley, Massachusetts, 2nd ed.
\end{thebibliography}

\end{document}
```


Nếu số lượng trích dẫn tài liệu tham khảo là 10 

```tex
\begin{thebibliography}{9}

\bibitem{rudin1976}
W. Rudin,
\emph{Principles of Mathematical Analysis},
3rd ed., McGraw-Hill, 1976.

\bibitem{spivak2008}
M. Spivak,
\emph{Calculus},
4th ed., Publish or Perish, 2008.

\bibitem{lang2002}
S. Lang,
\emph{Algebra},
3rd rev. ed., Springer, 2002.

\bibitem{munkres2000}
J. R. Munkres,
\emph{Topology},
2nd ed., Prentice Hall, 2000.

\bibitem{lay2016}
D. C. Lay,
\emph{Linear Algebra and Its Applications},
5th ed., Pearson, 2016.

\bibitem{folland1999}
G. B. Folland,
\emph{Real Analysis: Modern Techniques and Their Applications},
2nd ed., Wiley, 1999.

\bibitem{ahlfors1978}
L. V. Ahlfors,
\emph{Complex Analysis},
3rd ed., McGraw-Hill, 1978.

\bibitem{rotman1995}
J. J. Rotman,
\emph{An Introduction to the Theory of Groups},
4th ed., Springer, 1995.

\bibitem{fulton1969}
W. Fulton,
\emph{Algebraic Curves: An Introduction to Algebraic Geometry},
Addison-Wesley, 1969.

\bibitem{courant1953}
R. Courant, D. Hilbert,
\emph{Methods of Mathematical Physics},
Wiley-Interscience, 1953.

\end{thebibliography}
```

vượt quá số 9 ở trong dấu ngoặc nhọn được viết bên trong môi trường `thebibliography` và bên cạnh lệnh `\begin{thebibliography}`, thì ta có thể thấy rằng nội dung ở tài liệu thứ 10 là cuốn **Methods of Mathematical Physics** ở trong tài liệu sẽ bắt đầu bị lệch. 

Để khắc phục được điều này, ta chỉ cần thay đổi số thứ tự bên trong dấu ngoặc nhọn đấy từ 9 thành 10. 

```tex
\begin{thebibliography}{10}
. . . 
\end{thebibliography}
```

thì lúc này nội dung tài liệu tham khảo thứ 10 sẽ không bị lệch nữa.

Vậy nên, người dùng có thể tính chính xác số lượng tài liệu tham khảo mà mình cần đến để đưa ra con số chính xác. 

Tuy vậy, nếu như người dùng trong trường hợp muốn thêm một số tài liệu tham khảo nữa, lúc này vượt qua số lượng tính toán trước đó, thì sẽ thật phiền phức nếu ta phải cứ thay đổi số bên trong dấu ngoặc nhọn. 

Vậy nên ta có thể tính đến số theo đơn vị chục, trăm. 

Nếu như người dùng có số lượng tài liệu tham khảo bé hơn hoặc bằng 9, ta sẽ để số bên trong dấu ngoặc nhọn như đoạn mã ví dụ trên là 9. 

Còn nếu số lượng tài liệu tham khảo được tính bằng chục, ta sẽ đổi số bên trong dấu ngoặc nhọn lúc này là 99. Lúc này, dù ta có trích thêm 10, 20, 30 tài liệu tham khảo đi chăng nữa, mà vì số lượng ấy vẫn bé hơn 99, nên ta vẫn yên tâm rằng nội dung tài liệu tham khảo hiển thị trong trang tài liệu sẽ không bị lệch.


Để có thể trich dẫn được nhiều tài liệu tham khảo bên trong trang tài liệu, ta sẽ vẫn sử dụng lệnh `\cite{}`, và bên trong dấu ngoặc nhọn, nội dung các trích dẫn tương ứng ở lệnh `\bibitem{}` được ngăn cách bởi dấu phẩy. 

Ví dụ: 

```tex
\cite{rudin1976, spivak2008, lang2002}
```

---

### BibTeX

Thay vì sử dụng thủ công bằng môi trường **thebibliography** như trên, ta sẽ có một cách khác tiện lợi hơn. 

Ví dụ: 

```tex
\documentclass{article}

\usepackage{hyperref}

\begin{document}

\LaTeX{} \cite{latex2e} is a set of macros built atop \TeX{} \cite{texbook}.

\cite{knuth:1984,latex:companion,lesk:1977}

\bibliographystyle{plain} % We choose the "plain" reference style

\bibliography{refs} % Entries are in the refs.bib file

\end{document}
```

---

### Tài liệu tham khảo: 

\[1]: https://www.overleaf.com/learn/latex/Bibliography_management_with_bibtex 

\[2]: https://en.wikibooks.org/wiki/LaTeX/Bibliography_Managements 