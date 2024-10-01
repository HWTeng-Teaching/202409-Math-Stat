### 47. Urn A has four red, three blue, and two green balls. Urn B has two red, three blue, and four green balls. A ball is drawn from urn A and put into urn B, and then a ball is drawn from urn B.

#### a. What is the probability that a red ball is drawn from urn B?
We will use the law of total probability.

1. Probability of drawing a red ball from urn A and then a red ball from urn B:
   - Probability of drawing red from urn A: 4/9.
   - After transferring a red ball, urn B will have 3 red balls. The probability of drawing a red from urn B is 3/10.

   So, the probability of drawing red from urn A and then red from urn B is:
   4/9 * 3/10 = 12/90 = 2/15

2. Probability of drawing a blue ball from urn A and then a red ball from urn B:
   - Probability of drawing blue from urn A: 3/9.
   - After transferring a blue ball, urn B still has 2 red balls, so the probability of drawing a red from urn B is 2/10.

   So, the probability of drawing blue from urn A and then red from urn B is:
   3/9 * 2/10 = 6/90 = 1/15

3. Probability of drawing a green ball from urn A and then a red ball from urn B:
   - Probability of drawing green from urn A: 2/9.
   - After transferring a green ball, urn B still has 2 red balls, so the probability of drawing a red from urn B is 2/10.

   So, the probability of drawing green from urn A and then red from urn B is:
   2/9 * 2/10 = 4/90 = 2/45

Thus, the total probability of drawing a red ball from urn B is:
2/15 + 1/15 + 2/45 = 9/45 = 1/5

#### b. If a red ball is drawn from urn B, what is the probability that a red ball was drawn from urn A?
We use Bayes' Theorem here:
P(Red from A | Red from B) = P(Red from A and Red from B) / P(Red from B)

From part a, we know:
- P(Red from B) = 1/5
- P(Red from A and Red from B) = 2/15

Thus:
P(Red from A | Red from B) = (2/15) / (1/5) = 2/3

---
### 49. A fair coin is tossed three times.

#### a. What is the probability of two or more heads given that there was at least one head?
The sample space of all possible outcomes of three coin tosses is:
S = {HHH, HHT, HTH, HTT, THH, THT, TTH, TTT}

The event "at least one head" excludes TTT, so the conditional sample space is:
S' = {HHH, HHT, HTH, HTT, THH, THT, TTH}

Now, the event "two or more heads" consists of {HHH, HHT, HTH, THH}, so the probability is:
P(two or more heads | at least one head) = 4/7

#### b. What is the probability given that there was at least one tail?
The event "at least one tail" excludes HHH, so the conditional sample space is:
S'' = {HHT, HTH, HTT, THH, THT, TTH, TTT}

The event "two or more heads" consists of {HHT, HTH, THH}, so the probability is:
P(two or more heads | at least one tail) = 3/7

---

### 58. Drew’s scheme of increasing his chances to leave school early

Drew's logic seems flawed. The teacher randomly decides who will stay or leave using a three-sided die. Asking the teacher to reveal one of the students who will stay doesn't change Drew's probability of leaving, which remains 1/3 because the teacher’s choice does not affect the randomness of the original decision. Whether the teacher names Jason or Chris, Drew's chances are still 1/3, as he has only one out of three chances to leave.

Thus, Drew’s probability of leaving remains at 1/3, not 1/2.

---

### 74. What is the probability that the system works if each unit fails independently with probability p?

(1-p)^2+(1-p)^2+(1-p)
---

### 77. A player throws darts at a target. On each trial, independently of the other trials, he hits the bull’s-eye with probability 0.05.

How many times should he throw so that his probability of hitting the bull’s-eye at least once is 0.5?

Let n be the number of throws. The probability of not hitting the bull's-eye on a single trial is 1 - 0.05 = 0.95. The probability of not hitting the bull's-eye in n independent trials is 0.95^n.

We want the probability of hitting the bull's-eye at least once to be 0.5:
1 - 0.95^n = 0.5

0.95^n = 0.5

Taking the natural logarithm of both sides:
n * ln(0.95) = ln(0.5)

n = ln(0.5) / ln(0.95) ≈ -0.6931 / -0.0513 ≈ 13.5

So, the player should throw the dart **14 times** to have at least a 0.5 probability of hitting the bull’s-eye.
---

### Consider a Bernoulli trial, which is a random experiment with only two possible outcomes: success (with probability ( p )) and failure (with probability ( 1 - p )). Based on the Bernoulli trial, let ( X ) be a Bernoulli random variable, where:

### ( X(success) = 1 ), i.e., ( X ) maps success to 1.
### ( X(failure) = 0 ), i.e., ( X ) maps failure to 0.
### In other words, ( X = 1 ) represents a success, and ( X = 0 ) represents a failure.
 Consider a Bernoulli trial, which is a random experiment with only two possible outcomes:

- **Success** with probability **p**
- **Failure** with probability **1 - p**

Let \( X \) be a Bernoulli random variable, where:
- \( X = 1 \) represents success.
- \( X = 0 \) represents failure.

The **probability mass function (pmf)** of \( X \) is the function that gives the probability of each possible value of \( X \). The pmf is defined as:

\[
P(X = x) = 
\begin{cases}
p & \text{if } x = 1 \ (\text{success}) \\
1 - p & \text{if } x = 0 \ (\text{failure})
\end{cases}
\]

