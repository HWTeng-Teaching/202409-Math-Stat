## Q1 Find the mgf of Bernoulli and use it to find its mean and variance
### Moment-Generating Function

The probability mass function of the Bernoulli distribution is:

$$
P(X = x) =
\begin{cases}
p, & x = 1, \\
1-p, & x = 0.
\end{cases}
$$

The mgf is defined as:

$$
M(t) = \mathbb{E}[e^{tX}] = \sum_{x \in \{0, 1\}} e^{tx} P(X = x).
$$

So the mgf of the Bernoulli distribution is

$$
\begin{aligned}
M(t) &= e^{t \cdot 0} P(X = 0) + e^{t \cdot 1} P(X = 1) \\
&= e^0 (1-p) + e^t p \\
&= 1 - p + p e^t.
\end{aligned}
$$

### Mean and Variance

From the mgf:

1. **Mean**: The mean $E(X)$ is the first derivative of $M(t)$ evaluated at $t = 0$:

$$
\begin{aligned}
M'(t) &= \frac{d}{dt} \left( 1 - p + p e^t \right) \\
&= p e^t.
\end{aligned}
$$

At $t = 0$:

$$
M'(0) = p e^0 = p.
$$

Thus, the mean of the Bernoulli distribution is:

$$
E[X] = p.
$$

2. **Variance**: The second derivative of $M(t)$ at $t = 0$ gives $E[X^2]$. Using:

$$
\begin{aligned}
M''(t) &= \frac{d}{dt} \left( p e^t \right) \\
&= p e^t.
\end{aligned}
$$

Evaluate at $t = 0$:

$$
M''(0) = p e^0 = p.
$$

The variance is:

$$
\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2 = p - p^2 = p(1-p).
$$

## Q2 Find the mgf of Exponential and use it to find its mean and variance
### Moment-Generating Function

The probability density function of the exponential distribution is:

$$
f(x) = \lambda e^{-\lambda x}, \quad x \geq 0, \, \lambda > 0.
$$

The mgf is defined as:

$$
M(t) = \mathbb{E}[e^{tX}] = \int_0^\infty e^{tx} f(x) \, dx.
$$

Substituting the exponential density function:

$$
\begin{aligned}
M(t) &= \int_0^\infty e^{tx} \lambda e^{-\lambda x} \, dx \\
&= \lambda \int_0^\infty e^{x(t - \lambda)} \, dx.
\end{aligned}
$$

For convergence, we require $t < \lambda$. Under this condition:

$$
\begin{aligned}
M(t) &= \lambda \int_0^\infty e^{-x(\lambda - t)} \, dx, \quad \text{let } u = (\lambda - t)x, \, du = (\lambda - t)dx \\
&= \lambda \int_0^\infty \frac{e^{-u}}{\lambda - t} \, du \\
&= \frac{\lambda}{\lambda - t} \int_0^\infty e^{-u} \, du.
\end{aligned}
$$

The integral $\int_0^\infty e^{-u} \, du = 1$, so:

$$
M(t) = \frac{\lambda}{\lambda - t}, \quad t < \lambda.
$$

---

### Mean and Variance

From the mgf:

1. **Mean**: The mean $E(X)$ is the first derivative of $M(t)$ evaluated at $t = 0$:

$$
\begin{aligned}
M'(t) &= \frac{d}{dt} \left( \frac{\lambda}{\lambda - t} \right) \\
&= \lambda \cdot \frac{-1}{(\lambda - t)^2}.
\end{aligned}
$$

At $t = 0$:

$$
M'(0) = \lambda \cdot \frac{-1}{\lambda^2} = \frac{1}{\lambda}.
$$

Thus, the mean of the exponential distribution is:

$$
E[X] = \frac{1}{\lambda}.
$$

2. **Variance**: The second derivative of $M(t)$ at $t = 0$ gives $E[X^2]$. Using:

$$
\begin{aligned}
M''(t) &= \frac{d}{dt} \left( \lambda \cdot \frac{-1}{(\lambda - t)^2} \right) \\
&= \lambda \cdot \frac{2}{(\lambda - t)^3}.
\end{aligned}
$$

At $t = 0$:

$$
M''(0) = \lambda \cdot \frac{2}{\lambda^3} = \frac{2}{\lambda^2}.
$$

The variance is:

$$
\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2 = \frac{2}{\lambda^2} - \left(\frac{1}{\lambda}\right)^2 = \frac{1}{\lambda^2}.
$$


## Q3 Find the mgf of the gamma distribution and use it to find its mean and variance
### Moment-Generating Function
The probability density function of the gamma distribution is:

