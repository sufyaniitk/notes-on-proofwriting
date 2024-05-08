<span style='font-family: Calibri serif;'>

## 10 - To be or Not to be II

</span>

---

<span style='font-family: Bahnschrift;'>

Towards the end of the last discussion we explored counterexamples. I want to now shed some more light on 'Prove or disprove' problems. It is unlilkely that I will put in a detailed example, because the $n \geq 3$ demonstrated everything very well. This discussion will be a bit more abstract.

---

Prove or disprove problems come in many forms. A few I can think of:

- If $r$ satsifies $P(r)$, is it true it satisfies $Q(r)$?
- Suppose for $r$, $P(r)$ holds. Is it true that $Q(r)$ holds?
- Suppose for $r$, $\neg Q(r)$. What can you say about $P(r)$?

Here, $r$ could be any mathematical object - an invertible matrix, a set of polynomials, etc. and $P$ and $Q$ are mathematical statements that depend on the choice of the object.

All the above statements allude to the same implication $\forall r \space P(r) \implies Q(r)$, and you're being asked to check whether the implication holds or not.

In case you want to show the implication does hold, you would ideally employ some proving technique, assume $P(r)$ holds (either for every $r$, or WLG for some specific $r$), and show $Q(r)$ holds.

To show the implication is not true, it suffices to show its negation is true. So we negate the statement $\forall r \space P(r) \implies Q(r)$. Negating an implication is not as straightforward, so we replace it by its logical equivalent.

$$\forall r \space (\neg P(r) \vee Q(r))$$

Now let's negate the statement $\neg(\forall r \space (\neg P(r) \vee Q(r)))$. 

As we saw earlier, $\neg (\forall r \space P(r)) = \exists r \space \neg P(r)$. Using this on our statement above, we obtain

$$\exists r \space \neg (\neg P(r) \vee Q(r))$$

Using de Morgan's law, we finally obtain

$$\exists r \space (P(r) \wedge \neg Q(r))$$

Thus to show the original implication *doesn't* hold, it suffices to establish the existence of just one $r$ for which $P(r)$ (*ie, the hypothesis*) is true, **AND** $Q(r)$, (*ie the conclusion*) is false. Since an implication states that whenever $P$ is true $Q$ must be so, the existence of such $r$ *disproves* $\forall r \space P(r) \implies Q(r)$

At the point in time you're reading this, you have very little exposition to math and as such I am not sure what examples I could include. Here are a few from high school math:

---

1. $r$: a polynomial function in the set $\mathbb R[X]$. $P(r)$: $r$ is such that $\deg r \geq 1$. $Q(r)$: $r$ has atleast one real root. 
 Counterexample : $r = X^2 + 1$
1. $r$: a pair $(a, b)$ of $n \times n$ matrices. $P(r)$: $a$ and $b$ are invertible. $Q(r)$: $a + b$ is invertible
Counterexample: $r = (-I_n, I_n)$

For the following examples, try to correctly recognise $r$, $P(r)$, and $Q(r)$.

1. Every continuous everywhere function is differentiable somewhere. Counterexample - Weierstrass function
1. The integral of the derivative of every differentiable function differs from it only by a constant. Counterexample - Volterra's function
1. If an infinite series converges, every rearrangement of the series converges to the same limit. Counterexample - the famous expansion of $\ln 2$, $\sum _{n=1} ^\infty \dfrac {(-1)^{n+1}}{n}$

(I'm sorry for breaking your brain)

---

If you're clever, you might be thinking "wow, proving negations is easy, just find a counterexample!" and well, yes, that's the gist.

If you're too clever by about half, you'll think about some negation of a negation shenanigans and try to prove an implication with just one example.

There are systems where you can do that, and those are precisely the $\text{WLG}$ arguments we talked about. But obviously, that doesn't always work.

This was a relatively short one because we've already talked about mostly everything and my examples are subject to your limited exposure to topics in math. Anyway, all this discussion should be sufficient to give you a fundamental idea to build upon in your upcoming lectures.

</span>