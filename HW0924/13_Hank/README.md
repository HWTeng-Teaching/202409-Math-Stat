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
