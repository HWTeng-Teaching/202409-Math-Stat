# Q1
## Find the Mean and Variance of a Bernoulli Random Variable

A Bernoulli random variable $X$ has the following probability mass function (PMF):

$$
P(X = x) = 
\begin{cases}
p, & \text{when } x = 1, \\
1-p, & \text{when } x = 0.
\end{cases}
$$

where $p$ is the probability of success, $0 \leq p \leq 1$.

---

### Mean $E(X)$

We know that the **mean** of a random variable is:

$$
E(X) = \sum_x x \cdot P(X = x)
$$

#### Step 1: Simplify the summation

Since $X$ takes only two values, $0$ and $1$, the summation becomes:

$$
E(X) = 0 \cdot P(X = 0) + 1 \cdot P(X = 1)
$$

Substitute $P(X = 0) = 1-p$ and $P(X = 1) = p$:

$$
E(X) = 0 \cdot (1-p) + 1 \cdot p
$$

#### Step 2: Simplify

$$
E(X) = p
$$

Thus:

$$
E(X) = p
$$

---

### Variance $(\text{Var}(X))$

We know that the **variance** of a random variable is:

$$
\text{Var}(X) = E(X^2) - [E(X)]^2
$$

#### Step 1: Compute $E(X^2)$

For a Bernoulli random variable, $X^2 = X$, because $X$ takes values $0$ or $1$. Therefore:

$$
E(X^2) = E(X) = p
$$

#### Step 2: Substitute into the variance formula

Now we know:
- $E(X^2) = p$,
- $[E(X)]^2 = p^2$.

Substitute these into the variance formula:

$$
\text{Var}(X) = p - p^2
$$

Simplify:

$$
\text{Var}(X) = p(1 - p)
$$

---

### Final Results

1. **Mean**:

$$
E(X) = p
$$

2. **Variance**:

$$
\text{Var}(X) = p(1 - p)
$$

# Q2
## Find the Mean and Variance of a Expotential

An Exponential random variable $\(X\)$ has the following probability density function (PDF):

$$
f(x) = 
\begin{cases}
\lambda e^{-\lambda x}, & \text{when } x \geq 0, \\
0, & \text{when } x < 0,
\end{cases}
$$

where $\lambda\$ is the rate parameter, $\lambda > 0$.

---

### Mean $\(E(X)\)$

We know that the **mean** of a random variable is

$$
E(X) = \int_{-\infty}^\infty x f(x) dx
$$

#### Step 1: Simplify the integral

Since $f(x) = 0$ for $x < 0$ and  $f(x) = \lambda e^{-\lambda x}$ for $x \geq 0$, the integral becomes:

$$
E(X) = \int_{0}^\infty x \lambda e^{-\lambda x} dx
$$

#### Step 2: Solve the integral

$$
\begin{aligned}
E(X) &= \int_{0}^\infty x \lambda e^{-\lambda x} dx, \quad \text{by integral by part, let } u = x,  du = dx,  dv = \lambda e^{-\lambda x} dx,  v = -e^{-\lambda x} \\
&= -xe^{-\lambda x}\Big|^\infty\_0 + \int_{0}^\infty e^{-\lambda x} dx \\
&= 0 - \frac{1}{\lambda} e^{-\lambda x}\Big|_0^\infty\\
&= -(0-\frac{1}{\lambda})\\
&=\frac{1}{\lambda}
\end{aligned}
$$

Thus:

$$
E(X) = \frac{1}{\lambda}
$$

---

### Variance $(\text{Var}(X)\)$

We know that the **variance** of a random variable is 

$$
\text{Var}(X) = E(X^2) - [E(X)]^2
$$

and

$$
E(X^2) = \int_{-\infty}^\infty x^2 f_X(x) dx
$$

#### Step 1: Compute $E(X^2)$

Simplify the integral

Since $f(x) = 0$ for $x < 0$ and  $f(x) = \lambda e^{-\lambda x}$ for $x \geq 0$, the integral becomes:

$$
E(X^2) = \int_{0}^\infty x^2 \lambda e^{-\lambda x} dx
$$

Solve the integral

