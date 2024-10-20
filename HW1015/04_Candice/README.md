## Q1
## Write python codes to illustrate Propositions C and D

## Answer:

```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.stats as stats

# Proposition C: Simulate X ~ Exp(1) and calculate Z = F(X)
n_samples = 10000
X = np.random.exponential(scale=1, size=n_samples)  # X ~ Exp(1)
F_X = stats.expon.cdf(X)  # F(X) using the CDF of Exp(1), should follow Uniform(0,1)

# Proposition D: Simulate U ~ Uniform(0, 1) and calculate X = F^-1(U)
U = np.random.uniform(0, 1, size=n_samples)  # U ~ Uniform(0, 1)
F_inv_U = stats.expon.ppf(U)  # F^-1(U) using the inverse CDF (quantile function)

# Plot results for Proposition C
plt.figure(figsize=(12, 5))

plt.subplot(1, 2, 1)
plt.hist(F_X, bins=50, density=True, alpha=0.7, color='blue')
plt.title("Proposition C: Histogram of Z = F(X) \n(should be Uniform(0, 1))")
plt.xlabel("Z")
plt.ylabel("Density")

# Plot results for Proposition D
plt.subplot(1, 2, 2)
plt.hist(F_inv_U, bins=50, density=True, alpha=0.7, color='green')
plt.title("Proposition D: Histogram of X = F^-1(U) \n(should be Exp(1))")
plt.xlabel("X")
plt.ylabel("Density")

plt.tight_layout()
plt.show()
```
## Q2

## Q8
## Find the joint and marginal densities corresponding to the cdf

$$
F(x, y) = (1 - e^{-\alpha x})(1 - e^{-\beta y}), \quad x \geq 0, y \geq 0, \alpha > 0, \beta > 0
$$

## Answer:

### Joint Density
To find the joint density function \( f(x, y) \), differentiate the CDF \( F(x, y) \) with respect to both \( x \) and \( y \):

$$
f(x, y) = \frac{\partial^2 F(x, y)}{\partial x \partial y}
$$

First, differentiate \( F(x, y) \) with respect to \( x \):

$$
\frac{\partial F(x, y)}{\partial x} = \alpha e^{-\alpha x}(1 - e^{-\beta y})
$$

Then, differentiate with respect to \( y \):

$$
f(x, y) = \frac{\partial}{\partial y} \left[ \alpha e^{-\alpha x}(1 - e^{-\beta y}) \right] = \alpha e^{-\alpha x} \cdot \beta e^{-\beta y}
$$

Thus, the **joint density** is:

$$
f(x, y) = \alpha \beta e^{-\alpha x} e^{-\beta y}, \quad x \geq 0, y \geq 0
$$

### Marginal Density of \( X \)
To find the marginal density of \( X \), integrate the joint density over \( y \):

$$
f_X(x) = \int_0^\infty f(x, y) \, dy = \int_0^\infty \alpha \beta e^{-\alpha x} e^{-\beta y} \, dy = \alpha e^{-\alpha x}
$$

Thus, the marginal density of \( X \) is:

$$
f_X(x) = \alpha e^{-\alpha x}, \quad x \geq 0
$$

### Marginal Density of \( Y \)
Similarly, to find the marginal density of \( Y \), integrate the joint density over \( x \):

$$
f_Y(y) = \int_0^\infty f(x, y) \, dx = \int_0^\infty \alpha \beta e^{-\alpha x} e^{-\beta y} \, dx = \beta e^{-\beta y}
$$

Thus, the marginal density of \( Y \) is:

$$
f_Y(y) = \beta e^{-\beta y}, \quad y \geq 0
$$

