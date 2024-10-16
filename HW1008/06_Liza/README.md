by Liza

## Question 1
![image](https://github.com/user-attachments/assets/6e168c6f-b871-4463-b71f-abba419c70be)

## Solution 
The gamma function, **$Г(t)$**, is defined as 

$\Gamma(x) = \int_{0}^{\infty} t^{x-1} \cdot e^{-t} \, dt, \quad x > 0$

## Part A
For $\( x = 1 \)$:  
$\Gamma(1) = \int_{0}^{\infty} t^{1-1} e^{-t} \, dt = \int_{0}^{\infty} e^{-t}dt$

The integral $\(\int_{0}^{\infty} e^{-t} \, dt\)$ evaluates to 1:  
$\int_{0}^{\infty} e^{-t}  dt = \left[ -e^{-t} \right]_{0}^{\infty} = 0 - (-1) = 1$

So, $\Gamma(1) = 1$.

## Part B
To prove this, we’ll use integration by parts. Recall that:
$\int u \ dv = uv - \int v \, du$

Let’s apply this to $\Gamma(x+1)$:
$\Gamma(x+1) = \int_{0}^{\infty} t^x e^{-t} dt$

Let $\( u = t^x \)$ and $\( dv = e^{-t} \ dt \)$.

Then, $\( du = x t^{x-1} dt \)$ and $\( v = -e^{-t} \)$.

Now, integrate by parts:
$\int_{0}^{\infty} t^x e^{-t}\ dt$ = $\left[ -e^{-t} \right]_{0}^{\infty}$ + $\int_{0}^{\infty} t^{x-1} e^{-t} dt$ 
Evaluating the boundary term:

- As $\( t \to \infty \), \( t^x e^{-t} \to 0 \)$.
- As $\( t \to 0 \), \( t^x e^{-t} \to 0 \)$.

So, the boundary term is 0, and we get:
$\int_{0}^{\infty} t^x e^{-t} dt = 0 + \int_{0}^{\infty} x t^{x-1} e^{-t} dt = x \int_{0}^{\infty} t^{x-1} e^{-t} dt$

This simplifies to:
$\Gamma(x+1) = x \Gamma(x)$

## Part C
We can use the result from part (b) to show this. We have:
$\Gamma(n+1) = n \Gamma(n)$

If we continue applying this property, we get:
$\Gamma(n) = (n-1) \Gamma(n-1) = (n-1)(n-2) \Gamma(n-2) = \ldots = (n-1)!$

Since $\(\Gamma(1) = 1\)$, it follows that:
$\Gamma(n) = (n-1)!$
for $\( n = 1, 2, 3, \ldots \)$.

## Part D
![image](https://github.com/user-attachments/assets/dd8e7b6e-dd4e-48ed-bc8b-67a080ec11bd)



