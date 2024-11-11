# 03_Brian

by 王邦碩 Brian


## Q2  
### Explain what is the Leibniz integration rule  

#### Leibniz Integration Rule  

The **Leibniz integration rule**, also known as the **differentiation under the integral sign**, describes how to differentiate an integral with respect to a parameter. Consider an integral of the form:  

$$  
I(\alpha) = \int_{a(\alpha)}^{b(\alpha)} f(x, \alpha) \, dx  
$$  



##### Rule Statement  

The Leibniz rule states that the derivative of ( I($\alpha$)) with respect to ( $\alpha$) is given by:  

$$  
\frac{dI(\alpha)}{d\alpha} = \int_{a(\alpha)}^{b(\alpha)} \frac{\partial f(x, \alpha)}{\partial \alpha} \, dx + f(b(\alpha), \alpha) \cdot \frac{db(\alpha)}{d\alpha} - f(a(\alpha), \alpha) \cdot \frac{da(\alpha)}{d\alpha}
$$

## Q3  
### Explanation of the Given Probability Density Function (PDF) 

The image shows the joint probability density function (PDF) of two correlated random variables \( Y_1 \) and \( Y_2 \). Let's break it down:

#### Joint PDF of \( Y_1 \) and \( Y_2 \)

The joint PDF is expressed as:

$$
f_{Y_1, Y_2}(y_1, y_2) = \frac{1}{2\pi} \exp \left( -\frac{2y_1^2 - 2y_1y_2 + y_2^2}{2} \right) = \frac{1}{2\pi} \exp \left( \frac{2y_1^2 + y_2^2 - 2y_1y_2}{2} \right)
$$

This equation can be rewritten in a different form:

$$
f(y_1, y_2) = \frac{1}{2\pi \sigma_{Y_1} \sigma_{Y_2} \sqrt{1 - \rho^2}} \exp \left( -\frac{1}{2(1 - \rho^2)} \left[ \frac{(y_1 - \mu_{Y_1})^2}{\sigma_{Y_1}^2} + \frac{(y_2 - \mu_{Y_2})^2}{\sigma_{Y_2}^2} - \frac{2\rho(y_1 - \mu_{Y_1})(y_2 - \mu_{Y_2})}{\sigma_{Y_1} \sigma_{Y_2}} \right] \right)
$$

#### Parameters and Their Values

From the expressions, we identify:

- $\mu_{Y_1} = 0 \) and \( \mu_{Y_2} = 0 \) (the means of \( Y_1 \) and \( Y_2$
- We need to find the values of $\sigma_{Y_1}, \sigma_{Y_2}, \) and \( \rho$

By comparing coefficients, we have the following equalities:

1. $\sigma_{Y_1} \sigma_{Y_2} \sqrt{1 - \rho^2} = 1$
2. $(1 - \rho^2) \sigma_{Y_1}^2 = \frac{1}{2}$
3. $(1 - \rho^2) \sigma_{Y_2}^2 = 1$
4. $\frac{\rho}{(1 - \rho^2) \sigma_{Y_1} \sigma_{Y_2}} = 1$

##### Solving the Equations  

1. From equations (1) and (4), we find that:   
   $$\frac{\rho}{\sqrt{1 - \rho^2}} = 1 \implies \rho = \sqrt{\frac{1}{2}}$$    

2. Plugging $\rho = \sqrt{\frac{1}{2}}$ into equation (2) gives:  

   $$\sigma_{Y_1} = 1$$   

3. Similarly, plugging $\rho = \sqrt{\frac{1}{2}}$ into equation (3) gives:  

   $$\sigma_{Y_2} = \sqrt{2}$$  

##### Conclusion

Hence, we recognize that the vector \( (Y_1, Y_2) \) follows a bivariate normal distribution with parameters:  

$$
(Y_1, Y_2) \sim \mathcal{N}_2 \left( \left( 0, 0 \right), \left( \begin{array}{cc} 1 & 1 \\ 1 & 2 \end{array} \right) \right)
$$