This means:
- \( P(X = 1) = p \)
- \( P(X = 0) = 1 - p \)

Thus, the probability mass function of \( X \) describes the likelihood of success or failure in a Bernoulli trial.

---
### 2. An experiment consists of throwing a fair coin four times.

Let’s define the frequency function and cumulative distribution function for the following random variables:

#### (a) The number of heads before the first tail

- **Random Variable:** Let \( X_1 \) represent the number of heads before the first tail is observed.
- **Possible Values of \( X_1 \):** 0, 1, 2, 3, 4
- **Frequency Function of \( X_1 \):**
  - \( P(X_1 = 0) = 1/2 \) (The first toss is a tail)
  - \( P(X_1 = 1) = 1/4 \) (The first toss is heads, the second is tail)
  - \( P(X_1 = 2) = 1/8 \) (The first two tosses are heads, the third is tail)
  - \( P(X_1 = 3) = 1/16 \) (The first three tosses are heads, the fourth is tail)
  - \( P(X_1 = 4) = 1/16 \) (All four tosses are heads)
  
- **Cumulative Distribution Function (CDF):**
  - \( F_X(0) = P(X_1 ≤ 0) = 1/2 \)
  - \( F_X(1) = P(X_1 ≤ 1) = 1/2 + 1/4 = 3/4 \)
  - \( F_X(2) = P(X_1 ≤ 2) = 3/4 + 1/8 = 7/8 \)
  - \( F_X(3) = P(X_1 ≤ 3) = 7/8 + 1/16 = 15/16 \)
  - \( F_X(4) = P(X_1 ≤ 4) = 15/16 + 1/16 = 1 \)

#### (b) The number of heads following the first tail

- **Random Variable:** Let \( X_2 \) represent the number of heads following the first tail.
- **Possible Values of \( X_2 \):** 0, 1, 2, 3
- **Frequency Function of \( X_2 \):**
  - \( P(X_2 = 0) = 1/16 \) (If the first toss is a tail, no heads can follow)
  - \( P(X_2 = 1) = 4/16 = 1/4 \) (If the first tail occurs on toss 2 or 3)
  - \( P(X_2 = 2) = 6/16 = 3/8 \) (If the first tail occurs on toss 2 or 3 and we have more heads)
  - \( P(X_2 = 3) = 5/16 \) (If the first tail occurs on the fourth toss)
  
- **Cumulative Distribution Function (CDF):**
  - \( F_X(0) = P(X_2 ≤ 0) = 1/16 \)
  - \( F_X(1) = P(X_2 ≤ 1) = 1/16 + 1/4 = 5/16 \)
  - \( F_X(2) = P(X_2 ≤ 2) = 5/16 + 3/8 = 11/16 \)
  - \( F_X(3) = P(X_2 ≤ 3) = 11/16 + 5/16 = 1 \)

#### (c) The number of heads minus the number of tails

- **Random Variable:** Let \( X_3 \) represent the number of heads minus the number of tails.
- **Possible Values of \( X_3 \):** -4, -2, 0, 2, 4 (since the number of heads and tails can vary between 0 and 4)
- **Frequency Function of \( X_3 \):**
  - \( P(X_3 = -4) = 1/16 \) (If all tosses are tails)
  - \( P(X_3 = -2) = 4/16 = 1/4 \) (If there are 1 head and 3 tails)
  - \( P(X_3 = 0) = 6/16 = 3/8 \) (If there are 2 heads and 2 tails)
  - \( P(X_3 = 2) = 4/16 = 1/4 \) (If there are 3 heads and 1 tail)
  - \( P(X_3 = 4) = 1/16 \) (If all tosses are heads)
  
- **Cumulative Distribution Function (CDF):**
  - \( F_X(-4) = P(X_3 ≤ -4) = 1/16 \)
  - \( F_X(-2) = P(X_3 ≤ -2) = 1/16 + 1/4 = 5/16 \)
  - \( F_X(0) = P(X_3 ≤ 0) = 5/16 + 3/8 = 11/16 \)
  - \( F_X(2) = P(X_3 ≤ 2) = 11/16 + 1/4 = 15/16 \)
  - \( F_X(4) = P(X_3 ≤ 4) = 15/16 + 1/16 = 1 \)

#### (d) The number of tails times the number of heads

- **Random Variable:** Let \( X_4 \) represent the number of tails times the number of heads.
- **Possible Values of \( X_4 \):** 0, 2, 4, 6
- **Frequency Function of \( X_4 \):**
  - \( P(X_4 = 0) = 2/16 = 1/8 \) (If all tosses are heads or tails)
  - \( P(X_4 = 2) = 6/16 = 3/8 \) (If there are 1 head and 3 tails, or 3 heads and 1 tail)
  - \( P(X_4 = 4) = 6/16 = 3/8 \) (If there are 2 heads and 2 tails)
  - \( P(X_4 = 6) = 2/16 = 1/8 \) (If there are 3 heads and 1 tail)

- **Cumulative Distribution Function (CDF):**
  - \( F_X(0) = P(X_4 ≤ 0) = 1/8 \)
  - \( F_X(2) = P(X_4 ≤ 2) = 1/8 + 3/8 = 4/8 = 1/2 \)
  - \( F_X(4) = P(X_4 ≤ 4) = 1/2 + 3/8 = 7/8 \)
  - \( F_X(6) = P(X_4 ≤ 6) = 7/8 + 1/8 = 1 \)
