## Q1. 
### Questions 
A coin is tossed three times and the sequence of heads and tails is recorded.
a. List the sample space.
b. List the elements that make up the following events: (1) A = at least two
heads, (2) B = the first two tosses are heads, (3) C = the last toss is a tail. c. List the elements of the following events: (1) $A^{c}$, (2) A ∩ B, (3) A ∪ C.
### Answers
a.   
   $\Omega$ = \{HHH, HHT, HTH, HTT, THH, THT, TTH, TTT\}  
  
b.  
   $A^{c}$= \{HHH, HHT, HTH, THH\}  
   B = \{HHH, HHT\}  
   C = \{HHT, THT, HTT, TTT\}
## Q2.
### Questions
How many different meals can be made from four kinds of meat, six vegetables, and three starches if a meal consists of one selection from each group?  
### Answers
Multiply the number of options from each group  
4×6×3=72
the answer is 72
## Q3.
### Questions
If a five-letter word is formed at random (meaning that all sequences of five letters are equally likely), what is the probability that no letter occurs more than once?  
### Answers
26 English letters fromigng a 5 lettets word → total 26^5 possible words  
no letter is the same in the 5 letters word → 26×25×24×23×22 possiable words  
$26×25×24×23×22 \over 26^{5}$ = $303600 \over 456976$ ≈ 0.664
the answer is 0.664
## Q4.
### Questions
Prove: If A ⊆ B, then P(A) ≤ P(B)  
### Answers
Let P(A) denote the probability of event A and let P(B) denote the probability of event B  
B = A ∪ (B∖A)
P(A) + P(B∖A) = P(B) since A and B∖A are disjoint  
P(B∖A) ≥ 0  
thus P(A) ≤ P(B)  
## Q5.
### Questions
What is the coefficient of $$\(x^2 y^2 z^3)$$ in the Expansion of $$\(x + y + z)^7$$?  
### Answers
sum of exponents is 7  
exponents of x,y,z are 2,2, and 3 respectively  
$7! \over (2! \times 2! \times 3!)$ = $5040 \over (2 \times 2 \times 6)$ = 210  
the answer is 210  
## Q6.
### Questions
Suppose that 5 cards are dealt from a 52-card deck and the first one is a king. What is the probability of at least one more king?  
### Answers
P(at least one more king is dealt|first card dealt is a king) = 1 - P(no more king is dealt after the first card|first card dealt is a king)
P(no more king is dealt after the first card|first card dealt is a king) = $C\binom{48}{4} \over C\binom{51}{4}$ = 0.22
## Q7.
### Questions
An elevator containing five people can stop at any of seven floors. What is the probability that no two people get off at the same floor? Assume that the occupants act independently and that all floors are equally likely for each occupant.  
### Answers
Each person can choose 1 floor out of 7, thus there are $7^{5}$ possible outcomes  
To make sure no two people get off at the same floor, all five people have to get off at different floors   
$P\binom{7}{5} \over 7^{5}$ = $2520 \over 16807$ ≈ 0.15

the answer is 0.15
## Q8.
### Questions
Prove: P(ϕ) = 0  
### Answers
S = S∪ϕ  
S∩ϕ = ∅, S and ϕ are mutually exclusive 
P(S) = P(S ∪ ϕ) = P(S) + P(ϕ)   
P(S) + P(ϕ) = P(S)   
thus P(ϕ) = 0 
## Q9.
### Questions
Prove: P(A ∪ B) = P(A) + P(B) - P(A ∩ B)  
### Answers
P(A) = P(A ∩ B) + P(A\B)    
P(B) = P(A ∩ B) + P(B\A)   
P(A ∪ B) = P(A ∩ B) + P(A\B) + P(B\A)  
plus P(A ∩ B) at both side and we will got P(A ∪ B)+P(A ∩ B)  = P(A) + P(B)   
thus P(A ∪ B) = P(A) + P(B) - P(A ∩ B)
