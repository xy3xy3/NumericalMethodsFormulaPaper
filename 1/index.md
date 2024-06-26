# **第一章 数值分析与科学计算引论**

记 $x^*$ 为准确值， $x$ 为 $x^*$ 的一个近似值

**绝对误差** $e_p = |x - x^*| $  **相对误差** $e_r = \displaystyle \left|\frac{x-x^*}{x}\right| $

**相对误差限** $\displaystyle\varepsilon_r=\frac{\varepsilon}{\mid x\mid}\geqslant\frac{\mid x-x^*\mid}{\mid x\mid}=\mid e*{\mathrm{r}}\mid $

**条件数** $C_p =\displaystyle \left|\frac{f(x)-f(\tilde{x})}{f(x)}\right|/\left|\frac{\Delta x}{x}\right|\approx\left|\frac{xf'(x)}{f(x)}\right| $

$C_p\geqslant 10$ 就认为问题是病态的

**四则运算误差限**

- $\varepsilon(\hat{p_1}+\hat{p_2})<=\varepsilon(\hat{p_1})+\varepsilon(\hat{p_2}) $

- $\varepsilon(\hat{p_1}\hat{p_2})\approx|\hat{p_1}|\varepsilon(\hat{p_2})+|\hat{p_2}|\varepsilon(\hat{p_1}) $

- $\displaystyle\varepsilon\left(\frac{\hat{p_1}}{\hat{p_2}}\right)\approx\frac{|\hat{p_1}|\varepsilon(\hat{p_2})+|\hat{p_2}|\varepsilon(\hat{p_1})}{|\hat{p_2}|^2} $

**函数误差限** $\varepsilon(f(\hat{p}))\approx|f'(\hat{p})|\varepsilon(\hat{p}) $

若近似数有 $n$ 位有效数字，则可以写为 $\hat{p}=\pm10^m\times(a_1+a_2\times10^{-1}+\ldots+a_i\times10^{-(n-1)})$

其绝对误差限为 $|x-x^*|\leqslant\displaystyle \frac{1}{2}\times10^{m-n+1} $

其相对误差限 $\displaystyle\left|\frac{x-x^*}x\right|\leqslant\varepsilon_r\leqslant\frac{10^{1-n}}{2a_1}$

**秦九韶算法**


$p(x)=a_0x^n+a_1x^{n-1}+\cdotp\cdotp\cdotp+a_{n-1}x+a_n=(\cdots(a_0x+a_1)x+\cdots+a_{n-1})x+a_n  \quad a_0\neq0$ 

$\begin{cases}b_0=a_0,\\b_i=b_{i-1}x^*+a_i,\quad i=1,2,\cdotp\cdotp\cdotp,n,\end{cases}$

$b_{n}=p(x^{*})$ 为所求

