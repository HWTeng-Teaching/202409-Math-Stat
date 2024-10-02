# 01_Rix

by 周子揚 Rix

## Q1. 

### Questions 

Urn A has four red, three blue, and two green balls. Urn B has two red, three blue, and four green balls. A ball is drawn from urn A and put into urn B, and then a ball is drawn from urn B.  
a. What is the probability that a red ball is drawn from urn B?  
b. If a red ball is drawn from urn B, what is the probability that a red ball was drawn from urn A?

### Answers

a.  
A draw red and B draw red is $\frac{4}{9} \times \frac{3}{10} = \frac{12}{90}$  
A not draw red and B draw red is $\frac{5}{9} \times \frac{2}{10} = \frac{10}{90}$  
so the probability f a ball drawn from B is red is $\frac{12}{90} + \frac{10}{90} = \frac{11}{45}$  
  
b.  
By a, P(a red ball is drawn from urn B | a red ball was drawn from urn A) = $\large\frac{\frac{12}{90}}{\frac{11}{45}}$ = $\frac{6}{11}$

## Q2.

### Questions

A fair coin is tossed three times.  
a. What is the probability of two or more heads given that there was at least one head?  
b. What is the probability given that there was at least one tail?

### Answers

a.  
X = head times.  
P(X ≥ 2 | X ≥ 1) = $\frac{P(X = 3) + P(X = 2)}{P(X = 3) + P(X = 2) + P(X = 1)}$ = $\frac{\frac{1}{8} + \frac{3}{8}}{\frac{1}{8} + \frac{3}{8} + \frac{3}{8}}$ = $\frac{4}{7}$  
b.  
P(at least two heads | at least one tail) = $\frac{P(X = 2)}{P(X = 0) + P(X = 1) + P(X = 2)}$ = $\frac{\frac{3}{8}}{\frac{1}{8} + \frac{3}{8} + \frac{3}{8}}$ = $\frac{3}{7}$

## Q3.

### Questions

A teacher tells three boys, Drew, Chris, and Jason, that two of them will have to stay after school to help her clean erasers and that one of them will be able to leave. She further says that she has made the decision as to who will leave and who will stay at random by rolling a special three-sided Dungeons and Dragons die. Drew wants to leave to play soccer and has a clever idea about how to increase his chances of doing so. He figures that one of Jason and Chris will certainly stay and asks the teacher to tell him the name of one of the two who will stay. Drew’s idea is that if, for example, Jason is named, then he and Chris are left and they each have a probability .5 of leaving; similarly, if Chris is named, Drew’s probability of leaving is still .5. Thus, by merely asking the teacher a question, Drew will increase his probability of leaving from $\frac{1}{3}$ to $\frac{1}{2}$. What do you think of this scheme?

### Answers

There are three boys, one leave and two stay.  
Each one leave chance is $\frac{1}{3}$.  
D = Drew, C = Chris, J = Jason. L = leave, S = stay.  
D believe that if he ask teacher to name C or J to stay, then other two boys can have $\frac{1}{2}$ to leave.  
P(DL | CS) = $\frac{P(CS | DL) \times P(DL)}{P(CS)}$  
P(DL) = $\frac{1}{3}$  
P(CS | DL) = $\frac{1}{2}$  
P(CS | CL) = 0  
P(CS | JL) = 1  
P(CS) = $P(CS | DL) \times P(DL) + P(CS | CL) \times P(CL) + P(CS | JL) \times P(JL)$ = $\frac{1}{2}$  
P(DL | CS) = $\frac{1}{3}$  
So, the DL is still $\frac{1}{3}$, his chance doesn't increase.

## Q4.


### Questions

What is the probability that the following system works if each unit fails independently with probability p (see Figure 1.5)?

