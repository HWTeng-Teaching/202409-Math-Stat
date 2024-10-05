# HW0910

by 王邦碩 Brian

## Q1. 

### Question 

Find an expression for the cumulative distribution function of a geometric random variable.

### Solution
$P(X = k) = (1 - p)^{k-1}p$  
$CDF(X = k) = \sum_{k'=1}^{k} (1 - p)^{k'-1}p = 1 - (1-p)^k$  

## Q2

### Question 

If X is a geometric random variable, show that  
P(X > n + k − 1|X > n − 1) = P(X > k) In light of the construction of a geometric distribution from a sequence of independent Bernoulli trials, how can this be interpreted so that it is “obvious”?

### Solution
$\small P(X > n + k − 1| X > n − 1)$  

=  $\large\frac{P(X > n + k − 1)}{P(X > n − 1)}$  

=  $\Large\frac{(1-p)^{n + k − 1}}{(1-p)^{n − 1}}$  
=  $(1-p)^k$  
=  $\small P(X > k)$

## Q3

### Question

Suppose that in a city, the number of suicides can be approximated by a Poisson process with λ = .33 per month.  
a. Find the probability of k suicides in a year for k = 0, 1, 2,... . What is the most probable number of suicides?  
b. What is the probability of two suicides in one week?

### Solution
a)
λ -> 12 * 0.33 = 3.96  
$P(X = k) = \frac{e^{-λ}λ^k}{k!}$  
P(X = 0) = 0.0191   
P(X = 1) = 0.0755   
P(X = 2) = 0.1495  
P(X = 3) = 0.1973  
P(X = 4) = 0.1953  
P(X = 5) = 0.1547  
P(X = 6) = 0.1021   
P(X = 7) = 0.0578  
P(X = 8) = 0.0286  
P(X = 9) = 0.0126  
P(X = 10) = 0.0050  
X = 3 is the most probable  

b)
λ -> 0.33 / 4.33 = 0.0762  
P(X = 2) = 0.00269 = 0.27%

## Q4

### Question

Let F(x) = 1 − exp($−αx^β$) for x ≥ 0,α > 0,β > 0, and F(x) = 0 for x < 0.  
Show that F is a cdf, and find the corresponding density.

### Solution
#### A)
(1)  
$\exp(-\alpha x^\beta)$ is decreasing  
$\therefore F(x)$ is non-decreasing  

(2)  
$lim_{x \to \infty} −αx^β = -\infty$  
$\therefore$ $lim_{x \to \infty} F(x) = 1$  

(3)  
$F(x) = 0 for x < 0$  
$\therefore lim_{x \to -\infty} F(x) = 0$  

Therefore, $F(x)$ is a CDF  
#### B) 
$\frac{d}{dx} F(x) = \frac{d}{dx} \left( 1 - \exp(-\alpha x^\beta) \right)$  
$=-\exp(-\alpha x^\beta)(\frac{d}{dx}-\alpha x^\beta)$  
$=\exp(-\alpha x^\beta) \alpha \beta x^{\beta - 1}$  

Thus the $PDF(x)=$  
$\alpha \beta x^{\beta - 1} \exp(-\alpha x^\beta), if x \geq 0$  
$0, if x < 0$  

## Q5

### Question

Let f (x) = (1 + αx)/2 for −1 ≤ x ≤ 1 and f (x) = 0 otherwise, where −1 ≤ α ≤ 1. Show that f is a density, and find the corresponding cdf. Find the quartiles and the median of the distribution in terms of α.

### Solution
#### A)
(1)
−1 ≤ x, a ≤ 1  
−1 ≤ x * a ≤ 1  
$\therefore$ 0 ≤ f(x) ≤ 1, for x in $[-1, 1]$  
f(x) = 0, otherwise  

So, f(x)≥0 for all x∈R  
(2)  
$\int_{-1}^{1} f(x) \, dx$   
$= \int_{-1}^{1} \frac{1 + \alpha x}{2} \, dx$  
$= \int_{-1}^{1}\frac12 \, dx$  
$= 1$  
 
f(x) is a pdf  
#### B)

(1)
$CDF(x)$  
$=\int_{-1}^{x} \frac{1 + \alpha x'}{2} \, dx'$  
$= (1 / 2)*(x + 1 - \frac{a(x^2 + 1)}{2})$, for −1 ≤ x ≤ 1  
1, if x > 1  
0, if x < -1  
  
median: $(1 / 2)(x + 1 + \frac{a(x^2 - 1)}{2}) = 0.5, x = \frac {-1 + \sqrt{a^2 + 1}}a$  
1st quartiles: $(1 / 2)(x + 1 + \frac{a(x^2 - 1)}{2}) = 1/4, x = \frac {-1 + \sqrt{a^2 - a + 1}}a$  
3rd quartiles: $(1 / 2)(x + 1 + \frac{a(x^2 - 1)}{2}) = 3/4, x = \frac {-1 + \sqrt{a(a + 1) + 1}}a$  


## Q6 

### Question

Sketch the pdf and cdf of a random variable that is uniform on [−1, 1].

### Answer

PDF
![image](https://github.com/user-attachments/assets/edca4c01-2a51-4828-88c7-8c052374597c)

CDF
![image](https://github.com/user-attachments/assets/9942c033-f076-473a-be83-8489610562dd)

