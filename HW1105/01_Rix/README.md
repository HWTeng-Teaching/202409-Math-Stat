# 01_Rix

by 周子揚 Rix

## Q1. 

### Questions 

What are the key points in Lec 1105

### Answers

Functions of jointly distributed random variables  
![image](https://github.com/user-attachments/assets/17cd7c52-2442-464c-b4d5-bfb91bb21527)  
Inverse method, Polar method, Chi distribution  
Leibniz integral rule  
Sums of random variables

## Q2. 

### Questions 

Explain what is the Leibniz integration rule

### Answers

![image](https://github.com/user-attachments/assets/52e35e04-2a85-41df-b9f1-fd764f628d9e)
![image](https://github.com/user-attachments/assets/9c571e9b-50e6-4ba0-8a45-b703e4859ebf)
![image](https://github.com/user-attachments/assets/e680ff5e-5d19-41b9-8cfb-83e97f22afd2)


## Q3. 

### Questions 

Identity  the bivaraite normal disitriubtion of page 14 of the slides in class  
![image](https://github.com/user-attachments/assets/64286e1b-270c-4ef5-8b3b-1171ad29c7d2)


### Answers

![image](https://github.com/user-attachments/assets/136eaedf-9e25-4804-b2d1-031505b399b1)
![image](https://github.com/user-attachments/assets/a91ba58f-e509-4381-ac4b-9071283e4d2b)


## Q4. 

### Questions 

Use the inverse method to generate 1000 samples of stnadard normal

### Answers

```
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import norm

uniform_samples = np.random.uniform(0, 1, 1000)
normal_samples = norm.ppf(uniform_samples)

plt.hist(normal_samples, bins=50, density=True, alpha=0.5, color='skyblue', edgecolor='black')
xmin, xmax = plt.xlim()
x = np.linspace(xmin, xmax, 1000)
plt.plot(x, norm.pdf(x), 'r', lw=2, label='Standard Normal PDF')
plt.xlabel('Value')
plt.ylabel('Density')
plt.title('Histogram of Generated Standard Normal Samples')
plt.legend()
plt.show()
```
![11](https://github.com/user-attachments/assets/f63b28b3-6b12-4251-b806-8dfa4b8ba8d0)


## Q5. 

### Questions 

Use the polar method to generate 1000 samples of standard normal

### Answers

```
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import norm

num_samples = 1000
samples = []

while len(samples) < num_samples:
    u, v = np.random.uniform(-1, 1, 2)
    s = u**2 + v**2

    if s == 0 or s >= 1:
        continue

    factor = np.sqrt(-2 * np.log(s) / s)
    samples.append(u * factor)
    if len(samples) < num_samples:
        samples.append(v * factor)

plt.hist(samples, bins=50, density=True, alpha=0.5, color='skyblue', edgecolor='black')
xmin, xmax = plt.xlim()
x = np.linspace(xmin, xmax, 1000)
plt.plot(x, norm.pdf(x), 'r', lw=2, label='Standard Normal PDF')
plt.xlabel('Value')
plt.ylabel('Density')
plt.title('Histogram of Standard Normal Samples (Polar Method)')
plt.legend()
plt.show()
```
![12](https://github.com/user-attachments/assets/a3a4a5d4-a650-4d2d-8df5-f5abcf237783)

