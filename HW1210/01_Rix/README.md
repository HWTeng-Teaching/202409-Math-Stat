# 01_Rix

by 周子揚 Rix

## Q1. 

### Questions 

![image](https://github.com/user-attachments/assets/f39cd2e6-577d-4cca-a866-171c12552e98)


### Answers

![image](https://github.com/user-attachments/assets/88ee10e8-a9ea-4dd8-85f8-84454f0368de)


## Q2. 

### Questions 

![image](https://github.com/user-attachments/assets/808638a4-2cf7-4bd3-aacd-dbb71b415567)


### Answers

![image](https://github.com/user-attachments/assets/1d697e7d-def2-44ac-95bb-77639d1bd1f3)


## Q3. 

### Questions 

![image](https://github.com/user-attachments/assets/4201ed45-e4ae-4107-be59-2afde640afa1)


### Answers

![image](https://github.com/user-attachments/assets/96e2fad6-0660-478c-aa0d-aa81286e9a37)


## Q4. 

### Questions 

![image](https://github.com/user-attachments/assets/5dae1f26-0c17-4416-8c5e-8e116c1bf3b0)


### Answers

![image](https://github.com/user-attachments/assets/1f78e6f5-e908-4f24-b8f5-a84b12cdc062)


## Q5. 

### Questions 

![image](https://github.com/user-attachments/assets/893b2ee9-a14d-492d-97ab-0366d00696df)  
![image](https://github.com/user-attachments/assets/3e21f01a-cd51-4a02-8964-53c5ba0e6b15)


### Answers

![image](https://github.com/user-attachments/assets/41f8e728-a605-486f-a928-c2fa8de67bec)


## Q6. 

### Questions 

![image](https://github.com/user-attachments/assets/a73232b1-0e45-4a4a-a300-1909236c251c)
![image](https://github.com/user-attachments/assets/77edd8bd-862b-40a8-88e6-cd241b699a08)


### Answers

![image](https://github.com/user-attachments/assets/e55b874a-df46-4c1c-89ac-4cadcb99931e)
![image](https://github.com/user-attachments/assets/796886c7-4e54-4cea-95a2-d6f56debec21)


## Q7. 

### Questions 

![image](https://github.com/user-attachments/assets/fd6ff620-8a35-4176-b1f4-68f8e0b49ca0)


### Answers

![image](https://github.com/user-attachments/assets/9927b7c2-2f32-4a3d-8019-cb4f7d791c3a)


## Q8. 

### Questions 

![image](https://github.com/user-attachments/assets/749b708a-7c03-4f8c-b5c6-8c7c42306a31)
![image](https://github.com/user-attachments/assets/74f6bd34-09dd-4e0f-94e8-420f7315264a)


### Answers

![image](https://github.com/user-attachments/assets/58c72256-0630-48fa-b3c5-2d00c2106dba)


## Q9. 

### Questions 

![image](https://github.com/user-attachments/assets/74b340d2-f7e5-4300-8733-406c8961ed9c)


### Answers

```
import numpy as np
import matplotlib.pyplot as plt

# Parameters
mu = 0
sigma = 10
n = 25  # sample size
num_samples = 1000  # number of samples to generate

# Generate samples from N(mu, sigma^2)
samples = np.random.normal(mu, sigma, (num_samples, n))

# Calculate sample means (X-bar) and sample variances (s^2)
sample_means = np.mean(samples, axis=1)
sample_variances = np.var(samples, axis=1, ddof=1)  # Using ddof=1 for unbiased estimator of variance

# Plot the sampling distributions
fig, axs = plt.subplots(1, 2, figsize=(12, 6))

# Plot the distribution of X-bar (sample means)
axs[0].hist(sample_means, bins=30, color='skyblue', edgecolor='black', alpha=0.7)
axs[0].set_title('Sampling Distribution of X-bar')
axs[0].set_xlabel('Sample Mean (X-bar)')
axs[0].set_ylabel('Frequency')

# Plot the distribution of s^2 (sample variances)
axs[1].hist(sample_variances, bins=30, color='lightgreen', edgecolor='black', alpha=0.7)
axs[1].set_title('Sampling Distribution of Sample Variance (s^2)')
axs[1].set_xlabel('Sample Variance (s^2)')
axs[1].set_ylabel('Frequency')

# Show the plots
plt.tight_layout()
plt.show()
```
![image](https://github.com/user-attachments/assets/6f77ffba-3dc3-4695-9532-4e97d91852c9)
