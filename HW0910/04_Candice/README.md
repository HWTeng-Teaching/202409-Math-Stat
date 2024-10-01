### 1. A coin is tossed three times and the sequence of heads and tails is recorded.

#### a. List the sample space.

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
2. **A ∩ B = {HHH, HHT}**
3. **A ∪ C = {HHH, HHT, HTH, HTT, THH, THT, TTT}**

---

### 15. How many different meals can be made from four kinds of meat, six vegetables, and three starches if a meal consists of one selection from each group?

**4 meats × 6 vegetables × 3 starches = 72 meals**

---

### 27. If a five-letter word is formed at random (meaning that all sequences of five letters are equally likely), what is the probability that no letter occurs more than once?

There are 26 letters in the alphabet. 
**26 × 25 × 24 × 23 × 22**

The total number of possible five-letter sequences (with repetition allowed) is:

**26^5**

Thus, the probability that no letter occurs more than once is:

(26 × 25 × 24 × 23 × 22) / (26^5) = (26 × 25 × 24 × 23 × 22) / (26 × 26 × 26 × 26 × 26) = (25 × 24 × 23 × 22) / (26^4)**=303600
/456976 ≈ 0.664**


---

### 37. What is the coefficient of x²y²z³ in the expansion of (x + y + z)⁷?

7! / (a! b! c!) * x^a * y^b * z^c

where **a + b + c = 7**. For the term **x²y²z³**, **a = 2, b = 2, c = 3**. Therefore, the coefficient is:

7! / (2! 2! 3!) = 5040 / (2 × 2 × 6) = 210

So the coefficient of **x²y²z³** is **210**.

---

### 52. Suppose that 5 cards are dealt from a 52-card deck and the first one is a king. What is the probability of at least one more king?

Given that the first card is already a king, there are 51 cards remaining in the deck, and 3 of these are kings. The probability of **at least one more king** in the next 4 cards can be found by first calculating the probability of **no more kings** and subtracting that from 1.

First, calculate the probability of drawing no kings in the next 4 cards:

(48 / 51) × (47 / 50) × (46 / 49) × (45 / 48)
->
(48 / 51) × (47 / 50) = 2256 / 2550 ≈ 0.884  
0.884 × (46 / 49) ≈ 0.830  
0.830 × (45 / 48) ≈ 0.623

Thus, the probability of drawing no kings in the next 4 cards is approximately 0.623.

The probability of **at least one more king** is:

1 - 0.623 = 0.377

So, the probability of drawing **at least one more king** is approximately **0.377**.

---

### 33. An elevator containing five people can stop at any of seven floors. What is the probability that no two people get off at the same floor? Assume that the occupants act independently and that all floors are equally likely for each occupant.

If no two people get off at the same floor, then we are choosing 5 different floors for the 5 people from the 7 available floors. The number of ways to choose 5 distinct floors is:

**7 × 6 × 5 × 4 × 3**

The total number of possible ways the 5 people can get off (without the restriction) is:

**7^5**

Thus, the probability that no two people get off at the same floor is:

(7 × 6 × 5 × 4 × 3) / (7^5) = 2520 / 16807 ≈ 0.150


So the probability is approximately **0.150**.

---

# Question
## Prove: If A ⊆ B, then P(A) ≤ P(B)

# Answer
### Definitions
- Let \( P(A) \) denote the probability of event \( A \).
- Let \( P(B) \) denote the probability of event \( B \).

### Proof

1. **Understanding the Definition of Subset**:
   Since \( A⊆B \), every outcome in \( A \) is also an outcome in \( B \).

2. **Using the Additivity Property of Probability**:
   The probability of the union of two disjoint events is equal to the sum of their probabilities. We can express \( B \) as:
   <br>
   **B = A ∪ (B ∖ A)**
   <br>
   where \( B ∖ A \) is the set of outcomes in \( B \) that are not in \( A \).

3. **Disjoint Sets**:
   The sets \( A \) and \( B ∖ A \) are disjoint. Thus, we can apply the additivity property:
   <br>
   **P(B) = P(A) + P(B ∖ A)**

4. **Non-negativity of Probability**:
   Since probabilities are always non-negative, we have:
   <br>
   **P(B ∖ A) ≥ 0**

5. **Combining the Results**:
   From step 3, we can substitute the non-negativity into our equation:
   <br>
   **P(B) = P(A) + P(B ∖ A) ≥ P(A)**

6. **Conclusion**:
   Thus, we conclude:
   <br>
   **P(A) ≤ P(B)**
   <br>
   This completes the proof.

### Summary
If \( A \subseteq B \), then it follows that \( P(A) ≤ P(B) \).

---

### Proof: P(ϕ) = 0

1. **Definition of Probability:**
   The probability of any event \( A \), denoted by \( P(A) \), must satisfy two key axioms:
   
   - \( 0 \leq P(A) \leq 1 \) for any event \( A \)
   - \( P(S) = 1 \), where \( S \) is the sample space (the set of all possible outcomes)

2. **Empty Set (ϕ):**
   The empty set \( \varphi \) contains no elements, meaning it represents an event that cannot occur. By definition, there are no outcomes in \( \varphi \).

3. **Additivity Axiom:**
   The probability of the union of disjoint sets equals the sum of their probabilities:
   
   \[
   P(A \cup B) = P(A) + P(B)
   \]
   
   Since \( \varphi \) and \( S \) are disjoint (no overlap), we can write:
   
   \[
   P(S) = P(S \cup \varphi) = P(S) + P(\varphi)
   \]
   
4. **Final Step:**
   We know that \( P(S) = 1 \), so:
   
   \[
   1 = 1 + P(\varphi)
   \]
   
   Solving for \( P(\varphi) \), we get:
   
   \[
   P(\varphi) = 0
   \]
   
Thus, the probability of the empty set \( \varphi \) is **0**.

---
