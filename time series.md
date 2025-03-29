# Time series Note

## Autogressive model

An autoregressive model of order p:
xt = ϕ0 +ϕ1xt−1 +ϕ2xt−2 +...+ϕpxt−p +wt
- white noises: all uncorrelated, maen 0, finete varience
- Least squares estimators work if xt is weakly stationary
**weakly stationnary: **
  1. 均值为常数
  2. 协方差至与Δt有关

因果平稳过程（Causal stationary）：统计特性不随时间改变，且当前值仅依赖于当前及过去的信息。

非因果平稳过程（Not causal stationary）：统计特性不随时间改变，但当前值可能依赖于未来的信息。
AR(p) 因果平稳的条件：
Consider the corresponding polynomial
 ϕ(z) = 1−ϕ1z −...−ϕpzp = Πp(1-ri-1z), where ri, i = 1,...,p are the roots of ϕ(z).
 an AR(p) model is causal stationary if and only if |ri| > 1 for all i.
