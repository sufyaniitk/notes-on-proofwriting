<span style='font-family: Calibri serif;'>

## 12 - Lighting the Fuse

</span>

---

<span style='font-family: Bahnschrift;'>

The final proof technique I want to demonstrate is proof by induction. Induction is useful when you want to show some statement $P$ holds for all natural numbers $n \geq n_0$ for some fixed $n_0$.

Examples of these statements are the Fundamental Theorem of Arithmetic, $\sum _{k=1}^{n} k = \dfrac {n(n+1)}2$, the binomial theorem, $\cos nx$ is an $n$ degree polynomial in $\cos x$, the $\text{AM-GM}$ inequality etc.

The idea is to establish the truth for *some* $n \in \mathbb N$ and use it to establish truth for other $n$ using recurrences, breaking larger numbers into smaller numbers, etc.

Now, you're familiar with induction. For completeness, I'll cover a basic example, point out some common pitfalls, and then get to some more convoluted examples. Let's start with a straightforward example:

---

<span style='font-family: Calibri serif;'>

### Straightforward examples

</span>

**Q. Show that** $\sum_{k = 1}^{n}k = \dfrac{n(n+1)}2$

**Proof.** Step 1. (Base Case) For $n=1$. the expression clearly holds.

Step 2. (Induction Hypothesis) Suppose the statement holds for some natural number $m$ (just some number $m$. This is a *weak* induction hypothesis)

Step 3. (Complete the proof) The recurrence I have decided on here is showing $P(m) \implies P(m+1)$.

Observe, $\sum_{k=1}^{m+1} k = (m+1) + \sum_{k=1}^{m}k$.

Under the induction hypothesis, the RHS sum evaluates to $\frac {m(m+1)}{2}$. Thus the LHS sum overall is $(m+1) + \frac{m(m+1)}{2} = \frac{(m+1)(m+2)}{2} = \frac{(m+1)((m+1) + 1)}{2}$

Thus the required implication holds. $\square$

This is an example of using a recurrence (ie $P(m) \implies P(m+1)$) alongside a base case to complete the proof.

---

Now let's have a look at strong induction.

**Q. Show that every positive integer** $n > 1$ **is either prime or is equal to a product of primes**.

**Proof.** (Base Case) $n = 2$ is prime.

(Induction Hypothesis) Suppose for some natural $m$, the statement holds for every $k$, $2 \leq k \leq m$ (*every* number smaller than or equal to some m. This is a *strong* induction hypothesis)

(Complete the proof) Consider $m+1$. If it is prime, there is nothing to show. Otherwise, $m+1 = ab$ for some $a,b \in \mathbb N$. In particular, $1 < a, b < m + 1$.

By induction hypothesis, $a$ and $b$ are themselves products of primes. Thus $(m+1)$ is a product of those primes and we're done. $\square$

This is an example of the "building block" approach. I did not exploit the truth of the statement at $m$. I just used some arbitrary numbers smaller than $m+1$ (not even knowing which one) as "building blocks" for my proof.

---

<span style='font-family: Calibri serif;'>

### Some exotic examples

##### Euclid's Lemma for $n =2$

</span>

Recall that we used Euclid's Lemma while proving an integer is even iff its square is even.

Here, we will prove the lemma for $n = 2$. i.e, given any integer $m$, there is a unqiue $n$ such that precisely one of $m = 2n$ and $m = 2n+1$ holds.

We will be concerned with existence here. Uniqueness and showing exactly one of the above holds is not relevant to induction.

**Proof.** We will take 3 subcases, $m = 0$, $m > 0$, $m < 0$.

Subcase $m = 0$ is trivial. Consider the subcase $m > 0$

(Base Cases) for $m = 1$, $1 = 2 \times 0 + 1$ and for $m = 2$, $2 = 2\times 1$

(Induction Hypothesis) Suppose for positive integer $k$, Euclid's Lemma holds.

(Completion) Consider $k+1$. If $k$ has the form $2n$, $k + 1$ has the form $2n+1$. If $k$ has the form $2n + 1$, then $k + 1$ has the form $2(n+1)$. Thus Euclid's Lemma holds for $k+1$. $\square$

Finally consider the subcase $m < 0$.

