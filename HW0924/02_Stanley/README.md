### 47. Urn A has four red, three blue, and two green balls. Urn B has two red, three blue, and four green balls. A ball is drawn from urn A and put into urn B, and then a ball is drawn from urn B.  
### a. What is the probability that a red ball is drawn from urn B?  
### b. If a red ball is drawn from urn B, what is the probability that a red ball was drawn from urn A?  
a. two situation  
A red and B red  
A blue and B red  
(4/9)x(3/10)+(3/9)x(2/10)=11/45  
b.
P(a red ball is drawn from urn A | a red ball was drawn from urn B)= $\large\frac{\frac{12}{90}}{\frac{11}{45}}$ = $\frac{6}{11}$
### 49. A fair coin is tossed three times.  
### a. What is the probability of two or more heads given that there was at least one head?  
### b. What is the probability given that there was at least one tail?  
a.  
Let **A** be the event of getting two or more heads.  
Let **B** be the event of getting at least one head.  
We need to find the conditional probability P(A | B): $\large\frac{\frac{4}{8}}{\frac{7}{8}}$ = $\frac{4}{7}$  
b.  
Let **A** be the event of getting two or more heads.  
Let **B** be the event of getting at least one tail.  
We need to find the conditional probability P(A | B): $\large\frac{\frac{3}{8}}{\frac{7}{8}}$ = $\frac{3}{7}$  
### 58. A teacher tells three boys, Drew, Chris, and Jason, that two of them will have to stay after school to help her clean erasers and that one of them will be able to leave. She further says that she has made the decision as to who will leave and who will stay at random by rolling a special three-sided Dungeons and Dragons die. Drew wants to leave to play soccer and has a clever idea about how to increase his chances of doing so. He figures that one of Jason and Chris will certainly stay and asks the teacher to tell him the name of one of the two who will stay. Drew’s idea is that if, for example, Jason is named, then he and Chris are left and they each have a probability 0.5 of leaving; similarly, if Chris is named, Drew’s probability of leaving is still 0.5. Thus, by merely asking the teacher a question, Drew will increase his probability of leaving from  $\frac{1}{3}$ to  $\frac{1}{2}$ . What do you think of this scheme?  
### Initial Setup
- Each boy—Drew, Chris, and Jason—has an equal probability of leaving:
  - Probability Drew leaves:  $\frac{1}{3}$  
  - Probability Chris leaves:  $\frac{1}{3}$  
  - Probability Jason leaves:  $\frac{1}{3}$  

Drew's plan is to ask the teacher which one of Chris or Jason will stay, hoping this extra information will improve his chances of leaving. However, this reasoning is flawed.

### Step 1: The Teacher’s Response
If Drew asks the teacher who among Chris or Jason will stay, the teacher will provide a name. Here's what happens in each scenario:

- If **Drew is the one to leave** (probability  $\frac{1}{3}$), the teacher can randomly choose to name either Chris or Jason, as both will stay. Each has a  $\frac{1}{2}$ chance of being named.
- If **Chris is the one to leave** (probability  $\frac{1}{3}$), the teacher will definitely name Jason, since Drew is staying.
- If **Jason is the one to leave** (probability  $\frac{1}{3}$), the teacher will definitely name Chris, since Drew is staying.

While Drew gets some information from the teacher, it doesn't change the overall situation.

### Step 2: Conditional Probabilities
Drew mistakenly believes that this information increases his chances of leaving. In reality, the teacher’s response doesn't affect the likelihood of Drew being the one to leave. Let's break down why:

- If **Drew was already chosen to leave** (probability  $\frac{1}{3}$), the teacher will randomly name one of Chris or Jason.
- If **Chris was chosen to leave** (probability  $\frac{1}{3}$), the teacher will definitely name Jason.
- If **Jason was chosen to leave** (probability  $\frac{1}{3}$), the teacher will definitely name Chris.

