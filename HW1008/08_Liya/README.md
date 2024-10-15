# HW 1008 by LIYA
## Questions 2.49
<img width="633" alt="image" src="https://github.com/user-attachments/assets/d82382cf-e7c2-4898-bac6-6e65d73ef3b3">

### Solution
a) Lets define Gamma function 

$\\Gamma(x) = \int_0^\infty t^{x-1} e^{-t} \ dt\$

Now, lets input  \(x = 1\):

$\\Gamma(1) = \int_0^\infty t^{1-1} e^{-t} \ dt = \int_0^\infty e^{-t} \ dt\$

$\\int_0^\infty e^{-t} \ dt = \left[-e^{-t}\right]_0^\infty = 0 - (-1) = 1\$

Therefore, $\\Gamma(1) = 1$


b) lets input $\\Gamma(x + 1)\:$ in the formula 

$\\Gamma(x + 1) = \int_0^\infty t^{(x + 1) - 1} e^{-t} \ dt = \int_0^\infty t^x e^{-t} \ dt\$

Integration by parts:
$\ u = t^x,\  \\ therefore --> du = x * t^{x-1} dt\$

$\ dv = e^{-t} dt,\ \\ therefore -->  v = -e^{-t}\$

$\\int u \ dv = uv - \int v \ du\$
$\\int_0^\infty t^x e^{-t} \ dt = \left[ -t^x e^{-t} \right]_0^\infty + \int_0^\infty e^{-t} x t^{x-1} \ dt\$

$\\left[ -t^x e^{-t} \right]_0^\infty = 0 - 0 = 0\$

$\\Gamma(x + 1) = x \int_0^\infty t^{x-1} e^{-t} \ dt = x \Gamma(x)\$

Therefore, $\\Gamma(x + 1) = x \Gamma(x)\$


c) Lets use properties from (a) and (b);

1) $For \(n = 1\) :\$
   
 $\Gamma(1) = 1 = 0!\$


2) $For \(n = 2\):\$
   
  $\Gamma(2) = 1 \cdot \Gamma(1) = 1 = 1! \$

3) $For \(n = 3\):\$

  $\Gamma(3) = 2 \cdot \Gamma(2) = 2 \cdot 1 = 2 = 2! \$

  
4) For any positive integer \(n\), we can prove:

 #### Note
 
 We know $\(\Gamma(n) = (n - 1)!\)$
Using the recurrence relation:
$\\Gamma(n) = (n - 1) \Gamma(n - 1)\$

By induction or recursively:

Base case: $\(\Gamma(1) = 1 = 0!\)$ 

 Lets assume true for \(k\), then for \(k + 1\):
 
  $\\Gamma(k + 1) = k \Gamma(k) = k(k - 1)! = k! = (k + 1 - 1)! \$

  #### therefore, 

   $\\Gamma (n) = (n - 1)!\) holds for \ n = 1, 2, 3, \ldots\$


D) 










## Question 2.51


<img width="648" alt="image" src="https://github.com/user-attachments/assets/211a1fbd-0eda-4cbb-a480-48499da885c2">

