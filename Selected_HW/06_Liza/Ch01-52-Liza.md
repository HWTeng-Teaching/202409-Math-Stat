## Problem:
Suppose that 5 cards are dealt from a 52-card deck and the first one is a king.  
What is the probability of at least one more king?

## Solution: 
The total number of ways to deal 4 cards from the remaining 51 cards is calculated using the combination formula:
\[
\binom{51}{4} 
\]
This represents all the possible ways to choose 4 cards from 51.

- Since the first card is already a king, only 3 kings remain in the deck.
- We now calculate the number of ways to select 4 cards that **do not include any of the remaining 3 kings**. This is the number of ways to select 4 cards from the remaining 48 non-king cards:
$$\binom{48}{4}$$
The probability of dealing 4 cards without getting a king is:
\[
P(\text{no king}) = \frac{\binom{48}{4}}{\binom{51}{4}}
\]

The probability of getting **at least one more king** is the complement of the probability of getting no kings:
\[
P(\text{at least one king}) = 1 - P(\text{no king})
\]

\[
P(\text{at least one king}) = 1 - \frac{\binom{48}{4}}{\binom{51}{4}} = 0.22
\]
This is the probability of drawing at least one more king from the next 4 cards.
