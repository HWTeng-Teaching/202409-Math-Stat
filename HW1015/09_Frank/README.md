## Q1
Write python codes to illustrate Propositions C and D (suppose $X\sim exp(1)$)
## Solution
```
import numpy as np
import matplotlib-pyplot as plt
import seaborn as sns
np. random. seed (42)
n_samples = 10000
X_ samples = np. random. exponential(scale=1, size=n_samples)
Z_ samples = 1 - np. exp(-X_samples)
sns.histplot(Z_samples, bins=30, kde=True, color='blue')
plt. title("Histogram of Z = F(X) (Should follow Uniform[0,1])")
plt.xlabel ("Z")
plt.ylabel ("Density")
plt.show()
from scipy.stats import kstest
ks_statistic, p_value = kstest(Z_samples, 'uniform', args=(0, 1))
print(f"Kolmogorov-Smirnov Test Statistic: (ks_statistic}")
print (f"p-value: {p_value)")
```
```
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy.stats import expon
np.random.seed(42)
n_samples = 10000
U_samples = np.random.uniform(0, 1, size=n_samples)
X_samples = -np.log(1 - U_samples)
sns.histplot(X_samples, bins=30, kde=True, stat='density', color='green', label='Generated X from U')
x_vals = np.linspace(0, 10, 1000)
plt.plot(x_vals, expon.pdf(x_vals), 'r-', lw=2, label='Exp(1) PDF (Theoretical)')
plt.title("Histogram of X = F^-1(U)(Should follow Exp(1))")
plt.xlabel("X")
plt.ylabel("Density")
plt.legend()
plt.show()
from scipy.stats import kstest
ks_statistic, p_value = kstest(x_samples, 'expon', args=(0, 1))
print (f"Kolmogorov-Smirnov Test Statistic: {ks_statistic}")
print (f"p-value: {p_value}")
```
## Q2
## Solution
## Q3
## Solution
## Q4
## Solution
## Q5
## Solution
## Q6
## Solution
## Q7
## Solution
## Q8
## Solution
