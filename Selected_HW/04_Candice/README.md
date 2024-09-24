
# Question
## Prove: If A ⊆ B, then P(A) ≤ P(B)

# Answer
### Definitions
- Let \( P(A) \) denote the probability of event \( A \).
- Let \( P(B) \) denote the probability of event \( B \).

### Proof

1. **Understanding the Definition of Subset**:
   Since \( A \subseteq B \), every outcome in \( A \) is also an outcome in \( B \).

2. **Using the Additivity Property of Probability**:
   The probability of the union of two disjoint events is equal to the sum of their probabilities. We can express \( B \) as:
   \[
   B = A \cup (B \setminus A)
   \]
   where \( B \setminus A \) is the set of outcomes in \( B \) that are not in \( A \).

3. **Disjoint Sets**:
   The sets \( A \) and \( B \setminus A \) are disjoint. Thus, we can apply the additivity property:
   \[
   P(B) = P(A) + P(B \setminus A)
   \]

4. **Non-negativity of Probability**:
   Since probabilities are always non-negative, we have:
   \[
   P(B \setminus A) \geq 0
   \]

5. **Combining the Results**:
   From step 3, we can substitute the non-negativity into our equation:
   \[
   P(B) = P(A) + P(B \setminus A) \geq P(A)
   \]

6. **Conclusion**:
   Thus, we conclude:
   \[
   P(A) \leq P(B)
   \]
   This completes the proof.

### Summary
If \( A \subseteq B \), then it follows that \( P(A) \leq P(B) \).
