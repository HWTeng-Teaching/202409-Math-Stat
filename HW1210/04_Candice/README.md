![Page01](https://github.com/user-attachments/assets/79258594-a7bb-4e6f-b16d-50b5100717f1)
![Page02](https://github.com/user-attachments/assets/b8b9f958-fcc9-4968-85e7-0e01c39e50e0)
![Page03](https://github.com/user-attachments/assets/4e71a94f-f9a2-4f5a-81b3-fc103b329f40)
![Page04](https://github.com/user-attachments/assets/8566b04e-8a60-488c-8622-7ad535a29a30)
![Page05](https://github.com/user-attachments/assets/edd4cc02-b6c0-4b04-8dee-86b6cf369496)
![Page06](https://github.com/user-attachments/assets/a9f62353-9666-4de7-8247-3e78f7535e19)
![Page07](https://github.com/user-attachments/assets/0be3bede-bb26-4f59-bb74-75a801c7fdb6)
![Page08](https://github.com/user-attachments/assets/517894d9-1258-4235-be93-c67ca05570f5)
![Page09](https://github.com/user-attachments/assets/0697e3b0-a246-4f0c-b920-43bc5c63b13c)
![Page10](https://github.com/user-attachments/assets/edf07e4e-b170-40ba-b0d6-f38625590752)

# Q9
# Answer

```python
import numpy as np
import matplotlib.pyplot as plt

# Parameters
mu = 0  # Mean
sigma = 10  # Standard deviation
n = 25  # Sample size
num_samples = 1000  # Number of samples to simulate

# Initialize arrays to store sample statistics
sample_means = []
sample_variances = []

# Generate samples and calculate sample means and variances
for _ in range(num_samples):
    sample = np.random.normal(mu, sigma, n)  # Generate n samples
    sample_mean = np.mean(sample)  # Compute sample mean
    sample_variance = np.var(sample, ddof=1)  # Compute unbiased sample variance
    
    sample_means.append(sample_mean)
    sample_variances.append(sample_variance)

# Plot the sampling distribution of the sample mean
plt.figure(figsize=(12, 5))

plt.subplot(1, 2, 1)
plt.hist(sample_means, bins=30, density=True, alpha=0.7, edgecolor='black')
plt.title("Sampling Distribution of Sample Mean")
plt.xlabel("Sample Mean")
plt.ylabel("Density")

# Plot the sampling distribution of the sample variance
plt.subplot(1, 2, 2)
plt.hist(sample_variances, bins=30, density=True, alpha=0.7, edgecolor='black')
plt.title("Sampling Distribution of Sample Variance")
plt.xlabel("Sample Variance")
plt.ylabel("Density")

plt.tight_layout()
plt.show()


``` 


![IMG_2878586EE195-1](https://github.com/user-attachments/assets/910b640d-87a9-4390-8d65-38a2c13cbd16)
