## Q19
For a geometric distribution with probability mass function (PMF):

P(X = k) = $p(1-p)^{k-1}$,k = 1,2,3,...

F(k) = P(X $\le$ k) = $$\sum_{i=1}^k$$ $P(X=i)$  

F(k) = $p$ $$\sum_{i=1}^k$$ $(1-p)^{i-1}$  

This is a geometric series with first term a = 1 and common ratio r = 1 - p.

$$\sum_{i=1}^k$$ $(1-p)^{i-1}$ = $\frac{1-(1-p)^{k}}{1-(1-p)}$

Thus, CDF: $F(k) = 1-(1-p)^k, k = 1,2,3,...  $
