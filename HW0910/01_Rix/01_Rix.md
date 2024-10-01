# 01_Rix

by 周子揚 Rix

## Q1. 

### Questions 

1. A coin is tossed three times and the sequence of heads and tails is recorded.
a. List the sample space.
b. List the elements that make up the following events: (1) A = at least two
heads, (2) B = the first two tosses are heads, (3) C = the last toss is a tail. c. List the elements of the following events: (1) Aᶜ, (2) A ∩ B, (3) A ∪ C.

### Answers

a.   
   $\Omega$ = \{HHH, HHT, HTH, HTT, THH, THT, TTH, TTT\}  
  
b.  
   A = \{HHH, HHT, HTH, THH\}  
   B = \{HHT, HHH\}  
   C = \{HHT, HTT, THT, TTT\}  
  
c.  
   Aᶜ = \{THH, THT, TTH, TTT\}  
   A &#8745; B = \{HHH, HHT\}  
   A &#8746; C = \{HHH, HHT, HTH, HTT, THH, THT, TTT\}

## Q2.

### Questions

How many different meals can be made from four kinds of meat, six vegetables, and three starches if a meal consists of one selection from each group?

### Answers

Select each group once, so there will be $4 \times 6 \times 3 = 72$ different meals.

## Q3.

### Questions

If a five-letter word is formed at random (meaning that all sequences of five letters are equally likely), what is the probability that no letter occurs more than once?

### Answers

All possible words = $26 \times 26 \times 26 \times 26 \times 26$  
no letters occurs more than once = $26 \times 25 \times 24 \times 23 \times 22$  
so the probability p = $$\large{\frac{25 \times 24 \times 23 \times 22}{26 \times 26 \times 26 \times 26}}$$  

## Q4.

### Questions

Prove: If A ⊆ B, then P(A) ≤ P(B)

### Answers

All elements in A are also in B.  
B = A ∪ (B ∖ A), where (B ∖ A) is elements in B but not in A.  
so P(B) = P(A) + P(B ∖ A), since A and (B ∖ A) is disjoint.  
P(B \ A) ≥ 0, P(B) = P(B) = P(A) + P(B ∖ A), so P(B) ≥ P(A)  

## Q5.

### Questions

What is the coefficient of $$\(x^2 y^2 z^3)$$ in the expansion of $$\(x + y + z)^7$$?

### Answers

All the sum of exponents of x,y,z are 7.  
And the exponents of x,y,z we want is 2,2,3.  
so, the coefficient is $\frac{7!}{2!2!3!}$ by multinomial formula.  
$\frac{7!}{2!2!3!}$ = $\frac{5040}{2 \times 2 \times 6} = 210

## Q6.

### Questions

Suppose that 5 cards are dealt from a 52-card deck and the first one is a king. What is the probability of at least one more king?

### Answers

The way to choose 4 cards from 51 cards is $\binom{51}{4}$  
No king in the chosen 4 cards is $\binom{48}{4}$
At least one king in chosen 4 cards is 1 - $$\frac{\binom{48}{4}}{\binom{51}{4}}$$  
probability is 1 - $$\frac{194580}{249900}$$ = 1 - 0.77863 = 0.22137

## Q7.

### Questions

An elevator containing five people can stop at any of seven floors. What is the probability that no two people get off at the same floor? Assume that the occupants act independently and that all floors are equally likely for each occupant.

### Answers