![image](https://github.com/user-attachments/assets/d30504e6-06d6-4899-94eb-24011ba135c6)


### Answers

each unit has probability p to fail.  
P(First path not work) = 1 - P(First path work) = 1 - (1 - p)(1 - p)
P(Second path not work) = p  
P(Third path not work) = 1 - P(Third path work) = 1 - (1 - p)(1 - p)
P(System work) = 1 - P(System not work) = $1 - [1 - (1 - p)^2] \times p \times [1 - (1 - p)^2]$ = $1 - p[1 - (1 - p)^2]^2$

## Q5.

### Questions

A player throws darts at a target. On each trial, independently of the other trials, he hits the bull’s-eye with probability .05. How many times should he throw so that his probability of hitting the bull’s-eye at least once is .5?

### Answers

probability to hit eye in each trial = 0.05  
probability not to hit eye in n trials = $(1 - 0.05)^n$ = $0.95^n$  
solve $0.95^n$ ≤ 0.5  
find n :  
log($0.95^n$) ≤ log(0.5)  
nlog(0.95) ≤ log(0.5)  
n ≥ $\frac{log(0.5)}{log(0.95)}$ = 13.5  
n at least 14  
He should throw 14 times then the probability of hitting bull's-eye  at least once is 0.5.

## Q6.

### Questions

Consider a Bernoulli trial, which is a random experiment with only two possible outcomes: success (with probability p) and failure (with probability (1 - p). Based on the Bernoulli trial, let X be a Bernoulli random variable, where:  
X(success) = 1, i.e., X maps success to 1.  
X(failure) = 0, i.e., X maps failure to 0.  
In other words, X = 1 represents a success, and X = 0 represents a failure.  
Define the probability mass function (pmf) of X, i.e., write P(X = x) for all possible values of x.  

### Answers

P(X = 1) = p, it means probability of success.  
P(X = 0) = 1 - p, it means probability of failure.  
P(X = x) = 0, for x is not 1 or 0, it means probability of other outcome is 0.

## Q7.

### Questions

An experiment consists of throwing a fair coin four times. Find the frequency function and the cumulative distribution function of the following random variables:  
(a) the number of heads before the first tail  
(b) the number of heads following the first tail  
(c) the number of heads minus the number of tails  
(d) the number of tails times the number of heads.

### Answers

Sample space = {HHHH, HHHT, HHTH, HHTT, HTHH, HTHT, HTTH, HTTT, THHH, THHT, THTH, THTT, TTHH, TTHT, TTTH, TTTT}  
(a)  
f(X = 0) = $\frac{8}{16}$ , f(X = 1) = $\frac{4}{16}$ , f(X = 2) = $\frac{2}{16}$ , f(X = 3) = $\frac{1}{16}$ , f(X = 4) = $\frac{1}{16}$  
F(x) =  
&nbsp;&nbsp; 0, x < 0  
&nbsp;&nbsp; $\frac{8}{16}$ , 0 ≤ x < 1  
&nbsp;&nbsp; $\frac{12}{16}$ , 1 ≤ x < 2  
&nbsp;&nbsp; $\frac{14}{16}$ , 2 ≤ x < 3  
&nbsp;&nbsp; $\frac{15}{16}$ , 3 ≤ x < 4  
&nbsp;&nbsp; 1, 4 ≤ x  

(b)  
f(X = 0) = $\frac{5}{16}$ , f(X = 1) = $\frac{6}{16}$ , f(X = 2) = $\frac{4}{16}$ , f(X = 3) = $\frac{1}{16}$  
F(x) =  
&nbsp;&nbsp; 0, x < 0  
&nbsp;&nbsp; $\frac{5}{16}$ , 0 ≤ x < 1  
&nbsp;&nbsp; $\frac{11}{16}$ , 1 ≤ x < 2  
&nbsp;&nbsp; $\frac{15}{16}$ , 2 ≤ x < 3    
&nbsp;&nbsp; 1, 3 ≤ x  

(c)  
f(X = -4) = $\frac{1}{16}$ , f(X = -2) = $\frac{4}{16}$ , f(X = 0) = $\frac{6}{16}$ , f(X = 2) = $\frac{4}{16}$ , f(X = 4) = $\frac{1}{16}$  
F(x) =  
&nbsp;&nbsp; 0, x < -4  
&nbsp;&nbsp; $\frac{1}{16}$ , -4 ≤ x < -2  
&nbsp;&nbsp; $\frac{5}{16}$ , -2 ≤ x < 0  
&nbsp;&nbsp; $\frac{11}{16}$ , 0 ≤ x < 2  
&nbsp;&nbsp; $\frac{15}{16}$ , 2 ≤ x < 4  
&nbsp;&nbsp; 1, 4 ≤ x  

(d)  
f(X = 0) = $\frac{2}{16}$ , f(X = 3) = $\frac{8}{16}$ , f(X = 4) = $\frac{6}{16}$   
F(x) =  
&nbsp;&nbsp; 0, x < 0  
&nbsp;&nbsp; $\frac{2}{16}$ , 0 ≤ x < 3  
&nbsp;&nbsp; $\frac{10}{16}$ , 3 ≤ x < 4  
&nbsp;&nbsp; 1, 4 ≤ x  
