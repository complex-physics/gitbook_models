# Haldane Mode



参考文献

1. F. D. M. Haldane, Model for a Quantum Hall Effect without Landau Levels: Condensed-Matter Realization of the "Parity Anomaly" Phys. Rev. Lett. 61, 2015-2018 (1988).



加入第二邻近跃迁

<img src="https://jptanjing.oss-cn-beijing.aliyuncs.com/img/image-20211213220042859.png" style="zoom:33%;" />

这个第二邻近跃迁又称为Haldane项，用$m$表示，因为会打开一个能隙，形成等效质量
$$
\begin{aligned}
H_{m} &=m \sum_{i} C_{ R _{i}, 1}^{\dagger} C_{ R _{i}, 1}-C_{ R _{i}, 2}^{\dagger} C_{ R _{i}, 2} \\
&=-m \sum_{i, \sigma}(-1)^{\sigma} C_{ R _{i}, \sigma}^{\dagger} C_{ R _{i}, \sigma} \\
&=-m \sum_{ k , \sigma}(-1)^{\sigma} C_{ k , \sigma}^{\dagger} C_{ k , \sigma} \\
&=\sum_{ k }\left(\begin{array}{ll}
C_{ k , 1}^{\dagger} & C_{ k , 2}^{\dagger}
\end{array}\right) m \sigma_{z}\left(\begin{array}{l}
C_{ k , 1} \\
C_{ k , 2}
\end{array}\right)
\end{aligned}
$$
总哈密顿量
$$
H( k )=H_{T B}( k )+H_{m}( k )
$$


# Haldane模型的陈数

在泡利矩阵表示下的Haldane模型
$$
H( k , \phi)= h ( k , \phi) \cdot \sigma
$$
其中
$$
\begin{array}{l}
h_{x}=t_{1}\left[\cos \left(\frac{\sqrt{3}}{3} k_{y}\right)+2 \cos \left(\frac{k_{x}}{2}\right) \cos \left(\frac{\sqrt{3}}{6} k_{y}\right)\right] \\
h_{y}=t_{1}\left[\sin \left(\frac{\sqrt{3}}{3} k_{y}\right)-2 \cos \left(\frac{k_{x}}{2}\right) \sin \left(\frac{\sqrt{3}}{6} k_{y}\right)\right] \\
h_{z}=m+2 t_{2} \sin \phi\left[\sin \left(k_{x}\right)-2 \sin \left(\frac{k_{x}}{2}\right) \cos \left(\frac{\sqrt{3}}{2} k_{y}\right)\right]
\end{array}
$$


对于 $K$ 点 $\left(k_{x}, k_{y}\right)=\left(\frac{4 \pi}{3}, 0\right)$

- 展开 $\sin \left(\frac{k_{x}}{2}\right) \approx \frac{\sqrt{3}}{2}-\frac{1}{4} q_{x}$ 
- 展开 $\cos \left(\frac{\sqrt{3}}{2} k_{y}\right) \approx 1$ 
- 展开 $\sin k_{x} \approx-\frac{\sqrt{3}}{2}-\frac{1}{2} q_{x}$ 
- 其中 $q_{x}=k_{x}-\frac{4 \pi}{3}$

所以哈密顿量在 $K$ 点展开成
$$
H_{K} \approx-\frac{t_{1} \sqrt{3}}{2}\left(q_{x} \sigma_{x}-q_{y} \sigma_{y}\right)+\left(m-3 \sqrt{3} t_{2} \sin \phi\right) \sigma_{z}
$$
哈密顿量对于 $K^{\prime}$ 点 $\left(k_{x}, k_{y}\right)=\left(-\frac{4 \pi}{3}, 0\right)$ 展开成
$$
H_{K^{\prime}} \approx-\frac{t_{1} \sqrt{3}}{2}\left(q_{x} \sigma_{x}+q_{y} \sigma_{y}\right)+\left(m+3 \sqrt{3} t_{2} \sin \phi\right) \sigma_{z}
$$


当 $m \approx-3 \sqrt{3} t_{2} \sin \phi$，其中 $\phi>0$

本征方程
$$
\left(\begin{array}{cc}
u & -r e^{i \theta} \\
-r e^{-i \theta} & u
\end{array}\right)|-, k\rangle=-E|-, k\rangle
$$


<img src="https://jptanjing.oss-cn-beijing.aliyuncs.com/img/image-20211213221440379.png" style="zoom:50%;" />

因为有非平庸拓扑数，我们可以预期存在边界态

<img src="https://jptanjing.oss-cn-beijing.aliyuncs.com/img/image-20211213221716609.png" style="zoom: 50%;" />