# HOMEWORK 1 (0910) LIYA ##

# QUESTION 1.1


<img width="623" alt="image" src="https://github.com/user-attachments/assets/a3c9cc3b-1997-4450-bd11-8c0d3c66a8cc">
 
## a) List the sample space.

When a coin is tossed three times, the sample space \( S \) consist of HEAD (H) and TAILS (T)

So,


S = { HHH, HHT, HTH, HTT, THH, THT, TTH, TTT }

## b) List the elements that make up the following events: (1) A = at least two heads, (2) B = the first two tosses are heads, (3) C = the last toss is a tail.
(1) A = { HHH, HHT, HTH, THH }
(2) B = { HHH, HHT }
(3) C = { HHT, HTH, HTT, THT, TTH, TTT }

## c) List the elements of the following events: (1) A^c, (2) A ∩ B, (3) A ∪ C.
1) A^c = { HTT, THH, THT, TTH, TTT }
2) A ∩ B = { HHH, HHT }
3) A ∪ C = { HHH, HHT, HTH, THH, HTT, THT, TTH, TTT }


# QUESTION 1.15
<img width="639" alt="image" src="https://github.com/user-attachments/assets/2e7262a9-c3d3-4310-9ed7-a9b99cae1df6">

By using multiplication method:

TOTAL MEALS= 4 * 6* 3= 72
### Answer: 72

# QUESTION 1.27
 <img width="625" alt="image" src="https://github.com/user-attachments/assets/c59d82cf-20bb-42f1-bf0a-c42d1e2832d4">

1) Lets assume that therere 26 letters in the alphabet; therefore the total amount of words WITH POSSIBLE PEPETITION is:

$$TOTAL= \( 26^5 = 11881376 \) $$

2) Now, lets find the amount of words WITHOUT repetition ( at firsr we can use 26 letters, then 25,...)
   
   $$WITHOUT=  \( 26 \times 25 \times 24 \times 23 \times 22 = 303600 \) $$
   
4) P(no repitition)= 7893600/11881376= 0,6644
### Answer P= 0,664

# PROVE 

1. **NOTE**
    Lets assume that $$\( A \) and \( B \)$$ are two events such that $$\( A \subseteq B \)$$.
   Probability of an event $$\( A \), denoted \( P(A) \)$$, is the measure of the set $$\( A \)$$.


   Since $$\( A \subseteq B \)$$, lets express $$\( B \)$$ as:
   $$\( B = A \cup (B \setminus A) \)$$
    THEREFORE, $$\( B \setminus A \)$$ is the part of $$\( B \)$$ (not $$\( A \)$$).

3. **By Additive property**:
   The probability of the union of disjoint sets is
      $$\( P(B) = P(A) + P(B \setminus A) \)$$

Since,probabilities are always non-negative:
      $$\( P(B \setminus A) \geq 0 \)$$

**Finally,**
      $$\( P(B) = P(A) + P(B \setminus A) \geq P(A) \)$$

Thus, we conclude that if 

$$\( A \subseteq B \),\( P(A) \leq P(B) \)$$

proven.


# QUESTION 1.37
<img width="548" alt="image" src="https://github.com/user-attachments/assets/8f672bd0-ce6c-4244-898e-068ea1e45ae8">


Sum of powers $$\( x^2 y^2 z^3 \)$$ = 2 + 2 + 3= 7

therefore COEFFICIENT= $$\frac{7!}{2! 2! 3!}
\$$ = 210

### Answer= 210

# QUESTION 1.52
<img width="612" alt="image" src="https://github.com/user-attachments/assets/dc523ff9-11b1-4d45-b382-35d80c8857cb">

**NOTE** Since the first card is a king, there are 3 kings left...

1) All possible outcomes (taking 4 cards from 51) is

   $$\
\binom{51}{4}
\$$

2) IF there is no king

   $$\
\binom{48}{4}
\$$

### Lets find the probability of not getting anymore kings 
$$\
P(\text{no additional kings}) = \frac{\binom{48}{4}}{\binom{51}{4}}
\$$

Therefore, the probability of having **at least one more king** is:

$$\
P(\text{at least one more king}) = 1 - P(\text{no additional kings}) = 1 - \frac{\binom{48}{4}}{\binom{51}{4}}
\$$ = 0.2815
### Answer= 0,2815


# QUESTION 1.33
<img width="641" alt="image" src="https://github.com/user-attachments/assets/03108755-56a4-4c53-afcb-2e2443024f1b">

1) If we assighn every person with a floor ( no repitition)=

   
   $$\(7 \times6 \times5 \times4 \times3)$$ = 2520

2) with repetoition

   $$\ (7^ 5\)$$ = 16807

## Therefore, The probability that theres no 2 people go on the same floor is 

   $$\(2520 /16807)$$ = 0,1499= 14,99%

   ### Answer 14,99% or 0,1499



  # PROVE 

   