$$
\begin{aligned}
E(X^2) &= \int_{0}^\infty x^2 \lambda e^{-\lambda x} dx, \quad \text{by integral by part, let } u = x^2,  du = 2xdx,  dv = \lambda e^{-\lambda x} dx,  v = -e^{-\lambda x} \\
&= -x^2e^{-\lambda x}\Big|^\infty\_0 + \int_{0}^\infty 2xe^{-\lambda x} dx \\
&= 0 + \int_{0}^\infty 2xe^{-\lambda x} dx,\quad \text{by integral by part, let } u = 2x,  du = 2dx,  dv = e^{-\lambda x} dx,  v = -\frac{1}{\lambda}e^{-\lambda x} \\
&= -2xe^{-\lambda x}\Big|^\infty\_0 + \int_{0}^\infty \frac{2}{\lambda}e^{-\lambda x} dx \\
&=\frac{2}{\lambda^2}e^{-\lambda x}\Big|^\infty\_0\\
&=0-(0-\frac{2}{\lambda^2})\\
&=\frac{2}{\lambda^2}
\end{aligned}
$$

#### Step 2: Substitute into the variance formula

Now we know: $E(X^2) = \frac{2}{\lambda^2}$, and $E(X) = \frac{1}{\lambda}.$

Substitute these into the variance formula:

$$
\text{Var}(X) = \frac{2}{\lambda^2} - \left(\frac{1}{\lambda}\right)^2
$$

Simplify:

$$
\text{Var}(X) = \frac{2}{\lambda^2} - \frac{1}{\lambda^2}
$$

$$
\text{Var}(X) = \frac{1}{\lambda^2}
$$

---

### Final Results

1. **Mean**:

$$
E(X) = \frac{1}{\lambda}
$$

2. **Variance**:

$$
\text{Var}(X) = \frac{1}{\lambda^2}
$$

# Q3
## Find the Mean and Variance of a Gamma Random Variable
A Gamma random variable $X$ has the following probability density function (PDF):

$$
f(x) = 
\begin{cases}
\frac{\beta^\alpha x^{\alpha-1} e^{-\beta x}}{\Gamma(\alpha)}, & \text{when } x > 0, \\
0, & \text{when } x \leq 0,
\end{cases}
$$

where:
- $\alpha > 0$ is the shape parameter,
- $\beta > 0$ is the rate parameter,
- $\Gamma(\alpha)$ is the Gamma function:
  $$
  \Gamma(\alpha) = \int_0^\infty t^{\alpha-1} e^{-t} dt.
  $$

---

### Mean $E(X)$

We know that the **mean** of a random variable is:

$$
E(X) = \int_{-\infty}^\infty x f(x) dx
$$

#### Step 1: Simplify the integral

Since $f(x) = 0$ for $x \leq 0$, the integral reduces to:

$$
E(X) = \int_{0}^\infty x \cdot \frac{\beta^\alpha x^{\alpha-1} e^{-\beta x}}{\Gamma(\alpha)} dx
$$

Simplify the expression:

$$
E(X) = \frac{\beta^\alpha}{\Gamma(\alpha)} \int_{0}^\infty x^\alpha e^{-\beta x} dx
$$

#### Step 2: Solve the integral

Using the substitution $t = \beta x$, so $x = \frac{t}{\beta}$ and $dx = \frac{1}{\beta} dt$, the integral becomes:

$$
\int_{0}^\infty x^\alpha e^{-\beta x} dx = \frac{1}{\beta^{\alpha+1}} \int_{0}^\infty t^\alpha e^{-t} dt
$$

Recognizing that $\int_{0}^\infty t^\alpha e^{-t} dt = \Gamma(\alpha+1)$, and using the property $\Gamma(\alpha+1) = \alpha \Gamma(\alpha)$, we get:

$$
E(X) = \frac{\beta^\alpha}{\Gamma(\alpha)} \cdot \frac{\Gamma(\alpha+1)}{\beta^{\alpha+1}}
$$

Simplify:

$$
E(X) = \frac{\alpha \Gamma(\alpha)}{\Gamma(\alpha)} \cdot \frac{1}{\beta}
$$

$$
E(X) = \frac{\alpha}{\beta}
$$

Thus:

$$
E(X) = \frac{\alpha}{\beta}
$$

---

### Variance $(\text{Var}(X))$

We know that the **variance** of a random variable is:

$$
\text{Var}(X) = E(X^2) - [E(X)]^2
$$

and

$$
E(X^2) = \int_{-\infty}^\infty x^2 f_X(x) dx
$$

#### Step 1: Compute $E(X^2)$

Simplify the integral:

$$
E(X^2) = \int_{0}^\infty x^2 \cdot \frac{\beta^\alpha x^{\alpha-1} e^{-\beta x}}{\Gamma(\alpha)} dx
$$

Simplify the expression:

$$
E(X^2) = \frac{\beta^\alpha}{\Gamma(\alpha)} \int_{0}^\infty x^{\alpha+1} e^{-\beta x} dx
$$

