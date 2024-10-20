### Write python codes to illustrate Propositions C and D (suppose $X\sim exp(1)$)
### C:  
![image](https://github.com/user-attachments/assets/e9142bee-b32e-4440-bea4-371510d9175e)
### D:
![image](https://github.com/user-attachments/assets/3b20fbc9-b9b5-4b36-a880-8bf9672a5ee9)
### Write python codes to illustration Ch02.65 for α=2.
![image](https://github.com/user-attachments/assets/e2c81c70-6d68-41df-98b2-c69692f2cd25)
### Ch02.60 (Ch2.3)
# Lognormal Distribution

Given a random variable $\( Z \sim N(\mu, \sigma^2) \)$, we define $\( Y = \exp(Z) \)$. The probability density function (PDF) of \( Y \) is known as the **lognormal distribution**, because $\( \log(Y) \)$ is normally distributed. Below are the steps to derive the PDF.

## PDF Derivation

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
### Ch02.72 (Ch2.3)
### Ch03.03 (Ch3.2)
### Ch03.06 (Ch3.2)
### Ch03.07 (Ch3.2)
