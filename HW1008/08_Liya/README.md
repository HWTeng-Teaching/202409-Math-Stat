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
<img width="749" alt="image" src="https://github.com/user-attachments/assets/7faff3f6-f1ea-46c4-93a5-9035f68a7bf1">

## Quesrion 2.53
<img width="768" alt="image" src="https://github.com/user-attachments/assets/13fbce3f-a3c0-48c4-b3b8-3efff2b801bc">

<img width="760" alt="image" src="https://github.com/user-attachments/assets/790c8813-07a6-4c8c-b076-2799590f9440">


## Question 2.59

<img width="727" alt="image" src="https://github.com/user-attachments/assets/02b6c00b-8660-46b2-b3f0-0eb702222dc2">


## Question 2.65

<img width="732" alt="image" src="https://github.com/user-attachments/assets/d3a02c58-9080-44c2-b8de-0df0182e0c46">

## Proof C
<img width="721" alt="image" src="https://github.com/user-attachments/assets/8a2d1f96-396a-487f-90ab-e2e262edb805">

## Proof D
<img width="770" alt="image" src="https://github.com/user-attachments/assets/0002388e-4af4-4d33-a532-91d8260c884c">