None of this changes the initial probability that Drew was chosen to leave, which remains  $\frac{1}{3}$.  
revealing certain information doesn’t change the underlying probabilities in the way one might expect. In this case, even though the teacher provides a name, the probability of Drew leaving remains  $\frac{1}{3}$, as the decision was already made when the die was rolled.  
### 74. What is the probability that the following system works if each unit fails independently with probability p (see Figure 1.5)?  
![image](https://github.com/user-attachments/assets/dc98f59f-0b15-4e34-9790-608ec30a0850)  
P(First path not work) = 1 - P(First path work) = 1 - (1 - p)(1 - p)  
P(Second path not work) = p  
P(Third path not work) = 1 - P(Third path work) = 1 - (1 - p)(1 - p)  
P(System work) = 1 - P(System not work)= $1 - [1 - (1 - p)^2] \times p \times [1 - (1 - p)^2]$ = $1 - p[1 - (1 - p)^2]^2$  
### 77. A player throws darts at a target. On each trial, independently of the other trials, he hits the bull’s-eye with probability .05. How many times should he throw so that his probability of hitting the bull’s-eye at least once is .5?  
P(not hitting)=1−0.05=0.95  
P(no hits in n throws)= $0.95^n$
P(at least one hit)=1−P(no hits in n throws)=1− $0.95^n$  
$1−0.95^n$ ≥ 0.5  
0.5 ≥ $0.95^n$  
log($0.95^n$) ≤ log(0.5)  
nlog(0.95) ≤ log(0.5)  
n ≥ $\frac{log(0.5)}{log(0.95)}$ = 13.5  
n at least 14  
throw 14 times  
### Consider a Bernoulli trial, which is a random experiment with only two possible outcomes: success (with probability p) and failure (with probability (1 - p). Based on the Bernoulli trial, let X be a Bernoulli random variable, where: X(success) = 1, i.e., X maps success to 1.  X(failure) = 0, i.e., X maps failure to 0.  In other words, X = 1 represents a success, and X = 0 represents a failure.  Define the probability mass function (pmf) of X, i.e., write P(X = x) for all possible values of x.  
P(X = 1) = p, it means probability of success.  
P(X = 0) = 1 - p, it means probability of failure.  
P(X = x) = 0, for x is not 1 or 0, it means probability of other outcome is 0.  
### 2.02 An experiment consists of throwing a fair coin four times. Find the frequency function and the cumulative distribution function of the following random variables: (a) the number of heads before the first tail, (b) the number of heads following the first tail, (c) the number of heads minus the number of tails, and (d) the number of tails times the number of heads.  
Sample space = {HHHH, HHHT, HHTH, HHTT, HTHH, HTHT, HTTH, HTTT, THHH, THHT, THTH, THTT, TTHH, TTHT, TTTH, TTTT}  
a.  
Let (X) represent the number of heads before the first tail is observed  
( P(X= 0) = 1/2 ) 
( P(X= 1) = 1/4 ) 
( P(X= 2) = 1/8 ) 
( P(X= 3) = 1/16 ) 
( P(X= 4) = 1/16 )  
F(x) =  
&nbsp;&nbsp; 0, x < 0  
&nbsp;&nbsp; $\frac{1}{2}$ , 0 ≤ x < 1  
&nbsp;&nbsp; $\frac{3}{4}$ , 1 ≤ x < 2  
&nbsp;&nbsp; $\frac{7}{8}$ , 2 ≤ x < 3  
&nbsp;&nbsp; $\frac{15}{16}$ , 3 ≤ x < 4    
&nbsp;&nbsp; 1, 4 ≤ x  
b.  
Let (K) represent the number of heads following the first tail is observed  
( P(K= 0) = 5/16 ) 
( P(K= 1) = 6/16 ) 
( P(K= 2) = 4/16 ) 
( P(K= 3) = 1/16 )  
F(x) =  
&nbsp;&nbsp; 0, x < 0  
&nbsp;&nbsp; $\frac{5}{16}$ , 0 ≤ x < 1  
&nbsp;&nbsp; $\frac{11}{16}$ , 1 ≤ x < 2  
&nbsp;&nbsp; $\frac{15}{16}$ , 2 ≤ x < 3    
&nbsp;&nbsp; 1, 3 ≤ x  
c.  
Let (G) represent the number of heads minus the number of tails is observed  
( P(G= -4) = 1/16 ) 
( P(G= -2) = 4/16 ) 
( P(G= 0) = 6/16 ) 
( P(G= 2) = 4/16 ) 
( P(G= 4) = 1/16 )  
F(x) =  
&nbsp;&nbsp; 0, x < -4  
&nbsp;&nbsp; $\frac{1}{16}$ , -4 ≤ x < -2  
&nbsp;&nbsp; $\frac{5}{16}$ , -2 ≤ x < 0  
&nbsp;&nbsp; $\frac{11}{16}$ , 0 ≤ x < 2  
&nbsp;&nbsp; $\frac{15}{16}$ , 2 ≤ x < 4  
&nbsp;&nbsp; 1, 4 ≤ x  
d.  
Let (T) represent the number of tails times the number of heads is observed  
( P(G= 0) = 2/16 ) 
( P(G= 3) = 8/16 ) 
( P(G= 4) = 6/16 )  
F(x)=  
&nbsp;&nbsp; 0, x < 0  
&nbsp;&nbsp; $\frac{2}{16}$ , 0 ≤ x < 3  
&nbsp;&nbsp; $\frac{10}{16}$ , 3 ≤ x < 4  
&nbsp;&nbsp; 1, 4 ≤ x   

