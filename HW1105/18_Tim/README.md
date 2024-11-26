----------------------------------------------------------------------------
1.What are the key points in Lec 1105((我決定偷偷塞中文這邊老師簡報內容都是先利用joint distibution來驗證另一種方法的正確性

 1. joint density & transformation with example ( use joint distibution proof that R ~ chi(2) )
    可以用chi distubution算出一樣的答案
 2. bivariate normal density(since Y is the linear combination of X) 
    可以用一般的方法推出一樣的結果
    簡單來說因為X1 X2 ~ N(0,1) 所以平均都是0 表準差都是1 然後彼此joint都是0
    用這些性質去推出Y1 Y2
 3. leibniz integration rule
----------------------------------------------------------------------------
2.explain what is leibniz integration rule
  https://youtu.be/zbWihK9ibhc?si=zCuQF_Mpk9jIVPZ_
----------------------------------------------------------------------------
3.投影片裡有清楚說明
----------------------------------------------------------------------------
4.
![image](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1105/18_Tim/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-11-25%20192308.png)
----------------------------------------------------------------------------
5.
# steps explaination
1. **generate u1 u2 ( uniform distribution of [0,1] )**
2. **generate R, $\theta$**
  - $R = \sqrt{-2 \ln(U_1)}$.
  - $\theta = 2 \pi U_2$.
3. **calculate X,Y and make 1000samples**
  - $X = R \cos(\theta)$.
  - $Y = R \sin(\theta)$.

formula above is based on Box-Muller transformation and Rayleigh distribution
In the Box-Muller transformation, u is a uniform random variable on the interval (0,1), is essential for generating a Rayleigh-distributed radius R that allows us to produce independent standard normal samples.
![image](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1105/18_Tim/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-11-26%20103753.png)
![image](https://github.com/HWTeng-Teaching/202409-Math-Stat/blob/main/HW1105/18_Tim/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-11-26%20103759.png)
