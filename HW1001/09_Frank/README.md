## HW1001
### Q1
#### Problem
Find an expression for the cumulative distribution function of a geometric random
variable.
#### Solution
For a geometric distribution with probability mass function (PMF):  
P(X=k) = $(1−p)^{k−1}p$ ,k = 1,2,3,…  
CDF = F(k) = P(X≤k) = $\sum_{i=1}^{k} P(X=i)$ = $\sum_{i=1}^{k} (1−p)^{i−1}p$  
F(k)= p $\sum_{i=0}^{k-1}(1−p)^{i}$ = $1 − (1 − p)^k$ , k=1,2,3,…  
### Q2
#### Problem
If X is a geometric random variable, show that
P(X > n + k − 1|X > n − 1) = P(X > k)
In light of the construction of a geometric distribution from a sequence of independent Bernoulli trials, how can this be interpreted so that it is “obvious”?
#### Solution
P(X>n+k-1 | X>n-1) = $$\frac{P(X > n+k-1 \cap X > n-1)}{P(X > n-1)}$$  
∵ k>0 ∴ P $$(X > n+k-1 \cap X > n-1)$$=P(X > n+k-1)
=> $$\frac{P(X > n+k-1)}{P(X > n-1)}$$  
CDF of P(X≦k)=1- $$(1 - p)^{k}$$, we can get that P(X>k)= $$(1 - p)^{k}$$   
Change $$\frac{P(X > n+k-1)}{P(X > n-1)}$$ into CDF we can get $$\frac{(1 - p)^{n+k-1}}{(1 - p)^{n-1}}$$ = $$(1 - p)^{k}$$  
which equal to P(X>k)   
the probability of success in future trials is independent of failures that have already occurred this is called memoryless property so that the result is obvious
### Q3
#### Problem
Suppose that in a city, the number of suicides can be approximated by a Poisson
process with λ = .33 per month.
a. Find the probability of k suicides in a year for k = 0, 1, 2,... . What is the
most probable number of suicides?
b. What is the probability of two suicides in one week?
#### Solution
##### a. 
λ=0.33 per month => λ=0.33*12=3.96 per year  
X~Poisson  
P(X=k)= $$\frac{\lambda^k e^{-\lambda}}{k!}$$  
$$P(X = 0) \approx 0.01906$$    
$P(X = 1) \approx 0.07549$    
$P(X = 2) \approx 0.1495$    
$P(X = 3) \approx 0.1973$    
$P(X = 4) \approx 0.1953$    
$P(X = 5) \approx 0.1547$    
base on the λ per year, we can know that the most probable number is 4   
##### b.
λ=0.33 per month => λ=0.33*0.25=0.0825 per week  
P(X=2) $\approx 0.0031$  
### Q4
#### Problem
Let F(x) = 1 − exp(−αxβ) for x ≥ 0,α > 0,β > 0, and F(x) = 0 for x < 0.
Show that F is a cdf, and find the corresponding density.
#### Solution
A CDF if it satisfies the following properties:  

Non-decreasing  
examine the derivative of F(x) for x ≥ 0:  
F′(x) = $\frac{d}{dx}(1 − exp(−αx^β))$  
F′(x) = $0 − (−αβx^{β−1}exp(−αx^β))=αβx^{β−1}exp(−αx^β)$  
Since α > 0, β > 0, and $x^{β−1}$ ≥ 0 for x ≥ 0, we have: F′(x) ≥ 0  

Right-continuous  
The function F(x) is composed of continuous functions (the exponential function), so it is right-continuous for x ≥ 0.  

Limits  
For x < 0 : F(x) = 0  
Thus, lim x→−∞ F(x) = 0.  
For x → ∞ :  
lim x→∞ F(x) = 1

Thus, F(x) is a CDF

To find the corresponding probability density function (PDF), we differentiate F(x):  
f(x) =F′(x) = $αβx^{β−1}exp(−αx^β)$, x ≥ 0

The cumulative distribution function is given by:  
𝐹(𝑥) =  
{0 for 𝑥 < 0  
{1 − exp($−𝛼𝑥^𝛽$) for 𝑥 ≥ 0  

The corresponding probability density function is:  
f(x) = $αβx^{β−1}exp(−αx^β)$, x ≥ 0

### Q5
#### Problem
Let f (x) = (1 + αx)/2 for −1 ≤ x ≤ 1 and f (x) = 0 otherwise, where
−1 ≤ α ≤ 1. Show that f is a density, and find the corresponding cdf. Find the
quartiles and the median of the distribution in terms of α.
#### Solution
### Q6
#### Problem
#### Solution
