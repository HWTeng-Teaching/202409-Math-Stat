### 2.19 Find an expression for the cumulative distribution function of a geometric random variable.  
For a geometric distribution with probability mass function (PMF):  
P(X=k)= $(1−p)^{k−1}p$ ,for k=1,2,3,…  
CDF=F(k)=P(X≤k)= $\sum_{i=1}^{k} P(X = i)$ = $\sum_{i=1}^{k} (1−p)^{i−1}p$  
F(k)=p $\sum_{i=0}^{k-1}(1−p)^{i}$ = $1−(1−p)^k$  for k=1,2,3,…  

### 2.21  If X is a geometric random variable, show that P(X > n + k − 1|X > n − 1) = P(X > k) In light of the construction of a geometric distribution from a sequence of independent Bernoulli trials, how can this be interpreted so that it is “obvious”?.  
P(X>n+k−1∣X>n−1)= $\frac{P(X > n + k − 1 ∩ X > n − 1)}{P(X > n − 1)}$ = $\frac{P(X > n + k − 1)}{P(X > n − 1)}$  
P(X>n+k−1∣X>n−1)= $\frac{ (1-p)^{n+k-1} }{(1-p)^{n-1}}$ = $(1-p)^k$  
P(X>n+k−1∣X>n−1)=P(X>k)  
In terms of the geometric distribution and independent Bernoulli trials, this result can be interpreted as follows:  
A geometric random variable represents the number of trials until the first success in a sequence of independent Bernoulli trials.  
The memoryless property of the geometric distribution states that the probability of seeing a success after k more trials does not depend on how many trials have already occurred without success. In other words, once you're already at trial n, the process "restarts," and the probability of needing more than k additional trials is the same as it was at the beginning.  
This result reflects the memoryless property of the geometric distribution, which makes the conditional probability calculation straightforward. No matter how long you've been waiting (whether n or more trials), the probability of needing more than k additional trials remains 𝑃(𝑋>𝑘).  
### 2.30  Suppose that in a city, the number of suicides can be approximated by a Poisson process with λ = .33 per month.
### a. Find the probability of k suicides in a year for k = 0, 1, 2,... . What is the most probable number of suicides?
### b. What is the probability of two suicides in one week?
a.  
λyear=12×0.33=3.96 suicides per year.  
P(X=k) = $\frac{ e^{-λ}λ^k }{k!}$  
P(X=0)=0.0191  
P(X=1)=0.0755
P(X=2)=0.1495
P(X=3)=0.1973
P(X=4)=0.1953
P(X=5)=0.1547
P(X=6)=0.1021
P(X=7)=0.0578
P(X=8)=0.0286
P(X=9)=0.0126
P(X=10)=0.0050
P(X=11)=0.0018
P(X=12)=0.0006  
​X = 3 is the most probable  
b.  
λweek= $\frac{0.33 }{4.33}$ ≈0.0762  
P(X=2)= $\frac{0.0762^2e^{-0.0762} }{2}$ ≈0.00269  
Thus, the probability of two suicides in one week is approximately  0.27%.
### 2.33  Let F(x) = 1 − exp($−αx^β$) for x ≥ 0,α > 0,β > 0, and F(x) = 0 for x < 0.  Show that F is a cdf, and find the corresponding density.
exp($−αx^β$) is decreasing thus 1-exp($−αx^β$) is non decreasing  
For x < 0 : F(x) = 0 Thus, lim x→−∞ F(x) = 0.  
For x → ∞ : lim x→∞ F(x) = 1  
For 𝑥≥0, 𝐹(𝑥) is continuous. Additionally, 𝐹(𝑥) is zero for 𝑥<0, so it is right-continuous at 𝑥=0  
Thus, 𝐹(𝑥) satisfies all the conditions to be a valid CDF.  
f(x)= $\frac{d}{dx} F(x)$  
For 𝑥≥0 :f(x)= $\frac{d}{dx}$ (1 − exp($−αx^β$))  
after Differentiating:  
f(x)= $αβx^{β-1}exp(-αx^β)$  
the pdf is  
$αβx^{β-1}exp(-αx^β)$ for x≥0  
0                     for x<0

### 2.34  Let f (x) = (1 + αx)/2 for −1 ≤ x ≤ 1 and f (x) = 0 otherwise, where −1 ≤ α ≤ 1. Show that f is a density, and find the corresponding cdf. Find the quartiles and the median of the distribution in terms of α.
To verify that `f(x)` is a valid probability density function, it must satisfy:
- **Non-negativity**: For `-1 ≤ α ≤ 1`, `f(x) = (1 + αx) / 2 ≥ 0` for `-1 ≤ x ≤ 1`.  
**Total probability equals 1**: The integral of `f(x)` over its domain must equal 1:
  $\int_{-1}^{1} f(x) \ dx = \int_{-1}^{1} \frac{1 + \alpha x}{2} \, dx = 1.$
Thus, `f(x)` is a valid PDF.
####  Cumulative Distribution Function (CDF)  
The CDF `F(x)` is defined as: F(x) = $\int_{-\infty}^{x} f(t) dt$  
For `x < -1`, `F(x) = 0`. For `-1 ≤ x ≤ 1`, the CDF is given by:  
$F(x) = \frac{1}{2} \left( x + 1 + \frac{\alpha}{2} (x^2 - 1) \right)$  
For `x > 1`, `F(x) = 1`.  
#### Quartiles and Median  
The **median** `m` is the value where `F(m) = 0.5`. Solving the equation:  
$\frac{1}{2} \left( m + 1 + \frac{\alpha}{2} (m^2 - 1) \right) = 0.5$  
gives the median `m`.
𝑚 = $\frac{−1 + \sqrt{1 + 𝛼^2}}{2𝛼}$(since 𝑚 must be in the interval [-1, 1])  

Find the First Quartile Q1  
CDF 𝐹(𝑄1) = 0.25  
​Q1 = $\frac{−1 + \sqrt{1 - 𝛼 + 𝛼^2}}{𝛼}$  

Find the Third Quartile Q3  
CDF 𝐹(𝑄3) = 0.75  
​Q3 = $\frac{−1 + \sqrt{1 - 4𝛼 + 3𝛼^2}}{𝛼}$  
### 2.35  Sketch the pdf and cdf of a random variable that is uniform on [−1, 1].  
![image](https://github.com/user-attachments/assets/720a3d8d-cfd3-4289-a3db-fc7c6cbaf972)


