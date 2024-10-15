## Q1
49. The gamma function is a generalized factorial function.
### a. Show that Γ(1) = 1.

The gamma function is defined by the integral:

$$
\Gamma(x) = \int_0^\infty t^{x-1} e^{-t} \, dt
$$

For \( x = 1 \):

$$
\Gamma(1) = \int_0^\infty t^{1-1} e^{-t} \, dt = \int_0^\infty e^{-t} \, dt
$$

The integral evaluates to:

$$
\int_0^\infty e^{-t} \, dt = \left[-e^{-t}\right]_0^\infty = 0 - (-1) = 1
$$

$$
Thus, \Gamma(1) = 1 .
$$

### b. Show that Γ(x + 1) = x Γ(x) using integration by parts.

Using the definition of the gamma function:

$$
\Gamma(x + 1) = \int_0^\infty t^x e^{-t} \, dt
$$

Using integration by parts, let:

- \( u = t^x \)  (then \( du = x t^{x-1} \, dt \))
- \( dv = e^{-t} \, dt \) (then \( v = -e^{-t} \))

Applying integration by parts:

$$
\Gamma(x + 1) = \left[-t^x e^{-t}\right]_0^\infty + \int_0^\infty e^{-t} (x t^{x-1}) \, dt
$$

The boundary term evaluates to zero:

$$
\lim_{t \to \infty} (-t^x e^{-t}) = 0 \quad \text{and} \quad \lim_{t \to 0} (-t^x e^{-t}) = 0
$$

Thus:

$$
\Gamma(x + 1) = x \int_0^\infty t^{x-1} e^{-t} \, dt = x \Gamma(x)
$$

### c. Conclude that Γ(n) = (n - 1)! for n = 1, 2, 3, ...

Using the recurrence relation from part b, we can show:

$$
For \( n = 1 \): \( \Gamma(1) = 1 = 0! \)<br>
For \( n = 2 \): \( \Gamma(2) = 1 \cdot \Gamma(1) = 1 = 1! \)<br>
For \( n = 3 \): \( \Gamma(3) = 2 \cdot \Gamma(2) = 2 \cdot 1 = 2 = 2! \)
$$

$$
By induction, if \( \Gamma(k) = (k - 1)! \), then:
$$

$$
\Gamma(k + 1) = k \Gamma(k) = k (k - 1)! = k!
$$

$$
Thus, \( \Gamma(n) = (n - 1)! \) holds for all positive integers \( n \).
$$

### d. Use the fact that Γ(1/2) = √π to show that if n is an odd integer,

$$
\Gamma\left(\frac{n}{2}\right) = \sqrt{\pi} \frac{(n-1)!}{2^{n-1}} \binom{n-1}{\frac{n-1}{2}}.
$$

For an odd integer \( n \), we can write \( n = 2k + 1 \) for some integer \( k \). We can express:

$$
\Gamma\left(\frac{n}{2}\right) = \Gamma\left(k + \frac{1}{2}\right).
$$

Using the recurrence relation, we find:

$$
\Gamma\left(k + \frac{1}{2}\right) = \frac{(2k - 1)!!}{2^k} \sqrt{\pi},
$$

where \( (2k - 1)!! = \frac{(2k)!}{2^k k!} \).

Thus, we get:

$$
\Gamma\left(k + \frac{1}{2}\right) = \sqrt{\pi} \frac{(2k)!}{2^k k!} \cdot \frac{1}{2^k} = \sqrt{\pi} \cdot \frac{(n - 1)!}{2^{n - 1}} \cdot \binom{n - 1}{\frac{n - 1}{2}}.
$$

Therefore, we conclude:

$$
\Gamma\left(\frac{n}{2}\right) = \sqrt{\pi} \frac{(n - 1)!}{2^{n - 1}} \binom{n - 1}{\frac{n - 1}{2}}.
$$


## Q2
### Explanation

in this question we have to show that the normal density integrates to 1 and  
it is given that

$$
\int_{-\infty}^{\infty} \exp\left(-\frac{x^2}{2}\right) dx = \sqrt{2\pi}
$$

squaring both sides and re-express the problem as that of showing

$$
\left( \int_{-\infty}^{\infty} \exp\left(-\frac{x^2}{2}\right) dx \right) \left( \int_{-\infty}^{\infty} \exp\left(-\frac{y^2}{2}\right) dy \right) = 2\pi
$$

---

### Step 1 of 2

if $X \sim N(\mu, \sigma^2)$, then its pdf is:

