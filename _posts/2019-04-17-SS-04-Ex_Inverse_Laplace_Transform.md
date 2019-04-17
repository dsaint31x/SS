---
title:  "[SS] 04 Ex: Inverse Lapalce Transform"
date:   2019-04-17 23:47:59
author: dsaint31
categories: Signals_and_Systems
use_math: true
tags: Partial_Fraction_Decomposition
---


## 1. 다음 $X(s)$의 Inverse Laplace Transform을 구하라.

$$
X(s)=\frac{8s^2-7s-6}{s^3-s^2-6s}
$$

### sol.

$$
\begin {align*}
X(s)&=\frac{8s^2-7s-6}{s^3-s^2-6s}\\
&=\frac{8s^2-7s-6}{s(s-3)(s+2)}\\
&=\frac{A}{s}+\frac{B}{s-3}+\frac{C}{s+2}
\end {align*}
$$

distinct pole의 경우로서 다음과 같이 A,B,C를 구할 수 있음.

$$
\begin {align*}
A&= \left. \frac{8s^2-7s-6}{(s-3)(s+2)} \right |_{s=0} \\
&= \frac{0-0-6}{-3\cdot 2} \\
&= 1
\end {align*}
$$

$$
\begin {align*}
B&= \left. \frac{8s^2-7s-6}{(s)(s+2)} \right |_{s=3} \\
&= \frac{72-21-6}{3\cdot 5} = \frac{45}{15} \\
&= 3
\end {align*}
$$

$$
\begin {align*}
C&= \left. \frac{8s^2-7s-6}{(s)(s-3)} \right |_{s=-2} \\
&= \frac{32+14-6}{-2\cdot -5} = \frac{40}{10} \\
&= 4
\end {align*}
$$

이를 통해, $X(s)$는 다음과 같음.

$$
X(s)=\frac{1}{s}+\frac{3}{s-3}+\frac{4}{s+2}
$$

$x(t)$ 는 다음과 같음.

$$
x(t) = u(t) + 3e^{-(-3)t}u(t) + 4e^{-2t}u(t)
$$

ROC는 다음과 같음.
$$
Re(s)>0 \\
Re(s)>-(-3)=3 \\
Re(s)>-2\\
\therefore Re(s)>3
$$

----

## 2. 다음 $X(s)$의 Inverse Laplace Transform을 구하라.

$$
X(s)=\frac{8s+10}{(s+1)(s+2)^3} 
$$

### sol.

$$
\begin {align*}
X(s) &= \frac{8s+10}{(s+1)(s+2)^3} \\
&= \frac{A}{(s+1)}+\frac{B_1}{(s+2)}+\frac{B_2}{(s+2)^2}+\frac{B_3}{(s+2)^3}\\
\end {align*}
$$

$A$와  $B_3$는 distinct poles의 경우와 마찬가지로 구할 수 있음.

$$
\begin {align*}
A &=  \left . X(s)(s+1) \right |_{s=-1} \\
&= \left . \frac{8s+10}{(s+1)(s+2)^3}(s+1) \right |_{s=-1} \\
&= \frac {2}{1^3} \\
&= 2
\end {align*}
$$

$$
\begin {align*}
B_3 &=  \left . X(s)(s+2)^3 \right |_{s=-2} \\
&=  \left . \frac{8s+10}{(s+1)(s+2)^3}(s+2)^3 \right |_{s=-2} \\
&=  \left . \frac{8s+10}{(s+1)} \right |_{s=-2} \\
&= \frac {8\cdot-2+10}{(-1)} \\
&= 6
\end {align*}
$$

$B_2$는 다음과 같이 구함.

$$
\begin {align*}
B_2 &=  \left . \frac{ \text{d}}{\text{d}s} \left[ X(s)(s+2)^3\right] \right |_{s=-2} \\
&=  \left . \frac{8(s+1)-(8s+10)\cdot1}{(s+1)^2} \right |_{s=-2} \\
&= \frac {-2}{1} \\
&= -2
\end {align*}
$$

$B_1$은 다음과 같이 구함.

$$
\begin {align*}
B_1 &=  \left . \frac{1}{2}\frac{ \text{d}^2}{\text{d}s^2} \left[ X(s)(s+2)^3\right] \right |_{s=-2} \\
&=  \frac{1}{2}\left . \frac{ \text{d}}{\text{d}s}\frac{8(s+1)-(8s+10)\cdot1}{(s+1)^2} \right |_{s=-2} \\
&=  \frac{1}{2}\left . \frac{ \text{d}}{\text{d}s}\frac{-2}{(s+1)^2} \right |_{s=-2} \\
&= \frac{1}{2} \left .\frac {-2\cdot-2}{(s+1)^3} \right |_{s=-2}\\
&= \left .\frac {2}{(s+1)^3} \right |_{s=-2}\\
&= -2
\end {align*}
$$

이를 통해, $X(s)$는 다음과 같음.

$$
\begin {align*}
X(s) &= \frac{8s+10}{(s+1)(s+2)^3} \\
&= \frac{A}{(s+1)}+\frac{B_1}{(s+2)}+\frac{B_2}{(s+2)^2}+\frac{B_3}{(s+2)^3}\\
&= \frac{2}{(s+1)}+\frac{-2}{(s+2)}+\frac{-2}{(s+2)^2}+\frac{6}{(s+2)^3} \\
x(t)&= 2e^{-t} u(t)-2e^{-2t}u(t) -2te^{-2t}u(t)+6\cdot\frac{1}{2}t^2 e^{-2t}u(t) \\
&= 2e^{-t} u(t)-2e^{-2t}u(t) -2te^{-2t}u(t)+3t^2 e^{-2t}u(t)
\end {align*}
$$
