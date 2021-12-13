# Graphene like



1. 先计算石墨烯的基本模型，二次量子化紧束缚模型最近邻跃迁
2. 加入次近邻跃迁，不需要磁场也能打破时间反演对称性，得到Haldane模型(Anomalous Quantum Hall effect)
3. Haldane模型通过打破时间反演对称性得到非平庸拓扑态，现在我们想保留时间反演对称性下找到非平庸的拓扑态。有一种方法是把两个Haldane模型叠加在一起，得到了Kane-Mele模型(Spin Quantum Hall effect)

# Tight-Binding Approximation for graphene

<img src="https://jptanjing.oss-cn-beijing.aliyuncs.com/img/image-20210507163034955.png" style="zoom: 50%;" />

图中绿色的向量 $\vec{v}_{1}$ 和 $\vec{v}_{2}$. 作为基底，其他晶格上的原子可以用  $m \vec{v}_{1}+n \vec{v}_{2}$ 表示

-  $\vec{v}_{1}=(\sqrt{3} a, 0)$ 
-  $\vec{v}_{2}=(-\sqrt{3} / 2 a, 3 / 2 a)$. 

每个单位元胞有两种子晶格

-  $a$ 红色表示
-  $b$ 黑色表示

只考虑最近邻跃迁(nearest-neighbor (NN))，哈密顿量可以写成 
$$
H=-t \sum_{i, j } a_{i}^{\dagger} b_{j}-t \sum_{i, j } b_{i}^{\dagger} a_{j}
$$
对于一个晶格，跃迁出去的有三种

1. 沿着x轴旋转 $\theta=\pi / 2,$ $\vec{e}_{1}=(0, a)$
2. 沿着x轴旋转 $\theta=\pi / 2+2 \pi / 3=7 \pi / 6$，$\vec{e}_{2}=\left(-\frac{\sqrt{3}}{2} a,-\frac{a}{2}\right)$
3. 沿着x轴旋转 $\theta=\pi / 2+4 \pi / 3=11 \pi / 6,$ $\vec{e}_{3}=\left(\frac{\sqrt{3}}{2} a,-\frac{a}{2}\right)$

哈密顿量可以具体写成 
$$
H=-t \sum_{i}^{t} b_{r_{i}+{e}_{1}}-t \sum_{i} b_{r_{i}-e_{2}}-t \sum_{a_{r}^{+}}^{+} b_{r_{i}+ {e}_{3}}+h . c 
$$

## 动量空间

傅里叶变换到动量空间
$$
\begin{aligned}
&a_{k}=\frac{1}{\sqrt{N}} \sum_{i} a_{i} e^{i \vec{k} \cdot \vec{r}}\\
&a_{i}=\frac{1}{\sqrt{N}} \sum_{k} a_{k} e^{-i \vec{k} \cdot \vec{r}}\\
&b_{k}=\frac{1}{\sqrt{N}} \sum_{i} a_{i} e^{i \vec{k} \cdot \vec{r}}\\
&b_{i}=\frac{1}{\sqrt{N}} \sum_{k} a_{k} e^{-i \vec{k} \cdot \vec{r}}
\end{aligned}
$$
第一项变成
$$
\begin{aligned}
-t \sum_{i} a_{r_{i}}^{\dagger} b_{r_{i}+e_{1}}&=-\frac{t}{N} \sum_{i} \sum_{k} \sum_{k^{\prime}} a_{k}^{\dagger} e^{i \vec{k} \cdot \vec{r}_{i}} b_{k^{\prime}} e^{-i \vec{k} \cdot\left(\vec{r}_{i}+\vec{e}_{1}\right)}
\\&=-t \sum_{k} \sum_{k^{\prime}} a_{k}^{\dagger} b_{k^{\prime}} e^{-i \vec{k} \cdot \overrightarrow{e_{1}}} \frac{1}{N} \sum_{i} e^{i\left(\vec{k}-\vec{k}^{\prime}\right) \vec{r}_{i}}
\\&=-t \sum_{k} \sum_{k^{\prime}} a_{k}^{\dagger} b_{k^{\prime}} e^{-i \vec{k} \cdot \overrightarrow{e_{1}}} \delta_{k, k^{\prime}}
\\&=-t \sum_{k} a_{k}^{\dagger} b_{k} e^{-i \vec{k} \cdot \overrightarrow{e_{1}}}
\end{aligned}
$$
类似的，计算另外两项
$$
\begin{aligned}
H&=-t \sum_{i} a_{r_{i}}^{\dagger} b_{r_{i}+e_{1}}-t \sum_{i} a_{r_{i}}^{\dagger} b_{r_{i}+e_{2}}-t \sum_{i} a_{r_{i}}^{\dagger} b_{r_{i}+e_{3}}+h . c . \\
&=-t \sum_{k} a_{k}^{\dagger} b_{k}\left(e^{-i \vec{k} \cdot \overrightarrow{e_{1}}}+e^{-i \vec{k} \cdot \overrightarrow{e_{2}}}+e^{-i \vec{k} \cdot \overrightarrow{e_{3}}}\right)-t \sum_{k} b_{k}^{\dagger} a_{k}\left(e^{i \vec{k} \cdot \overrightarrow{e_{1}}}+e^{i \vec{k} \cdot \overrightarrow{e_{2}}}+e^{i \vec{k} \cdot \overrightarrow{e_{3}}}\right) \\
&=\sum_{k}\left(\begin{array}{ccc}
a_{k} \dagger & b_{k}^{\dagger}
\end{array}\right)\left(\begin{array}{cc}
0 & \mathcal{H}_{12}(\vec{k}) \\
\mathcal{H}_{21}(\vec{k}) & 0
\end{array}\right)\left(\begin{array}{c}
a_{k} \\
b_{k}
\end{array}\right)

