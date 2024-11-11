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
# Q3
## Problem
Identity  the bivaraite normal disitriubtion of page 14 of the slides in class  
![image](https://github.com/user-attachments/assets/64286e1b-270c-4ef5-8b3b-1171ad29c7d2)
## Solution
The **Leibniz rule for integration** provides a way to differentiate an integral with variable limits or a variable integrand. There are two common forms of the Leibniz rule: 

1. **Leibniz Integral Rule (Differentiation under the Integral Sign)**
2. **Leibniz Rule for Differentiation of an Integral with Variable Limits**

### 1. Leibniz Integral Rule (Differentiation under the Integral Sign)

This rule allows you to differentiate an integral whose integrand depends on a parameter.

**Statement:**

If \( f(x, t) \) is a function of \( x \) and \( t \), and the partial derivatives \( \frac{\partial}{\partial x} f(x, t) \) exist and are continuous, then:

\[
\frac{d}{dx} \left( \int_{a}^{b} f(x, t) \, dt \right) = \int_{a}^{b} \frac{\partial}{\partial x} f(x, t) \, dt
\]

**Explanation:**
- \( x \) is the parameter with respect to which we differentiate.
- \( t \) is the variable of integration.
- The limits \( a \) and \( b \) are constants.

This form of the Leibniz rule is useful in physics and engineering for problems involving integrals with parameters.

### Example:

Consider the integral:

\[
I(x) = \int_{0}^{1} (x^2 + t^2) \, dt
\]

To find \( I'(x) \), we apply the Leibniz rule:

\[
I'(x) = \int_{0}^{1} \frac{\partial}{\partial x} (x^2 + t^2) \, dt = \int_{0}^{1} 2x \, dt = 2x \cdot \left( \int_{0}^{1} dt \right) = 2x
\]

### 2. Leibniz Rule for Differentiation of an Integral with Variable Limits

This rule extends the concept to integrals where the limits themselves are functions of \( x \).

**Statement:**

If \( f(x, t) \) is continuous and \( a(x) \) and \( b(x) \) are differentiable functions of \( x \), then:

[
frac{d}{dx} left( int_{a(x)}^{b(x)} f(x, t) , dt right) = fbig(x, b(x)big) cdot b'(x) - fbig(x, a(x)big) cdot a'(x) + int_{a(x)}^{b(x)} frac{partial}{partial x} f(x, t) , dt
]

**Explanation:**
- The first two terms account for the changes in the limits ( a(x) ) and ( b(x) ).
- The last term accounts for the change in the integrand with respect to ( x ).
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
