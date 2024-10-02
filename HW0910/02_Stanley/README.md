### 1.A coin is tossed three times and the sequence of heads and tails is recorded. a. List the sample space. b. List the elements that make up the following events: (1) A = at least two heads, (2) B = the first two tosses are heads, (3) C = the last toss is a tail. c. List the elements of the following events: (1) Aᶜ, (2) A ∩ B, (3) A ∪ C. 
a.   
Ω= {HHH, HHT, HTH, HTT, THH, THT, TTH, TTT}   
b.  
(1) A = {HHH, HHT, HTH, THH}  
(2) B = {HHT, HHH}  
(3) C = {HHT, HTT, THT, TTT}  
c.  
(1) Aᶜ = {THH, THT, TTH, TTT}  
(2) A ∩ B = {HHH, HHT}  
(3) A ∪ C = {HHH, HHT, HTH, HTT, THH, THT, TTT}  
### 15.How many different meals can be made from four kinds of meat, six vegetables, and three starches if a meal consists of one selection from each group?  
we need to multiply the number of options in each category  
4×6×3=72  
### 27.If a five-letter word is formed at random (meaning that all sequences of five letters are equally likely), what is the probability that no letter occurs more than once?  
26 English letters →total 26^5 possible words  
no letter is the same so 26×25×24×23×22 possiable words  
26×25×24×23×22/26^5 =303600 /456976 ≈ 0.664  
### Prove: If A ⊆ B, then P(A) ≤ P(B)  
Let ( P(A) ) denote the probability of event ( A ) and Let ( P(B) ) denote the probability of event ( B )  
B = A ∪ (B ∖ A)  
P(B) = P(A) + P(B ∖ A) since they are disjoint  
P(B ∖ A) ≥ 0  
P(B) = P(A) + P(B ∖ A) ≥ P(A)  
then P(A) ≤ P(B)  
### 37.What is the coefficient of $$\(x^2 y^2 z^3)$$ in the Expansion of $$\(x + y + z)^7$$?  
sum of exponents is 7  
exponents of x is 2,exponents of y is 2,exponents of z is 3  
7! / (2! 2! 3!) = 5040 / (2 × 2 × 6) = 210  
the answer is 210  
### 52.Suppose that 5 cards are dealt from a 52-card deck and the first one is a king.What is the probability of at least one more king?  
P(at least two king)=1-P(one king) since their must be one king  
P(at least two king)=1-($\binom{48}{4}$ / $\binom{51}{4}$)=0.22  
### 33.An elevator containing five people can stop at any of seven floors. What is the probability that no two people get off at the same floor? Assume that the occupants act independently and that all floors are equally likely for each occupant.  
each one can choose 1 floor out of 7. Hence, the possible outcome is 7^5  
five people to stop at five different floors to make sure that no two people get off at the same time  
=> $$\binom{7}{5} \times 5!$$  
the answer is $$\binom{7}{5} \times 5!$$  / 7^5=360/2401=0.15  
### Prove: P(ϕ) = 0  
S=S∪∅  
S∩∅=∅, so Sand ∅ are mutually exclusive.  
P(S) = P(S ∪ ϕ) = P(S) + P(ϕ)  
1 + P(ϕ) = 1  
so P(ϕ) = 0  
### Prove: P(A ∪ B) = P(A) + P(B) - P(A ∩ B)  
P(A)=P(A ∩ B)+P(A\B)    
P(B)=P(A ∩ B)+P(B\A)  
You also know from set theory that the union A∪B is the disjoint union of A∩B, A\B,and B\A  
![image](https://github.com/user-attachments/assets/19856ecc-4ae9-43ad-ba5e-0302fa3fd34f)  
P(A ∪ B)=P(A ∩ B)+P(A\B)+P(B\A)  
plus P(A ∩ B) at both side and we will got P(A ∪ B)+P(A ∩ B)  = P(A) + P(B)  
thus P(A ∪ B) = P(A) + P(B) - P(A ∩ B)
.
 

