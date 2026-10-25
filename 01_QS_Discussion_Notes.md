# 1 讨论时间

# 2 SSH 
## 2.1 2026/10/19
- [ ] 依靠磁场是否能实现 CDW-SDW 相变区分，现象不明显。下一步需要考虑
- [x] 是否需要考虑自旋，考虑具体任务 ✅ 2026-10-23
- [ ] 电荷如何初始化，半填充话比较简单

## 2.2 2026/10/21
- [x] 整理 MBL10d 变磁场是否是可信的，峰宽等 ✅ 2026-10-23
![585](file-20261023154701223.png)
![602](file-20261023162959369.png)


## 2.3 2026/10/23
- [ ] ==蜂窝网自动识别，高精度校准虚拟电极和自动电荷初始化。适用性不好==
![584](file-20261023161113495.png)
- [ ] 稳定性不好，可能由于温度原因。30mk-20mk
- [ ] 


## 2.4 2026/10/25
- [ ] 粒子数变化重构测量原理

系统的哈密顿量为：

$$
H=H_{\mathrm{tunnel}}+H_{\mathrm{interaction}}
-\sum_i\delta_i n_i.
$$
在格点 i 施加化学势变化：
$$
\delta_i\rightarrow\delta_i+d\delta_i.
$$
Hellmann–Feynman 定理：
$$
dE_N=\langle\Psi_N|dH|\Psi_N\rangle.
$$
$$
\boxed{
\frac{\partial E_N}{\partial\delta_i}
=-\langle n_i\rangle_N
}
$$

下面，考虑第 N 个电子到 N+1 电子填充：
$$
\begin{aligned}
d\mu_N
&=dE_N-dE_{N-1}\\
&=-\langle n_i\rangle_Nd\delta_i
+\langle n_i\rangle_{N-1}d\delta_i\\
&=-\left(
\langle n_i\rangle_N-\langle n_i\rangle_{N-1}
\right)d\delta_i.
\end{aligned}
$$

于是可以通过测量微分重构出，当第 N 个电子到 N+1 电子填充时候，第 i 个格点的粒子数变化：
$$
\boxed{
\frac{\partial\mu_N}{\partial\delta_i}
=-\Delta n_i^{(N)}
}
$$
所有格点的粒子数满足归一化关系：
$$
\sum_i\Delta n_i^{(N)}=1
$$
从 $N=0$ 开始测量，可以直接获得绝对占据数。
$$
\langle n_i\rangle_N
=-\sum_{k=1}^N
\frac{\partial\mu_k^*}{\partial\delta_i}

$$
下图是仿真结果，由于能级结构存在 anti-crossing，直接从 gg-map 求斜率需要非常高精度。可以采用锁相放大的技术。
![](file-20261025214230060.png)
![](file-20261025214353779.png)



# 3 Orb
## 3.1 2026/10/19
- [x] 轨道态波函数初步复现 ✅ 2026-10-23
	复现实验文章
	找其他文章复现
- [x] 理论的文章 fig5 补充一致性 ✅ 2026-10-22

## 3.2 2026/10/21
- [ ] 与实验文章对应不好，可能有无序等参数没有考虑，单壳层结构和原文一致
Localized orbitals and tunnel couplings from general confinement potentials in gate-defined quantum-dot arrays



