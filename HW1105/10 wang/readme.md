# 	HW1106Q1

## Key Points:

### 1. Proposition A (Transformation of Joint Distributions)
- If \( X \) and \( Y \) are jointly distributed continuous random variables and we apply a transformation:
  \[
  u = g_1(x, y), \quad v = g_2(x, y),
  \]
  then the joint density of \( (U, V) \) is:
  \[
  f_{UV}(u, v) = f_{XY}(h_1(u, v), h_2(u, v)) \left| J \right|.
  \]

### 2. Proof Sketch
- The change of variables technique is used to derive the transformed joint density.

### 3. Example 1: Polar Coordinates Transformation
- Transform independent normal random variables \( X \) and \( Y \) into polar coordinates \( R \) and \( \theta \):
  \[
  f_{R\theta}(r, \theta) = \frac{1}{2\pi} r \exp\left(-\frac{r^2}{2}\right), \quad 0 \leq r, \ 0 \leq \theta \leq 2\pi.
  \]

### 4. Example 2: Linear Transformation of Normal Variables
- Given \( Y_1 = X_1 \) and \( Y_2 = X_1 + X_2 \), find the joint density of \( Y_1 \) and \( Y_2 \):
  \[
  f_{Y_1 Y_2}(y_1, y_2) = \frac{1}{2\pi} \exp\left(-\frac{1}{2} \left( 2y_1^2 + 2y_1 y_2 + y_2^2 \right) \right).
  \]

### 5. Finding Distributions of Transformed Variables
- Use Proposition A or differentiate the CDF to find the PDF of transformed variables.

### 6. Leibniz Integral Rule
- This rule allows differentiation under the integral sign when computing the PDF of transformed variables.

### 7. Convolution of Distributions
- The sum of independent random variables is the convolution of their individual distributions.

### 8. Example: Sum of Independent Exponential Random Variables
- The sum \( S = T_1 + T_2 \) of independent exponential variables follows a Gamma distribution.

### 9. Ratio of Random Variables
- For \( Z = Y/X \), the CDF and PDF can be derived by integrating over the joint density of \( X \) and \( Y \).

### 10. Example: Ratio of Normal Random Variables
- The ratio \( Z = Y/X \) follows a Cauchy distribution with:
  \[
  f_Z(z) = \frac{1}{\pi (1 + z^2)}.
  \]

# HW1106Q2

# Leibniz Integration Rule

The **Leibniz Integration Rule** is a formula for differentiating an integral with respect to a parameter. This rule is particularly useful when the limits of integration or the integrand depend on a variable that is being differentiated.

### Statement of the Leibniz Rule

Suppose you have an integral of the form:

$$
I(\alpha) = \int_{a(\alpha)}^{b(\alpha)} f(x, \alpha) \, dx,
$$

where:

$$
- \( f(x, \alpha) \) is a function of both \( x \) and a parameter \( \alpha \),
- The limits of integration \( a(\alpha) \) and \( b(\alpha) \) are functions of \( \alpha \).

$$
The Leibniz rule states that the derivative of the integral with respect to \( \alpha \) is:

$$
\frac{d}{d\alpha} I(\alpha) = \frac{d}{d\alpha} \int_{a(\alpha)}^{b(\alpha)} f(x, \alpha) \, dx = \int_{a(\alpha)}^{b(\alpha)} \frac{\partial}{\partial \alpha} f(x, \alpha) \, dx + f(b(\alpha), \alpha) \cdot b'(\alpha) - f(a(\alpha), \alpha) \cdot a'(\alpha).
$$

### Explanation

1. **The Integral of the Derivative**: 

   The first term, 

   $$
   \int_{a(\alpha)}^{b(\alpha)} \frac{\partial}{\partial \alpha} f(x, \alpha) \, dx,
   $$

   represents the change in the integral due to the direct dependence of the integrand on \( \alpha \).

2. **The Boundary Terms**: 

   The terms 

   $$
   f(b(\alpha), \alpha) \cdot b'(\alpha) \quad \text{and} \quad -f(a(\alpha), \alpha) \cdot a'(\alpha)
   $$

   account for the change in the limits of integration with respect to \( \alpha \). If the limits depend on \( \alpha \), the values of the integrand at the boundaries contribute to the rate of change of the integral.

### Example

Consider the following integral where the upper limit depends on a parameter \( \alpha \):

$$
I(\alpha) = \int_0^{\alpha} e^{-x^2} \, dx.
$$

To differentiate this with respect to \( \alpha \), apply the Leibniz rule:

