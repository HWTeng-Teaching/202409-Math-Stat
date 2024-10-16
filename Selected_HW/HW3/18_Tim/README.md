![photo](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/Selected_HW/HW3/18_Tim/IMG_0772.jpeg)

# Cumulative Distribution Function of a Geometric Random Variable

The cumulative distribution function (CDF) of a geometric random variable \( X \) with parameter \( p \) (the probability of success on each trial) is derived as follows:

1. The probability mass function (PMF) of a geometric random variable is:

   $P(X = k) = (1 - p)^{k-1} p \quad \text{for } k = 1, 2, 3, \dots$

2. The cumulative distribution function (CDF), \( F_X(k) \), is the probability that the random variable takes a value less than or equal to \( k \):

   $F_X(k) = P(X \leq k) = \sum_{i=1}^{k} P(X = i)$

3. Substitute the PMF into the sum:

   $F_X(k) = \sum_{i=1}^{k} (1 - p)^{i-1} p$

4. Since \( p \) is constant, factor it out of the sum:

   $F_X(k) = p \sum_{i=1}^{k} (1 - p)^{i-1}$

5. The sum of a geometric series is:

   $\sum_{i=0}^{k-1} r^i = \frac{1 - r^k}{1 - r}, \quad \text{for } |r| < 1$

6. Applying this formula with \( r = 1 - p \):

   $F_X(k) = p \cdot \frac{1 - (1 - p)^k}{1 - (1 - p)}$

7. Simplifying:

   $F_X(k) = 1 - (1 - p)^k$

Thus, the CDF of a geometric random variable \( X \) is:

$F_X(k) = 1 - (1 - p)^k \quad \text{for } k = 1, 2, 3, \dots$

This represents the cumulative probability that the first success occurs on or before the \( k \)-th trial.

