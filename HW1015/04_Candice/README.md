## Q1
## Write python codes to illustrate Propositions C and D

## Answer:

```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.stats as stats

# Proposition C: Simulate X ~ Exp(1) and calculate Z = F(X)
n_samples = 10000
X = np.random.exponential(scale=1, size=n_samples)  # X ~ Exp(1)
F_X = stats.expon.cdf(X)  # F(X) using the CDF of Exp(1), should follow Uniform(0,1)

# Proposition D: Simulate U ~ Uniform(0, 1) and calculate X = F^-1(U)
U = np.random.uniform(0, 1, size=n_samples)  # U ~ Uniform(0, 1)
F_inv_U = stats.expon.ppf(U)  # F^-1(U) using the inverse CDF (quantile function)

# Plot results for Proposition C
plt.figure(figsize=(12, 5))

plt.subplot(1, 2, 1)
plt.hist(F_X, bins=50, density=True, alpha=0.7, color='blue')
plt.title("Proposition C: Histogram of Z = F(X) \n(should be Uniform(0, 1))")
plt.xlabel("Z")
plt.ylabel("Density")

# Plot results for Proposition D
plt.subplot(1, 2, 2)
plt.hist(F_inv_U, bins=50, density=True, alpha=0.7, color='green')
plt.title("Proposition D: Histogram of X = F^-1(U) \n(should be Exp(1))")
plt.xlabel("X")
plt.ylabel("Density")

plt.tight_layout()
plt.show()
```
![截圖 2024-10-20 下午11 22 54](https://github.com/user-attachments/assets/9a8e4b88-252c-4e7c-a81c-4570e290b6cf)


## Q2
## Write python codes to illustration Ch02.65 for α = 2.

## Answer:
```python
import numpy as np
import matplotlib.pyplot as plt

# Define the inverse CDF for α = 2
def inverse_cdf(u):
    # This is derived from solving the quadratic equation for the CDF of α = 2
    # F(x) = 0.5 * (x + x^2 + 1), solve for x in terms of u
    return (-1 + np.sqrt(1 + 4*u)) / 2

# Number of samples
n_samples = 10000

# Generate uniform random numbers
U = np.random.uniform(0, 1, size=n_samples)

# Apply the inverse CDF to get samples from the target distribution
X = inverse_cdf(U)

# Plot the histogram of the generated samples
plt.hist(X, bins=50, density=True, alpha=0.7, color='purple', label='Generated Samples')

# Plot the actual PDF for comparison
x_vals = np.linspace(-1, 1, 500)
pdf_vals = (1 + 2*x_vals) / 2
plt.plot(x_vals, pdf_vals, 'r-', label='PDF (α=2)')

plt.title("Generated Samples vs PDF for α = 2")
plt.xlabel("x")
plt.ylabel("Density")
plt.legend()
plt.show()
```

![截圖 2024-10-20 下午11 24 19](https://github.com/user-attachments/assets/3843f0b3-5819-4f6d-b67c-d6e9d49478db)

## Q3
## find the probability density function (PDF) of Y= exp(Z),where Z ~ N(μ, σ²) Which is called the lognormal density, since log Y is normally distributed.

## Answer

The PDF of Z is:

f_Z(z) = (1 / (√(2πσ²))) * exp(-(z - μ)² / (2σ²))

 Y = exp(Z), so

Z = log(Y)

The relationship between the PDFs of Z and Y is:

f_Y(y) = f_Z(z) * |dz/dy|

Since Z = log(Y), we have dz/dy = 1/y. Therefore, the PDF of Y becomes:

f_Y(y) = f_Z(log(y)) * (1 / y)

Substituting the PDF of Z into the equation:

f_Y(y) = (1 / (√(2πσ²))) * exp(-(log(y) - μ)² / (2σ²)) * (1 / y)

The PDF of the lognormal random variable Y is:

f_Y(y) = (1 / (yσ√(2π))) * exp(-(log(y) - μ)² / (2σ²)), for y > 0

## Q4 

## Find the density of cX when X follows a Gamma distribution. Show that only λ is affected by such a transformation, which justifies calling λ a scale parameter.

## Answer 

The PDF of X is:

$$
f_X(x) = \frac{1}{\Gamma(k) \lambda^k} x^{k-1} e^{-x / \lambda}, \quad x > 0
$$

Since Y = cX, we have:

$$
X = \frac{Y}{c}
$$

and

$$
\frac{dX}{dY} = \frac{1}{c}
$$

The PDF of Y is given by:

$$
f_Y(y) = f_X\left(\frac{y}{c}\right) \cdot \left|\frac{dX}{dY}\right|
$$

Substituting 

$$
\( \frac{dX}{dY} = \frac{1}{c} \)
$$

$$
f_Y(y) = \frac{1}{c} f_X\left(\frac{y}{c}\right)
$$


$$
f_Y(y) = \frac{1}{c} \cdot \frac{1}{\Gamma(k) \lambda^k} \left(\frac{y}{c}\right)^{k-1} \exp\left(-\frac{y}{c\lambda}\right)
$$


$$
f_Y(y) = \frac{1}{\Gamma(k)} \cdot \frac{1}{(c\lambda)^k} \cdot y^{k-1} \exp\left(-\frac{y}{c\lambda}\right), \quad y > 0
$$


The PDF of Y = cX is still a Gamma distribution with the same shape parameter k, but the scale parameter λ is replaced by cλ. This shows that only the scale parameter λ is affected by multiplying X by a constant c, which justifies calling λ a scale parameter.

## Q5

## One of the most commonly used (but not one of the best) methods of generating pseudorandom numbers is the linear congruential method, which works as follows. Let x₀ be an initial number (the “seed”). The sequence is generated recursively as:

$$
x_n = (a x_{n-1} + c) \mod m
$$

### a. 
Choose values of a, c, and m, and try this out. Do the sequences "look" random?

### b.
Making good choices of a, c, and m involves both art and theory. The following are some values that have been proposed:

1. a = 69069, c = 0, m = 2³¹
2. a = 65539, c = 0, m = 2³¹

The latter is an infamous generator called **RANDU**. Try out these schemes and examine the results.

## Answer

```python
# Linear Congruential Generator (LCG) function
def lcg(a, c, m, seed, n):
    """Linear Congruential Generator to generate n pseudorandom numbers"""
    x = seed
    results = []
    for _ in range(n):
        x = (a * x + c) % m
        results.append(x)
    return results

# Part (a): Choose values of a, c, and m
a = 5
c = 3
m = 16
seed = 7
n = 20  # Number of random numbers to generate

# Generate the sequence
sequence = lcg(a, c, m, seed, n)

# Output the results for Part (a)
print("LCG with a = 5, c = 3, m = 16:")
print(sequence)

# Part (b): RANDU and alternative scheme
# (1) RANDU values: a=69069, c=0, m=2^31
a_randu = 69069
c_randu = 0
m_randu = 2**31

# Generate the RANDU sequence
randu_sequence = lcg(a_randu, c_randu, m_randu, seed, n)

# Output the results for RANDU scheme
print("\nRANDU Generator (a = 69069, c = 0, m = 2^31):")
print(randu_sequence)

# (2) RANDU values: a=65539, c=0, m=2^31
a_randu = 65539
c_randu = 0
m_randu = 2**31

randu_sequence = lcg(a_randu, c_randu, m_randu, seed, n)

# Output the results for RANDU scheme
print("\nRANDU Generator (a = 65539, c = 0, m = 2^31):")
print(randu_sequence)$
```
OUTPUT
(a)
LCG with a = 5, c = 3, m = 16:

[6, 1, 8, 11, 10, 5, 12, 15, 14, 9, 0, 3, 2, 13, 4, 7, 6, 1, 8, 11]

The result seems random.
(b)

RANDU Generator (a = 69069, c = 0, m = 2^31):

[483483, 1181432607, 285076179, 1796522487, 258989515, 1755507343, 2062423939, 526220007, 1476404731, 537340159, 735037235, 1773345495, 1470130475, 972449391, 1408412131, 903188935, 104060763, 1892553439, 1591308179, 1851510711]

RANDU Generator (a = 65539, c = 0, m = 2^31):

[458773, 2752575, 12386493, 49545783, 185796261, 668865519, 193543117, 1583919975, 1319180853, 102256287, 1625811933, 244630423, 1867860677, 415555663, 714973421, 549839559, 1159243861, 2006907135, 1608248061, 177258743]

The result seems random but only with odd numbers.

## Q6

## Three players play 10 independent rounds of a game, and each player has a probability of 1/3 of winning each round. Find the joint distribution of the number of games won by each of the three players.

## Answer

This problem can be solved using the **multinomial distribution**, which generalizes the binomial distribution to multiple outcomes.

Let:
- X₁ be the number of games won by player 1,
- X₂ be the number of games won by player 2,
- X₃ be the number of games won by player 3.

**multinomial distribution**.

The probability mass function (PMF) for the multinomial distribution is given by:

$$
P(X_1 = x_1, X_2 = x_2, X_3 = x_3) = \frac{10!}{x_1! x_2! x_3!} \left( \frac{1}{3} \right)^{x_1} \left( \frac{1}{3} \right)^{x_2} \left( \frac{1}{3} \right)^{x_3}
$$

subject to the condition:

$$
x_1 + x_2 + x_3 = 10
$$

Therefore, the joint distribution of the numbers of games won by each player is:

$$
P(X_1 = x_1, X_2 = x_2, X_3 = x_3) = \frac{10!}{x_1! x_2! x_3!} \left( \frac{1}{3} \right)^{x_1} \left( \frac{1}{3} \right)^{x_2} \left( \frac{1}{3} \right)^{x_3}
$$

where:

$$
x_1 + x_2 + x_3 = 10, x_i>=0
$$

## Q7

## A point is chosen randomly in the interior of an ellipse:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

## Find the marginal densities of the \(x\) and \(y\) coordinates of the point.

## Answer


$$
f_{X,Y}(x, y) = \frac{1}{\pi a b}, \quad \text{for } \frac{x^2}{a^2} + \frac{y^2}{b^2} \leq 1
$$

The joint density is 0 outside the ellipse.

$$
f_X(x) = \int_{-\sqrt{b^2 \left(1 - \frac{x^2}{a^2}\right)}}^{\sqrt{b^2 \left(1 - \frac{x^2}{a^2}\right)}} f_{X,Y}(x, y) \, dy
$$


$$
f_X(x) = \frac{1}{\pi a b} \int_{-\sqrt{b^2 \left(1 - \frac{x^2}{a^2}\right)}}^{\sqrt{b^2 \left(1 - \frac{x^2}{a^2}\right)}} 1 \, dy
$$

The length of the interval for y is:

$$
2 \sqrt{b^2 \left(1 - \frac{x^2}{a^2}\right)}
$$

Thus, the marginal density  f_X(x) becomes:

$$
f_X(x) = \frac{1}{\pi a b} \cdot 2 \sqrt{b^2 \left(1 - \frac{x^2}{a^2}\right)} = \frac{2}{\pi a} \sqrt{1 - \frac{x^2}{a^2}}, \quad -a \leq x \leq a
$$

$$
f_Y(y) = \int_{-\sqrt{a^2 \left(1 - \frac{y^2}{b^2}\right)}}^{\sqrt{a^2 \left(1 - \frac{y^2}{b^2}\right)}} f_{X,Y}(x, y) \, dx
$$


$$
f_Y(y) = \frac{1}{\pi a b} \int_{-\sqrt{a^2 \left(1 - \frac{y^2}{b^2}\right)}}^{\sqrt{a^2 \left(1 - \frac{y^2}{b^2}\right)}} 1 \, dx
$$

The length of the interval for x is:

$$
2 \sqrt{a^2 \left(1 - \frac{y^2}{b^2}\right)}
$$

Thus, the marginal density f_Y(y) becomes:

$$
f_Y(y) = \frac{1}{\pi a b} \cdot 2 \sqrt{a^2 \left(1 - \frac{y^2}{b^2}\right)} = \frac{2}{\pi b} \sqrt{1 - \frac{y^2}{b^2}}, \quad -b \leq y \leq b
$$

- The marginal density of x is:

$$
f_X(x) = \frac{2}{\pi a} \sqrt{1 - \frac{x^2}{a^2}}, \quad -a \leq x \leq a
$$

- The marginal density of y is:

$$
f_Y(y) = \frac{2}{\pi b} \sqrt{1 - \frac{y^2}{b^2}}, \quad -b \leq y \leq b
$$

## Q8
## Find the joint and marginal densities corresponding to the cdf

$$
F(x, y) = (1 - e^{-\alpha x})(1 - e^{-\beta y}), \quad x \geq 0, y \geq 0, \alpha > 0, \beta > 0
$$

## Answer:

### Joint Density
To find the joint density function \( f(x, y) \), differentiate the CDF \( F(x, y) \) with respect to both \( x \) and \( y \):

$$
f(x, y) = \frac{\partial^2 F(x, y)}{\partial x \partial y}
$$

First, differentiate \( F(x, y) \) with respect to \( x \):

$$
\frac{\partial F(x, y)}{\partial x} = \alpha e^{-\alpha x}(1 - e^{-\beta y})
$$

Then, differentiate with respect to \( y \):

$$
f(x, y) = \frac{\partial}{\partial y} \left[ \alpha e^{-\alpha x}(1 - e^{-\beta y}) \right] = \alpha e^{-\alpha x} \cdot \beta e^{-\beta y}
$$

Thus, the **joint density** is:

$$
f(x, y) = \alpha \beta e^{-\alpha x} e^{-\beta y}, \quad x \geq 0, y \geq 0
$$

### Marginal Density of \( X \)
To find the marginal density of \( X \), integrate the joint density over \( y \):

$$
f_X(x) = \int_0^\infty f(x, y) \, dy = \int_0^\infty \alpha \beta e^{-\alpha x} e^{-\beta y} \, dy = \alpha e^{-\alpha x}
$$

Thus, the marginal density of \( X \) is:

$$
f_X(x) = \alpha e^{-\alpha x}, \quad x \geq 0
$$

### Marginal Density of \( Y \)
Similarly, to find the marginal density of \( Y \), integrate the joint density over \( x \):

$$
f_Y(y) = \int_0^\infty f(x, y) \, dx = \int_0^\infty \alpha \beta e^{-\alpha x} e^{-\beta y} \, dx = \beta e^{-\beta y}
$$

Thus, the marginal density of \( Y \) is:

$$
f_Y(y) = \beta e^{-\beta y}, \quad y \geq 0
$$

