# Q1. Mean and Variance of a Bernoulli Random Variable

A **Bernoulli random variable** $X$ takes two possible values: 

$X = 1$ (success) with probability $p$,

$X = 0$ (failure) with probability $1 - p$.

The probability mass function (PMF) is given by:

$$
P(X = x) = 
\begin{cases} 
p, & \text{if } x = 1, \\
1 - p, & \text{if } x = 0.
\end{cases}
$$

## 1. Mean of Bernoulli Random Variable

The **mean** (or expected value) of a random variable \( X \) is defined as:

$$
E(X) = \sum_x x \cdot P(X = x)
$$

For a Bernoulli random variable:

$$
E(X) = (1 \cdot P(X = 1)) + (0 \cdot P(X = 0))
$$

Substitute $P(X = 1) = p$ and $P(X = 0) = 1 - p$:

$$
E(X) = (1 \cdot p) + (0 \cdot (1 - p))
$$

$$
E(X) = p
$$

Thus, the **mean** of a Bernoulli random variable is:

$$
\mu = p
$$

## 2. Variance of Bernoulli Random Variable

The **variance** of a random variable $X$ is defined as:

$$
\text{Var}(X) = E\big[(X - \mu)^2\big]
$$

Alternatively, we use the formula:

$$
\text{Var}(X) = E(X^2) - [E(X)]^2
$$

### Step 1: Compute $E(X^2)$

For a Bernoulli random variable:

$$
E(X^2) = \sum_x x^2 \cdot P(X = x)
$$

Since $X$ only takes values $0$ or $1$:

$$
E(X^2) = (1^2 \cdot P(X = 1)) + (0^2 \cdot P(X = 0))
$$

$$
E(X^2) = (1 \cdot p) + (0 \cdot (1 - p)) = p
$$

### Step 2: Compute $\text{Var}(X)$

Using the formula:

$$
\text{Var}(X) = E(X^2) - [E(X)]^2
$$

Substitute $E(X^2) = p$ and $E(X) = p$:

$$
\text{Var}(X) = p - p^2
$$

$$
\text{Var}(X) = p(1 - p)
$$

## Final Results:

1. **Mean**:
   
$$
\mu = E(X) = p
$$

2. **Variance**:

$$
\text{Var}(X) = p(1 - p)
$$

# Q2. Mean and Variance of an Exponential Random Variable

The **Exponential distribution** models the time until the occurrence of an event in a Poisson process. It is defined by the parameter $\lambda > 0$, which represents the rate of the event per unit time.

The probability density function (PDF) of an Exponential random variable $X$ is:

$$
f_X(x) = 
\begin{cases} 
\lambda e^{-\lambda x}, & \text{if } x \geq 0, \\
0, & \text{if } x < 0.
\end{cases}
$$

## 1. Mean of Exponential Random Variable

The **mean** (or expected value) of $X$ is given by:

$$
E(X) = \int_{-\infty}^{\infty} x f_X(x) dx
$$

### Step 1: Substituting the PDF
Since the PDF $f_X(x) = 0$ for $x < 0$, we only integrate over $[0, \infty)$:

$$
E(X) = \int_{0}^{\infty} x \cdot \lambda e^{-\lambda x} dx
$$

### Step 2: Solving the Integral
To solve this, we use **integration by parts**:

\begin{align*}
\int x e^{-\lambda x} dx &= -\frac{x}{\lambda} e^{-\lambda x} - \int -\frac{1}{\lambda} e^{-\lambda x} dx \\
&= -\frac{x}{\lambda} e^{-\lambda x} + \frac{1}{\lambda^2} e^{-\lambda x} + C
\end{align*}

Substituting back:

$$
E(X) = \lambda \left[ -\frac{x}{\lambda} e^{-\lambda x} + \frac{1}{\lambda^2} e^{-\lambda x} \right]_{0}^{\infty}
$$

### Step 3: Evaluate Limits
At $x \to \infty$, $e^{-\lambda x} \to 0$. At $x = 0$, the terms simplify:

$$
E(X) = \lambda \left[ 0 + \frac{1}{\lambda^2} - 0 \right]
$$

$$
E(X) = \frac{1}{\lambda}
$$

Thus, the **mean** is:

$$
E(X) = \frac{1}{\lambda}
$$

## 2. Variance of Exponential Random Variable

The **variance** is defined as:
$$
\text{Var}(X) = E(X^2) - [E(X)]^2
$$

### Step 1: Compute $E(X^2)$
The second moment $E(X^2)$ is:

$$
E(X^2) = \int_{0}^{\infty} x^2 \cdot \lambda e^{-\lambda x} dx
$$

Using integration by parts again, let $u = x^2$ and $dv = \lambda e^{-\lambda x} dx$. The result is:

$$
E(X^2) = \frac{2}{\lambda^2}
$$

### Step 2: Compute Variance
Now substitute $E(X) = \frac{1}{\lambda}$ and $E(X^2) = \frac{2}{\lambda^2}$ into the variance formula:

$$
\text{Var}(X) = E(X^2) - [E(X)]^2
$$

$$
\text{Var}(X) = \frac{2}{\lambda^2} - \left(\frac{1}{\lambda}\right)^2
$$

$$
\text{Var}(X) = \frac{2}{\lambda^2} - \frac{1}{\lambda^2}
$$

$$
\text{Var}(X) = \frac{1}{\lambda^2}
$$

## Final Results:

1. **Mean**:

$$
E(X) = \frac{1}{\lambda}
$$

2. **Variance**:

$$
\text{Var}(X) = \frac{1}{\lambda^2}
$$




