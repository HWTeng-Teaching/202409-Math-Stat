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
Write python codes to illustration Ch02.65 for α=2
## Solution
```
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
def inverse_cdf(u):
  a = 1
  b = 1
  c =1 - 2* u
  discriminant = np.sqrt (b**2 - 4 * a * c)
  x1 = (-b + discriminant) / (2 * a)
  x2 = (-b - discriminant) / (2 * a)
  return np.where((x1 >= -1) & (x1 <= 1), x1, X2)
n_samples = 10000
U_samples = np.random.uniform(0, 1, size=n_samples)
X_samples = inverse_cdf(U_samples)
sns.histplot(X_samples, bins=30, kde=True, stat='density', color='purple', label= 'Generated X from U')
def theoretical_ pdfx, alpha=2):
  return (1 + alpha * x) / 2
x vals = np. linspace(-1, 1, 1000)
plt-plot(x_vals, theoretical_pdf(x_vals), 'r-', Iw=2, label='Theoretical PDF')
pit.title("Generated samples vs. Theoretical PDF")
plt.xlabel("X")
plt.ylabel("Density")
plt.legend()
plt.show()
```
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