Using the same substitution $t = \beta x$, the integral becomes:

$$
\int_{0}^\infty x^{\alpha+1} e^{-\beta x} dx = \frac{1}{\beta^{\alpha+2}} \int_{0}^\infty t^{\alpha+1} e^{-t} dt
$$

Recognizing that $\int_{0}^\infty t^{\alpha+1} e^{-t} dt = \Gamma(\alpha+2)$, and using the property $\Gamma(\alpha+2) = (\alpha+1)\alpha \Gamma(\alpha)$, we get:

$$
E(X^2) = \frac{\beta^\alpha}{\Gamma(\alpha)} \cdot \frac{\Gamma(\alpha+2)}{\beta^{\alpha+2}}
$$

Simplify:

$$
E(X^2) = \frac{(\alpha+1)\alpha \Gamma(\alpha)}{\Gamma(\alpha)} \cdot \frac{1}{\beta^2}
$$

$$
E(X^2) = \frac{(\alpha+1)\alpha}{\beta^2}
$$

#### Step 2: Compute variance

Substitute $E(X^2)$ and $[E(X)]^2$ into the variance formula:

$$
\text{Var}(X) = \frac{(\alpha+1)\alpha}{\beta^2} - \left(\frac{\alpha}{\beta}\right)^2
$$

Simplify:

$$
\text{Var}(X) = \frac{\alpha^2 + \alpha}{\beta^2} - \frac{\alpha^2}{\beta^2}
$$

$$
\text{Var}(X) = \frac{\alpha}{\beta^2}
$$

---

### Final Results

1. **Mean**:

$$
E(X) = \frac{\alpha}{\beta}
$$

2. **Variance**:

$$
\text{Var}(X) = \frac{\alpha}{\beta^2}
$$

# Q4
## Find the Mean and Variance of a Normal Random Variable

A Normal random variable $X$ has the following probability density function (PDF):

$$
f(x) = \frac{1}{\sqrt{2\pi \sigma^2}} e^{-\frac{(x - \mu)^2}{2\sigma^2}}, \quad -\infty < x < \infty
$$

where:
- $\mu$ is the mean (center of the distribution),
- $\sigma^2$ is the variance (spread of the distribution).

---

### Mean $E(X)$

We know that the **mean** of a random variable is:

$$
E(X) = \int_{-\infty}^\infty x f(x) dx
$$

#### Step 1: Simplify the integral

Substitute the PDF of the Normal distribution into the formula:

$$
E(X) = \int_{-\infty}^\infty x \cdot \frac{1}{\sqrt{2\pi \sigma^2}} e^{-\frac{(x - \mu)^2}{2\sigma^2}} dx
$$

#### Step 2: Solve the integral

By symmetry of the Normal distribution:
- The distribution is centered at $\mu$, and $x$ is symmetrically distributed around $\mu$. Therefore, the **mean** of a Normal random variable is:

$$
E(X) = \mu
$$

---

### Variance $(\text{Var}(X))$

We know that the **variance** of a random variable is:

$$
\text{Var}(X) = E(X^2) - [E(X)]^2
$$

and

$$
E(X^2) = \int_{-\infty}^\infty x^2 f(x) dx
$$

#### Step 1: Compute $E(X^2)$

Substitute the PDF into the formula for $E(X^2)$:

$$
E(X^2) = \int_{-\infty}^\infty x^2 \cdot \frac{1}{\sqrt{2\pi \sigma^2}} e^{-\frac{(x - \mu)^2}{2\sigma^2}} dx
$$

Simplify by completing the square and using the properties of the Normal distribution. After calculation, the result is:

$$
E(X^2) = \sigma^2 + \mu^2
$$

#### Step 2: Compute variance

Now substitute $E(X^2) = \sigma^2 + \mu^2$ and $[E(X)]^2 = \mu^2$ into the variance formula:

$$
\text{Var}(X) = (\sigma^2 + \mu^2) - \mu^2
$$

Simplify:

$$
\text{Var}(X) = \sigma^2
$$

---

### Final Results

1. **Mean**:

$$
E(X) = \mu
$$

2. **Variance**:

$$
\text{Var}(X) = \sigma^2
$$

![HW1119-2](https://github.com/user-attachments/assets/035aa928-6565-4149-84a4-52b8d9666145)
![HW1119-3](https://github.com/user-attachments/assets/09c9ed9a-e3ad-4298-9098-c6a998c2e9b3)
![HW1119-4](https://github.com/user-attachments/assets/5f0fc2a6-9ca1-4cf4-b1c6-fe05a9a7b71f)
