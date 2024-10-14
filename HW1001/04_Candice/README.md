## CH2.19
## Find an expression for the cumulative distribution function of a geometric random variable.

## Answer


The cumulative distribution function (CDF) of a geometric random variable  X , with success probability  p , is given by:

$$
F_X(x) = 1 - (1 - p)^{\lfloor x \rfloor} \quad \text{for} \quad x \geq 1
$$

where  \lfloor x \rfloor  is the greatest integer less than or equal to  x , and  p  is the probability of success in each trial.

## CH2.21
## If X is a geometric random variable, show that P(X > n + k − 1|X > n − 1) = P(X > k) In light of the construction of a geometric distribution from a sequence of independent Bernoulli trials, how can this be interpreted so that it is “obvious”?

## Answer


Given that  X  is a geometric random variable, we want to show that:

$$
P(X > n + k - 1 \mid X > n - 1) = P(X > k)
$$


1.	Conditional Probability Definition:
By the definition of conditional probability:
$$
P(X > n + k - 1 \mid X > n - 1) = \frac{P(X > n + k - 1 \text{ and } X > n - 1)}{P(X > n - 1)}
$$
Since  X > n + k - 1  implies  X > n - 1 , the intersection simplifies to:
$$
P(X > n + k - 1 \mid X > n - 1) = \frac{P(X > n + k - 1)}{P(X > n - 1)}
$$
	2.	Using the Geometric Distribution:
For a geometric random variable with success probability  p , we know that:
$$
P(X > m) = (1 - p)^m
$$
Applying this to the conditional probability:
$$
P(X > n + k - 1 \mid X > n - 1) = \frac{(1 - p)^{n + k - 1}}{(1 - p)^{n - 1}} = (1 - p)^k
$$
	3.	Simplifying:
This result shows:
$$
P(X > n + k - 1 \mid X > n - 1) = (1 - p)^k = P(X > k)
$$

Thus, we have shown that:

$$
P(X > n + k - 1 \mid X > n - 1) = P(X > k)
$$
## CH2.30
## Suppose that in a city, the number of suicides can be approximated by a Poisson process with λ = .33 per month.

## a. Find the probability of k suicides in a year for k = 0, 1, 2,... . What is the most probable number of suicides?

## b. What is the probability of two suicides in one week?

## Answer

a. Probability of  k  suicides in a year

The Poisson distribution formula is:

$$
P(X = k) = \frac{(\lambda t)^k e^{-\lambda t}}{k!}
$$

Here:
$$
\lambda = 0.33  suicides per month
t = 12  months in a year
\lambda t = 0.33 \times 12 = 3.96 
$$

The probability for  k  suicides in a year is:

$$
P(X = k) = \frac{(3.96)^k e^{-3.96}}{k!}
$$

For different values of  k :

$$
P(X = 0) \approx 0.019 
P(X = 1) \approx 0.075 
P(X = 2) \approx 0.148 
P(X = 3) \approx 0.195 
P(X = 4) \approx 0.193 
$$

The most probable number of suicides is 3.

b.Probability of two suicides in one week

To find the weekly rate of suicides:

$$
\lambda_{\text{week}} = \frac{0.33}{4.33} \approx 0.076  suicides per week
$$

For  k = 2  suicides in one week:

$$
P(X = 2) = \frac{(0.076)^2 e^{-0.076}}{2!} \approx 0.0027
$$

The probability of two suicides in one week is 0.0027 or 0.27%.

## CH2.33
##  Let F(x) = 1 − exp(−αx^β) for x ≥ 0,α > 0,β > 0, and F(x) = 0 for x < 0. Show that F is a cdf, and find the corresponding density.

## Answer

Given the cumulative distribution function (CDF):

\[
F(x) =
\begin{cases} 
1 - \exp(-\alpha x^\beta) & \text{for } x \geq 0 \\
0 & \text{for } x < 0 
\end{cases}
\]

where \( \alpha > 0 \) and \( \beta > 0 \), we will show that \( F(x) \) is a valid CDF and find the corresponding probability density function (PDF).

Validating \( F(x) \) as a CDF

For \( F(x) \) to be a valid CDF, it must satisfy:

1. **Non-decreasing**:
   - Since \( \exp(-\alpha x^\beta) \) is a decreasing function, \( F(x) = 1 - \exp(-\alpha x^\beta) \) is non-decreasing for \( x \geq 0 \).

2. **Limit properties**:
   - \( F(x) = 0 \) for \( x < 0 \).
   - As \( x \to \infty \), \( F(x) \to 1 \), which means \( F(x) \) approaches 1 as \( x \) becomes large.

3. **Range**:
   - \( F(x) \) is between 0 and 1 for all \( x \), so it is a valid CDF.

Finding the PDF

To find the PDF, we take the derivative of the CDF \( F(x) \). For \( x \geq 0 \):

