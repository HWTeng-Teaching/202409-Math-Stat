## Q1: What are the key points in Lec 1105

<img width="876" alt="截圖 2024-11-12 凌晨12 08 37" src="https://github.com/user-attachments/assets/5b451d61-ef63-4eaa-829a-ee0cb63f7698">
<img width="817" alt="截圖 2024-11-12 凌晨12 09 22" src="https://github.com/user-attachments/assets/d2139cee-63d6-4074-8ab9-3694d5c9f457">

## Q2: Explain what is the Leibniz integration rule
$$\frac{d}{d𝑧}\left(\int_{a(𝑧)}^{b(𝑧)} f(𝑧, u)du\right)\=f\left(𝑧, b(𝑧)\right)\frac{d}{d𝑧}b(𝑧)-f\left(𝑧, a(z)\right)\frac{d}{d𝑧}a(𝑧)+\int_{a(𝑧)}^{b(𝑧)} \frac{d}{d𝑧}f(𝑧, u)du$$

1. The first term represents the effect of changes in the upper limit $$b(𝑧)$$ with respect to 𝑧.
2. The second term represents the effect of changes in the upper limit $$a(𝑧)$$ with respect to 𝑧.
3. The third term represents the effect of changes in 𝑧 within the integrand 𝑓(𝑧,𝑢) itself.

## Q3: Identity  the bivaraite normal disitriubtion of page 14 of the slides in class
<img width="931" alt="截圖 2024-11-12 凌晨2 00 32" src="https://github.com/user-attachments/assets/dcd05242-fe65-42d6-8613-07c596faf8f4">

## Q4: Use the inverse method to generate 1000 samples of standard normal
```
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import norm

# Step 1: Generate 1000 samples
uniform_samples = np.random.uniform(0, 1, 1000)
normal_samples = norm.ppf(uniform_samples)

# Step 2: Plot histogram of samples
plt.hist(normal_samples, bins=30, density=True, alpha=0.6, color='skyblue', edgecolor='black')

# Step 3: Overlay the standard normal distribution curve for comparison
x = np.linspace(-4, 4, 1000)
plt.plot(x, norm.pdf(x), 'r-', lw=2, label='Standard Normal PDF')

# Step 4: Add labels and legend
plt.xlabel('Value')
plt.ylabel('Density')
plt.legend()
plt.title('Histogram of Generated Samples vs. Standard Normal Distribution')
plt.show()
```
<img width="508" alt="截圖 2024-11-12 凌晨2 07 09" src="https://github.com/user-attachments/assets/4a1c084d-2b39-4fb8-bb76-282b1468f497">

## Q5: Use the polar method to generate 1000 samples of standard normal
```
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import norm

normal_samples = []

while len(normal_samples) < 1000:
    # Step 1: Generate two uniform random variables in the range [-1, 1]
    u1, u2 = np.random.uniform(-1, 1, 2)
    
    # Step 2: Calculate S
    S = u1**2 + u2**2
    
    # Step 3: Check if S is in the unit circle (S < 1)
    if S < 1 and S > 0:  # Ensure S is positive to avoid division by zero
        # Step 4: Calculate the two normal samples
        multiplier = np.sqrt(-2 * np.log(S) / S)
        z1 = u1 * multiplier
        z2 = u2 * multiplier
        normal_samples.append(z1)
        normal_samples.append(z2)

normal_samples = normal_samples[:1000]
normal_samples = np.array(normal_samples)  # Optional: convert to numpy array

plt.hist(normal_samples, bins=30, density=True, alpha=0.6, color='skyblue', edgecolor='black')

x = np.linspace(-4, 4, 1000)
plt.plot(x, norm.pdf(x), 'r-', lw=2, label='Standard Normal PDF')

plt.xlabel('Value')
plt.ylabel('Density')
plt.legend()
plt.title('Histogram of Polar Method Samples vs. Standard Normal Distribution')
plt.show()
```
<img width="517" alt="截圖 2024-11-12 凌晨2 12 16" src="https://github.com/user-attachments/assets/aa2f6a7a-2563-4668-a982-a6534e641178">
