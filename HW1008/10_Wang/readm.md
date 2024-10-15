## HW1008Q1

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
\Gamma\left(\frac{n}{2}\right) = \sqrt{\pi} \frac{(n-1)!}{2^{n-1}} \frac{n-1}{\frac{n-1}{2}}.
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

## HW1008Q2

<img width="1022" alt="截圖 2024-10-14 上午9 43 20" src="https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1008/10_Wang/S__1138695_0.jpg">

## HW1008Q3


Let \( X \) be a normal random variable with \( \mu = 5 \) and \( \sigma = 10 \).

## (a) Find P(X > 10)

1. Standardize the value 10:
   - Calculate \( Z = (10 - 5) / 10 = 0.5 \).

2. Find P(Z > 0.5). Using the standard normal distribution table:
   - P(Z < 0.5) is approximately 0.6915.

3. Therefore,
   - P(Z > 0.5) = 1 - P(Z < 0.5) = 1 - 0.6915 = 0.3085.

**Result:** P(X > 10) is approximately 0.3085.

---

## (b) Find P(-20 < X < 15)

1. Standardize the values:
   - For -20: \( Z = (-20 - 5) / 10 = -2.5 \).
   - For 15: \( Z = (15 - 5) / 10 = 1 \).

2. Find P(-2.5 < Z < 1):
   - P(Z < -2.5) is approximately 0.0062.
   - P(Z < 1) is approximately 0.8413.

3. Therefore,
   - P(-2.5 < Z < 1) = P(Z < 1) - P(Z < -2.5) = 0.8413 - 0.0062 = 0.8351.

**Result:** P(-20 < X < 15) is approximately 0.8351.

---

## (c) Find the value of x such that P(X > x) = 0.05

1. We want P(Z > z) = 0.05, which implies P(Z < z) = 0.95.
2. From the standard normal distribution table, we find z such that P(Z < z) = 0.95:
   - z is approximately 1.645.

3. Convert back to x:
   - Set 1.645 = (x - 5) / 10.

4. Solving for x:
   - x - 5 = 1.645 * 10, which gives x - 5 = 16.45, so x = 21.45.

**Result:** The value of x such that P(X > x) = 0.05 is approximately 21.45.


---

### Summary of Answers
- **(a)** P(X > 10) is approximately 0.3085.
- **(b)** P(-20 < X < 15) is approximately 0.8351.
- **(c)** x is approximately 21.45.


## HW1008Q4

Let \( U \) be a uniform random variable on the interval \([-1, 1]\). We want to find the density function of \( Y = U^2 \).

Step 1: Identify the Distribution of \( U \)

The probability density function (pdf) of \( U \) is given by:

$$
f_U(u) = 
\begin{cases} 
\frac{1}{2} & \text{for } -1 \leq u \leq 1 \\ 
0 & \text{otherwise} 
\end{cases}
$$

Step 2: Determine the Range of \( Y \)

Since \( U \) takes values in \([-1, 1]\), the values of \( Y = U^2 \) will range from \( 0 \) to \( 1 \).

Step 3: Find the Cumulative Distribution Function (CDF) of \( Y \)

The cumulative distribution function (CDF) of \( Y \), denoted \( F_Y(y) \), is defined as:

$$
F_Y(y) = P(Y \leq y) = P(U^2 \leq y)
$$

This can be expressed as:

$$
P(-\sqrt{y} \leq U \leq \sqrt{y})
$$

for \( 0 \leq y \leq 1 \).

Calculating this, we have:

$$
F_Y(y) = P(-\sqrt{y} \leq U \leq \sqrt{y}) = \int_{-\sqrt{y}}^{\sqrt{y}} f_U(u) \, du
$$

Substituting \( f_U(u) = \frac{1}{2} \):

$$
F_Y(y) = \int_{-\sqrt{y}}^{\sqrt{y}} \frac{1}{2} \, du = \frac{1}{2} \left[ u \right]_{-\sqrt{y}}^{\sqrt{y}} = \frac{1}{2} \left( \sqrt{y} - (-\sqrt{y}) \right) = \frac{1}{2} (2\sqrt{y}) = \sqrt{y}
$$

Step 4: Differentiate the CDF to Find the PDF

The probability density function \( f_Y(y) \) is obtained by differentiating \( F_Y(y) \):

$$
f_Y(y) = \frac{d}{dy} F_Y(y) = \frac{d}{dy} (\sqrt{y}) = \frac{1}{2\sqrt{y}}
$$

Step 5: Specify the Range of \( y \)

The pdf is defined for \( 0 < y < 1 \). Thus, we have:

$$
f_Y(y) = 
\begin{cases} 
\frac{1}{2\sqrt{y}} & \text{for } 0 < y < 1 \\ 
0 & \text{otherwise} 
\end{cases}
$$

Final Result:

The density function of \( Y = U^2 \) is:

$$
f_Y(y) = 
\begin{cases} 
\frac{1}{2\sqrt{y}} & \text{for } 0 < y < 1 \\ 
0 & \text{otherwise} 
\end{cases}
$$

## HW1008 Q5

# Proposition C

Let Z = F(X); then Z has a uniform distribution on [0, 1].

## Proof

1. **Find the CDF of Z**: To find the distribution of Z, we can assume the cdf of random varible Z is f(z), 
   <br>
   f(z) = P(Z ≤ z) for z ∈ [0, 1]:
   
   P(Z ≤ z) = P(F(X) ≤ z)

2. **Use the Properties of the CDF**: Since cdf is a strictly increasing function(the definaition of cdf),<br> the event F(X) ≤ z is equivalent to X ≤ F<sup>-1</sup>(z):
   <br>
   P(F(X) ≤ z) = P(X ≤ F<sup>-1</sup>(z))

3. **Apply the Definition of the CDF**: By the definition of the CDF:
   <br>
   P(X ≤ F<sup>-1</sup>(z)) = F(F<sup>-1</sup>(z))
   
   F(F<sup>-1</sup>(z)) evaluates the CDF at the point where the cumulative probability is z.

5. **Simplify**: For a continuous random variable, F(F<sup>-1</sup>(z)) = z for z ∈ [0, 1]:
   <br>
   P(Z ≤ z) = z

6. **Conclusion**: Since P(Z ≤ z) = z for 0<=z<=1, this shows that Z follows a uniform distribution on [0, 1].

## HW1008Q6

PROOF $P(X\le x)$ = $F(x)$

 $P(X\le x)$ = $P(F^{-1}(U) \le x)$

 = $P(U \le F(x))$ (F is monotone increasing function, $F(F^{-1}(U))=U$)

 = $F(x)$  (U is uniform on [0,1], so $P(U \le F(x))$ = $F(x)$ )

 Therefore, the cdf of x is F

 ## HW1008Q7

 <img width="1022" alt="截圖 2024-10-14 上午9 43 20" src="https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1008/10_Wang/S__1138693_0.jpg">
