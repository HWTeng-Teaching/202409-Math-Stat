# 01_Rix

by 周子揚 Rix

## Q1. 

### Questions 

Find an expression for the cumulative distribution function of a geometric random variable.

### Answers

For a geometric random variable X, which represents the number of trials until the first success in a sequence of independent Bernoulli trials with success probability p.  

The PMF of a geometric random variable X is:  
P(X = k) = $p(1 − p)^{k−1}$, k = 1, 2, 3,…  

F(k) = P(X ≤ k) = $\sum_{i=1}^{k} P(X = i)$  
geometric random variable : F(k) = p $\sum_{i=1}^{k} (1 - p)^{i-1}$ 

This is a geometric series with the first term 1 and common ratio 1 − p. The sum of the first k terms of a geometric series is:  
$\sum_{i=0}^{k-1} (1 - p)^i$ = $\frac{1 - (1 - p)^k}{1 - (1 - p)}$  
Thus, CDF : F(k) = $1 - (1 - p)^k$ , k = 1, 2, 3,…  
This gives the probability that the first success occurs on or before the k-th trial.

## Q2. 

### Questions 

If X is a geometric random variable, show that  
P(X > n + k − 1|X > n − 1) = P(X > k)  
In light of the construction of a geometric distribution from a sequence of independent Bernoulli trials, how can this be interpreted so that it is “obvious”?

### Answers

CDF of geometric random variable is P(X > n) = $(1 - p)^n$  
P(X > n + k − 1 | X > n − 1) = $\frac{P(X > n + k − 1 ∩ X > n − 1)}{P(X > n − 1)}$  

Since X > n + k − 1 implies X > n − 1, we have :  
P(X > n + k − 1 ∩ X > n − 1) = P(X > n + k − 1)  
so that, P(X > n + k − 1 | X > n − 1) = $\frac{P(X > n + k − 1)}{P(X > n − 1)}$

Turn to CDF :  
​P(X > n + k − 1 | X > n − 1) = $\frac{(1 - p)^{n+k-1}}{(1 - p)^{n-1}}$ = $(1 - p)^k$  

This is precisely the probability that X > k:  
P(X > n + k − 1 ∣ X > n − 1) = P(X > k)

The geometric distribution can be interpreted as the number of independent Bernoulli trials until the first success. In this context:  
P(X > n − 1) means the probability that the first success hasn't occurred by trial n − 1, i.e., the first n − 1 trials were all failures.
Given that we know the first n − 1 trials were failures, the distribution "resets," and the process essentially starts fresh from trial n.

Thus, the probability P(X > n + k − 1 ∣ X > n − 1) is the probability that we observe another k consecutive failures starting from trial n, which is the same as the probability of having k consecutive failures starting from the first trial. This explains why:  
P(X > n + k − 1 ∣ X > n − 1) = P(X > k)

This result is "obvious" because the geometric distribution exhibits the memoryless property, meaning the probability of success in future trials is independent of the number of failures that have already occurred.

## Q3. 

### Questions 

Suppose that in a city, the number of suicides can be approximated by a Poisson process with λ = .33 per month.  
a. Find the probability of k suicides in a year for k = 0, 1, 2,... . What is the most probable number of suicides?  
b. What is the probability of two suicides in one week?

### Answers

a.  
Since there are 12 months in a year, the rate λ for one year is:
λyear = 12 × 0.33 = 3.96  
The probability of observing k events (suicides in this case) in a given time period for a Poisson distribution is given by:  
P(X = k) = $\frac{e^{−λ}λ^k}{k!}$  
P(X = 0) $\approx 0.01876$  
P(X = 1) $\approx 0.0744$  
P(X = 2) $\approx 0.1381$  
P(X = 3) $\approx 0.1882$  
P(X = 4) $\approx 0.1961$  
P(X = 5) $\approx 0.1569$  
​Since λ is 3.96, the most probable number is close to it. It's 4.

b.  
Since there are about 4.33 weeks in a month, the rate for one week is:  
λweek = $\frac{0.33}{4.33} \approx 0.0763$  
P(X = 2) $\approx 0.0054$  

## Q4. 

### Questions 

Let F(x) = 1 − exp($−αx^β$) for x ≥ 0,α > 0,β > 0, and F(x) = 0 for x < 0.  
Show that F is a cdf, and find the corresponding density.

### Answers

F(x) is a CDF if it satisfies the following properties:  

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

## Q5. 

### Questions 

Let f (x) = (1 + αx)/2 for −1 ≤ x ≤ 1 and f (x) = 0 otherwise, where −1 ≤ α ≤ 1. Show that f is a density, and find the corresponding cdf. Find the quartiles and the median of the distribution in terms of α.

### Answers

f(x) is a Density if it satisfies the following properties:  

Non-negativity  
For f(x) to be non-negative in the interval [−1,1]:  
f(x)= $\frac{1 + αx}{2}$ ≥ 0 for −1 ≤ x ≤ 1  
f(x) is non-negative if:  
If α ≥ 0, f(x) is non-negative for all x ∈ [−1,1].
If α < 0, we require that - $\frac{1}{α}$ ≤ 1, which holds true for −1 ≤ α < 0.  
So, f(x) ≥ 0 for −1 ≤ α ≤ 1.  

Normalization  
calculate the integral of f(x):
$\int_{-1}^{1} f(x) dx$ = 1  
Thus, f(x) is normalized.  

The cumulative distribution function F(x) is defined as:  
F(x) = $\int_{−∞}^{x} f(t) dt$  
For x < −1: F(x) = 0  
For −1 ≤ x ≤ 1: F(x) = $\int_{-1}^{x} \frac{1+αt}{2} dt$ = $\frac{1}{2}(x + 1) + \frac{α}{4}(x^2 − 1)$  
For x > 1: F(x) = 1  

Median  
The median is the value m such that F(m) = 0.5.  
Choosing the positive root gives:  
𝑚 = $\frac{−1 + \sqrt{1 + 𝛼^2}}{2𝛼}$(since 𝑚 must be in the interval [-1, 1])  

Find the First Quartile Q1  
CDF 𝐹(𝑄1) = 0.25  
​Q1 = $\frac{−1 + \sqrt{1 - 𝛼 + 𝛼^2}}{𝛼}$  

Find the Third Quartile Q3  
CDF 𝐹(𝑄3) = 0.75  
​Q3 = $\frac{−1 + \sqrt{1 - 4𝛼 + 3𝛼^2}}{𝛼}$  

## Q6. 

### Questions 

Sketch the pdf and cdf of a random variable that is uniform on [−1, 1].

### Answers

1. Probability Density Function
   The pdf of a uniform random variable X that is uniform on [−1,1] is defined as:  
f(x) =  
{ $\frac{1}{2}$ if −1 ≤ x ≤ 1  
{ 0 otherwise
​
2. Cumulative Distribution Function
   The cdf F(x) of a uniform random variable on [−1,1] is calculated as:  
F(x) =  
{ 0 if x < -1  
{ $\frac{x + 1}{2}$ if −1 ≤ x ≤ 1
{ 1 if x > 1

Sketch of the pdf and cdf  
![image](https://github.com/user-attachments/assets/3631470f-bd26-4256-b691-78566b8933ab)

