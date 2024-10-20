## Q1
Write python codes to illustrate Propositions C and D (suppose $X\sim exp(1)$)
## Solution
```
import numpy as np import matplotlib-pyplot as plt import seaborn as sns
np. random. seed (42)
n_samples = 10000
X_ samples = np. random. exponential(scale=1, size=n_samples)
_ samples = 1 - np. exp(-_samples)
sns.histplot(Z_samples, bins=30, kde=True, color='blue')
plt. title("Histogram of Z = F(X) (Should follow Uniform[®,1])")
plt.xlabel ("z")
plt. ylabel ("Density")
plt. show
from scipy.stats import kstest
ks_statistic, P_value = kstestZ samples, 'uniform', args=(0, 1)D
print(f"Kolmogorov-Smirnov Test Statistic: (ks_statistic}")
print (f"p-value: {p_value)")
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
