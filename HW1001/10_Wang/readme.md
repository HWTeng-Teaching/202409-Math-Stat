### Q1 : Find an expression for the cumulative distribution function of a geometric random variable.
Let \( X \) be a geometric random variable representing the number of trials until the first success, with success probability \( p \). The CDF is defined as:

$$ 
F_X(k) = P(X \leq k) 
$$

For a geometric distribution, the probability that the first success occurs on or before the \( k \)-th trial can be expressed as the sum of probabilities from the first trial to the \( k \)-th trial. The probability of having the first success on the \( n \)-th trial is given by:

$$ 
P(X = n) = (1 - p)^{n-1} p 
$$

Thus, the CDF can be computed as:

$$ 
F_X(k) = P(X \leq k) = \sum_{n=1}^{k} P(X = n) = \sum_{n=1}^{k} (1 - p)^{n-1} p 
$$

### Q2

To show that 

$$ 
P(X > n + k - 1 \mid X > n - 1) = P(X > k), 
$$ 

we can use the memoryless property of the geometric distribution.

The left-hand side can be expressed using the definition of conditional probability:

$$ 
P(X > n + k - 1 \mid X > n - 1) = \frac{P(X > n + k - 1 \cap X > n - 1)}{P(X > n - 1)}. 
$$

Since \(X > n + k - 1\) implies \(X > n - 1\), we have:

$$ 
P(X > n + k - 1 \cap X > n - 1) = P(X > n + k - 1). 
$$

Thus, we can rewrite the conditional probability as:

$$ 
P(X > n + k - 1 \mid X > n - 1) = \frac{P(X > n + k - 1)}{P(X > n - 1)}. 
$$

For a geometric random variable \(X\) with success probability \(p\):

$$ 
P(X > m) = (1 - p)^m. 
$$

Applying this to our expression, we have:

$$ 
P(X > n + k - 1) = (1 - p)^{n + k - 1}, 
$$
$$ 
P(X > n - 1) = (1 - p)^{n - 1}. 
$$

Substituting these into our conditional probability gives:

$$ 
P(X > n + k - 1 \mid X > n - 1) = \frac{(1 - p)^{n + k - 1}}{(1 - p)^{n - 1}} = (1 - p)^{k} = P(X > k). 
$$

In simple terms, if you have already failed in the first \(n - 1\) trials, the situation resets, and you only need to consider the next \(k\) trials as a new series of independent trials. This is what makes the memoryless property of the geometric distribution "obvious."

#### Q3

### a.
The Poisson distribution is given by the formula:

$$ 
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!} 
$$

where \( \lambda \) is the average rate of occurrences in the interval, and \( k \) is the number of occurrences.

Given that \( \lambda = 0.33 \) per month, the annual rate \( \lambda_{year} \) is:

$$ 
\lambda_{year} = 0.33 \times 12 = 3.96 
$$

Now, we calculate the probabilities for \( k = 0, 1, 2, \ldots \):

$$ 
P(X = 0) = \frac{3.96^0 e^{-3.96}}{0!} = e^{-3.96} \approx 0.0189 
$$

**For \( k = 1 \)**:

$$ 
P(X = 1) = \frac{3.96^1 e^{-3.96}}{1!} = 3.96 e^{-3.96} \approx 0.0755
$$

**For \( k = 2 \)**:

$$ 
P(X = 2) = \frac{3.96^2 e^{-3.96}}{2!} = \frac{3.96^2}{2} e^{-3.96} \approx 0.149
$$

**For \( k = 3 \)**:
   
$$ 
P(X = 3) = \frac{3.96^3 e^{-3.96}}{3!} = \frac{3.96^3}{6} e^{-3.96} \approx 0.197 
$$

**For \( k = 4 \)**:

$$ 
P(X = 4) = \frac{3.96^4 e^{-3.96}}{4!} = \frac{3.96^4}{24} e^{-3.96} \approx 0.1955 
$$

ans :The most probable number of suicides is where \( P(X = k) \) is maximized. From our calculations, both \( k = 3 \)  yield the highest probabilities. Thus, the most probable number of suicides in a year is 3 .

### b.

There are approximately 4.33 weeks in a month (52 weeks/year ÷ 12 months/year). Therefore, the weekly rate is:

$$ 
\lambda_{week} = \frac{0.33}{4.33} \approx 0.0763 
$$

Using the Poisson formula:

$$ 
P(X = 2) = \frac{0.0763^2 e^{-0.0763}}{2!} 
$$

Calculating this gives:

$$ 
P(X = 2) \approx \frac{0.0058 \cdot 0.9264}{2} \approx 0.0027 
$$

ans : **Probability of Two Suicides in One Week**: Approximately 0.0027

### Q4

Since \( F(x) \) satisfies all three properties of a CDF, it is a valid cumulative distribution function.


The probability density function \( f(x) \) is found by differentiating the CDF \( F(x) \):

$$ 
f(x) = \frac{d}{dx} F(x). 
$$

For \( x \geq 0 \):

$$ 
f(x) = \frac{d}{dx} \left( 1 - \exp(-\alpha x^\beta) \right) = 0 + \alpha \beta x^{\beta - 1} \exp(-\alpha x^\beta). 
$$

Thus, the probability density function is:

$$ 
f(x) = \alpha \beta x^{\beta - 1} \exp(-\alpha x^\beta) \quad \text{for } x \geq 0. 
$$

### Q5

Given the probability density function (PDF):

$$
f(x) = 
\begin{cases} 
\frac{1 + \alpha x}{2} & \text{for } -1 \leq x \leq 1 \\ 
0 & \text{otherwise} 
\end{cases}
$$

The cumulative distribution function \( F(x) \) is defined as:

## Calculation of the CDF

### 1. For \( x < -1 \)

For \( x < -1 \):

$$
F(x) = 0.
$$

### 2. For \( -1 \leq x \leq 1 \)

For \( -1 \leq x \leq 1 \):

We compute:

$$
F(x) = \int_{-1}^{x} \frac{1 + \alpha t}{2} \, dt.
$$

Breaking this into two parts:

1. **Integral of 1**:
   $$ 
   \int_{-1}^{x} 1 \, dt = x + 1. 
   $$

2. **Integral of \( t \)**:
   $$ 
   \int_{-1}^{x} t \, dt = \left[ \frac{t^2}{2} \right]_{-1}^{x} = \frac{x^2}{2} - \frac{1}{2} = \frac{x^2 - 1}{2}. 
   $$

Combining these results gives:

$$
F(x) = \frac{1}{2} (x + 1) + \frac{\alpha}{2} \left( \frac{x^2 - 1}{2} \right).
$$

This simplifies to:

$$
F(x) = \frac{x + 1}{2} + \frac{\alpha (x^2 - 1)}{4}.
$$

### 3. For \( x > 1 \)

For \( x > 1 \):

$$
F(x) = 1.
$$

## Final Form of the CDF

Thus, the cumulative distribution function \( F(x) \) is given by:

$$
F(x) = 
\begin{cases} 
0 & \text{for } x < -1 \\ 
\frac{x + 1}{2} + \frac{\alpha (x^2 - 1)}{4} & \text{for } -1 \leq x \leq 1 \\ 
1 & \text{for } x > 1 
\end{cases}.
$$

##Calculate Q1,Q2,Q3

Use completing square to caculate cdf function F(X) = 0.25 , F(X) = 0.5 , F(X) = 0.75

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