$$f(x) = \frac{\lambda^\alpha}{\Gamma(\alpha)} x^{\alpha-1} e^{-\lambda x}, \quad x \geq 0.$$

The mgf is defined as:

$$
M(t) = \mathbb{E}[e^{tX}] = \int_0^\infty e^{tx} f(x) \ dx.
$$

So the mgf of the gamma distribution is

$$
\begin{aligned}
M(t) &= \int_0^\infty e^{tx} \frac{\lambda^\alpha}{\Gamma(\alpha)} x^{\alpha-1} e^{-\lambda x} \ dx\\
&= \frac{\lambda^\alpha}{\Gamma(\alpha)} \int_0^\infty x^{\alpha-1} e^{-x(\lambda - t)} \ dx,\quad \text{let } u = x(\lambda-t),  du = (\lambda-t)dx\\
&= \frac{\lambda^\alpha}{\Gamma(\alpha)} \int_0^\infty \frac{(\frac{u}{\lambda-t})^{\alpha-1}}{\lambda-t} e^{-u} \ du\\
&= \frac{\lambda^\alpha}{\Gamma(\alpha)} \int_0^\infty \frac{u^{\alpha-1}}{(\lambda-t)^\alpha} e^{-u} \ du\\
&= \frac{\lambda^\alpha}{\Gamma(\alpha)(\lambda-t)^\alpha} \int_0^\infty u^{\alpha-1} e^{-u} \ du,\quad \text{gamma function is defined as } \Gamma(\alpha)=\int_0^\infty u^{\alpha-1} e^{-u} \ du, \alpha>0\\
&= \frac{\lambda^\alpha}{\Gamma(\alpha)(\lambda-t)^\alpha}\Gamma(\alpha)\\
&= \frac{\lambda^\alpha}{(\lambda-t)^\alpha}
\end{aligned}
$$

### Mean and Variance
From the mgf:
1. **Mean**: The mean $\(E(X)\)$ is the first derivative of  $M(t)$ evaluated at $t = 0$:

$$
\begin{aligned}
M'(t) &= \frac{-\lambda^\alpha \cdot \alpha (\lambda-t)^{\alpha-1} \cdot (-1)}{(\lambda-t)^{2\alpha}} \\
&= \lambda^\alpha \cdot \alpha (\lambda-t)^{-\alpha-1} \\
&= \left(\frac{\lambda}{\lambda-t}\right)^\alpha \cdot \alpha \cdot \frac{1}{\lambda-t} \\
&= \alpha \frac{\lambda^\alpha}{(\lambda-t)^{\alpha+1}}
\end{aligned}
$$

At $t = 0$:

$$
M'(0) = \alpha \frac{\lambda^\alpha}{\lambda^{\alpha+1}} = \frac{\alpha}{\lambda} = \text{the mean of gamma dostribution}
$$

2. **Variance**: The second derivative of $M(t)$ at $t = 0$ gives $\mathbb{E}[X^2]$. Using:

$$
\begin{aligned}
M''(t) &= \alpha\lambda^\alpha \cdot \frac{(\alpha+1)(\lambda-t)^\alpha}{(\lambda-t)^{2\alpha+2}} \\
&= \frac{\alpha(\alpha+1)\lambda^\alpha}{(\lambda-t)^{\alpha+2}}
\end{aligned}
$$

evaluating at $t = 0$:

$$
M''(0) = \frac{\alpha(\alpha + 1)}{\lambda^2}.
$$

The variance is:

$$
\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2 = \frac{\alpha(\alpha + 1)}{\lambda^2} - \left(\frac{\alpha}{\lambda}\right)^2 = \frac{\alpha}{\lambda^2}.
$$
The variance is:

$$
\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2 = p - p^2 = p(1-p).
$$

## Q4 Find the mgf of the normal distribution and use it to find its mean and variance
### Moment-Generating Function

The probability density function of the normal distribution is:

$$
f(x) = \frac{1}{\sqrt{2\pi \sigma^2}} e^{-\frac{(x - \mu)^2}{2\sigma^2}}, \quad -\infty < x < \infty.
$$

The mgf is defined as:

$$
M(t) = \mathbb{E}[e^{tX}] = \int_{-\infty}^\infty e^{tx} f(x) \, dx.
$$

Substitute the normal density function:

$$
\begin{aligned}
M(t) &= \int_{-\infty}^\infty e^{tx} \frac{1}{\sqrt{2\pi \sigma^2}} e^{-\frac{(x - \mu)^2}{2\sigma^2}} \, dx \\
&= \frac{1}{\sqrt{2\pi \sigma^2}} \int_{-\infty}^\infty e^{-\frac{(x - \mu)^2}{2\sigma^2} + tx} \, dx.
\end{aligned}
$$

