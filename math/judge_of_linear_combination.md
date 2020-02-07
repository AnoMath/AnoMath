# 線型独立性の判定
なぜ，いくつかのベクトルが線型独立かどうかを判定するとき，それらを列ベクトルとして持つ行列に基本変形を施してその階数が退化しているかどうかを見れば良いのか？
<br>

問：３つのベクトル$$\left( \begin{array}{c} 1 \\ 2 \\ 3 \end{array} \right), \left( \begin{array}{c} 4 \\ 5 \\ 6 \end{array} \right), \left( \begin{array}{c} 7 \\ 8 \\ 9 \end{array} \right)$$が線型独立か，線型従属かを調べよ．

解：$a,b,c\in\mathbb{R}$，$$\mathbf{e_1}=\left( \begin{array}{c} 1 \\ 0 \\ 0 \end{array} \right), \mathbf{e_2}=\left( \begin{array}{c} 0 \\ 1 \\ 0 \end{array} \right), \mathbf{e_3}=\left( \begin{array}{c} 0 \\ 0 \\ 1 \end{array} \right)$$として，
$$\begin{eqnarray*}
a\left( \begin{array}{c} 1 \\ 2 \\ 3 \end{array} \right)+ b\left( \begin{array}{c} 4 \\ 5 \\ 6 \end{array} \right)+ c\left( \begin{array}{c} 7 \\ 8 \\ 9 \end{array} \right) &=& a(\mathbf{e_1}+4\mathbf{e_2}+7\mathbf{e_3})+b(2\mathbf{e_1}+5\mathbf{e_2}+8\mathbf{e_3})+c(3\mathbf{e_1}+6\mathbf{e_2}+9\mathbf{e_3})\\
&=& (a+4b+7c)\mathbf{e_1}+(2a+5b+8c)\mathbf{e_2}+(3a+6b+9c)\mathbf{e_3}
\end{eqnarray*}$$


と表せる．

補題：次の２つの条件は同値．
1. ３つのベクトル$x_1, x_2, x_3\in\mathbb{R}^3$が線型独立である．
2. ３つのベクトル$x_1, x_2, x_3$は，線型空間$<x_1, x_2, x_3>$の基底である．

但し，$$<x_1, x_2, x_3>=\{ ax_1+bx_2+cx_3 \in\mathbb{R}^3 : a,b,c\in\mathbb{R} \}$$である．

これを用いて，

[戻る](home)