\[
f(x) = \frac{d}{dx} \left( 1 - \exp(-\alpha x^\beta) \right)
\]

Using the chain rule:

\[
f(x) = \alpha \beta x^{\beta - 1} \exp(-\alpha x^\beta)
\]

For \( x < 0 \), the PDF is:

\[
f(x) = 0
\]

So,
The corresponding PDF is:

\[
f(x) =
\begin{cases}
\alpha \beta x^{\beta - 1} \exp(-\alpha x^\beta) & \text{for } x \geq 0 \\
0 & \text{for } x < 0
\end{cases}
\]

## CH2.34
## Let f(x) = (1+αx)/2 for −1 ≤ x ≤ 1 and f(x) = 0 otherwise, where −1 ≤ α ≤ 1. Show that f is a density, and find the corresponding cdf. Find the quartiles and the median of the distribution in terms of α.

## Answer 

$$
f(x) = \frac{1 + α x}{2} \quad \text{for} \quad -1 \leq x \leq 1
$$

$$
f(x) = 0 \quad \text{otherwise}
$$

where $-1 \leq α \leq 1$.

1. Showing $f(x)$ is a Probability Density Function (PDF)

To prove that $f(x)$ is a valid PDF, we need to verify:

1. **Non-Negativity**: $f(x) \geq 0$ for all $x$.
2. **Normalization**: The total area under the curve should equal 1, i.e., the integral of $f(x)$ over its range must be 1.

1.1 Non-Negativity

For $x$ in the interval $[-1, 1]$, we check whether $f(x)$ is non-negative:

$$
f(x) = \frac{1 + α x}{2}
$$

- When `α >= 0`, the minimum value occurs at `x = -1`, and:
 
$$ f(-1) = \frac{1 - α}{2} $$
  
  Since $-1 \leq α \leq 1$, we have $f(-1) \geq 0$.
  
- When $α < 0$, the minimum value occurs at $x = 1$, and:
  
$$ f(1) = \frac{1 + α}{2} $$
  
  Again, $f(1) \geq 0$ because $-1 \leq α \leq 1$.

Thus, $f(x)$ is non-negative for all $x$.


1.2 Normalization

We need to verify that the integral of $f(x)$ over $[-1, 1]$ equals 1:

$$
\int_{-1}^{1} \frac{1 + α x}{2} , dx
$$

Breaking it into two parts:

$$
\frac{1}{2} \int_{-1}^{1} 1 , dx + \frac{α}{2} \int_{-1}^{1} x , dx
$$

Evaluating both integrals:

- The integral of `1` over `[-1, 1]` is `2`.
 - The integral of `x` over `[-1, 1]` is `0`.

Thus, the total is:

$$
\frac{1}{2} \times 2 + \frac{α}{2} \times 0 = 1
$$

This confirms that the total area under $f(x)$ is 1, so $f(x)$ is a valid PDF.

2. Cumulative Distribution Function (CDF)

The cumulative distribution function $F(x)$ is the integral of the PDF from $-\infty$ to $x$.

$$
F(x) = 0 \quad \text{for} \quad x < -1
$$

For $-1 \leq x \leq 1$:

$$
F(x) = \int_{-1}^{x} \frac{1 + α t}{2} , dt
$$

Evaluating the integral:

$$
F(x) = \frac{x + 1}{2} + \frac{α (x^2 - 1)}{4}
$$

Thus, the CDF is:

$$
F(x) =
\begin{cases}
0 & \text{for } x < -1 \\
\frac{x + 1}{2} + \frac{\alpha (x^2 - 1)}{4} & \text{for } -1 \leq x \leq 1 \\
1 & \text{for } x > 1
\end{cases}
$$

3. Quartiles and Median

To find the quartiles and median, we solve for the values of $x$ that satisfy $F(x) = 0.25$, $F(x) = 0.5$, and $F(x) = 0.75$.

General Formula

For $F(x) = p$, we solve:

$$
\frac{x + 1}{2} + \frac{α (x^2 - 1)}{4} = p
$$

Multiplying both sides by 4:

$$
2(x + 1) + α (x^2 - 1) = 4p
$$

Simplifying:

$$
α x^2 + 2x + (2 - α - 4p) = 0
$$

This is a quadratic equation in $x$, which we can solve using the quadratic formula:

$$
x = \frac{-2 + \sqrt{4 - 4α (2 - α - 4p)}}{2α}
$$

Simplifying further:

$$
x = \frac{-1 + \sqrt{(1 - α)^2 + 4α p}}{α}
$$


Thus:

- First Quartile (p = 0.25):

$$
Q1 = \frac{-1 + \sqrt{1 - α + α^2}}{α}
$$
- Median (p = 0.5):

$$
Median = \frac{-1 + \sqrt{1 + α^2}}{α}
$$
- Third Quartile (p = 0.75):

$$
Q3 = \frac{-1 + \sqrt{1 + 3α + α^2}}{α}
$$



