<span style='font-family: Calibri serif;'>

## 7 - True or False?

</span>

---

<span style='font-family: Bahnschrift;'>

We ended the last discussion with something that is nothing short of diabolical. Proving statements are equivalent does not necessarily mean they hold.

In this discussion, we will look at a few examples of what I am trying to say here.

---

<span style='font-family: Calibri serif;'>

### The limits of sin

</span>

Our first example comes from single variable calculus and real analysis. You may be familiar with the question of the following limit:

$$
L = \lim _{x \rightarrow 0} \dfrac {\sin x} x
$$

A novice new to solving problems and fresh out of his last lecture in calculus would say "use L'Hopitale's rule!"

The correct way to deal with this idiot is to ask him for a proof of L'Hopitale's rule, and a proof that $\sin x \rightarrow 0$ as $x \rightarrow 0$.

But let's say we entertain him for a moment. Let's take L'Hopitale's rule for granted and compute the limit.

$$
L = \lim _{x \rightarrow 0} \dfrac{\frac{d}{dx}\sin x}{\frac{d}{dx}x}
$$

Of course, since he skipped all his classes, he has no idea what the derivative of $\sin x$ is. A lot of confidence in proclaiming $\frac{d}{dx}x = 1$, however. I'll leave you to figure out why.

Anyway, let's find the derivative of $\sin x$ at $x = 0$. Using first principle, we want to find

$$
\lim _{h \rightarrow 0} \dfrac{\sin (0+h) - \sin 0}{(0+h) - 0}
$$

Et voila! The same limit. 

Now look at the situation we have here. If I know that the derivative of the $\sin$ at $x = 0$ is $1$, I already know the limit. But if I know that the value of the limit is $1$, I know the value of the derivative.

And so, we have an equivalence! $(\sin' x)_{x = 0} = 1 \iff \lim _{x \rightarrow 0} \dfrac {\sin x} x = 1$

---

<span style='font-family: Calibri serif;'>

### Pythagoras or cosine?

</span>

Our next example comes from an old friend in Euclidean Geometry. Have a good look at this arbitrary triangle:

![](/files/N7_1.png)

I don't know how to label sides so just follow the usual convention. (i.e, side opposite $A$ is $a$ etc). Call the length $|AM|$, $m$ for simplicity.

$AM$ is the altitude from $A$. Thus, $m = c\sin\beta = b\sin\gamma$.

Note $|CM| = b\cos\gamma$ and thus $|BM| = a - b\cos\gamma$.

Focus on the right triangle $\Delta BMA$. Suppose the Pythagorean Theorem holds. Then, we may conclude

$$
(a - b\cos\gamma)^2 + (b\sin\gamma)^2 = c^2
$$

Expanding,

$$
a^2 -2ab\cos\gamma + b^2\cos^2\gamma +b^2\sin^2\gamma = c^2
$$

Knowing $\sin^2\gamma + \cos^2\gamma = 1$ (this is equivalent to Pythagorean theorem, and hence safe to assume) we obtain the simplification

$$
c^2 = a^2 + b^2 - 2ab\cos\gamma
$$

Cyclic variants of the result follow by simple relabeling.

However, suppose $\angle C$ was right. Then, $\cos\gamma = 0$ and hence we obtain $c^2 = a^2 + b^2$.

The cosine law and Pythagorean Theorem are equivalents of each other, provided $\cos \frac \pi 2 = 0$

But we used Pythagoras to prove cosine law in the first place! If they're equivalent, is the argument we've given circuler?

**No.** But you need to understand in what context it could be circular.

In a bi-implication, we are *supposed to* use one statement to prove the other and vice versa. **That is perfectly fine**. Above, we saw assuming Pythagoras gives cosine and assuming cosine gives Pythagoras. No problem, the statements are equivalent.

The problem arises when I am given **Q. Prove that the cosine law is true for all triangles** and I use Pythagoras to prove it. Here, I am being asked to prove something, but I already assumed it!

Thus, showing the bi-implication shows the statements are equivalent. It DOES NOT establish whether the statements are true or false or depend on the variables. ABSOLUTELY NO CONCLUSIONS can be drawn from an equivalence.

This is why to prove the Pythagorean theorem, we must look elsewhere. Proof by similar triangles, areas, etc. If the truth of something is to be established, we cannot use its equivalents *unless their truth has been established independently*.

i.e., if you really want to show cosine using Pythagoras, you must first show Pythagoras by some technique that does not require cosine.

I hope this section is clear. If not, go through it again.

---

<span style='font-family: Calibri serif;'>

### To b or not to b

</span>

Our final example comes from Linear Algebra. Given a square matrix $A$ of order $n$, the following are equivalent:

- $\forall \space b \in \mathbb R^n, \exists^! \space x \in \mathbb R^n, Ax = b$
- $\exists \space B \in M_n(\mathbb R), AB = I_n = BA$

I'm not doing the proof for this, literally trivial. What the equivalence is saying is every vector $b$ has a unique preimage iff $A$ is invertible. Indeed if $A$ is invertible the preimage is $A^{-1}b$, and if every $b$ has a unique preimage, take the preimages for $(1, 0, ..., 0)^T$, $(0, 1, ..., 0)^T$, $...$, $(0, 0, ..., 1)^T$ and arrange them into columns to obtain the inverse of $A$.

Note how the truth or falsehoods of the statements depends on the choice of $A$. Compare this to the above example where both statements are true for every triangle.

Here, for a given $A$, they may be true, or they may be false, BUT, they'll *always have the same truth value.* You cannot find an invertible matrix with no preimage for some $b$. Similarly, you cannot find a matrix with a unique preimage for every $b$ that is noninvertible.

In the first example, we saw a logical equivalence which *we have no idea is true or false*. It does not depend on any external variable. All we know is that the limit is 1 iff the derivative is 1. Thus we need to evaluate either the limit or the derivative using other techniques to obtain the truth values of these statements.

---

Logically equivalent statements are true together and false together. Their truth value may be fixed (in case they are equivalents of some theorem), dependent on an external variable (a matrix), require further evaluation (the limit), or literally just for you to decide (Axiom of Choice)

Working with equivalences is intricate business and requires precision - you should be aware of exactly what it is you're doing. Establishing equivalence? Or establishing truthhood?

Clarity on just this one question will mostly keep you out of trouble.
</span>