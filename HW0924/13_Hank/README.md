## Q47
### a.

P(red from A) = $\frac{4}{9}$

P(blue from A) = $\frac{1}{3}$

P(green from A) = $\frac{2}{9}$

then B has

P(red from B) = $\frac{3}{10}$

P(blue from B) = $\frac{1}{5}$

P(green from B) = $\frac{1}{5}$

$\frac{4}{9}$ $\times$ $\frac{3}{10}$ + $\frac{1}{3}$ $\times$ $\frac{1}{5}$ + $\frac{2}{9}$ $\times$ $\frac{1}{5}$ = $\frac{11}{45}$

### b.

P(red from A | red from B) = $\frac{\frac{4}{9} \times \frac{3}{10}}{\frac{11}{45}}$ = $\frac{6}{11}$

## Q49
### a.
$\frac{\frac{1}{2}}{1 - \frac{1}{8}}$ = $\frac{4}{7}$ 
### b.
$\frac{\frac{3}{8}}{1 - \frac{1}{8}}$ = $\frac{3}{7}$ 

## Q58
- There are three boys: **Drew**, **Chris**, and **Jason**.
- One boy will leave, and two will stay.
- Each boy has an equal chance of being the one who leaves: **1/3**.

### Possible Outcomes
1. **Drew leaves**; Chris and Jason stay.
2. **Chris leaves**; Drew and Jason stay.
3. **Jason leaves**; Drew and Chris stay.

### Drew's Plan
Drew asks the teacher to name one of Chris or Jason who will stay. He believes that once the teacher names one of them, the remaining two boys (including himself) have an equal **1/2** chance of leaving.

- **If Drew leaves** 
  - The teacher randomly names Chris or Jason (each with probability **1/2**) since both are staying.
  
- **If Chris leaves** 
  - The teacher must name Jason as the one staying among Chris and Jason.
  
- **If Jason leaves** 
  - The teacher must name Chris as the one staying among Chris and Jason.

### Conditional Probability Calculation

Suppose the teacher says "Jason will stay." The probability that Drew is the one leaving is calculated using Bayes' Theorem:

**P(Drew leaves | Teacher says Jason stays) = [P(Teacher says Jason stays | Drew leaves) × P(Drew leaves)] / P(Teacher says Jason stays)**

### Compute the Probabilities

- **P(Drew leaves) = 1/3**
- **P(Teacher says Jason stays | Drew leaves) = 1/2**
- **P(Teacher says Jason stays | Chris leaves) = 1**
- **P(Teacher says Jason stays | Jason leaves) = 0**

P(Teacher says Jason stays) is the total probability that the teacher says "Jason will stay":

P(Teacher says Jason stays) =  
&nbsp;&nbsp;&nbsp;&nbsp;[P(Teacher says Jason stays | Drew leaves) × P(Drew leaves)] +  
&nbsp;&nbsp;&nbsp;&nbsp;[P(Teacher says Jason stays | Chris leaves) × P(Chris leaves)] +  
&nbsp;&nbsp;&nbsp;&nbsp;[P(Teacher says Jason stays | Jason leaves) × P(Jason leaves)]  

P(Teacher says Jason stays) = (1/2 × 1/3) + (1 × 1/3) + (0 × 1/3) =  
&nbsp;&nbsp;&nbsp;&nbsp;1/6 + 1/3 + 0 = **1/2**

P(Drew leaves | Teacher says Jason stays) = (1/2 × 1/3) / (1/2) = (1/6) / (1/2) = **1/3**

### Conclusion

Drew's probability of leaving remains **1/3** even after the teacher reveals who among Chris and Jason will stay. His scheme does **not** increase his chances.

## Q74
(1) The probability that the fist path or third path will not work

$1-(1-p)^2$

(2) The probability that the second path will not work

$p

(3) The probability that the whole system will work

$1-(p(1-(1-p)^2)^2)$

# Q77

$1-(1-0.05)^n$ $\ge 0.5$ 

$(0.95)^n \le 0.5$

$n\log 0.95 \le \log 0.5$

$n \ge 13.5134$

$n = 14$

## Consider a Bernoulli trial...
$P(x=\chi)$ 

$= p if \chi = 1$

$= 1-p if \chi = 0$

$= 0 if \chi \ne 0 and \chi \ne 1$

## Q2
### a.
X = the number of heads before the first tail

P(0) = 1/2      

P(1) = 1/4

P(2) = 1/8              

P(3) = 1/16

P(4) = 1/16

F(X) = 0 , X < 0

F(X) = 1/2 , 0 <= X < 1

F(X) = 3/4 , 1 <= X < 2

F(X) = 7/8 , 2 <= X < 3

F(X) = 15/16 , 3 <= X < 4

F(X) = 1 , X >= 4

### b.
X = the number of heads following the first tail

P(0) = 5/16      

P(1) = 3/8

P(2) = 1/4              

P(3) = 1/16

F(X) = 0 , X < 0

F(X) = 5/16 , 0 <= X < 1

F(X) = 11/16 , 1 <= X < 2

F(X) = 15/16 , 2 <= X < 3

F(X) = 1 , X >= 3

### c.
X = the number of heads minus the number of tails

P(-4) = 1/16      

P(-2) = 1/4

P(0) = 3/8              

P(2) = 1/4

P(4) = 1/16

F(X) = 0 , X < -4

F(X) = 1/16 , -4 <= X < -2

F(X) = 5/16 , -2 <= X < 0

F(X) = 11/16 , 0 <= X < 2

F(X) = 15/16 , 2 <= X < 4

F(X) = 1 , X >= 4

### d.
X =  the number of tails times the number of heads

P(0) = 1/8      

P(3) = 1/2

P(4) = 3/8  

F(X) = 0 , X < 0

F(X) = 1/8 , 0 <= X < 3

F(X) = 5/8 , 3 <= X < 4

F(X) = 1 , X >= 4
