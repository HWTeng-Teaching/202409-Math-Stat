## Q1: What are the key points in Lec 1105

<img width="1007" alt="截圖 2024-11-12 下午1 38 40" src="https://github.com/user-attachments/assets/ef15b40c-4fcb-40ee-b241-65d2a0cf3619">
<img width="1007" alt="截圖 2024-11-12 下午1 38 51" src="https://github.com/user-attachments/assets/2af86b28-bfac-49dd-b660-a93a6f2461d0">
<img width="924" alt="截圖 2024-11-12 下午1 39 02" src="https://github.com/user-attachments/assets/d16c826a-20a8-48de-9c36-122298841d9b">
<img width="914" alt="截圖 2024-11-12 下午1 39 38" src="https://github.com/user-attachments/assets/78d49d87-6f10-46b2-ad65-a11c9ba37ce2">
<img width="997" alt="截圖 2024-11-12 下午1 39 58" src="https://github.com/user-attachments/assets/dbd07f17-8643-471d-9f9c-04121dd39f90">

## Q2: Explain what is the Leibniz integration rule

The **Leibniz integration rule** refers to a method for differentiating an integral whose limits of integration or the integrand depend on a parameter. It provides a systematic way to take the derivative of an integral where the upper and/or lower limits of integration are variable functions.

**General form of Leibniz's rule**:
If we have an integral of the form:

$$
I(z) = \int_{a(z)}^{b(z)} f(z, u) \, du
$$

where $a(z)$ and $b(z)$ are functions of $z$, and $f(z, u)$ is a function of $z$ and $u$, then the derivative of $I(z)$ with respect to $z$ is given by:

$$
\frac{d}{dz}I(z) = f(z, b(z)) \frac{d}{dz}b(z) - f(z, a(z)) \frac{d}{dz}a(z) + \int_{a(z)}^{b(z)} \frac{\partial}{\partial z} f(z, u)du
$$

### Explanation:
- The **first term** $f(z, b(z)) \frac{d}{dz}b(z)$ accounts for the change in the integral's value due to the change in the upper limit $b(z)$.
  
- The **second term** $-f(z, a(z)) \frac{d}{dz}a(z)$ represents the change due to the change in the lower limit $a(z)$.

  
- The **third term** $\int_{a(z)}^{b(z)} \frac{\partial}{\partial z} f(z, u)du$ accounts for the direct change in the integrand $f(z, u)$ with respect to $z$ over the interval of integration.

## Q3: Identity  the bivaraite normal disitriubtion of page 14 of the slides in class

<img width="923" alt="截圖 2024-11-12 下午1 34 06" src="https://github.com/user-attachments/assets/3edf74ab-de17-4067-ae15-8b03147d28b6">

## Q4: Use the inverse method to generate 1000 samples of stnadard normal

<img width="938" alt="截圖 2024-11-11 下午8 31 09" src="https://github.com/user-attachments/assets/0cad6012-3c45-4bcb-a131-7c102310dcbb">
<img width="564" alt="截圖 2024-11-11 下午8 32 29" src="https://github.com/user-attachments/assets/2054a237-cffc-45fb-bbc9-e3508b2300a9">

## Q5: Use the polar method to generate 1000 samples of standard normal

<img width="583" alt="截圖 2024-11-11 下午8 32 38" src="https://github.com/user-attachments/assets/87723224-483e-4f22-80af-67f38f81c77e">
<img width="583" alt="截圖 2024-11-11 下午8 32 46" src="https://github.com/user-attachments/assets/0ca9afad-6edb-41d0-98b6-e3fc302e9d81">
