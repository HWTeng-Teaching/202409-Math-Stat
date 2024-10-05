# HW0924

by 王邦碩 Brian

## Q1

### Question 

Urn A has four red, three blue, and two green balls. Urn B has two red, three blue, and four green balls. A ball is drawn from urn A and put into urn B, and then a ball is drawn from urn B.
a. What is the probability that a red ball is drawn from urn B?  
b. If a red ball is drawn from urn B, what is the probability that a red ball was drawn from urn A?  

### Solution
A)  
A draw red : $\frac49$ * $\frac3{10}$ = $\frac{12}{90}$  
A draw not red : $\frac59$ * $\frac2{10}$ = $\frac{10}{90}$  
$\frac{12}{90}$ + $\frac{10}{90}$ = $\frac{22}{90}$ = $\frac{11}{45}$  

B)
P(B draw red | A draw red)  
= $\frac{P(B\space draw\space red\space and\space A\space draw\space red)}{P(A\space draw\space red)}$  
= $\huge\frac{\frac{12}{90}}{\frac{22}{90}}$  

= $\large\frac6{11}$  

## Q2

### Question 

A fair coin is tossed three times.  
a. What is the probability of two or more heads given that there was at least one head?  
b. What is the probability given that there was at least one tail?  

### Solution
A)  
P(2 head or 3 head | at least one head)  
= $\huge\frac{HHH, HHT, HTH, THH}{HHH, HHT, HTH, THH, HTT,  THT, TTH}$  
= $\Large\frac47$  

B)
P(2 head or 3 head | at least one tail)  
= $\huge\frac{HHH, HHT, HTH, THH}{HHT, HTH, THH, HTT,  THT, TTH, TTT}$  
= $\Large\frac37$  

## Q3

### Question 

A teacher tells three boys, Drew, Chris, and Jason, that two of them will have to stay after school to help her clean erasers and that one of them will be able to leave. She further says that she has made the decision as to who will leave and who will stay at random by rolling a special three-sided Dungeons and Dragons die. Drew wants to leave to play soccer and has a clever idea about how to increase his chances of doing so. He figures that one of Jason and Chris will certainly stay and asks the teacher to tell him the name of one of the two who will stay. Drew’s idea is that if, for example, Jason is named, then he and Chris are left and they each have a probability .5 of leaving; similarly, if Chris is named, Drew’s probability of leaving is still .5. Thus, by merely asking the teacher a question, Drew will increase his probability of leaving from $\frac{1}{3}$ to $\frac{1}{2}$. What do you think of this scheme?

### Solution  
Wrong,  
P(Chris and Jason stay | Teacher say Chris)  
= $\large\frac{\frac{1}{3}}{P(Chris\space and\space Jason\space stay) * P(teacher\space choose\space to\space say\space Jason) + P(Drew\space and\space Jason\space stay)}$  
= $\large\frac{\frac{1}{3}}{\frac13 * \frac12 + \frac13}$  
=1/3    
So the probability remains the same whether asking teacher  

## Q4

### Question 
What is the probability that the following system works if each unit fails independently with probability p (see Figure 1.5)?
![image](https://hackmd.io/_uploads/HJrfSvTAC.png)

### Solution
Top not work: $1-(1-p)^2$  
Middle not work: $p$  
Botton not work: $1-(1-p)^2$  

1-P(no one work)  
= $1-p(1-(1-p)^2)^2$

## Q5

### Question 
A player throws darts at a target. On each trial, independently of the other trials, he hits the bull’s-eye with probability .05. How many times should he throw so that his probability of hitting the bull’s-eye at least once is .5?

### Solution
$1 - 0.95^n >= 0.5$  
n >= 14

## Q6

### Question 
Consider a Bernoulli trial, which is a random experiment with only two possible outcomes: success (with probability p) and failure (with probability (1 - p). Based on the Bernoulli trial, let X be a Bernoulli random variable, where: X(success) = 1, i.e., X maps success to 1. X(failure) = 0, i.e., X maps failure to 0. In other words, X = 1 represents a success, and X = 0 represents a failure. Define the probability mass function (pmf) of X, i.e., write P(X = x) for all possible values of x.
### Solution
P(X = 1) = p  
P(X = 0) = 1 - p  
P(x != 0, 1) = 0  

## Q7

### Question
An experiment consists of throwing a fair coin four times. Find the frequency function and the cumulative distribution function of the following random variables: (a) the number of heads before the first tail, (b) the number of heads following the first tail, (c) the number of heads minus the number of tails, and (d) the number of tails times the number of heads.

### Solution
(a)  
X : the number of heads before the first tail  
P(X = 0) = 1/2  
P(x = 1) = 1/2 * 1/2  
P(x = 2) = 1/2 * 1/2 * 1/2  
P(x = 3) = 1/2 * 1/2 * 1/2  
P(x = 4) = 1/2 * 1/2 * 1/2 * 1/2   
CDF(x) =   
0, x < 0   
1/2, 0 <= x < 1  
3/4,  1 <= x < 2   
7/8, 2 <= x < 3   
15/16, 3 <= x < 4   
1, 4 <= x  




(b)  
X: the number of heads following the first tail  
P(X = 0) = 5/16  
P(x = 1) = 6/16  
P(x = 2) = 4/16    
P(x = 3) = 1/2 * 1/2 * 1/2 * 1 / 2  
CDF(x) =  
0, x < 0  
5/16, 0 <= x < 1   
11/16, 1 <= x < 2   
15/16, 2 <= x < 3   
1, 3 <= x  


(c)
X: the number of heads minus the number of tails  
P(X = -4) = 1/16  
P(x = -2) = 4/16  
P(x = 0)  = 6/16  
P(x = 2)  = 4/16  
P(x = 4)  = 1/16  
CDF(x) =  
0, & x < -4   
1/16, -4 <= x < -2   
5/16, -2 <= x < 0   
11/16, 0 <= x < 2  
15/16, 2 <= x < 4   
1, 4 <= x  

(d)  
X: the number of tails times the number of heads.  
P(X = 0) = 2/16  
P(x = 3) = 8/16  
P(x = 4)  = 6/16  
CDF(x) =  
0, x < 0  
2/16, 0 <= x < 3  
10/16, 3 <= x < 4  
1, 4 <= x


