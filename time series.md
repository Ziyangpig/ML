# Time series Note

## Autogressive model

### basic concept
An autoregressive model of order p:
xt = ϕ0 +ϕ1xt−1 +ϕ2xt−2 +...+ϕpxt−p +wt
- white noises: all uncorrelated, maen 0, finete varience
- Least squares estimators work if xt is weakly stationary

**weakly stationnary**
  1. 均值为常数
  2. 协方差至与Δt有关

**causal stationary**  

因果平稳过程（Causal stationary）：统计特性不随时间改变，且当前值仅依赖于当前及过去的信息。

非因果平稳过程（Not causal stationary）：统计特性不随时间改变，但当前值可能依赖于未来的信息。  

### Causal stationary for AR(1)  
xt = ϕxt−1 +wt  
- |φ|<1, weakly stationary, causal
- |φ|>1, weakly stationary, noncausal
- |φ|=1, not weakly stationary

### Causal stationary for AR(p)  
AR(p) 因果平稳的条件：
Consider the corresponding polynomial
 $ϕ(z) = 1−ϕ_1z −...−ϕ_pz^p = Πp(1-r_i^{-1}z)$, where r_i, i = 1,...,p are the roots of ϕ(z).
 an AR(p) model is causal stationary if and only if |ri| > 1 for all i.

 Note:  
 $ ϕ(z)X_t = w_t $ => $ X_t = ϕ^{-1}(z) w_t $, 因此ϕ(z)必须可逆，也就是ϕ^{-1}(z)展开对应的无穷级数必须收敛

 ### OLS估计器的渐进性质  
 1. 如果xt是causal stationary，且wt服从正太分布，那么随着样本量n增大，参数的估计变量渐进服从正态分布
 2. 

### ACF function for AR(1)
![image](https://github.com/user-attachments/assets/3e30e229-02cf-42a4-8e8a-610fd05c2576)


### inverse operator  
ϕ^{-1}(z) = φ(z) ,   φ(z)ϕ(z) = 1
 A general technique for finding the coefficients of a linear process
 is by matching coefficients. 

## MA
definition:   The moving average model of order q, MA(q), is  xt = wt +θ1wt−1 +θ2wt−2 +...+θqwt−q, where wt ∼ wn(0,σ2 w) and θ1,...,θq= 0 are parameters.

property:
 By definition, MA(q) is causal station1ary
 - 明显，均值为常数
 - ACF：也很好求，且至与Δt有关

### ACF for MA(1)  
![image](https://github.com/user-attachments/assets/5a9eda39-fa56-4261-9a83-93aa90ba8b2e)

 
