### HW1015 Q1

<img width="1022" alt="截圖 2024-10-14 上午9 43 20" src="https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1015/10_Wang/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-10-22%20155202.png">

### HW1015 Q2

<img width="1022" alt="截圖 2024-10-14 上午9 43 20" src="https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1015/10_Wang/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-10-22%20164524.png">

<img width="1022" alt="截圖 2024-10-14 上午9 43 20" src="https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1015/10_Wang/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-10-22%20164529.png">

### HW1015 Q3

$$
Let \( Z \sim N(\mu, \sigma^2) \). To find the density function of \( Y = e^Z \), we follow these steps:
$$

## Step 1: Find the CDF of \( Y \)

1. Since \( Y = e^Z \), we express \( Z \) in terms of \( Y \):

   $$
   Z = \ln(Y)
   $$

2. The cumulative distribution function (CDF) of \( Y \) is given by:
   
   $$
   F_Y(y) = P(Y \leq y) = P(e^Z \leq y) = P(Z \leq \ln(y)) \quad \text{for } y > 0
   $$

3. The CDF of \( Z \) is:
    
   $$
   F_Z(z) = \Phi\left(\frac{z - \mu}{\sigma}\right)
   $$
   
   where \( \Phi \) is the CDF of the standard normal distribution.


5. Therefore, the CDF of \( Y \) can be expressed as:
   
   $$
   F_Y(y) = \Phi\left(\frac{\ln(y) - \mu}{\sigma}\right) \quad \text{for } y > 0
   $$

## Step 2: Differentiate to Find the PDF of \( Y \)

1. To find the PDF \( f_Y(y) \), we differentiate the CDF:
    
   $$
   f_Y(y) = \frac{d}{dy} F_Y(y)
   $$

2. Using the chain rule:

   $$
   f_Y(y) = \frac{d}{dy} \Phi\left(\frac{\ln(y) - \mu}{\sigma}\right) = \phi\left(\frac{\ln(y) - \mu}{\sigma}\right) \cdot \frac{1}{\sigma y}
   $$
   
   where \( \phi \) is the PDF of the standard normal distribution, given by:
   
   $$
   \phi(z) = \frac{1}{\sqrt{2\pi}} e^{-\frac{z^2}{2}}
   $$

4. Substituting back:
    
   $$
   f_Y(y) = \frac{1}{\sigma y} \cdot \phi\left(\frac{\ln(y) - \mu}{\sigma}\right)
   $$

5. Substituting \( \phi \):
   
   $$
   f_Y(y) = \frac{1}{\sigma y \sqrt{2\pi}} e^{-\frac{(\ln(y) - \mu)^2}{2\sigma^2}}
   $$

## Final Form of the Lognormal Density Function

Thus, the PDF of \( Y = e^Z \) is given by:
   
   
   $$
   f_Y(y) = \frac{1}{\sigma y \sqrt{2\pi}} e^{-\frac{(\ln(y) - \mu)^2}{2\sigma^2}}, \quad y > 0
   $$


This function is known as the **lognormal density function**, as it describes a random variable whose logarithm is normally distributed.
