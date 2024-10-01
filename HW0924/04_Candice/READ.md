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
