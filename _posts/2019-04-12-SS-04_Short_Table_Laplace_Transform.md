---
title:  "[SS] 04 Table : Laplace Transform"
date:   2018-04-12 13:33:59
author: dsaint31
categories: Signals_and_Systems
use_math: true
tags: Laplace
---

# A Short Table of Laplace Transforms 
@(Signal and System)[Laplace]

| # | $x(t)$             | $X(s)$ |
|---|--------------------|----------------------|
|1| $\delta(t)$ | $1$|
|2| $u(t)$ | $\frac{1}{s}$|
|3| $\frac{t^n}{n!}u(t)$ | $\frac{1}{s^{n+1}}$|
|4| $e^{-at} u(t)$ | $\frac{1}{s+a}$|
|5| $\frac{t^ne^{-at}}{n!} u(t)$ | $\frac{1}{(s+a)^{n+1}}$|
|6| $\sin{\omega_0 t} \quad u(t)$ | $\frac{\omega_0}{(s^2+\omega_0^2)}$|
|7| $\cos{\omega_0 t} \quad u(t)$ | $\frac{s}{(s^2+\omega_0^2)}$|
|8| $t\sin{\omega_0 t} \quad u(t)$ | $\frac{2\omega_0 s}{(s^2+\omega_0^2)^2}$|
|9| $t\cos{\omega_0 t} \quad u(t)$ | $\frac{s^2-\omega_0^2}{(s^2+\omega_0^2)^2}$|
|10| $e^{-at}\sin{\omega_0 t} \quad u(t)$ | $\frac{\omega_0}{(s+a)^2+\omega_0^2}$|
|11| $e^{-at}\cos{\omega_0 t} \quad u(t)$ | $\frac{s+a}{(s+a)^2+\omega_0^2}$|
|12| $Ae^{-at}\cos{\omega_0 t} \quad u(t) +Be^{-at}\sin{\omega_0 t} \quad u(t)$ | $\frac{A(s+a)-B\omega_0}{(s+a)^2+\omega_0^2}$|
|13| $Ae^{-at}\cos{\omega_0 t} \quad u(t) +\left(\frac{(B-Aa)}{\omega_0}\right)e^{-at}\sin{\omega_0 t} \quad u(t)$ | $\frac{As-B}{(s+a)^2+\omega_0^2}$|
