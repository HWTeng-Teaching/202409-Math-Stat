# HW0910

by 王邦碩 Brian

## Q1. 

### Question 

A coin is tossed three times and the sequence of heads and tails is recorded.
a. List the sample space.
b. List the elements that make up the following events: (1) A = at least two
heads, (2) B = the first two tosses are heads, (3) C = the last toss is a tail. c. List the elements of the following events: (1) Aᶜ, (2) A ∩ B, (3) A ∪ C.

### Solution

A) HHH, HHT, HTH, THH, HTT, THT, THH, TTT  
B)   
&emsp;    (1) A = {HHH, HHT, HTH, THH}  
&emsp;    (2) B = {HHH, HHT}  
&emsp;    (3) C = {HTT, TTT}   
C)  
&emsp;    Aᶜ = {HTT, THT, THH, TTT}    
&emsp;    A &#8745; B = {HHH, HHT}    
&emsp;    A &#8746; C = {HHH, HHT, HTH, THH, HTT, TTT}  

## Q2
### Question

How many different meals can be made from four kinds of meat, six vegetables, and three starches if a meal consists of one selection from each group?

### Solution
Multiply the number of choice of each group
4 * 6 * 3 = 72

## Q3
### Question
If a five-letter word is formed at random (meaning that all sequences of five letters
are equally likely), what is the probability that no letter occurs more than once?
### Solution
#### Step 1: All Possible Words
26 English letters $\rightarrow$ total 26^5 possible words

#### Step 2: Words with no repeated letters

- For the first letter: 26 choices (all letters are available).
- For the second letter: 25 choices (one letter has already been used).
- For the third letter: 24 choices.
- For the fourth letter: 23 choices.
- For the fifth letter: 22 choices.

$\rightarrow$ 26 * 25 * 24 * 23 * 22 possible words that no letter occurs more than once

#### Step 3: Final Answer
$$\small{\frac{26 * 25 * 24 * 23 * 22}{26^5} = \frac{25 * 24 * 23 * 22}{26^4}}$$

## Q4
### Question 
Prove: If A ⊆ B, then P(A) ≤ P(B) 

### Solution

P(B) 
= P(A / B) + P(A &#8745; B) + P(B / A)
= 0 + P(A) + P(B / A)
&ge; P(A)

## Q5
### Question 
What is the coefficient of $(x^2 y^2 z^3)$ in the expansion of $(x + y + z)^7$?

### Solution

$\large\frac{7!}{2!2!3!} = 210$

## Q6
### Question 
Suppose that 5 cards are dealt from a 52-card deck and the first one is a king. What is the probability of at least one more king?

### Solution

Total possibility: $\binom{51}{4}$  
No king in the rest 4 cards: $\binom{48}{4}$  
1 - $\binom{48}{4}$/ $\binom{51}{4}$ = 1 - 0.7786 = 0.2214

## Q7
### Question
An elevator containing five people can stop at any of seven floors. What is the probability that no two people get off at the same floor? Assume that the occupants act independently and that all floors are equally likely for each occupant.

### Solution
Total possibility: $7^5$  
No two people get off at the same floor: $7×6×5×4×3$   
$\large\frac{7×6×5×4×2}{7^5} = 0.1499$

## Q8
### Question
Prove: P($\emptyset$)= 0

### Question
For any set A,
P(A)   
= P(A &#8746; $\emptyset$)   
= P(A \ $\emptyset$) + P(A &#8745; $\emptyset$) + P($\emptyset$ \ A)  
=P(A) + 0 + P($\emptyset$)  
So P($\emptyset$) = 0  

## Q9
### Question
Prove: P(A ∩ B) = P(A) + P(B) - P(A ∪ B)

### Solution
A∪B = (A \ B)∪(A ∩ B)∪(B \ A)  
p(A∪B) = P(A \ b) + P(A ∩ B) + P(B \ A)  
P(A ∩ B) = P(A \ b) + P(A ∪ B) + P(B \ A)