Combine the exponents:

$$
-\frac{(x - \mu)^2}{2\sigma^2} + tx = -\frac{1}{2\sigma^2} \left( (x - \mu)^2 - 2t\sigma^2 x \right).
$$

Complete the square for \( (x - \mu)^2 - 2t\sigma^2 x \):

$$
(x - \mu)^2 - 2t\sigma^2 x = \left( x - (\mu + t\sigma^2) \right)^2 - t^2\sigma^4.
$$

Substitute back:

$$
\begin{aligned}
M(t) &= \frac{1}{\sqrt{2\pi \sigma^2}} \int_{-\infty}^\infty e^{-\frac{1}{2\sigma^2} \left( \left( x - (\mu + t\sigma^2) \right)^2 - t^2\sigma^4 \right)} \, dx \\
&= \frac{1}{\sqrt{2\pi \sigma^2}} e^{\frac{t^2\sigma^2}{2}} \int_{-\infty}^\infty e^{-\frac{\left( x - (\mu + t\sigma^2) \right)^2}{2\sigma^2}} \, dx.
\end{aligned}
$$

The integral is the normalization constant of the normal distribution and evaluates to 1:

$$
M(t) = e^{\mu t + \frac{t^2 \sigma^2}{2}}.
$$

Thus, the mgf of the normal distribution is:

$$
M(t) = e^{\mu t + \frac{t^2 \sigma^2}{2}}.
$$

---

### Mean and Variance

From the mgf:

1. **Mean**: The mean $E(X)$ is the first derivative of $M(t)$ evaluated at $t = 0$:

$$
\begin{aligned}
M'(t) &= \frac{d}{dt} \left( e^{\mu t + \frac{t^2 \sigma^2}{2}} \right) \\
&= e^{\mu t + \frac{t^2 \sigma^2}{2}} \cdot \left( \mu + t\sigma^2 \right).
\end{aligned}
$$

At $t = 0$:

$$
M'(0) = e^{0} \cdot \mu = \mu.
$$

Thus, the mean of the normal distribution is:

$$
E[X] = \mu.
$$

2. **Variance**: The second derivative of $M(t)$ at $t = 0$ gives $E[X^2]$. Using:

$$
\begin{aligned}
M''(t) &= \frac{d}{dt} \left( e^{\mu t + \frac{t^2 \sigma^2}{2}} \cdot \left( \mu + t\sigma^2 \right) \right) \\
&= e^{\mu t + \frac{t^2 \sigma^2}{2}} \cdot \left( \sigma^2 + (\mu + t\sigma^2)^2 \right).
\end{aligned}
$$

At $t = 0$:

$$
M''(0) = e^0 \cdot \left( \sigma^2 + \mu^2 \right) = \sigma^2 + \mu^2.
$$

The variance is:

$$
\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2 = (\sigma^2 + \mu^2) - \mu^2 = \sigma^2.
$$

![HW1126-2](https://github.com/user-attachments/assets/ea843e3d-86fd-4f52-bb9c-b992c41863f2)
![HW1126-3](https://github.com/user-attachments/assets/195c6b00-67dd-453d-b945-4bf86e90da74)
![HW1126-4](https://github.com/user-attachments/assets/a4c7f47b-3edd-49a0-850d-9f4e00a48398)
<img width="1200" alt="截圖 2024-12-03 下午2 34 54" src="https://github.com/user-attachments/assets/55cdadb9-beb3-4015-871a-acf813b5e793">
<img width="1200" alt="截圖 2024-12-03 下午2 36 02" src="https://github.com/user-attachments/assets/96d8c565-82ec-483c-a5f1-5af415e86716">
<img width="1200" alt="截圖 2024-12-03 下午2 37 30" src="https://github.com/user-attachments/assets/bc85cf91-db90-4d29-8582-bbe76c89a754">
![HW1126-6](https://github.com/user-attachments/assets/fffe6a3a-0b71-4625-8ab1-f043d04dfd93)
![HW1126-7](https://github.com/user-attachments/assets/9c49a86b-18c1-4423-b36c-ec4cd6eaee73)
![HW1126-8](https://github.com/user-attachments/assets/896d141a-59ee-4bec-963e-ed301dbc3b05)
<img width="1200" alt="截圖 2024-12-03 下午2 38 22" src="https://github.com/user-attachments/assets/f026a6d2-453b-4853-b5c4-8c3808a3ba48">