\end{aligned}
$$
其中
$$
\begin{aligned}
&\mathcal{H}_{12}(\vec{k})=-t\left[\exp \left(-i \vec{k} \cdot \vec{e}_{1}\right)+\exp \left(-i \vec{k} \cdot \vec{e}_{2}\right)+\exp \left(-i \vec{k} \cdot \vec{e}_{3}\right)\right)\\
&\mathcal{H}_{21}(\vec{k})=\mathcal{H}_{12}(\vec{k})^{*}=-t\left[\exp \left(i \vec{k} \cdot \vec{e}_{1}\right)+\exp \left(i \vec{k} \cdot \vec{e}_{2}\right)+\exp \left(i \vec{k} \cdot \vec{e}_{3}\right)\right]
\end{aligned}
$$

矩阵
$$
\mathcal{H}(\vec{k})=\left(\begin{array}{cc}
0 & \mathcal{H}_{12}(\vec{k}) \\
\mathcal{H}_{21}(\vec{k}) & 0
\end{array}\right)
$$
本征值
$$
\begin{aligned}
\epsilon_{\pm}(\vec{k})=&\pm\left|\mathcal{H}_{12}(\vec{k})\right|
\\=&\pm|t| \sqrt{3+2 \cos \left(\sqrt{3} k_{x} a\right)+4 \cos \left(\frac{\sqrt{3}}{2} k_{x} a\right) \cos \left(\frac{3}{2} k_{y} a\right)}
\end{aligned}
$$

## 闭合点

色散  $\epsilon_{\pm}$ 是 $\vec{k}$ 空间的周期性函数。

- 低带 $\epsilon_{-}$ 的最小值在 $k=0$. 
- 低带 $\epsilon_{-}$ 的最大值在布里渊区的六角晶格的角上。

六角晶格有六个角，但是

1.  $\theta=0$，$ \theta=2 \pi / 3$ ，$\theta=4 \pi / 3$ 三个点是等价的点
2.  $\theta=\pi $，$ \theta=\pi+2 \pi / 3$ ，$\theta=\pi+4 \pi / 3$ 三个点是等价的点

