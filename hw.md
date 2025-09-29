## 1)Rank the following functions by order of growth. That is, find an arrangement $f_{1},f_{2}..., f_{10}$ of the functions such that $f_{1}= \Omega (f_{2}),f_{2}= \Omega (f_{3}),...,f_{9}= \Omega (f_{10})$. You don’t need to prove.  
sol: $n!>2^{n}>\frac{3}{2}^{n}>n^{2}=4^{lgn}>nlgn>n>lgn>lg^{\star}n>1$
me
## 2)Indicate, for each pair of $(A,B)$ , whether 𝐴 is $O,o,\Omega,\omega, \Theta$ of B. Assume that $𝑘 \ge 1, \epsilon > 0$, and $𝑐 > 1$ are constants. Write you answer in the for of "yes" or "no".
sol:
| A          | B            | O   | o   | $\Omega$ | $\omega$ | $\Theta$ |
|------------|--------------|-----|-----|----------|----------|----------|
| $lg^{k}n$  | $n^{\epsilon}$ |  yes  |  yes   |      no    |     no     |     no     |
| $n^{k}$    | $c^{n}$      |  yes |  yes   | no | no |     no     |


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

## 4)Use the substitution method to show that $T(n)=T(n-1)+n$ has solution $T(n)=O(n^{2})$.  
sol: Suppose that $T(n)<=n^{2}$, for some constant $c>0$, for all $n>n_{0}-(\star)$. By indution on n, when n=2, $T(2)=T(1)+2=3<=4c$, which implies that $c>=\frac{3}{4}>0$, $(\star)$ is true. Assume $(\star)$ hold for $2,...,n-1$. Then 

$$ 
\begin{align}
T(n) &= T(n-1)+ n \\ 
&\le c(n-1)^{2} + n \\ 
&=cn^{2}-2cn+(c+n) \\ 
\end{align} 
$$

Since for all $c \ge 1$, we have $T(n) \le cn^{2},$ for some n is larger. Then $(\star)$ holds for all $n \in \mathbb{N}.$

## 5) i)Sketch the recursion tree for $T(n)=3T(n-1)+n$ and ii)guess a good asymptotic upper bound on its solution; you don't need to verify your answer in (ii).  
sol:  
i)  <img width="900" height="300" alt="image" src="https://github.com/user-attachments/assets/fa666c01-ec69-405a-b730-dfef672c9738" />

ii) $O(3^{n})$.  

## 6)Use the master method to derive asymptotic tight bound for $T(n)=2T(\frac{n}{4})+\sqrt{n}.$
sol: Take $a=2,b=4$, and we have $n^{lg_{4}(2)}=\sqrt{n}$. Let $k=0$. Then $f(n)=\Omega(\sqrt{n}lg^{k}n)=\Omega(\sqrt{n})$.By master method of case 2, we get $T(n)=\Theta(\sqrt{n}lg(n))$.

## 7）Use the master method to derive asymptotic tight bound for $T(n)=2T(\frac{n}{4})+n$.  
sol: Take $a=2,b=4$, we have watershed function $n^{lg_{4}}2=n^{\frac{1}{2}}$. Let $\epsilon =0.1, c=\frac{3}{4}$. 
Then $f(n)=\Omega(n^{lg_{4}(2)+\epsilon})$, and $af(\frac{n}{b})=2f(\frac{n}{4})=\frac{n}{2} \lt \frac{3}{4}n=cf(n).$ Therefore, by master method of case 3, $T(n)= \Theta(n)$

## 8)Draw the decision tree for insertion sort operating on four elements.  
sol:<img width="900" height="450" alt="image" src="https://github.com/user-attachments/assets/36a25a41-444b-4372-8c0a-16e18bdc0b98" />


## 9)In the algorithm SELECT, the input are divided into groups of 5. 
i) Show that the algorithm runs in linear time if the input are divided into groups of 7 instead of 5.   
ii) Show that the algorithm does not run in linear time if the input are divided into groups of 3.

i)   
~Partition the n elements into $\lceil \frac{n}{7} \rceil$ groups of 7 elemetnts, and at most one group made of the remaining n mod 5 elements.--(i)  
~Find the median of each of the $\lceil \frac{n}{7} \rceil$ groups.---(ii)  
~Use algorithm SELECT recursively to find the median x of the $\lceil \frac{n}{7} \rceil$, and it will give us median of medians, we call it 'p'.---(iii)  
~Step(iii) make sure that exits $\frac{n}{14} \text{ median} \ge p$ and for each group there extis four elements $\ge$ it medians $\ge p$. Thus we have $\frac{2n}{7} \ge p$, and for the worst case, have $\frac{5n}{7}$ elements need to do recursive after partition.---(iv)  

Therefore, step(i),(ii) take $O(n)$ times, and step(iii) takes $T(\lceil \frac{n}{7} \rceil)$, and step(iv) takes $T(\frac{5n}{7})$ times.
Hence, we conclude the recursive $T(n)=T(\lceil \frac{n}{7} \rceil)+T(\frac{5n}{7})+O(n)$.  
Now, we want to show $T(n)=O(n)$. Guess $T(n) \le cn$ for some constant c. For all $n \le 7$, cleary $T(n)=c_{0}$, and so $T(n)\le Cn \text{ for c} \ge 7c_{0}$. Assume the statement true for all $m<n$. Then

$$
\begin{align}
T(n)&=T(\frac{n}{7})+T(\frac{5n}{7})+n \\
    &\le c(\frac{n}{7}) +c\frac{5n}{7}+n \\
    &=\frac{6cn}{7} +n \\
    &\le cn. \\
\end{align}
$$

By induction we have show that $T(n)=O(n)$ for all $n \ge7, c= 7c_{0}$

ii)Similar analysis to (i), then we get $T(n)=T(\frac{n}{3})+T(\frac{2n}{3})+n$. Guess $T(n)=O(nlgn)$, which implies that we want to show $T(n) \le cnlgn$.


