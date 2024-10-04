## Problem 19

Find an expression for the cumulative distribution function of a geometric random variable.

---

## Solution

We start by defining the geometric probability:

\[
P(X = k) = q^{k-1} p = (1 - p)^{k-1} p
\]

with \( k \) a nonzero integer.

The cumulative distribution function at \( x \) represents the probability of the random variable being smaller than or equal to \( x \):

\[
F(x) = P(X \leq x)
\]

If \( x < 1 \), then there are no values smaller than \( x \) that have a nonzero probability. Thus:

\[
F(x) = P(X \leq x) = 0
\]

If \( m \leq x < m+1 \) with \( m \) an integer, then we note that \( 1, 2, 3, \dots, m \) are smaller than or equal to \( x \):

\[
F(x) = P(X \leq x) = \sum_{k=1}^{m} P(X = k) = \sum_{k=1}^{m} (1 - p)^{k-1} p = p \sum_{k=1}^{m} (1 - p)^{k-1}
\]

This simplifies to:

\[
= p \frac{1 - (1 - p)^m}{1 - (1 - p)} = p \frac{1 - (1 - p)^m}{p} = 1 - (1 - p)^m
\]

Thus, combining these results, we obtain:

\[
F(x) = 
\begin{cases}
0 & x < 1 \\
1 - (1 - p)^m & m \leq x < m+1
\end{cases}
\]

where \( m \) is a positive integer.