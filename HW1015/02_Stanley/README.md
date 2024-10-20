### Write python codes to illustrate Propositions C and D (suppose $X\sim exp(1)$)
### C:  
![image](https://github.com/user-attachments/assets/e9142bee-b32e-4440-bea4-371510d9175e)
### D:
![image](https://github.com/user-attachments/assets/3b20fbc9-b9b5-4b36-a880-8bf9672a5ee9)
### Write python codes to illustration Ch02.65 for α=2.
![image](https://github.com/user-attachments/assets/e2c81c70-6d68-41df-98b2-c69692f2cd25)
### Ch02.60 (Ch2.3)
#### Lognormal Distribution

Given a random variable $\( Z \sim N(\mu, \sigma^2) \)$, we define $\( Y = \exp(Z) \)$. The probability density function (PDF) of \( Y \) is known as the **lognormal distribution**, because $\( \log(Y) \)$ is normally distributed. Below are the steps to derive the PDF.

#### PDF Derivation

1. **Normal Distribution PDF of \( Z \)**:
   $\[
   f_Z(z) = \frac{1}{\sqrt{2\pi\sigma^2}} \exp\left( -\frac{(z - \mu)^2}{2\sigma^2} \right)
   \]$
   where $\( Z \sim N(\mu, \sigma^2) \)$.

2. **Transformation**:
   Since $\( Y = \exp(Z) \), we have \( Z = \log(Y) \)$.

3. **Change of Variables**:
   Using the change of variables formula:
   $\[
   f_Y(y) = f_Z(\log(y)) \cdot \left| \frac{d}{dy} \log(y) \right|
   \]$
   The derivative $\( \frac{d}{dy} \log(y) = \frac{1}{y} \)$.

4. **Final PDF**:
   $\[
   f_Y(y) = \frac{1}{y \sigma \sqrt{2\pi}} \exp\left( -\frac{(\log(y) - \mu)^2}{2\sigma^2} \right), \quad y > 0.
   \]$
   This is the PDF of the **lognormal distribution**.
### Ch02.61 (Ch2.3)
#### Density of $\( cX \)$ When $\( X \)$ Follows a Gamma Distribution

Let $\( X \sim \text{Gamma}(\alpha, \lambda) \)$ be a gamma-distributed random variable with shape parameter $\( \alpha \)$ and rate parameter $\( \lambda \)$. The probability density function (PDF) of $\( X \)$ is:

$$
f_X(x) = \frac{\lambda^\alpha}{\Gamma(\alpha)} x^{\alpha-1} e^{-\lambda x}, \quad x > 0.
$$

Now, we wish to find the density of $\( Y = cX \)$, where $\( c > 0 \)$ is a constant.

#### Transformation

Given the transformation $\( Y = cX \)$, we use the change of variables technique to find the PDF of $\( Y \)$.

1. The inverse transformation is $\( X = \frac{Y}{c} \)$.
2. The derivative of the inverse transformation is:

$$
\frac{dX}{dY} = \frac{1}{c}.
$$

Using the change of variables formula, the PDF of \( Y \) is:

$$
f_Y(y) = f_X\left(\frac{y}{c}\right) \cdot \left| \frac{d}{dy} \left( \frac{y}{c} \right) \right|
$$

Since \( \frac{d}{dy} \left( \frac{y}{c} \right) = \frac{1}{c} \), we have:

$$
f_Y(y) = f_X\left(\frac{y}{c}\right) \cdot \frac{1}{c}.
$$

Substitute the PDF of \( X \):

$$
f_Y(y) = \frac{\lambda^\alpha}{\Gamma(\alpha)} \left(\frac{y}{c}\right)^{\alpha-1} e^{-\lambda \frac{y}{c}} \cdot \frac{1}{c}.
$$

Simplifying this expression:

$$
f_Y(y) = \frac{\lambda^\alpha}{c^\alpha \Gamma(\alpha)} y^{\alpha-1} e^{-\frac{\lambda}{c} y}.
$$

Thus, the PDF of \( Y = cX \) is:

$$
f_Y(y) = \frac{\left(\frac{\lambda}{c}\right)^\alpha}{\Gamma(\alpha)} y^{\alpha-1} e^{-\frac{\lambda}{c} y}, \quad y > 0.
$$

#### Conclusion: $\( \lambda \)$ as a Scale Parameter

From the final expression, we can see that the transformation $\( X \to cX \)$ only affects the rate parameter $\( \lambda \)$, replacing it with $\( \frac{\lambda}{c} \)$. The shape parameter $\( \alpha \)$ remains unchanged. This demonstrates that $\( \lambda \)$ is a **scale parameter** because scaling $\( X \)$ by $\( c \)$ only scales the rate parameter, justifying its interpretation as a scale parameter in the gamma distribution.

### Ch02.72 (Ch2.3)
#### part a
![image](https://github.com/user-attachments/assets/79c5256d-1b28-4157-9d18-32944f6deecf)  
Scheme a: [0, 1, 6, 7, 4, 5, 2, 3, 0, 1, 6, 7, 4, 5, 2, 3, 0, 1, 6, 7]---not random
#### part b ---- odd then odd, even than even
![image](https://github.com/user-attachments/assets/a83c8eb4-231b-4697-8977-47694982ade5)  
Scheme 1:  
[69069, 475559465, 654291925, 1790562961, 957348637, 2091487033, 2135332261, 381957665, 1744831853, 1303896393, 1945705589, 560118449, 2050718909, 1672838233, 201201733, 435810369, 1855566093, 270364777, 1454463253, 1184851665]-----random  
![image](https://github.com/user-attachments/assets/21a904e6-5a74-4887-adf0-a462f77203e0)  
Scheme 2 (RANDU):  
[65539, 393225, 1769499, 7077969, 26542323, 95552217, 334432395, 1146624417, 1722371299, 14608041, 1766175739, 1875647473, 1800754131, 366148473, 1022489195, 692115265, 1392739779, 2127401289, 229749723, 1559239569]---random
### Ch03.03 (Ch3.2)
#### Joint Distribution of Games Won by Three Players

Three players play 10 independent rounds of a game, where each player has a probability of \( \frac{1}{3} \) of winning each round. We want to find the joint distribution of the numbers of games won by each of the three players.

#### Problem Setup

Let:
- \( X_1 \): the number of games won by Player 1,
- \( X_2 \): the number of games won by Player 2,
- \( X_3 \): the number of games won by Player 3.

We are interested in the joint distribution of \( (X_1, X_2, X_3) \).

#### Distribution

Since there are three players and the total number of games is 10, the number of wins for each player follows a multinomial distribution. The parameters for this distribution are:
- Total number of trials (games), \( n = 10 \),
- The probabilities of winning for each player: 
  - $\( p_1 = \frac{1}{3} \)$,
  - $\( p_2 = \frac{1}{3} \)$,
  - $\( p_3 = \frac{1}{3} \)$.

The joint distribution of $\( (X_1, X_2, X_3) \)$ is given by:

$$
P(X_1 = k_1, X_2 = k_2, X_3 = k_3) = \frac{10!}{k_1! k_2! k_3!} p_1^{k_1} p_2^{k_2} p_3^{k_3}
$$

where:
- $\( k_1 + k_2 + k_3 = 10 \)$ (the total number of games played),
- $\( k_1, k_2, k_3 \geq 0 \)$ (the number of games won by each player).

Substituting the values for \( p_1 \), \( p_2 \), and \( p_3 \):

$$
P(X_1 = k_1, X_2 = k_2, X_3 = k_3) = \frac{10!}{k_1! k_2! k_3!} \left(\frac{1}{3}\right)^{k_1} \left(\frac{1}{3}\right)^{k_2} \left(\frac{1}{3}\right)^{k_3}
$$

This can be simplified to:

$$
P(X_1 = k_1, X_2 = k_2, X_3 = k_3) = \frac{10!}{k_1! k_2! k_3!} \left(\frac{1}{3}\right)^{10}
$$

#### Summary

Thus, the joint distribution of the number of games won by each of the three players is given by:

$$
P(X_1 = k_1, X_2 = k_2, X_3 = k_3) = \frac{10!}{k_1! k_2! k_3!} \left(\frac{1}{3}\right)^{10}, \quad \text{for } k_1 + k_2 + k_3 = 10 \text{ and } k_1, k_2, k_3 \geq 0.
$$

This represents a multinomial distribution with parameters $\( n = 10 \)$ and $\( p_1 = p_2 = p_3 = \frac{1}{3} \)$.

### Ch03.06 (Ch3.2)
# Marginal Densities of Points Chosen Randomly in an Ellipse

Consider a point chosen randomly in the interior of an ellipse defined by the equation:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1.
$$

We aim to find the marginal densities of the $\( x \)$ and $\( y \) $coordinates of the point.

## Step 1: Area of the Ellipse

The area $\( A \)$ of the ellipse can be calculated using the formula:

$$
A = \pi a b.
$$

## Step 2: Uniform Distribution Inside the Ellipse

When a point is chosen uniformly from the interior of the ellipse, the joint density function \( f_{X,Y}(x,y) \) is given by:

$$
f_{X,Y}(x,y) = \frac{1}{A} = \frac{1}{\pi ab}
$$

for points $\( (x,y) \)$ that satisfy the ellipse equation$ \( \frac{x^2}{a^2} + \frac{y^2}{b^2} < 1 \)$, and $\( 0 \)$ otherwise.

## Step 3: Marginal Densities

To find the marginal densities \( f_X(x) \) and \( f_Y(y) \), we need to integrate the joint density over the respective variable.

### Marginal Density of \( X \)

The marginal density \( f_X(x) \) is obtained by integrating \( f_{X,Y}(x,y) \) over all \( y \):

$$
f_X(x) = \int_{-\sqrt{b^2(1 - \frac{x^2}{a^2})}}^{\sqrt{b^2(1 - \frac{x^2}{a^2})}} f_{X,Y}(x,y) \, dy.
$$

Substituting \( f_{X,Y}(x,y) \):

$$
f_X(x) = \int_{-\sqrt{b^2(1 - \frac{x^2}{a^2})}}^{\sqrt{b^2(1 - \frac{x^2}{a^2})}} \frac{1}{\pi ab} \, dy.
$$

Calculating the integral:

$$
f_X(x) = \frac{1}{\pi ab} \cdot \left[2\sqrt{b^2(1 - \frac{x^2}{a^2})}\right] = \frac{2\sqrt{b^2(1 - \frac{x^2}{a^2})}}{\pi ab}.
$$

Thus, the marginal density of \( X \) is:

$$
f_X(x) = \frac{2b}{\pi a} \sqrt{1 - \frac{x^2}{a^2}}, \quad \text{for } -a < x < a.
$$

### Marginal Density of \( Y \)

Similarly, the marginal density \( f_Y(y) \) is found by integrating \( f_{X,Y}(x,y) \) over all \( x \):

$$
f_Y(y) = \int_{-\sqrt{a^2(1 - \frac{y^2}{b^2})}}^{\sqrt{a^2(1 - \frac{y^2}{b^2})}} f_{X,Y}(x,y) \, dx.
$$

Substituting \( f_{X,Y}(x,y) \):

$$
f_Y(y) = \int_{-\sqrt{a^2(1 - \frac{y^2}{b^2})}}^{\sqrt{a^2(1 - \frac{y^2}{b^2})}} \frac{1}{\pi ab} \, dx.
$$

Calculating this integral:

$$
f_Y(y) = \frac{1}{\pi ab} \cdot \left[2\sqrt{a^2(1 - \frac{y^2}{b^2})}\right] = \frac{2\sqrt{a^2(1 - \frac{y^2}{b^2})}}{\pi ab}.
$$

Thus, the marginal density of \( Y \) is:

$$
f_Y(y) = \frac{2a}{\pi b} \sqrt{1 - \frac{y^2}{b^2}}, \quad \text{for } -b < y < b.
$$

## Summary

The marginal densities of the \( x \) and \( y \) coordinates of a point chosen randomly in the interior of the ellipse are:

1. **Marginal Density of \( X \)**:

   $$f_X(x) = \frac{2b}{\pi a} \sqrt{1 - \frac{x^2}{a^2}}$$ , for -a ≤ x ≤ a.
   

2. **Marginal Density of \( Y \)**:

   $$f_Y(y) = \frac{2a}{\pi b} \sqrt{1 - \frac{y^2}{b^2}}$$ ,for -b ≤ y ≤ b.
  

### Ch03.07 (Ch3.2)
# Joint and Marginal Densities from the CDF

Given the cumulative distribution function (CDF):

$$
F(x, y) = (1 - e^{-\alpha x})(1 - e^{-\beta y}), \quad x \geq 0, y \geq 0, \quad \alpha > 0, \beta > 0,
$$

we aim to find the **joint probability density function (PDF)** and the **marginal densities** for \( x \) and \( y \).

## Step 1: Joint Density Function

To find the joint density function \( f(x, y) \), we differentiate the CDF \( F(x, y) \) with respect to both \( x \) and \( y \):

$$
f(x, y) = \frac{\partial^2}{\partial x \, \partial y} F(x, y).
$$

### Partial Derivatives:

1. **With respect to \( x \):**

   Using the product rule:

   $$\frac{\partial}{\partial x} F(x, y) = (1 - e^{-\beta y}) \cdot \alpha e^{-\alpha x}$$

2. **With respect to \( y \):**

   Differentiating the result with respect to \( y \):

   $$f(x, y) = \alpha e^{-\alpha x} \cdot \beta e^{-\beta y}$$

Thus, the **joint density function** is:

$$
f(x, y) = \alpha \beta e^{-\alpha x} e^{-\beta y}, \quad x \geq 0, y \geq 0.
$$

This represents the PDF of two independent exponential distributions with parameters $\( \alpha \) and \( \beta \)$.

## Step 2: Marginal Density of \( X \)

To find the **marginal density** of \( X \), we integrate the joint density over \( y \):

$$
f_X(x) = \int_0^{\infty} f(x, y) \, dy.
$$

Substituting \( f(x, y) = \alpha \beta e^{-\alpha x} e^{-\beta y} \):

$$
f_X(x) = \alpha e^{-\alpha x} \int_0^{\infty} \beta e^{-\beta y} \, dy = \alpha e^{-\alpha x}.
$$

Thus, the marginal density of \( X \) is:

$$
f_X(x) = \alpha e^{-\alpha x}, \quad x \geq 0.
$$

This is the PDF of an exponential distribution with parameter $\( \alpha \)$.

## Step 3: Marginal Density of \( Y \)

Similarly, the **marginal density** of \( Y \) is found by integrating the joint density over \( x \):

$$
f_Y(y) = \int_0^{\infty} f(x, y) \, dx.
$$

Substituting \( f(x, y) = \alpha \beta e^{-\alpha x} e^{-\beta y} \):

$$
f_Y(y) = \beta e^{-\beta y} \int_0^{\infty} \alpha e^{-\alpha x} \, dx = \beta e^{-\beta y}.
$$

Thus, the marginal density of \( Y \) is:

$$
f_Y(y) = \beta e^{-\beta y}, \quad y \geq 0.
$$

This is the PDF of an exponential distribution with parameter $\( \beta \)$.

## Summary

1. **Joint Density Function**:

   $$f(x, y) = \alpha \beta e^{-\alpha x} e^{-\beta y}, \quad x \geq 0, y \geq 0$$

2. **Marginal Density of \( X \)**:

   $$f_X(x) = \alpha e^{-\alpha x}, \quad x \geq 0$$

3. **Marginal Density of \( Y \)**:

   $$f_Y(y) = \beta e^{-\beta y}, \quad y \geq 0$$

Both marginal densities correspond to exponential distributions with parameters $\( \alpha \) and \( \beta \)$, respectively.
