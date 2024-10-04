## Problem 19

Find an expression for the cumulative distribution function of a geometric random variable.

---

## Solution

### Definition of Geometric Probability:

The probability mass function of a geometric random variable is given by:

\[ P(X = k) = q^{k-1} p = (1 - p)^{k-1} p \]

where \( k \) is a nonzero integer.

### Cumulative Distribution Function (CDF):

The cumulative distribution function at \( x \) represents the probability that the random variable is less than or equal to \( x \):

\[ F(x) = P(X ≤ x) \]

#### Case 1: \( x < 1 \)

If \( x < 1 \), then there are no values smaller than \( x \) that have a nonzero probability. Thus, the CDF is:

\[ F(x) = P(X ≤ x) = 0 \]

#### Case 2: \( m ≤ x < m + 1 \)

If \( m ≤ x < m + 1 \) where \( m \) is an integer, the values \( 1, 2, 3, …, m \) are less than or equal to \( x \). Therefore, the cumulative probability is the sum of the individual probabilities:

\[ F(x) = P(X ≤ x) = \sum_{k=1}^{m} P(X = k) = \sum_{k=1}^{m} (1 - p)^{k-1} p \]

This simplifies to:

\[ F(x) = p \sum_{k=1}^{m} (1 - p)^{k-1} \]

This is a geometric series that sums to:

\[ F(x) = p \frac{1 - (1 - p)^m}{1 - (1 - p)} = p \frac{1 - (1 - p)^m}{p} = 1 - (1 - p)^m \]

### Final Expression:

Combining these results, the cumulative distribution function is:

\[
F(x) =
\begin{cases}
0 & \text{if } x < 1 \\
1 - (1 - p)^m & \text{if } m ≤ x < m + 1
\end{cases}
\]

where \( m \) is a positive integer.