$$
\frac{d}{d\alpha} I(\alpha) = e^{-\alpha^2} \cdot 1 - 0 \cdot 0 = e^{-\alpha^2}.
$$

Here, the integrand is \( e^{-x^2} \), and the upper limit is \( \alpha \), so the Leibniz rule gives us the derivative \( e^{-\alpha^2} \).

### Applications

- **Differentiating with Respect to a Parameter**: Leibniz's rule is useful for computing derivatives of integrals when the integrand or the limits depend on a parameter.
  
- **Changing Limits of Integration**: It can also be applied in cases where the limits of integration are functions of the parameter being differentiated.

- **Probability Theory**: In statistics, Leibniz's rule is frequently used when computing moments, expectation, or distributions that involve integrals with varying limits or integrands that depend on parameters.

### Conclusion

The Leibniz integration rule is a powerful tool for differentiating integrals with respect to parameters, especially when the limits of integration themselves are functions of that parameter. It generalizes the concept of differentiating an integral by handling both the changes in the integrand and the boundary terms.

# HW1106 Q3

# Q3: Identifying the Bivariate Normal Distribution

We are given that \(X_1\) and \(X_2\) are independent standard normal random variables, and we define new random variables \(Y_1\) and \(Y_2\) as follows:

$$
Y_1 = X_1, \quad Y_2 = X_1 + X_2
$$

### Step 1: Inverse Transformation

We want to express \(X_1\) and \(X_2\) in terms of \(Y_1\) and \(Y_2\). From the definitions:

$$
Y_1 = X_1 \quad \Rightarrow \quad X_1 = Y_1
$$

$$
Y_2 = X_1 + X_2 \quad \Rightarrow \quad X_2 = Y_2 - Y_1
$$

Thus, the inverse transformation is:

$$
X_1 = Y_1, \quad X_2 = Y_2 - Y_1
$$

### Step 2: Jacobian Determinant

To compute the joint pdf of \(Y_1\) and \(Y_2\), we need the Jacobian determinant of the transformation. The Jacobian matrix is:

$$
J = \begin{vmatrix}
\frac{\partial X_1}{\partial Y_1} & \frac{\partial X_1}{\partial Y_2} \\
\frac{\partial X_2}{\partial Y_1} & \frac{\partial X_2}{\partial Y_2}
\end{vmatrix}
= \begin{vmatrix}
1 & 0 \\
-1 & 1
\end{vmatrix} = 1
$$

### Step 3: Joint Probability Density Function (pdf)

Since \(X_1\) and \(X_2\) are independent standard normal random variables, their joint pdf is:

$$
f_{X_1, X_2}(x_1, x_2) = \frac{1}{2\pi} e^{-\frac{x_1^2 + x_2^2}{2}}
$$

Substituting the inverse transformation \(x_1 = y_1\) and \(x_2 = y_2 - y_1\), we get:

$$
f_{Y_1, Y_2}(y_1, y_2) = f_{X_1, X_2}(y_1, y_2 - y_1) \cdot |J|
$$

Since the Jacobian determinant is 1, we have:

$$
f_{Y_1, Y_2}(y_1, y_2) = \frac{1}{2\pi} e^{-\frac{y_1^2 + (y_2 - y_1)^2}{2}}
$$

Now, expand the term \((y_2 - y_1)^2\):

$$
(y_2 - y_1)^2 = y_2^2 - 2y_1y_2 + y_1^2
$$

So the joint pdf becomes:

$$
f_{Y_1, Y_2}(y_1, y_2) = \frac{1}{2\pi} e^{-\frac{y_1^2 + y_2^2 - 2y_1y_2 + y_1^2}{2}}
$$

Simplifying the expression:

$$
f_{Y_1, Y_2}(y_1, y_2) = \frac{1}{2\pi} e^{-\frac{2y_1^2 - 2y_1y_2 + y_2^2}{2}}
$$

Thus, the joint pdf is:

$$
f_{Y_1, Y_2}(y_1, y_2) = \frac{1}{2\pi} e^{-\frac{2y_1^2 - 2y_1y_2 + y_2^2}{2}} \quad \text{for} \quad -\infty \leq y_1, y_2 \leq \infty
$$

# HW1106 Q4
Use the polar method to generate 1000 samples of standard normal
![image](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1105/10%20wang/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-11-12%20161129.png)

![image](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1105/10%20wang/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-11-12%20161137.png)


# HW 1106 Q5
![image](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1105/10%20wang/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-11-12%20161403.png)

![image](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1105/10%20wang/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-11-12%20161409.png)