$$
f_X(x) = \frac{1}{\sigma \sqrt{2\pi}} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right)
$$

where, $\mu \in \mathbb{R}, \sigma > 0$ and $X \in \mathbb{R}$.

we have to show

$$
\int_{-\infty}^{\infty} f_X(x) dx = 1.
$$

firstly let's prove the lemma:

**Lemma:**

$$
\int_{-\infty}^{\infty} \exp\left(-\frac{x^2}{2}\right) dx = \sqrt{2\pi}
$$

let's denote the integral on the left side as $I$. instead of calculating $I$, we'll calculate $I^2$.

as the function under the integral is always strictly positive, we can apply fubini's theorem:

$$
I^2 = \left( \int_{-\infty}^{\infty} \exp\left(-\frac{x^2}{2}\right) dx \right) \cdot \left( \int_{-\infty}^{\infty} \exp\left(-\frac{y^2}{2}\right) dy \right)
$$

$$
= \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} \exp\left( -\frac{x^2 + y^2}{2} \right) dxdy
$$

$$
= \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} \exp\left( -\frac{r^2}{2} \right) dxdy
$$

$$
= \left[ \begin{aligned}
x &= r\cos\varphi \\
y &= r\sin\varphi \\
J &= \begin{vmatrix} \cos\varphi & -r\sin\varphi \\ \sin\varphi & r\cos\varphi \end{vmatrix} = r \\
x^2 + y^2 &= r^2
\end{aligned} \right]
$$

$$
= \int_0^{2\pi} \int_0^{\infty} \exp\left(-\frac{r^2}{2}\right) rdrd\varphi
$$

$$
= \left[ \begin{aligned}
t &= \frac{r^2}{2} \quad r = 0 \Rightarrow t = 0 \\
dt &= r \, dr \quad r = +\infty \Rightarrow t = +\infty
\end{aligned} \right]
$$

$$
= \int_0^{2\pi} \int_0^{\infty} \exp(-t) dtd\varphi
$$

$$
= \int_0^{2\pi} \left[ -\exp(-t)\Big|_0^{\infty} \right] d\varphi
$$

$$
= \int_0^{2\pi} (0 - 1) d\varphi
$$

$$
= \int_0^{2\pi} 1 d\varphi
$$

$$
= 2\pi
$$

hence, the square root of $I^2$ yields:

$$
I = \sqrt{2\pi}
$$

---

### Step 2 of 2

now get returning to our initial statement:

$$
\int_{-\infty}^{\infty} f_X(x) = \int_{-\infty}^{\infty} \frac{1}{\sigma\sqrt{2\pi}} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right) dx
$$

$$
= \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right) dx
$$

$$
= \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} \exp\left(-\frac{y^2}{2}\right) dy \quad \left[ \begin{aligned}
y &= \frac{x-\mu}{\sigma} \quad x = -\infty \Rightarrow y = -\infty \\
dy &= \frac{1}{\sigma} dx \quad x = +\infty \Rightarrow y = +\infty
\end{aligned} \right]
$$

$$
= \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} \exp\left(-\frac{y^2}{2}\right) dy
$$

$$
= \frac{1}{\sqrt{2\pi}} \cdot \sqrt{2\pi}
$$

$$
= 1.
$$

## Q3
### explanation

it is given that $X$ is a random variable with normal distribution with:

$\mu = 5$  
$\sigma = 10$

we have to find:  
(a) $P(X > 10)$  
(b) $P(-20 < X < 15)$  
(c) the value of $x$ such that $P(X > x) = 0.05$.

---

### step 1 of 3

(a) the standardized score is the value $x$ decreased by the mean and then divided by the standard deviation:

$$
z = \frac{x - \mu}{\sigma} \\
z = \frac{10 - 5}{10} \\
\approx 0.50.
$$

the probability of obtaining values below the z-score is then given in the normal probability table in the appendix in the row with 0.5 and in the column with 0.00:

$$
P(Z < 0.50) = 0.6915
$$

on using the complement rule:

$$
P(X > 10) = P(Z > 0.50) \\
= 1 - P(Z < 0.50) \\
= 1 - 0.6915 \\
= 0.3085 \\
= 30.85 \%.
$$

---

### step 2 of 3

(b) the standardized score is the value $x$ decreased by the mean and then divided by the standard deviation:

$$
z = \frac{x - \mu}{\sigma} \\
z = \frac{-20 - 5}{10} \\
\approx -2.50 \\
z = \frac{x - \mu}{\sigma} \\
z = \frac{15 - 5}{10} \\
\approx 1.00
$$

