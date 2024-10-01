# 07_Jocelyn

by 林嘉佳 Jocelyn

## Q33.

### Question

33. An elevator containing five people can stop at any of seven floors. What is the probability that no two people get off at the same floor? Assume that the occupants act independently and that all floors are equally likely for each occupant.

### Answer

**Step 1: Calculate the sample space**
<br> There are 5 people, and each can choose 1 floor out of 7. Hence, the possible outcome is 

$$7^5$$

**Step 2: Calculate the outcomes**
<br> Since there are only 5 people, so only 5 floor will be occupied. We then use the combination formula:

$$\binom{7}{5}$$

Next, since those 5 people are not constrained in any floor. So there are 5! of possible arrangement.

Therefore, the outcomes will be:

$$\binom{7}{5} \times 5!$$

**Step 3: Calculate the probability**
<br>The probability that no two people get off at the same floor is:

$$P = \frac{\text{Possible Outcome}}{\text{Sample Space}}$$

$$P = \frac{\binom{7}{5} \times 5!}{7^5} = \frac{360}{2401} \approx {0.15}$$

TA 施昱全(James) reviewed on 20240924 and score $\textbf{\textcolor{red}{100}}$