(Base cases) $m = -1$ and $m = -2$ work with $2(-1) + 1$ and $2(-1)$ respectively.

(Induction Hypothesis) Suppose for negative integer $k$, Euclid's Lemma holds.

(Completion) Consider $k - 1$. If $k = 2n$, then $k - 1$ = $2(n-1) + 1$. If $k = 2n + 1$, then $k - 1 = 2n$. Thus Euclid's Lemma holds for $k-1$ $\square$

And that does it. It is impossible for us to hav left out any integer (think about why this is true).

---

<span style='font-family: Calibri serif;'>

#### AM-GM Inequality

</span>

For any number $n$ of positive real numbers $a_1, a_2, ..., a_n$, the following inequality holds:

$$
\dfrac{a_1 + a_2 + \dots + a_n}{n} \geq {^n} \sqrt{a_1a_2\dots a_n}
$$

with equiality iff $a_1 = a_2 = \dots = a_n$. Again, I will only show the inequality.

We proceed by induction on the number of variables. But this will be unlike anything you've seen so far.

(Base Case) For $n = 1$ the inequallity is trivial.

(Induction Hypothesis) Suppose that given *any* $k$ positive reals, $1 \leq k \leq m$ , the inequality holds.

(Completion) First we'll show the inequality holds for $2m$. Let $a_1, a_2, \dots a_m, a_{m+1}, a_{m+2}, \dots a_{2m}$ be positive reals. Group them into $a_1, \dots a_m$ and $a_{m+1} \dots a_{2m}$.

By IH, we can apply the inequality to both sides to obtain

$$
\dfrac{a_1 + \dots + a_m}{m} \geq {^m}\sqrt{a_1\dots a_m}
$$

and

$$
\dfrac{a_{m+1}+\dots + a_{2m}}{m} \geq {^m}\sqrt{a_{m+1}\dots a_{2m}}
$$

Note the LHS. Those are still positive reals. And the inequality holds for 2 variables (IH). Using it,

$$
\dfrac{\dfrac{a_1 + \dots + a_m}{m} + \dfrac{a_{m+1}+\dots + a_{2m}}{m}}{2} \geq \sqrt{{^m}\sqrt{a_1\dots a_m}\cdot {^m}\sqrt{a_{m+1}\dots a_{2m}}}
$$

Simplifying, we obtain

$$
\dfrac{a_1 + \dots + a_{2m}}{2m} \geq {^{2m}} \sqrt{a_1\dots a_{2m}}
$$

which shows the inequality for $2m$ variables.

Finally, we'll show the inequality for $m-1$ variables under the same IH.

Consider positive reals $a_1, a_2, \dots a_{m-1}$. Since the inequality holds for *any* $m$ variables, it holds for the above $m-1$ and $a_m = \frac{a_1 + \dots + a_{m-1}}{m-1}$

Let's apply the inequality

$$
\dfrac{a_1 + \dots a_{m-1} + \frac{a_1 + \dots + a_{m-1}}{m-1}}{m} \geq {^m}\sqrt{a_1\dots a_{m-1}\cdot(\frac{a_1+\dots+a_{m-1}}{m-1})}
$$

The LHS simplifies to $\dfrac{a_1 + \dots + a_{m-1}}{m-1}$. Thus 

$$
(\dfrac{a_1 + \dots + a_{m-1}}{m-1})^m = a_1\dots a_{m-1}\cdot(\frac{a_1+\dots+a_{m-1}}{m-1})
$$

Removing one copy of the fraction from either side,

$$(\dfrac{a_1 + \dots + a_{m-1}}{m-1})^{m-1} \geq a_1\dots a_{m-1}$$

And we're done. $\square$.

---

Or are we? Those of you still awake would have noticed our proof for $k \rightarrow 2k$ relies on the inequality being true for $2$ variables. But the inequality being true for $2$ variables relies on the $k \rightarrow 2k$ implication holding in the first place.

Thus we need to find a different proof for $2$ variables. That is easily done by considering $(\sqrt {a_1} - \sqrt{a_2})^2 \geq 0$. What I wanted to emphasise is that you have to have a *very* clear image of how your chain of implications works, and fix it wherever necessary. More on this in the next.


</span>
