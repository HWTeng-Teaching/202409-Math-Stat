## Prove: $P(A \cap B) = P(A) + P(B) - P(A \cup B)$

$$ A \cup B = A \cup (B - AB) $$

and

$$ A(B - AB) = \emptyset $$

so $A$ and $B - AB$ are mutually exclusive events and

$$ P(A \cup B) = P(A \cup (B - AB)) = P(A) + P(B - AB) \quad \text{(Theorem 1.2)} $$

Now, since $AB \subseteq B$, Theorem 1.5 implies that

$$ P(B - AB) = P(B) - P(AB) \quad \text{(Theorem 1.5)} $$

Therefore, we get

$$ P(A \cup B) = P(A) + P(B) - P(AB) $$

Finally, rearranging the terms gives:

$$ P(A \cap B) = P(A) + P(B) - P(A \cup B) $$

### Theorem 1.2

Let {A1, A2, ..., An} be a mutually exclusive set of events. Then

$$
P\left( \bigcup_{i=1}^{n} A_i \right) = \sum_{i=1}^{n} P(A_i)
$$

(axiom 3)

### Theorem 1.5

If A ⊆ B, then

$$
P(B - A) = P(BA^c) = P(B) - P(A)
$$
