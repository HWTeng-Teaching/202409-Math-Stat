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

![image](https://github.com/user-attachments/assets/4db3d87f-b5b6-4d35-b330-0cee2a989107)

![image](https://github.com/user-attachments/assets/5f39cb6b-8f0c-4339-8fee-88ad96cfd5f9)
