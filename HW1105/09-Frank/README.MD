# Q1
## Problem
What are the key points in Lec 1105
## Solution
**Inverse method**: mapping jointly continuous random variables(change bases)

**Jacobian matrix and its determinant**
# Q2
## Problem
Explain what is the Leibniz integration rule
## Solution
**Statement:**

If f(x,t) is a function of x and t, and the partial derivatives $$\frac{\partial}{\partial x} \times f(x,t)$$ exist and are continuous, then:

$$
\frac{\partial}{\partial x} \left( \int_{a}^{b} f(x, t) \, dt \right) = \int_{a}^{b} \frac{\partial}{\partial x} \times f(x,t) \, dt
$$

**Explanation:**
- \( x \) is the parameter with respect to which we differentiate.
- \( t \) is the variable of integration.
- The limits \( a \) and \( b \) are constants.

This form of the Leibniz rule is useful in physics and engineering for problems involving integrals with parameters.
# Q3
## Problem
Identity the bivaraite normal disitriubtion of page 14 of the slides in class  
![image](https://github.com/user-attachments/assets/64286e1b-270c-4ef5-8b3b-1171ad29c7d2)
## Solution
The bivariate normal distribution identified on page 14 is characterized by the following joint density function:

$$
f_{Y_1, Y_2}(y_1, y_2) = \frac{1}{2 \pi \sigma_{Y_1} \sigma_{Y_2} \sqrt{1 - \rho^2}} \exp \left( -\frac{1}{2(1 - \rho^2)} \left( \frac{(y_1 - \mu_{Y_1})^2}{\sigma_{Y_1}^2} + \frac{(y_2 - \mu_{Y_2})^2}{\sigma_{Y_2}^2} - \frac{2 \rho (y_1 - \mu_{Y_1})(y_2 - \mu_{Y_2})}{\sigma_{Y_1} \sigma_{Y_2}} \right) \right).
$$

In this particular example:
- **Means**: $\mu_{Y_1} = 0$ and $\mu_{Y_2} = 0$,
- **Standard Deviations**: $\sigma_{Y_1} = 1$ and $\sigma_{Y_2} = 2$,
- **Correlation**: $\rho = \frac{1}{2}$.

Thus, the distribution is:

$$
(Y_1, Y_2) \sim N_2 \left( \begin{pmatrix} 0 \\ 0 \end{pmatrix}, \begin{pmatrix} 1 & \frac{1}{2} \\ \frac{1}{2} & 2 \end{pmatrix} \right),
$$

where $N_2$ denotes the bivariate normal distribution.
# Q4
## Problem
Use the inverse method to generate 1000 samples of stnadard normal
## Solution
![code](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1105/09-Frank/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-11-11%20204550.png)
![graph](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1105/09-Frank/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-11-11%20204611.png)
# Q5
## Problem
Use the polar method to generate 1000 samples of standard normal
## Solution
![code](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1105/09-Frank/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-11-11%20210013.png)
![graph](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1105/09-Frank/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-11-11%20210027.png)
