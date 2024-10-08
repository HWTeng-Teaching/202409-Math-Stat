## Q19
For a geometric distribution with probability mass function (PMF):

P(X = k) = $p(1-p)^{k-1}$,k = 1,2,3,...

F(k) = P(X $\le$ k) = $$\sum_{i=1}^k$$ $P(X=i)$  

F(k) = $p$ $$\sum_{i=1}^k$$ $(1-p)^{i-1}$  

This is a geometric series with first term a = 1 and common ratio r = 1 - p.

$$\sum_{i=1}^k$$ $(1-p)^{i-1}$ = $\frac{1-(1-p)^{k}}{1-(1-p)}$

Thus, CDF: $F(k) = 1-(1-p)^k, k = 1,2,3,...  $

## Q21
$P(x > n+k-1|X> n-1)$ = $\frac{P(X>n+k-1 \cap X>n-1)}{P(X>n-1)}$

since $x > n + k -1$ implies $x > n - 1$

$P(X>n+k-1 \cap X>n-1)$ can be simplified as $P(X>n+k-1)$

according to CDF, $P(X>k) = (1-p)^k$

$P(x > n+k-1|X> n-1)$ = $\frac{(1-p)^{n+k-1}}{(1-p)^{n-1}}$ = $(1-p)^k$

So it is obvious that $P(x > n+k-1|X> n-1)$ = $P(x>k)$

## Q30
### a.
$\lambda_{year}$ = $0.33 \times 12 = 3.96$

$p(X=k) = \frac{e^{-\lambda}\lambda^{k}}{k!}$

$P(X=0) \approx 0.0191$ , $P(X=1) \approx 0.0755$ , $P(X=2) \approx 0.1495$ , $P(X=3) \approx 0.1973$

$P(X=4) \approx 0.1953$ , $P(X=5) \approx 0.1547$ , $P(X=6) \approx 0.1021$ , $P(X=7) \approx 0.0578$

The most probable number of suicides is 3.
### b.
$\lambda_{week}$ = $\frac{3.96}{52} \approx 0.0762