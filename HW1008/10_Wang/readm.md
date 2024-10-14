## 49. The gamma function is a generalized factorial function.

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
