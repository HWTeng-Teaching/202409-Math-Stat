# Q1. Mean and Variance of a Bernoulli Random Variable

A **Bernoulli random variable** $X$ takes two possible values: 

&#8226; $X = 1$ (success) with probability $p$,

&#8226; $X = 0$ (failure) with probability $1 - p$.

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

$$
\begin{aligned}
\int x e^{-\lambda x} dx &= -\frac{x}{\lambda} e^{-\lambda x} - \int -\frac{1}{\lambda} e^{-\lambda x} dx \\
&= -\frac{x}{\lambda} e^{-\lambda x} + \frac{1}{\lambda^2} e^{-\lambda x} + C
\end{aligned}
$$

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
\begin{aligned}
\text{Var}(X) &= E(X^2) - [E(X)]^2 \\
&= \frac{2}{\lambda^2} - \left(\frac{1}{\lambda}\right)^2 \\
&= \frac{2}{\lambda^2} - \frac{1}{\lambda^2} \\
&= \frac{1}{\lambda^2}
\end{aligned}
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

# Q3. Mean and Variance of a Gamma Random Variable

The **Gamma distribution** is defined by two parameters:

&#8226; $\alpha$ (shape parameter)

&#8226; $\beta$ (rate parameter, also written as $\theta = \frac{1}{\beta}$, the scale parameter)

The probability density function (PDF) is:

$$
f_X(x) = \frac{\beta^\alpha x^{\alpha-1} e^{-\beta x}}{\Gamma(\alpha)}, \quad x > 0,  \alpha > 0,  \beta > 0
$$

where $\Gamma(\alpha)$ is the Gamma function:

$$
\Gamma(\alpha) = \int_{0}^\infty t^{\alpha-1} e^{-t} dt
$$

## 1. Mean of the Gamma Distribution

The **mean** (expected value) of a Gamma random variable $X$ is defined as:

$$
E(X) = \int_{0}^\infty x f_X(x) dx
$$

### Step 1: Substitute the PDF

$$
E(X) = \int_{0}^\infty x \cdot \frac{\beta^\alpha x^{\alpha-1} e^{-\beta x}}{\Gamma(\alpha)} dx
$$

Simplify:

$$
E(X) = \frac{\beta^\alpha}{\Gamma(\alpha)} \int_{0}^\infty x^\alpha e^{-\beta x} dx
$$

### Step 2: Use the Gamma Function Property
The Gamma function is defined as:

$$
\Gamma(\alpha) = \int_{0}^\infty t^{\alpha-1} e^{-t} dt
$$

Using the substitution $t = \beta x$ (so $x = \frac{t}{\beta}$ and $dx = \frac{1}{\beta} dt$):

$$
\int_{0}^\infty x^\alpha e^{-\beta x} dx = \frac{\Gamma(\alpha + 1)}{\beta^{\alpha+1}}
$$

Substitute this into the equation for $E(X)$:

$$
E(X) = \frac{\beta^\alpha}{\Gamma(\alpha)} \cdot \frac{\Gamma(\alpha + 1)}{\beta^{\alpha+1}}
$$

Simplify using the property $\Gamma(\alpha + 1) = \alpha \Gamma(\alpha)$:

$$
E(X) = \frac{\beta^\alpha \cdot \alpha \Gamma(\alpha)}{\Gamma(\alpha) \beta^{\alpha+1}}
$$

$$
E(X) = \frac{\alpha}{\beta}
$$

Thus, the **mean** is:

$$
E(X) = \frac{\alpha}{\beta}
$$

## 2. Variance of the Gamma Distribution

The **variance** is defined as:

$$
\text{Var}(X) = E(X^2) - [E(X)]^2
$$

### Step 1: Compute $E(X^2)$

$$
E(X^2) = \int_{0}^\infty x^2 f_X(x) dx
$$

Substitute the PDF:

$$
E(X^2) = \frac{\beta^\alpha}{\Gamma(\alpha)} \int_{0}^\infty x^{\alpha+1} e^{-\beta x} dx
$$

Using the same substitution as before:

$$
\int_{0}^\infty x^{\alpha+1} e^{-\beta x} dx = \frac{\Gamma(\alpha + 2)}{\beta^{\alpha+2}}
$$

Substitute this into the equation for $E(X^2)$:

$$
E(X^2) = \frac{\beta^\alpha}{\Gamma(\alpha)} \cdot \frac{\Gamma(\alpha + 2)}{\beta^{\alpha+2}}
$$

Simplify using the property $\Gamma(\alpha + 2) = (\alpha + 1)\alpha \Gamma(\alpha)$:

$$
E(X^2) = \frac{\beta^\alpha \cdot (\alpha + 1)\alpha \Gamma(\alpha)}{\Gamma(\alpha) \beta^{\alpha+2}}
$$

$$
E(X^2) = \frac{(\alpha + 1)\alpha}{\beta^2}
$$

### Step 2: Compute Variance
Now substitute $E(X^2) = \frac{(\alpha + 1)\alpha}{\beta^2}$ and $E(X) = \frac{\alpha}{\beta}$ into the variance formula:

$$
\begin{aligned}
\text{Var}(X) &= E(X^2) - [E(X)]^2 \\
&= \frac{(\alpha + 1)\alpha}{\beta^2} - \left(\frac{\alpha}{\beta}\right)^2 \\
&= \frac{(\alpha + 1)\alpha}{\beta^2} - \frac{\alpha^2}{\beta^2} \\
&= \frac{\alpha}{\beta^2}
\end{aligned}
$$

