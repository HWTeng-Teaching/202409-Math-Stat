![image](https://github.com/user-attachments/assets/14c8ac72-029c-468e-9a03-01f3dc045ff0)
### a.
The marginal frequency function of \(X\), \( P(X = x) \), is obtained by summing over the values of \( Y \) for each value of \( X \).

- \( P(X = 1) = 0.10 + 0.05 + 0.02 + 0.02 = 0.19 \)
- \( P(X = 2) = 0.05 + 0.20 + 0.05 + 0.02 = 0.32 \)
- \( P(X = 3) = 0.02 + 0.05 + 0.20 + 0.04 = 0.31 \)
- \( P(X = 4) = 0.02 + 0.02 + 0.04 + 0.10 = 0.18 \)

Thus, the marginal distribution of $\(X\)$ is:

![image](https://github.com/user-attachments/assets/31f43312-6948-494e-8022-bf972b1a9ced)


#### Marginal Frequency Function of Y

The marginal frequency function of \(Y\), \( P(Y = y) \), is obtained by summing over the values of \( X \) for each value of \( Y \).

- \( P(Y = 1) = 0.10 + 0.05 + 0.02 + 0.02 = 0.19 \)
- \( P(Y = 2) = 0.05 + 0.20 + 0.05 + 0.02 = 0.32 \)
- \( P(Y = 3) = 0.02 + 0.05 + 0.20 + 0.04 = 0.31 \)
- \( P(Y = 4) = 0.02 + 0.02 + 0.04 + 0.10 = 0.18 \)

Thus, the marginal distribution of \(Y\) is:  

![image](https://github.com/user-attachments/assets/eac79417-2397-48d3-9e99-69ffb83e4b37)
### b.
To find $\( P(X = x \mid Y = 1) \)$, we use the formula:

$\[
P(X = x \mid Y = 1) = \frac{P(X = x, Y = 1)}{P(Y = 1)}
\]$

We already know \( P(Y = 1) = 0.19 \). Using the joint probabilities from the table:

- $\( P(X = 1 \mid Y = 1) = \frac{0.10}{0.19} \approx 0.526 \)$
- $\( P(X = 2 \mid Y = 1) = \frac{0.05}{0.19} \approx 0.263 \)$
- $\( P(X = 3 \mid Y = 1) = \frac{0.02}{0.19} \approx 0.105 \)$
- $\( P(X = 4 \mid Y = 1) = \frac{0.02}{0.19} \approx 0.105 \)$

Thus, the conditional distribution of$ \(X\)$ given $\(Y = 1\)$ is:

![image](https://github.com/user-attachments/assets/76cd6f7b-4a12-4e52-aa6c-011f3cfa4c11)


### Conditional Frequency of Y given X = 1

To find $\( P(Y = y \mid X = 1) \)$, we use the formula:

$\[
P(Y = y \mid X = 1) = \frac{P(X = 1, Y = y)}{P(X = 1)}
\]$

We already know $\( P(X = 1) = 0.19 \)$. Using the joint probabilities from the table:

- $\( P(Y = 1 \mid X = 1) = \frac{0.10}{0.19} \approx 0.526 \)$
- $\( P(Y = 2 \mid X = 1) = \frac{0.05}{0.19} \approx 0.263 \)$
- $\( P(Y = 3 \mid X = 1) = \frac{0.02}{0.19} \approx 0.105 \)$
- $\( P(Y = 4 \mid X = 1) = \frac{0.02}{0.19} \approx 0.105 \)$

Thus, the conditional distribution of $\(Y\)$ given $\(X = 1\)$ is:  

![image](https://github.com/user-attachments/assets/f27a7f67-935a-4bec-9035-6c231cfa9f0c)
_________________
![image](https://github.com/user-attachments/assets/4d520c5d-49ec-41ed-8a88-b92384b9724d)
### a. Probability Calculations

We compute the following probabilities by integrating the joint density function over the appropriate regions.

#### (i) $\( P(X > Y) \)$

To find $\( P(X > Y) \)$, we integrate over the region where $\( x > y \)$ :
$\[
P(X > Y) = \int_0^1 \int_0^x \frac{6}{7} (x + y)^2 \, dy \, dx
\]$

#### (ii) $\( P(X + Y \leq 1) \)$

We integrate over the region where $\( x + y \leq 1 \)$ :
$\[
P(X + Y \leq 1) = \int_0^1 \int_0^{1-x} \frac{6}{7} (x + y)^2 \, dy \, dx
\]$

#### (iii) $\( P(X \leq \frac{1}{2}) \)$

We integrate over the region where $\( x \leq \frac{1}{2} \)$ :
$\[
P(X \leq \frac{1}{2}) = \int_0^{1/2} \int_0^1 \frac{6}{7} (x + y)^2 \, dy \, dx
\]$

### b. Marginal Densities

#### Marginal Density of$ \( X \)$, $\( f_X(x) \)$

To find the marginal density of $\(X\)$, we integrate out $\(y\)$ :
$\[
f_X(x) = \int_0^1 \frac{6}{7} (x + y)^2 \, dy
\]$

#### Marginal Density of $\( Y \)$ , $\( f_Y(y) \)$

To find the marginal density of $\(Y\)$ , we integrate out $\(x\)$ :
$\[
f_Y(y) = \int_0^1 \frac{6}{7} (x + y)^2 \, dx
\]$

### c. Conditional Densities

#### Conditional Density of $\( X \) given \( Y = y \)$

The conditional density $\( f_{X|Y}(x \mid y) \)$ is given by:
$\[
f_{X|Y}(x \mid y) = \frac{f(x, y)}{f_Y(y)} = \frac{\frac{6}{7} (x + y)^2}{f_Y(y)}, \quad 0 \leq x \leq 1
\]$

#### Conditional Density of $\( Y \) given \( X = x \)$

The conditional density $\( f_{Y|X}(y \mid x) \)$ is given by:
$\[
f_{Y|X}(y \mid x) = \frac{f(x, y)}{f_X(x)} = \frac{\frac{6}{7} (x + y)^2}{f_X(x)}, \quad 0 \leq y \leq 1
\]$

![image](https://github.com/user-attachments/assets/3864889d-d19d-46b9-a04d-8e5386ab3950)
## a. Marginal Densities of \(X\) and \(Y\)

### Step 1: Find the Total Area of the Region

The region is bounded by $\( y = 1 - x^2 \)$ and $\( x \)$ ranges from $\(-1\) to \(1\)$. The area $\(A\)$ of the region is:
$\[
A = \int_{-1}^1 \int_0^{1 - x^2} dy \, dx = \int_{-1}^1 (1 - x^2) \, dx
\]$
Solving:
$\[
A = \int_{-1}^1 1 \, dx - \int_{-1}^1 x^2 \, dx = 2 - \frac{2}{3} = \frac{4}{3}
\]$

Thus, the total area of the region is $\( A = \frac{4}{3} \)$.

### Step 2: Joint Density Function $\( f(x, y) \)$

Since the distribution is uniform, the joint density function is constant and given by:
$\[
f(x, y) = \frac{1}{A} = \frac{3}{4}
\]$
for $\( -1 \leq x \leq 1 \) and \( 0 \leq y \leq 1 - x^2 \)$.

### Step 3: Marginal Density of $\( X \)$, $\( f_X(x) \)$

To find the marginal density of $\(X\)$, integrate the joint density over $\(y\)$:
$\[
f_X(x) = \int_0^{1 - x^2} \frac{3}{4} \, dy = \frac{3}{4} (1 - x^2)
\]$
Thus, the marginal density of $\(X\)$ is:
$\[
f_X(x) = \frac{3}{4} (1 - x^2), \quad -1 \leq x \leq 1
\]$

### Step 4: Marginal Density of $\( Y \)$, $\( f_Y(y) \)$

To find the marginal density of $\(Y\)$, we determine the range of $\(x\)$ for a given $\(y\)$. From $\( y \leq 1 - x^2 \)$, we get $\( |x| \leq \sqrt{1 - y} \)$. Thus, $\( x \)$ ranges from $\(-\sqrt{1 - y}\)$ to $\( \sqrt{1 - y} \)$. The marginal density of $\(Y\)$ is:
$\[
f_Y(y) = \int_{-\sqrt{1 - y}}^{\sqrt{1 - y}} \frac{3}{4} \, dx = \frac{3}{2} \sqrt{1 - y}, \quad 0 \leq y \leq 1
\]$

### b. Conditional Densities

#### Conditional Density of $\(Y\)$ given $\(X = x\)$

The conditional density $\( f_{Y|X}(y \mid x) \)$ is given by:
$\[
f_{Y|X}(y \mid x) = \frac{f(x, y)}{f_X(x)} = \frac{\frac{3}{4}}{\frac{3}{4} (1 - x^2)} = \frac{1}{1 - x^2}, \quad 0 \leq y \leq 1 - x^2
\]$

#### Conditional Density of $\(X\)$ given $\(Y = y\)$

The conditional density $\( f_{X|Y}(x \mid y) \)$ is given by:
$\[
f_{X|Y}(x \mid y) = \frac{f(x, y)}{f_Y(y)} = \frac{\frac{3}{4}}{\frac{3}{2} \sqrt{1 - y}} = \frac{1}{2\sqrt{1 - y}}, \quad -\sqrt{1 - y} \leq x \leq \sqrt{1 - y}
\]$


![image](https://github.com/user-attachments/assets/2b17092b-896a-4eb0-a9c7-aa8c314bd06c)
Let $\( U_1 \), \( U_2 \), and \( U_3 \)$ be independent random variables uniformly distributed on $\([0, 1]\)$. We are tasked with finding the probability that the quadratic equation:

$\[
U_1 x^2 + U_2 x + U_3 = 0
\]$

has real roots, i.e., the discriminant $\( \Delta = U_2^2 - 4 U_1 U_3 \geq 0 \)$.

#### Step 1: Condition for Real Roots

For the quadratic equation to have real roots, the discriminant must satisfy:

$\[
U_2^2 \geq 4 U_1 U_3
\]$

Thus, the probability we seek is:

$\[
P(U_2^2 \geq 4 U_1 U_3)
\]$

#### Step 2: Setting Up the Integral

The probability can be calculated as the volume of the region in the unit cube $\([0, 1]^3\)$ where $\( U_2^2 \geq 4 U_1 U_3 \)$. This volume is given by the triple integral:

$\[
P(U_2^2 \geq 4 U_1 U_3) = \int_0^1 \int_0^1 \int_0^{\min\left(1, \frac{U_2^2}{4U_1}\right)} dU_3 \, dU_2 \, dU_1
\]$

#### Step 3: Splitting the Integral

We need to split the region of integration into two cases:
1. For $\( 0 \leq U_2 \leq 2\sqrt{U_1} \)$, we have $\( \min\left(1, \frac{U_2^2}{4U_1}\right) = \frac{U_2^2}{4U_1} \)$.
2. For $\( 2\sqrt{U_1} \leq U_2 \leq 1 \)$, we have $\( \min\left(1, \frac{U_2^2}{4U_1}\right) = 1 \)$.

Thus, the integral becomes:

$\[
P(U_2^2 \geq 4 U_1 U_3) = \int_0^1 \left[ \int_0^{2\sqrt{U_1}} \frac{U_2^2}{4 U_1} dU_2 + \int_{2\sqrt{U_1}}^1 1 \, dU_2 \right] dU_1
\]$

#### Step 4: Solving the First Integral

For $\( 0 \leq U_2 \leq 2\sqrt{U_1} \)$, the first integral is:

$\[
\int_0^{2\sqrt{U_1}} \frac{U_2^2}{4U_1} dU_2 = \frac{1}{4 U_1} \int_0^{2\sqrt{U_1}} U_2^2 \, dU_2
\]$

The integral of $\( U_2^2 \)$ is:

$\[
\frac{1}{4 U_1} \cdot \frac{(2 \sqrt{U_1})^3}{3} = \frac{2 \sqrt{U_1}}{3}
\]$

#### Step 5: Solving the Second Integral

For $\( 2 \sqrt{U_1} \leq U_2 \leq 1 \)$, the second integral is:

$\[
\int_{2\sqrt{U_1}}^1 1 \, dU_2 = 1 - 2 \sqrt{U_1}
\]$

#### Step 6: Combine and Integrate Over $\( U_1 \)$

Now, combine the integrals:

$\[
P(U_2^2 \geq 4 U_1 U_3) = \int_0^1 \left( \frac{2 \sqrt{U_1}}{3} + 1 - 2 \sqrt{U_1} \right) dU_1
\]$

Simplify the integrand:

$\[
\frac{2 \sqrt{U_1}}{3} + 1 - 2 \sqrt{U_1} = 1 - \frac{4 \sqrt{U_1}}{3}
\]$

Now, integrate with respect to $\( U_1 \)$:

$\[
\int_0^1 \left( 1 - \frac{4 \sqrt{U_1}}{3} \right) dU_1 = \left[ U_1 \right]_0^1 - \frac{4}{3} \int_0^1 \sqrt{U_1} \, dU_1
\]$

The integral of $\( \sqrt{U_1} \)$ is:

$\[
\int \sqrt{U_1} \, dU_1 = \frac{2}{3} U_1^{3/2}
\]$

Thus:

$\[
\frac{4}{3} \int_0^1 \sqrt{U_1} \, dU_1 = \frac{4}{3} \cdot \frac{2}{3} = \frac{8}{9}
\]$

#### Final Step: Compute the Probability

Now subtract the result:

$\[
P(U_2^2 \geq 4 U_1 U_3) = 1 - \frac{8}{9} = \frac{1}{9}
\]$

#### Conclusion

The probability that the quadratic equation $\( U_1 x^2 + U_2 x + U_3 = 0 \)$ has real roots is:

$\[
P(\text{real roots}) = \boxed{\frac{1}{9}}$
_______________________________________________________________________________________________
![image](https://github.com/user-attachments/assets/4db3d87f-b5b6-4d35-b330-0cee2a989107)
![image](https://github.com/user-attachments/assets/2dfe7c45-670e-468f-ad0c-549c380e6b83)

_________________________________________________________________________________________________-
![image](https://github.com/user-attachments/assets/5f39cb6b-8f0c-4339-8fee-88ad96cfd5f9) 
### Step 1: Understanding the Variables

- Let $\(N(t_0, t_1)\)$ be the number of events in the interval $\((t_0, t_1)\)$.
- Let $\(N(t_0, t_2)\)$ be the number of events in the interval $\((t_0, t_2)\)$.
- The time intervals can be expressed as:
  - $\(N(t_0, t_1)\)$ corresponds to events that occur between $\(t_0\)$ and $\(t_1\)$.
  - $\(N(t_1, t_2)\)$ corresponds to events that occur between $\(t_1\)$ and $\(t_2\)$.

### Step 2: Properties of a Poisson Process

- For a Poisson process with rate $\(\lambda\)$, the number of events in any interval of length $\(t\)$ follows a Poisson distribution:
  $\[
  N(a, b) \sim \text{Poisson}(\lambda (b - a)).
  \]$
- The counts in disjoint intervals are independent.

### Step 3: Distributions of Counts

- The total number of events in the interval $\((t_0, t_2)\)$ can be expressed as:
  $\[
  N(t_0, t_2) = N(t_0, t_1) + N(t_1, t_2).
  \]$
- Therefore, we know:
  - $\(N(t_0, t_2) \sim \text{Poisson}(\lambda (t_2 - t_0))\)$.
  - $\(N(t_0, t_1) \sim \text{Poisson}(\lambda (t_1 - t_0))\)$.
  - $\(N(t_1, t_2) \sim \text{Poisson}(\lambda (t_2 - t_1))\)$.

### Step 4: Conditional Distribution

- Given $\(N(t_0, t_2) = n\)$, we want to find the distribution of $\(N(t_0, t_1)\)$.
- Since the counts are independent, we can think of the distribution of $\(N(t_0, t_1)\)$ as a multinomial distribution where:
  - The total $\(n\)$ events are distributed among the intervals $\((t_0, t_1)\)$ and $\((t_1, t_2)\)$.

### Step 5: Applying the Multinomial Distribution

- The conditional distribution $\(N(t_0, t_1) | N(t_0, t_2) = n\)$ follows a binomial distribution because:
  $\[
  N(t_0, t_1) | N(t_0, t_2) = n \sim \text{Binomial}\left(n, \frac{t_1 - t_0}{t_2 - t_0}\right).
  \]$
- The parameter $\(p = \frac{t_1 - t_0}{t_2 - t_0}\)$ represents the proportion of the length of the interval $\((t_0, t_1)\)$ relative to the total length of the interval $\((t_0, t_2)\)$.

### Conclusion

The conditional distribution of $\(N(t_0, t_1)\)$ given $\(N(t_0, t_2) = n\)$ is:

$\[
N(t_0, t_1) | N(t_0, t_2) = n \sim \text{Binomial}\left(n, \frac{t_1 - t_0}{t_2 - t_0}\right).
\]$

This reflects that given a fixed number of events $\(n\)$, the number of events in the subinterval $\((t_0, t_1)\)$ follows a binomial distribution based on the proportion of the interval lengths.
