### 1. A coin is tossed three times and the sequence of heads and tails is recorded.

#### a. List the sample space.
The sample space for tossing a coin three times is the set of all possible outcomes:

**S = {HHH, HHT, HTH, HTT, THH, THT, TTH, TTT}**

#### b. List the elements that make up the following events:
1. **A = at least two heads**:  
   **A = {HHH, HHT, HTH, THH}**
2. **B = the first two tosses are heads**:  
   **B = {HHH, HHT}**
3. **C = the last toss is a tail**:  
   **C = {HHT, HTT, THT, TTT}**

#### c. List the elements of the following events:
1. **Ac = complement of A**:  
   **Ac = {HTT, THT, TTH, TTT}**
2. **A ∩ B (intersection of A and B)**:  
   **A ∩ B = {HHH, HHT}**
3. **A ∪ C (union of A and C)**:  
   **A ∪ C = {HHH, HHT, HTH, HTT, THH, THT, TTT}**

---

### 15. How many different meals can be made from four kinds of meat, six vegetables, and three starches if a meal consists of one selection from each group?

The number of different meals is the product of the choices available in each category:

**4 meats × 6 vegetables × 3 starches = 72 meals**

---

### 27. If a five-letter word is formed at random (meaning that all sequences of five letters are equally likely), what is the probability that no letter occurs more than once?

There are 26 letters in the alphabet. The number of ways to choose 5 distinct letters without repetition is:

**26 × 25 × 24 × 23 × 22**

The total number of possible five-letter sequences (with repetition allowed) is:

**26^5**

Thus, the probability that no letter occurs more than once is:

\[
\frac{26 × 25 × 24 × 23 × 22}{26^5} = \frac{26 × 25 × 24 × 23 × 22}{26 × 26 × 26 × 26 × 26} = \frac{25 × 24 × 23 × 22}{26^4}
\]

---

### 37. What is the coefficient of x²y²z³ in the expansion of (x + y + z)⁷?

The multinomial expansion of **(x + y + z)⁷** is given by the general term:

\[
\frac{7!}{a!b!c!} x^a y^b z^c
\]

where **a + b + c = 7**. For the term **x²y²z³**, **a = 2, b = 2, c = 3**. Therefore, the coefficient is:

\[
\frac{7!}{2!2!3!} = \frac{5040}{2 × 2 × 6} = 210
\]

So the coefficient of **x²y²z³** is **210**.

---

### 52. Suppose that 5 cards are dealt from a 52-card deck and the first one is a king. What is the probability of at least one more king?

Given that the first card is already a king, there are 51 cards remaining in the deck, and 3 of these are kings. The probability of **at least one more king** in the next 4 cards can be found by first calculating the probability of **no more kings** and subtracting that from 1.

The probability of drawing no kings in the next 4 cards is:

\[
\frac{48}{51} \times \frac{47}{50} \times \frac{46}{49} \times \frac{45}{48}
\]

The probability of **at least one more king** is:

\[
1 - \left( \frac{48}{51} \times \frac{47}{50} \times \frac{46}{49} \times \frac{45}{48} \right)
\]

---

### 33. An elevator containing five people can stop at any of seven floors. What is the probability that no two people get off at the same floor? Assume that the occupants act independently and that all floors are equally likely for each occupant.

If no two people get off at the same floor, then we are choosing 5 different floors for the 5 people from the 7 available floors. The number of ways to choose 5 distinct floors is:

**7 × 6 × 5 × 4 × 3**

The total number of possible ways the 5 people can get off (without the restriction) is:

**7^5**

Thus, the probability that no two people get off at the same floor is:

\[
\frac{7 × 6 × 5 × 4 × 3}{7^5} = \frac{2520}{16807}
\]

So the probability is approximately **0.150**.
