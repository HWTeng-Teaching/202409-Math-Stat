by Liza

## Question 1
<img src="https://github.com/user-attachments/assets/6e168c6f-b871-4463-b71f-abba419c70be" alt="image" width="570" height="200">


## Solution 
The gamma function, **$Г(t)$**, is defined as 

$\Gamma(x) = \int_{0}^{\infty} t^{x-1} \cdot e^{-t} \ dt, \quad x > 0$

## Part A: Show that $\Gamma(1) = 1$.
For $\( x = 1 \)$:  
$\Gamma(1) = \int_{0}^{\infty} t^{1-1} e^{-t} \ dt = \int_{0}^{\infty} e^{-t}dt$

The integral $\int_{0}^{\infty} e^{-t} dt$ evaluates to 1:  
$\int_{0}^{\infty} e^{-t}  dt = \left[ -e^{-t} \right]_{0}^{\infty} = 0 - (-1) = 1$

So, $\Gamma(1) = 1$.

## Part B Show that  $\Gamma(x+1) = x\Gamma(x)$
To prove this, we’ll use integration by parts. Recall that:  
<img src="https://github.com/user-attachments/assets/5a92b12d-1267-4ba9-aa83-79ffed09e841" alt="image" width="170" height="70">


Let’s apply this to $\Gamma(x+1)$:
$\Gamma(x+1) = \int_{0}^{\infty} t^x e^{-t} dt$

<img src="https://github.com/user-attachments/assets/8f0886ea-45e0-4790-8d58-98d1791c526f" alt="image" width="550" height="500">


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
<img src="https://github.com/user-attachments/assets/dd8e7b6e-dd4e-48ed-bc8b-67a080ec11bd" alt="image" width="465" height="640">


## Question 2

## Solution 
![image](https://github.com/user-attachments/assets/ed69ad40-02d2-472b-be4a-a93f553e47e2)
![image](https://github.com/user-attachments/assets/7254b520-42a5-4be3-ac2f-db54a684915c)
![image](https://github.com/user-attachments/assets/2b1bd13a-c1d2-43bb-b224-c0810735cb01)

![image](https://github.com/user-attachments/assets/19102c35-2605-44a0-bbbc-5712dfbe95e4)
![image](https://github.com/user-attachments/assets/4e7a4627-409b-4c12-9674-25099b308d3c)

![image](https://github.com/user-attachments/assets/088c4b25-7936-4a53-bbec-d426b5a87d3a)




