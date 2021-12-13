<!-- toc -->



在普通SHH模型的格点加上位能(on-site potential) $\Delta$
$$
\begin{aligned}
H=&H_{S S H}+\sum_{j}(-1)^{i} \Delta c_{i}^{\dagger} c_{i}
\\=&H_{S S H}+\sum_{j} \Delta c_{j}^{\dagger} c_{j}-\Delta d_{j}^{\dagger} d_{j}
\end{aligned}
$$
傅里叶变换
$$
c_{j}=\frac{1}{\sqrt{N}} \sum_{k} e^{i j k} c_{k}, \quad d_{j}=\frac{1}{\sqrt{N}} \sum_{k} e^{i j k} d_{k}
$$
新增加的项变为
$$
\begin{aligned}
\Delta \sum_{j} c_{j}^{\dagger} c_{j}-d_{j}^{\dagger} d_{j} &=\frac{\Delta}{N} \sum_{j, k, k^{\prime}} e^{i j\left(k^{\prime}-k\right)}\left(c_{k}^{\dagger} c_{k^{\prime}}-d_{k}^{\dagger} d_{k^{\prime}}\right) \\
&=\Delta \sum_{k}\left(c_{k}^{\dagger} c_{k}-d_{k}^{\dagger} d_{k}\right), \\
&=\sum_{k}\left(c_{k}^{\dagger} d_{k}^{\dagger}\right)\left(\begin{array}{cc}
\Delta & 0 \\
0 & -\Delta
\end{array}\right)\left(\begin{array}{l}
c_{k} \\
d_{k}
\end{array}\right) \\
&=\sum_{k}\left(c_{k}^{\dagger} d_{k}^{\dagger}\right) h^{\prime}(k) \cdot \sigma\left(\begin{array}{c}
c_{k} \\
d_{k}
\end{array}\right)
\end{aligned}
$$
其中
$$
h ^{\prime}(k)=(0,0, \Delta)
$$
最后哈密顿量为
$$
h = h _{S S H}+ h ^{\prime}=(v+w \cos k, w \sin k, \Delta)
$$
本征能量
$$
E_{\pm}=\pm| h |=\pm \sqrt{\Delta^{2}+v^{2}+w^{2}+2 v w \cos k}
$$