the probability of obtaining values below the z-score $2.50$ is then given in the normal probability table in the appendix in the row with $2.5$ and in the column with $0.00$:

$$
P(Z < 2.50) = 0.9938
$$

the probability of obtaining values below the z-score $1.00$ is then given in the normal probability table in the appendix in the row with $1.0$ and in the column with $0.00$:

$$
P(Z < 1.00) = 0.8413
$$

on using complement rule:

$$
P(-20 < X < 15) = P(-2.50 < Z < 1.00) \\
= P(Z < 1.00) - P(Z < -2.50) \\
= P(Z < 1.00) - P(Z > 2.50) \\
= P(Z < 1.00) - (1 - P(Z < 2.50)) \\
= 0.8413 - (1 - 0.9938) \\
= 0.8413 - 0.0062 \\
= 0.8351 \\
= 83.51 \%.
$$

---

### step 3 of 3

determining the $z$-score in the normal probability table corresponding to a probability of $0.95$:

$$
z = 1.645
$$

we take the average of $1.64$ and $1.65$ because $0.95$ lies exactly in the middle between $0.9495$ and $0.9505$.  
the probability of obtaining values below the $z$-score is then given in the normal probability table in the appendix:

$$
P(Z < 1.645) = 0.95
$$

on using the complement rule:

$$
1 - P(Z > 1.645) = 0.95 \\
P(Z > 1.645) = 0.05
$$

hence we found the $z$-score but we need to determine the corresponding value of $x$.  
the corresponding value $x$ is the mean increased by the product of the $z$-score and standard deviation:

$$
x = \mu + z\sigma \\
x = 5 + 1.645(10) \\
x = 21.45
$$

hence

$$
P(X > 21.45) = 0.05 \\
P(Z > 1.645) = 0.05.
$$

---

### final answer

hence (a) $P(X > 10) = 30.85 \%$  
(b) $P(-20 < X < 15) = 83.51 \%$  
(c) $x = 21.45$.

## Q4
### step 1

given, $U$ is uniform on $[-1,1]$. so, the probability density function of $U$ is:  

$$
f_U(u) = \frac{1}{1 - (-1)} = \frac{1}{2} \quad \text{for} \quad u \in [-1, 1]
$$

$$
= 0, \text{otherwise}
$$

---

### step 2

now, the cumulative distribution of $U^2$ is:  

$$
F_{U^2}(u) = P(U^2 \leq u) = P\left(-\sqrt{u} \leq U \leq \sqrt{u}\right)
$$

$$
= \int_{-\sqrt{u}}^{\sqrt{u}} \frac{1}{2} du = \left(\frac{1}{2}\right) \times \left[u\right]_{-\sqrt{u}}^{\sqrt{u}} = \left(\frac{1}{2}\right) \times \left[\sqrt{u} - (-\sqrt{u})\right] = \sqrt{u}
$$

for $u \in [0, 1]$.

now, $0 \leq u \leq 1 \implies U^2 \leq 1$.

now, the probability density function of $U^2$ is:  

$$
f_{U^2}(u) = \frac{d}{du}\left[F_{U^2}(u)\right] = \frac{d}{du}\left(\sqrt{u}\right) = \frac{1}{2\sqrt{u}},
$$

for $u \in [0, 1]$,

and $f_{U^2}(u) = 0$, otherwise.

---

### explanation:

the probability density function is the derivative of the cumulative distribution function.

---

### answer

the density function of $U^2$ is:  

$$
f_{U^2}(u) = \frac{1}{2\sqrt{u}} \quad \text{for} \quad u \in [0, 1]
$$

$$
= 0, \text{otherwise}.
$$

---

## Proposition C

**Statement:**  
let $Z = F(X)$, where $F$ is the cumulative distribution function (CDF) of $X$. then, $Z$ has a uniform distribution on $[0,1]$.

**Proof:**  
to show that $Z$ follows a uniform distribution on $[0,1]$, we need to prove that the CDF of $Z$ is the CDF of the uniform distribution.

1. start by expressing the CDF of $Z$ as:
   $$P(Z \leq z) = P(F(X) \leq z)$$
   
2. since $F(X)$ is the CDF of $X$, which is a monotonic function, we can invert it:
   $$P(F(X) \leq z) = P(X \leq F^{-1}(z))$$
   
