# Problem:
###### 1-58
A teacher tells three boys, Drew, Chris, and Jason, that two of them will have
to stay after school to help her clean erasers and that one of them will be able to
leave. She further says that she has made the decision as to who will leave and who
will stay at random by rolling a special three-sided Dungeons and Dragons die.
Drew wants to leave to play soccer and has a clever idea about how to increase his
chances of doing so. He figures that one of Jason and Chris will certainly stay and
asks the teacher to tell him the name of one of the two who will stay. Drew’s idea
is that if, for example, Jason is named, then he and Chris are left and they each
have a probability .5 of leaving; similarly, if Chris is named, Drew’s probability
of leaving is still .5. Thus, by merely asking the teacher a question, Drew will
increase his probability of leaving from 1/3 to 1/2 . What do you think of this scheme?

# Solution:

- There are three boys: **Drew**, **Chris**, and **Jason**.
- One boy will leave, and two will stay.
- Each boy has an equal chance of being the one who leaves: **1/3**.

## Possible Outcomes
1. **Drew leaves**; Chris and Jason stay.
2. **Chris leaves**; Drew and Jason stay.
3. **Jason leaves**; Drew and Chris stay.

## Drew's Plan
Drew asks the teacher to name one of Chris or Jason who will stay. He believes that once the teacher names one of them, the remaining two boys (including himself) have an equal **1/2** chance of leaving.

- **If Drew leaves** 
  - The teacher randomly names Chris or Jason (each with probability **1/2**) since both are staying.
  
- **If Chris leaves** 
  - The teacher must name Jason as the one staying among Chris and Jason.
  
- **If Jason leaves** 
  - The teacher must name Chris as the one staying among Chris and Jason.

## Conditional Probability Calculation

Suppose the teacher says "Jason will stay." The probability that Drew is the one leaving is calculated using Bayes' Theorem:

**P(Drew leaves | Teacher says Jason stays) = [P(Teacher says Jason stays | Drew leaves) × P(Drew leaves)] / P(Teacher says Jason stays)**

### Compute the Probabilities

- **P(Drew leaves) = 1/3**
- **P(Teacher says Jason stays | Drew leaves) = 1/2**
- **P(Teacher says Jason stays | Chris leaves) = 1**
- **P(Teacher says Jason stays | Jason leaves) = 0**

P(Teacher says Jason stays) is the total probability that the teacher says "Jason will stay":

P(Teacher says Jason stays) =  
&nbsp;&nbsp;&nbsp;&nbsp;[P(Teacher says Jason stays | Drew leaves) × P(Drew leaves)] +  
&nbsp;&nbsp;&nbsp;&nbsp;[P(Teacher says Jason stays | Chris leaves) × P(Chris leaves)] +  
&nbsp;&nbsp;&nbsp;&nbsp;[P(Teacher says Jason stays | Jason leaves) × P(Jason leaves)]  

P(Teacher says Jason stays) = (1/2 × 1/3) + (1 × 1/3) + (0 × 1/3) =  
&nbsp;&nbsp;&nbsp;&nbsp;1/6 + 1/3 + 0 = **1/2**

P(Drew leaves | Teacher says Jason stays) = (1/2 × 1/3) / (1/2) = (1/6) / (1/2) = **1/3**

## Conclusion

Drew's probability of leaving remains **1/3** even after the teacher reveals who among Chris and Jason will stay. His scheme does **not** increase his chances.

  