分别标记为
$$
\begin{aligned}
K&=\left(\frac{4 \pi}{3 \sqrt{3} a}, 0\right)\\
K^{\prime}&=\left(-\frac{4 \pi}{3 \sqrt{3} a}, 0\right)
\end{aligned}
$$
在这些点上， $\epsilon_{+}=\epsilon_{-}=0$
$$
\begin{aligned}
\epsilon_{\pm}(\vec{K}) &=\pm\left|\mathcal{H}_{12}(\vec{K})\right|=\pm|t| \sqrt{3+2 \cos \left(\sqrt{3} k_{x} a\right)+4 \cos \left(\frac{\sqrt{3}}{2} k_{x} a\right) \cos \left(\frac{3}{2} k_{y} a\right)}
\\&=
\pm |t| \sqrt{\left(3+2 \cos \left(\sqrt{3} \frac{4 \pi}{3 \sqrt{3} a} a\right)+4 \cos \left(\frac{\sqrt{3}}{2} \frac{4 \pi}{3 \sqrt{3} a}\right) \cos \left(\frac{3}{2} \times 0\right)\right)}
\\&=
 \pm|t| \sqrt{3+2 \cos \left(\frac{4 \pi}{3}\right)+4 \cos \left(\frac{2 \pi}{3}\right)}
 \\&=\pm|t| \sqrt{3+2 \times\left(-\frac{1}{2}\right)+4 \times\left(-\frac{1}{2}\right)}
 \\&=\sqrt{3-3}=0
\end{aligned}
$$
所以两个能带在这六个点上相交

<img src="https://jptanjing.oss-cn-beijing.aliyuncs.com/img/image-20210507163301124.png" style="zoom:50%;" />



## Dirac 点

在 $\mathrm{K}$ 和 $\mathrm{K}^{\prime}$ 点上，对色散线性化 $\epsilon_{\pm} \propto \pm(k-K) .$
$$
\begin{aligned}
\epsilon_{\pm}(\vec{k})  &=\epsilon_{\pm}(\vec{K}+\vec{q})
\\
&=\pm|t| \sqrt{\left(3+2 \cos \left[\sqrt{3}\left(\frac{4 \pi}{3 \sqrt{3} a}+q_{x}\right) a\right]+4 \cos \left[\frac{\sqrt{3}}{2}\left(\frac{4 \pi}{3 \sqrt{3} a}+q_{x}\right) a\right] \cos \left(\frac{3}{2} q_{y} a\right)\right)}
\\
& =\pm \frac{3}{2}|t| a \sqrt{q_{x}^{2}+q_{y}^{2}}+O\left(q^{2}\right)\\
&=\pm \frac{3}{2}|t| a q+O\left(q^{2}\right)
\end{aligned}
$$

画出图像

<img src="https://jptanjing.oss-cn-beijing.aliyuncs.com/img/image-20210507163406068.png" style="zoom:50%;" />

在 $\mathrm{K}$ 点附近
$$
\begin{aligned}
\mathcal{H}(k)&=\mathcal{H}(K+q)\\
&=\frac{3}{2} t a\left(\begin{array}{cc}
0 & q_{x}-i q_{y} \\
q_{x}+i q_{y} & 0
\end{array}\right)+O\left(q^{2}\right) \approx \frac{3}{2} t a\left(q_{x} \sigma_{x}+q_{y} \sigma_{y}\right)\\
&=c \vec{q} \cdot \vec{\sigma}
\end{aligned}
$$
在  $\mathrm{K}^{\prime}$ 点附近 
$$
\begin{aligned}
\mathcal{H}(k)&=\mathcal{H}\left(K^{\prime}+q\right)\\
&=-\frac{3}{2} \operatorname{ta}\left(\begin{array}{cc}
0 & q_{x}+i q_{y} \\
q_{x}-i q_{y} & 0
\end{array}\right)+O\left(q^{2}\right) 
\\
&\approx-\frac{3}{2} \operatorname{ta}\left(q_{x} \sigma_{x}-q_{y} \sigma_{y}\right)\\
&=-c \vec{q} \cdot\left(\sigma_{x} \vec{\sigma} \sigma_{x}\right)
\end{aligned}
$$
其中 c 是光速

1. 每个 $\mathrm{K}$ 或 $\mathrm{K}^{\prime}$ 点是一个外尔费米子
2.  $\mathrm{K}$ 和 $\mathrm{K}^{\prime}$ 两个外尔费米子，有不同的手征，合成一个狄拉克费米子

符合狄拉克方程
$$
i \partial_{t} \psi=\left(\begin{array}{cc}
0 & c \vec{q} \cdot \vec{\sigma} \\
c \vec{q} \cdot \vec{\sigma} & 0
\end{array}\right) \psi
$$


