3. by the definition of the CDF, $P(X \leq F^{-1}(z)) = F(F^{-1}(z))$. since $F(F^{-1}(z)) = z$, we get:
   $$P(Z \leq z) = z$$

thus, the CDF of $Z$ is the CDF of the uniform distribution on $[0,1]$. therefore, $Z$ has a uniform distribution on $[0,1]$.

---

## Proposition D

**Statement:**  
let $U$ be a uniform random variable on $[0,1]$, and let $X = F^{-1}(U)$. then the CDF of $X$ is $F$.

**Proof:**  
to show that $X = F^{-1}(U)$ has the CDF $F$, we compute its CDF.

1. begin by expressing the CDF of $X$ as:
   $$P(X \leq x) = P(F^{-1}(U) \leq x)$$
   
2. since $F^{-1}$ is the inverse of the CDF $F$, we can apply $F$ to both sides:
   $$P(F^{-1}(U) \leq x) = P(U \leq F(x))$$
   
3. since $U$ is uniformly distributed on $[0,1]$, we know that $P(U \leq F(x)) = F(x)$. hence, we have:
   $$P(X \leq x) = F(x)$$

thus, the CDF of $X$ is $F$, as required.

### Practical Application:
proposition D is particularly useful for generating random variables with a given CDF $F$. many computer systems and statistical packages provide routines to generate pseudorandom numbers uniformly distributed on $[0, 1]$. using proposition D, if you have such a routine, you can generate random variables with any CDF $F$ by applying $F^{-1}$ to these uniform random numbers. this method is efficient as long as $F^{-1}$ can be computed easily.

---

## Q7
### explanation

it is given that $f(x) = \frac{1 + \alpha y}{2}, x \in [-1, 1], \alpha \in [-1, 1]$, and we have to find how random variables with the following density function can be generated from a uniform random number generator.

---

### step 1 of 2

let $U$ be a uniform random variable on $[0,1]$, and let $X$ be a random variable whose probability density function is the one given in the exercise.  
let's find the CDF of the random variable $X$:

$$
F(x) = P(X \leq x)
$$

$$
= \int_{-\infty}^{x} f_X(y)dy
$$

$$
= \int_{-1}^{x} \frac{1 + \alpha y}{2} dy
$$

$$
= \frac{1}{2} \int_{-1}^{x} 1 dy + \frac{\alpha}{2} \int_{-1}^{x} y dy
$$

$$
= \frac{1}{2} (x + 1) + \frac{\alpha}{2} \frac{y^2}{2} \Big|_{-1}^{x}
$$

$$
= \frac{x + 1}{2} + \frac{\alpha}{4}(x^2 - 1)
$$

according to the proposition, if we define:  

$$
X = F^{-1}(U)
$$

then the CDF of such random variable $X$ is $F$ and PDF is $f$.  
so, now we need to find the formula for $F^{-1}$. since $F$ is a parabola, we can find its inverse by using the formula for the roots of a quadratic equation.

the following holds for $y \in [0,1]$:  

$$
F(x) = y
$$

$$
\frac{x + 1}{2} + \alpha \frac{(x^2 - 1)}{4} = y
$$

$$
2(x + 1) + \alpha (x^2 - 1) = 4y
$$

$$
\alpha x^2 + 2x + (2 - \alpha - 4y) = 0
$$

$$
x_{1,2} = \frac{1}{\alpha} \left( -1 \pm \sqrt{1 - \alpha(2 - \alpha - 4y)} \right)
$$

---

### step 2 of 2

we can choose the $+$ sign in the above formula, so that the values of $x$ are in the interval $[-1,1]$ as they are supposed to be. if we choose the $-$ sign, the image of the function $F^{-1}$ is not in the interval $[0,1]$, as it should be since the random variable $U$ takes values only there.  
therefore, substituting $y$ with $U$ in the above relation, and using the $+$ sign yields that the inverse function of $F$ applied to the random variable $U$ is:

$$
X = F^{-1}(U)
$$

$$
= \frac{1}{\alpha} \left( -1 + \sqrt{1 - \alpha(2 - \alpha - 4U)} \right)
$$

so, once we have generated our random numbers from the uniform random variable $U$, following the above rule, we can transform those values into another set of random numbers, so that they would follow a distribution whose PDF is the given function $f$.

---

### final answer

hence,  

$$
X = \frac{1}{\alpha} \left( -1 + \sqrt{1 - \alpha(2 - \alpha - 4U)} \right)
$$  

is the formula to generate random variables with the given density function from a uniform random number generator.