Thus, the **variance** is:

$$
\text{Var}(X) = \frac{\alpha}{\beta^2}
$$

## Final Results

1. **Mean**:

$$
E(X) = \frac{\alpha}{\beta}
$$

2. **Variance**:

$$
\text{Var}(X) = \frac{\alpha}{\beta^2}
$$

# Q4. Mean and Variance of a Normal Distribution

The **Normal distribution** is defined by two parameters:

&#8226; $\mu$ (mean): the center of the distribution.

&#8226; $\sigma^2$ (variance): a measure of the spread of the distribution.

The probability density function (PDF) is:

$$
f_X(x) = \frac{1}{\sqrt{2 \pi \sigma^2}} e^{-\frac{(x - \mu)^2}{2 \sigma^2}}, \quad -\infty < x < \infty
$$

## 1. Mean of the Normal Distribution

The **mean** (expected value) of $X$ is:

$$
E(X) = \int_{-\infty}^\infty x f_X(x) dx
$$

### Step 1: Substituting the PDF

$$
E(X) = \int_{-\infty}^\infty x \cdot \frac{1}{\sqrt{2 \pi \sigma^2}} e^{-\frac{(x - \mu)^2}{2 \sigma^2}} dx
$$

### Step 2: Simplify
Using a substitution $z = \frac{x - \mu}{\sigma}$, so $x = z \sigma + \mu$ and $dx = \sigma dz$, the integral becomes:

$$
E(X) = \int_{-\infty}^\infty (\sigma z + \mu) \cdot \frac{1}{\sqrt{2 \pi \sigma^2}} e^{-\frac{z^2}{2}} \sigma dz
$$

Split the integral:

$$
E(X) = \frac{(\sigma)^2}{\sqrt{2 \pi \sigma^2}} \int_{-\infty}^\infty z e^{-\frac{z^2}{2}} dz + \frac{\mu}{\sqrt{2 \pi}} \int_{-\infty}^\infty e^{-\frac{z^2}{2}} dz
$$

### Step 3: Evaluate Each Integral
1. The first integral:

$$
\int_{-\infty}^\infty z e^{-\frac{z^2}{2}} dz = 0
$$
   
(This is because the function $z e^{-\frac{z^2}{2}}$ is odd and symmetric about $z = 0$.)

2. The second integral:

$$
\int_{-\infty}^\infty e^{-\frac{z^2}{2}} dz = \sqrt{2 \pi}
$$

Substitute back:

$$
E(X) = \mu
$$

Thus, the **mean** of the normal distribution is:

$$
E(X) = \mu
$$

## 2. Variance of the Normal Distribution

The **variance** is defined as:

$$
\text{Var}(X) = E(X^2) - [E(X)]^2
$$

### Step 1: Compute $E(X^2)$

$$
E(X^2) = \int_{-\infty}^\infty x^2 f_X(x) dx
$$

Substitute the PDF:

$$
E(X^2) = \int_{-\infty}^\infty x^2 \cdot \frac{1}{\sqrt{2 \pi \sigma^2}} e^{-\frac{(x - \mu)^2}{2 \sigma^2}} dx
$$

Using the same substitution $z = \frac{x - \mu}{\sigma}$, so $x = z \sigma + \mu$:

$$
E(X^2) = \int_{-\infty}^\infty [(z \sigma + \mu)^2] \cdot \frac{1}{\sqrt{2 \pi}} e^{-\frac{z^2}{2}} dz
$$

Expand \( (z \sigma + \mu)^2 \):

$$
(z \sigma + \mu)^2 = z^2 \sigma^2 + 2z \sigma \mu + \mu^2
$$

Substitute this back into the integral:

$$
E(X^2) = \frac{1}{\sqrt{2 \pi}} \int_{-\infty}^\infty (z^2 \sigma^2 + 2z \sigma \mu + \mu^2) e^{-\frac{z^2}{2}} dz
$$

Split into three integrals:

$$
E(X^2) = \frac{\sigma^2}{\sqrt{2 \pi}} \int_{-\infty}^\infty z^2 e^{-\frac{z^2}{2}} dz + \frac{2 \sigma \mu}{\sqrt{2 \pi}} \int_{-\infty}^\infty z e^{-\frac{z^2}{2}} dz + \frac{\mu^2}{\sqrt{2 \pi}} \int_{-\infty}^\infty e^{-\frac{z^2}{2}} dz
$$

1. The second term vanishes because:

$$   
\int_{-\infty}^\infty z e^{-\frac{z^2}{2}} dz = 0
$$

3. The first term:

$$
\int_{-\infty}^\infty z^2 e^{-\frac{z^2}{2}} dz = \sqrt{2 \pi}
$$

4. The third term:
   
$$
\int_{-\infty}^\infty e^{-\frac{z^2}{2}} dz = \sqrt{2 \pi}
$$

Substitute back:

$$
E(X^2) = \sigma^2 + \mu^2
$$

### Step 2: Compute Variance

$$
\begin{aligned}
\text{Var}(X) &= E(X^2) - [E(X)]^2 \\
&= (\sigma^2 + \mu^2) - \mu^2 \\
&= \sigma^2 
\end{aligned}
$$

## Final Results

1. **Mean**:

$$
E(X) = \mu
$$

2. **Variance**:

$$
\text{Var}(X) = \sigma^2
$$




