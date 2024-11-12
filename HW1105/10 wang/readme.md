# Key Points from Chapter 3.6: Functions of Jointly Distributed Random Variables

## 1. Jointly Distributed Random Variables
- Consider two continuous random variables \( X \) and \( Y \) that are jointly distributed.
- The variables are transformed into new variables \( U \) and \( V \) using the functions \( u = g_1(x, y) \) and \( v = g_2(x, y) \).

## 2. Transformation and Inversion
- The transformation should be invertible: \( x = h_1(u, v) \) and \( y = h_2(u, v) \).
- The Jacobian determinant \( J \) of the inverse transformation must exist and be non-zero.

## 3. Proposition A (Main Result)
- If \( X \) and \( Y \) are continuous random variables, and we apply a transformation \( (x, y) \to (u, v) \), the joint density of \( (U, V) \) is:
  \[
  f_{UV}(u, v) = f_{XY}(h_1(u, v), h_2(u, v)) |J|
  \]
- Here, \( |J| \) is the absolute value of the Jacobian determinant of the inverse transformation.

## 4. Example A - Transformation to Polar Coordinates
- For independent standard normal variables \( X \) and \( Y \), converting to polar coordinates:
  \[
  R = \sqrt{X^2 + Y^2}, \quad \theta = \tan^{-1}\left(\frac{Y}{X}\right)
  \]
- The joint density of \( (R, \theta) \) is derived using Proposition A:
  \[
  f_{R\theta}(r, \theta) = \frac{1}{2\pi} r \exp\left(-\frac{r^2}{2}\right)
  \]
  - Here, \( R \sim \chi(2) \) (chi-distribution with 2 degrees of freedom) and \( \theta \sim \text{Unif}(0, 2\pi) \).

## 5. Example B - Linear Transformation
- If \( X_1 \) and \( X_2 \) are independent standard normal random variables, and \( Y_1 = X_1 \), \( Y_2 = X_1 + X_2 \), the joint density of \( (Y_1, Y_2) \) is:
  \[
  f_{Y_1 Y_2}(y_1, y_2) = \frac{1}{2\pi} \exp\left(-y_1^2 - 2y_1 y_2 + y_2^2\right)
  \]
  - This is a bivariate normal distribution.

## 6. Distribution of Functions of Random Variables
- To find the distribution of a function \( Z = f(X, Y) \), two methods can be used:
  - **Method 1 (Proposition A)**: Apply the transformation and use the Jacobian.
  - **Method 2 (CDF Approach)**: Find the CDF of \( Z \), differentiate it to get the PDF.

## 7. Leibniz Integral Rule
- The Leibniz integral rule is used for differentiating under the integral sign, which is useful in complex transformations of random variables.

## 8. Convolutions of Probability Distributions
- **Discrete Random Variables**: For independent random variables \( X \) and \( Y \), the probability distribution of \( Z = X + Y \) is the convolution of the individual probability mass functions (PMFs):
  \[
  p_Z(z) = \sum_{x=-\infty}^{\infty} p_X(x) p_Y(z - x)
  \]
- **Continuous Random Variables**: For independent random variables \( X \) and \( Y \), the PDF of \( Z = X + Y \) is the convolution of the individual PDFs:
  \[
  f_Z(z) = \int_{-\infty}^{\infty} f_X(x) f_Y(z - x) dx
  \]

## 9. Example with Sum of Exponentials
- If \( T_1 \sim \text{Exp}(\lambda) \) and \( T_2 \sim \text{Exp}(\lambda) \), the sum \( S = T_1 + T_2 \) follows a Gamma distribution with shape parameter 2 and rate \( \lambda \):
  \[
  f_S(s) = \lambda^2 s \exp(-\lambda s)
  \]
  - This is a Gamma distribution with shape \( k = 2 \) and rate \( \lambda \).

## 10. Example with Quotients of Random Variables
- If \( Z = Y / X \), where \( X \) and \( Y \) are independent normal random variables, the density of \( Z \) is derived through integration and results in a **Cauchy distribution**:
  \[
  f_Z(z) = \frac{1}{\pi (1 + z^2)}
  \]

## Summary of Methods

### Method 1: Function of Random Variables
- Apply **Proposition A**: Calculate the Jacobian and use the formula for the joint density.

### Method 2: CDF Approach
- Use the cumulative distribution function (CDF) of the transformed variable and differentiate it to find the PDF.

## Additional Resources:
- For further understanding of convolutions, check the following links:
  - [Convolution of Probability Distributions](https://en.wikipedia.org/wiki/List_of_convolutions_of_probability_distributions)
