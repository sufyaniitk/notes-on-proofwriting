<span style='font-family: Calibri serif;'>

## 11- Proofs by Contradiction

</span>

---

<span style='font-family: Bahnschrift;'>

<!--irrationality of sqrt 2,  Cantor's thm-->

Having now completed what comprises about half a course in mathematical logic (lol, not), it is time we get back to what we originally set out to do and discuss another proofwriting technique. I'm picking up the pace a bit here because we've already discussed a lot of nuance I would otherwise point out.

---

I'm sure you are all familiar with the proof that the square root of 2 is irrational. Let's have a look.

**Q. Show that the square root of 2 is irrational**

**Proof.** *Suppose otherwise*, and that there are integers $p, q >0$ such that $\dfrac{p^2}{q^2} =2$. *Suppose* $\gcd(p, q) =1$. Cross multiplying above, $p^2 = 2q^2$ thus $p^2$ is even thus $p$ is even, so $p = 2p'$

Substituting back $(2p')^2 = 2q^2$ gives $4p'^2 = 2q^2$, which gives $q^2$ is even and hence $q$ is even.

Thus, $p$ and $q$ are both even thus $\dfrac {p}{q}$ fails to be in simplest terms. Contradiction. $\square$

What I want you to observe is the overall structure of the proof as I have presented it.

1. Assume $r = \sqrt 2$ is rational
1. Assume $r$ has simplest form $\frac p q$
1. Show that the simplest form is, in fact, not simplest (this is direct)
1. ???
1. Profit

In a proof by contradiction, it is always essential to point out *what exactly is being contradicted*. Here, in the last line, I have stated that $\frac p q$ being in lowest terms is being contradicted. But it is not clear why that should mean $\sqrt 2$ being rational is contradicted.

Let's add to our list of assumptions (and facts) that `for every rational number r = p/q, there exist p' and q' with r = p'/q' and gcd(p', q') = 1`

Now look at our chain of arguments.

1. $\sqrt 2 \in \mathbb Q \implies \exist p, q \in \mathbb Z^+, p^2 = 2q^2$

1. $\exist p, q \in \mathbb Z^+, p^2 = 2q^2 \implies \exist p', q' \in \mathbb Z^+, p'^2 = 2q'^2, \gcd(p', q') = 1$

1. $p'^2 = 2q'^2 \implies \gcd(p', q') = 2$

We have established 3. is true. Due to 3., the consequent of 2. is false, i.e., the consequent of 2 is contradicted. This is what we pointed out.

This in turn contradicts the consequent of 1., which contradicts the antecedent of 1.

So between our original contradiction (existence of simplest form) and what we want to show ($\sqrt 2$ being rational), we need a chain of implications. Contradicting *anything* within this chain of implications is enough to contradict the required statement.

Let me rephrase. Here, we do not need to show that $\sqrt 2$ is irrational directly. I observe that every rational number has a simplest form. Thus if I show that $\sqrt 2$ fails to have a simplest form, it couldn't be rational.

To some extent, all proofs abuse the contrapositive. If we are able to show the contradiction in its entirety (i.e. if we could've contradicted $\sqrt 2 \in \mathbb Q$ directly), it would've just been a proof by contrapositive. Here, we contradict a necessary condition. This is essentially the distinction between a proof by contrapositive and one by contradiction.

---

As another example, I will now present a proof of Cantor's Theorem.

**Theorem. (Cantor)** Given a set $A$ and its power set $\mathcal P(A)$, there is no bijective function $f: A \rightarrow \mathcal P(A)$

**Proof.** Suppose $f$ is a bijection between $A$ and $\mathcal P(A)$. For a given $a \in A$, $a$ can either fall into $f(a)$, or not fall into $f(a)$.

Let $B$ be the set of all $a$ such that $a \notin f(a)$

Since $f$ is bijective, it is surjective, thus there is some $b$ in $A$ such that $f(b) = B$.

Now suppose $b \in B$. By definition, $b \in f(b)$. But then $b \notin B$.

Similarly suppose $b \notin B$ ie $b \notin f(b)$. But then by definition of $B$, $b \in B$.

And so, $b \in B \iff b \notin B$

We have thus obtained a contradiction. But what exactly is it we're contradicting? One possible answer is the existence of $B$, but $B$ is a perfectly well defined set (see Axiom of Specification)

Thus the only candidate is the existence of $b$. If $b$ exists, we get a contradiction. Thus $b$ cannot exist. But $b$ was by definition the pre-image of $B$. 

We have thus constructed a set for which there is no pre-image under $f$ and thus we contradict surjectivity of $f$. By extension, $f$ fails to be bijective as well. $\square$

Again, I did not have to prove $f$ fails to be a bijection directly, that would've been a full fledged proof by contrapositive. Instead, I contradict a necessary condition - $f$ is surjective - and it takes care of the rest.

You should observe I had to be clever (normies would call this step 4) and *construct* a set with no pre-image. You have to do this often. You have to be clever and just with the limited info you have about a system, *construct* objects (sequences, sets, etc) with desired properties. Obviously, constructions are often required in existence proofs. Here, the existence of a set without a pre-image.

---

You should have noticed I'm picking up the pace with these examples, as after all this discussion on logic, you should notice some nuance on your own. If you get stuck, read through the previous sections again and try to reconstruct the presented proofs on your own, that should be helpful.

In the next, I will discuss another proof technique, and revisit an assumption we made in [N6](/N6_Contrapositive_Proofs.md)

</span>