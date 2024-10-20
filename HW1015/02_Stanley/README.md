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
### Ch03.07 (Ch3.2)
