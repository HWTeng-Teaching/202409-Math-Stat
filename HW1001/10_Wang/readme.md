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




