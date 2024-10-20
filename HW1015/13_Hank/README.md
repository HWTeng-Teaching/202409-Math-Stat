## Q1
write python code to illustrate Proposition C and D (suppose $X\sim \exp(1)$)
![image](https://github.com/user-attachments/assets/6294fce0-1d59-49cf-989d-59285bf6f3d1)
![image](https://github.com/user-attachments/assets/d3ecdd17-a5c7-4c24-af0d-6d349e0f08f0)
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import norm

# Number of samples
n_samples = 10000

# Proposition C: F(X) -> Uniform(0, 1)
# Generate samples from a normal distribution
X = np.random.normal(0, 1, n_samples)

# Apply the CDF of the normal distribution to transform X
Z = norm.cdf(X)

# Proposition C: Z should now be uniformly distributed
plt.figure(figsize=(10, 4))
plt.subplot(1, 2, 1)
plt.hist(Z, bins=30, density=True, alpha=0.6, color='g')
plt.title("Proposition C: Z = F(X) ~ Uniform(0, 1)")

# Proposition D: Inverse transformation from Uniform(0, 1) to X
# Generate uniform samples between [0, 1]
U = np.random.uniform(0, 1, n_samples)

# Apply the inverse CDF (percent point function) of the normal distribution
X_inverse = norm.ppf(U)

# Proposition D: X_inverse should now be normally distributed
plt.subplot(1, 2, 2)
plt.hist(X_inverse, bins=30, density=True, alpha=0.6, color='b')
plt.title("Proposition D: X = F^(-1)(U) ~ N(0, 1)")

plt.tight_layout()
plt.show()
```

## Q2
write python code to illustration Ch02.65 for $\alpha$ = $0.5$
![image](https://github.com/user-attachments/assets/3c6c69f0-4306-41de-86ea-229763a8f578)

```python
import numpy as np
import matplotlib.pyplot as plt

# Define the inverse CDF for α = 2
def inverse_cdf(u):
    # This is derived from solving the quadratic equation for the CDF of α = 2
    # F(x) = 0.5 * (x + x^2 + 1), solve for x in terms of u
    return (-1 + np.sqrt(1 + 4*u)) / 2

# Number of samples
n_samples = 10000

# Generate uniform random numbers
U = np.random.uniform(0, 1, size=n_samples)

# Apply the inverse CDF to get samples from the target distribution
X = inverse_cdf(U)

# Plot the histogram of the generated samples
plt.hist(X, bins=50, density=True, alpha=0.7, color='purple', label='Generated Samples')

# Plot the actual PDF for comparison
x_vals = np.linspace(-1, 1, 500)
pdf_vals = (1 + 2*x_vals) / 2
plt.plot(x_vals, pdf_vals, 'r-', label='PDF (α=2)')

plt.title("Generated Samples vs PDF for α = 2")
plt.xlabel("x")
plt.ylabel("Density")
plt.legend()
plt.show()
```
![2041d285-ca34-4608-abc9-46a14493a66d](https://github.com/user-attachments/assets/27af9661-ae57-4bf7-a5e1-9b21895ec71a)
