<!-- toc -->



# 模型哈密顿量

在一维Kitaev链基础上
$$
H=\sum_{j}\left[-\mu c_{j}^{\dagger} c_{j}+\left(-t c_{j}^{\dagger} c_{j+1}+\Delta c_{j+1}^{\dagger} c_{j}^{\dagger}+H . c .\right)\right]
$$
引入在位势能及跃迁振幅中均引入调制函数。

- 在位势能调制函数

$$
V_{j}=V \cos \left(2 \pi \alpha j+\varphi_{V}\right)
$$

- 跃迁振幅调制函数

$$
t_{j}=t\left[1+\lambda \cos \left(2 \pi \alpha j+\varphi_{\lambda}\right)\right]
$$

在这些调制函数中, 如果 $\alpha$ 取为无理数，得到Aubry-André-Harper(AAH)模型
$$
H=\sum_{j=1}^{N} V_{j} c_{j}^{\dagger} c_{j}+\sum_{j=1}^{N-1}\left[-t_{j} c_{j+1}^{\dagger} c_{j}+\Delta c_{j+1}^{\dagger} c_{j}^{\dagger}+H . c .\right] .
$$
为方便讨论, 这里我们取 $\alpha=1 / 2, \varphi_{V}=\varphi_{\lambda}=\varphi$ 。
$$
\begin{aligned}
H=&-V \cos \varphi \sum_{j}\left(c_{2 j-1}^{\dagger} c_{2 j-1}-c_{2 j}^{\dagger} c_{2 j}\right) \\
&-t \sum_{j}\left[(1-\lambda \cos \varphi) c_{2 j}^{\dagger} c_{2 j-1}+(1+\lambda \cos \varphi) c_{2 j+1}^{\dagger} c_{2 j}+H . c .\right] \\
&+\Delta \sum_{j}\left(c_{2 j}^{\dagger} c_{2 j-1}^{\dagger}+c_{2 j+1}^{\dagger} c_{2 j}^{\dagger}+H . c .\right)
\end{aligned}
$$
极限

- 当 $\mu=\Delta=0$ 时, 该模型可简化为 $SSH$ 模型; 
- 如果 $\lambda=0$, 则可简化为常规的一维 Kitaev 模型。

# 拓扑性质

## 能谱

将哈密顿量在动量空间中表示出来，写成矩阵形式
$$
H=\frac{1}{2} \sum_{q} \Psi^{\dagger} H (q) \Psi
$$
其中

1. 基底算符

$$
\Psi=\left[\begin{array}{llll}
c_{q A}^{\dagger} & c_{q B}^{\dagger} & c_{-q A} & c_{-q B}
\end{array}\right]^{T},
$$

2. 哈密顿量矩阵

$$
H (q)=\left(\begin{array}{cccc}
-V \cos \varphi & g(q) & 0 & h(q) \\
g^{*}(q) & V \cos \varphi & -h^{*}(q) & 0 \\
0 & -h(q) & V \cos \varphi & -g(q) \\
h^{*}(q) & 0 & -g^{*}(q) & -V \cos \varphi
\end{array}\right)
$$

其中

- $g(q)=-t\left[(1-\lambda \cos \varphi)+(1+\lambda \cos \varphi) e^{-i q}\right]$
- $h(q)=-\Delta\left(1-e^{-i q}\right)$

对角化矩阵，得到的本征值即系统的本征能量为
$$
E^{2}(q)=(V \cos \varphi)^{2}+|g(q)|^{2}+|h(q)|^{2} \pm 2 \sqrt{(V \cos \varphi)^{2}|h(q)|^{2}+4 \Delta^{2} t^{2}(\lambda \cos \varphi)^{2}(\cos q-1)^{2}}
$$

## 对称性

1. 时间反演对称
2. 子晶格对称性
3. 粒子-空穴对称性



系统是时间反演对称的
$$
T H (q) T ^{-1}= H (-q)
$$
当 $V=0$ 时, 系统还具有子晶格对称性
$$
C _{1} H (q) C _{1}^{-1}=- H (q)
$$
粒子-空穴对称性



> BDI 拓扑类的拓扑不变量为整数 $Z$ 。

## 拓扑量子数



$V=0$ 的情开，系统的拓扑量子数定义为
$$
N_{1}=\operatorname{Tr} \int_{-\pi}^{\pi} \frac{d q}{4 \pi i} C _{1} G ^{-1} \partial_{q} G ,
$$




# 局域化现象