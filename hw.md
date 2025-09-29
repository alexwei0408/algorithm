## 1)Rank the following functions by order of growth. That is, find an arrangement $f_{1},f_{2}..., f_{10}$ of the functions such that $f_{1}= \Omega (f_{2}),f_{2}= \Omega (f_{3}),...,f_{9}= \Omega (f_{10})$. You don’t need to prove.  
sol: $n!>2^{n}>\frac{3}{2}^{n}>n^{2}=4^{lgn}>nlgn>n>lgn>lg^{\star}n>1$

## 2)Indicate, for each pair of $(A,B)$ , whether 𝐴 is $O,o,\Omega,\omega, \Theta$ of B. Assume that $𝑘 \ge 1, \epsilon > 0$, and $𝑐 > 1$ are constants. Write you answer in the for of "yes" or "no".
sol:

## 3)Use Strassen’s algorithm to compute

$$
\begin{pmatrix}
6 &8\\
4 &2
\end{pmatrix}
\begin{pmatrix}
1&7 \\
3&5
\end{pmatrix}
$$

Note that you need to give $A_{11}, A_{12}, A_{21}, A_{22}, \;
B_{11}, B_{12}, B_{21}, B_{22}, \;
S_{1}, \ldots, S_{10}, \;
P_{1}, \ldots, P_{7}, \;
C_{11}, C_{12}, C_{21}, C_{22}.$

sol: Take

$$
\begin{align}
A_{11}&=6,A_{12}&=8,A_{21}&=4,A_{22}&=2; \\
B_{11}&=1,B_{12}&=7,B_{21}&=3,B_{22}&=5; \\
\end{align}
$$

Compute $S_{1,\cdots,S_{10}}$

$$
\begin{align}
S_1  &= B_{12}-B_{22} = 7-5=2, \\
S_2  &= A_{11}+A_{12} = 6+8=14, \\
S_3  &= A_{21}+A_{22} = 4+2=6, \\
S_4  &= B_{21}-B_{11} = 3-1=2, \\
S_5  &= A_{11}+A_{22} = 6+2=8, \\
S_6  &= B_{11}+B_{22} = 1+5=6, \\
S_7  &= A_{12}-A_{22} = 8-2=6, \\
S_8  &= B_{21}+B_{22} = 3+5=8, \\
S_9  &= A_{11}-A_{21} = 6-4=2, \\
S_{10} &= B_{11}+B_{12} = 1+7=8.
\end{align}
$$

Compute $P_{1},\cdots,P{7}$

$$
\begin{align}
P_1 &= A_{11} \cdot S_1 = 6 \cdot 2 = 12, \\
P_2 &= S_2 \cdot B_{22} = 14 \cdot 5 = 70, \\
P_3 &= S_3 \cdot B_{11} = 6 \cdot 1 = 6, \\
P_4 &= A_{22} \cdot S_4 = 2 \cdot 2 = 4, \\
P_5 &= S_5 \cdot S_6 = 8 \cdot 6 = 48, \\
P_6 &= S_7 \cdot S_8 = 6 \cdot 8 = 48, \\
P_7 &= S_9 \cdot S_{10} = 2 \cdot 8 = 16.
\end{align}
$$

Compute $C_{11}, C_{12}, C_{21}, C_{22}$

$$
\begin{align}
C_{11} &= P_5 + P_4 - P_2 + P_6 = 48+4-70+48 = 30, \\
C_{12} &= P_1 + P_2 = 12+70 = 82, \\
C_{21} &= P_3 + P_4 = 6+4 = 10, \\
C_{22} &= P_5 + P_1 - P_3 - P_7 = 48+12-6-16 = 38.
\end{align}
$$

Final answer

$$
\begin{pmatrix}
30&82 \\
10&38
\end{pmatrix}
$$
