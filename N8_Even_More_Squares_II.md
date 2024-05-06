<span style='font-family: Calibri serif;'>

## 8 - Even More on Squares

</span>

---

<span style='font-family: Bahnschrift;'>

I want to take a moment to emphasize the importance of recognising antecedents and consequents in compound statements.

In the last discussion we recognised that that the Pythaogorean theorem holds if and only if the cosine rule holds. 

When I say "Pythagorean Theorem holds", I don't mean it applies. I mean that it is true. So; the Pythagorean Theorem is true if and only if the cosine rule is true. 

You'll see what I'm trying to say once I write down these statements a little more precisely.

---

The cosine rule is simple, for *any* triangle $ABC$, $b^2 = a^2 + c^2 -2ac\cos\beta$

The Pythagoras Theorem states that for a right triangle $DEF$ right angled at $E$, $e^2 = d^2 + f^2$. In fact, this is an equivalence. Let's have a look.

---

To prove an equivalence, we need to prove both implications, for which antecedents and consequents should be clear.

What I will show is `In a triangle ABC, angle A is right if and only if a^2 = b^2 + c^2`

$(\rightarrow)$ Here's our triangle. (I am having so much fun making these pictures in $\LaTeX$. It is exhausting but so satisfying.)

![](/files/N8_1.png)

I've already assumed $\angle A$ is right. No probs, this was the antecedent anyway. Once you have this diagram everything falls into place nicely.

$a_b = b\cos\gamma$ and $a_c = c\cos\beta$ are immediate. Borrowing the values of the cosines from the larger right triangle, we see that $a_b = \dfrac {b^2} a$ and $a_c = \dfrac {c^2} a$. Finally,

$$
a^2 = a(a_b + a_c) = a\dfrac{(b^2+c^2)}{a} = b^2+c^2
$$

And done. Now for the opposite direction.

---

$(\leftarrow)$ Consider a triangle $DEF$ that satisfies $e^2 = d^2 + f^2$. What I will do here is borrow from Euclidean Geometry the side length formulae $d = 2R\sin\delta$, $f = 2R\sin\phi$, $e = 2R\sin(\pi - (\delta + \phi)) = 2R\sin(\delta + \phi)$

Knowing $e^2 = d^2 + f^2$, substituting back in,

$$
4R^2\sin^2\delta + 4R^2\sin^2\phi = 4R^2\sin^2(\delta + \phi)
$$

some cacellations and an expansion

$$
\sin^2\delta + \sin^2\phi = \sin^2\delta\cos^2\phi+\sin^2\phi\cos^2\delta +2\sin\delta\sin\phi\cos\delta\cos\phi
$$

What I'm about to do here (and its explanation later) could turn mind-bending, but try to follow through.

Remember, I'm trying to prove that a the square of the longest length is the sum of the squares of the other two sides iff the triangle is right-angled. I've already proved the right side implication and am currently proving the left one.

Now, I'll move some terms around, 

$$
\sin^2\delta(1-\cos^2\phi) + \sin^2\phi(1-\cos^2\delta) = 2\sin\delta\sin\phi\cos\delta\cos\phi
$$

And in the next step,

$$
\sin^2\delta\sin^2\phi + \sin^2\phi\sin^2\delta = 2\sin\delta\sin\phi\cos\delta\cos\phi
$$

Those of you who are still awake will spot it. I seem to have used the identity $\sin^2\theta + \cos^2\theta = 1$. But that holds iff the Pythagorean Theorem holds. But I'm proving the Pythagorean theorem? How can I use that as an assumption?

Be assured, all is fine. I'll address it. Moving ahead,

$$
2\sin^2\delta\sin^2\phi = 2\sin\delta\sin\phi\cos\delta\cos\phi
$$

Since neither $\sin$ term is $0$, we can cancel them

$$
\sin\delta\sin\phi - \cos\delta\cos\phi = 0\\
\\ \text{ thus }
\cos(\delta+\phi) = 0
$$

And therefore $\delta+\phi = \dfrac \pi 2$, Thus $\angle E = \pi - \dfrac \pi 2 = \dfrac \pi 2$ which concludes the proof. 

---

So what about the little inconsistency that I left in? Well, for starters, Pythagorean Theorem refers only to the forward implication.

That unnecessary detail aside, suppose the forward implication (`right angled implies sum of squares`) holds. That is enough to conclude the `sin^2 + cos^2` identity. (Think through this)

What I've done above is first I prove the right side implication, and then *use it* to prove the left side implication.

I start out wanting to prove $p \iff q$. I first assumed $p$ and showed $q$, thus establishing $p \implies q$.

Then when I get to the converse, I want to prove $q \implies p$. Thus I assume $q$, and want to show $p$. Along the way, I *use* $p \implies q$. I use a statement that I have already established is true. You **can** do this. You cannot assume $p$ when setting out to prove $q \implies p$, but if you have already established $p \implies q$, you absolutely can use that.

---

You should have npticed there's a bunch of implications and equivalences surrounding the Pythagorean Theorem. So let's have a look at the whole picture.

Let $r$ denote the statement `a given triangle is right angled`.

Let $s$ denote the statement `the sum of squares of the smaller sides of a given triangle is equal to the square of the largest side`.

Let $c$ denote the cosine rule for all triangles.

Let $t$ denote the sine-cosine trigonometric identity for all angles.

Finally, let $p$ denote the Pythagorean Theorem: $r \implies s$

We established earlier that $p \iff c$. Writing the compound statement, $(r \implies s) \iff c$.

We established right now that $r \iff s$. Writing the proof, we used the chain of implications $r \implies s \implies t$.

Note, $r \implies s$ and $s \implies t$ but $r \implies (s \implies t)$ is NOT a conclusion of this. $s \implies t$ is a completely different statement on its own (and doesn't even make sense).

Similarly, $c \implies (r \implies s)$ but does $c$ imply either individually? No!

---

Finally, when we prove $(r \implies s) \iff c$ and $r \iff s$,  *neither proof has an impact on the other*.

In the first, we assume the implication $r \implies s$ and prove $c$. The latter proof establishes that the impllication $r \implies s$ is true. But again, IT DOES NOT ESTABLISH whether $r$ is true.

Take your time, read through this as many times as you need, and ask questions if necessary. As I said before, equivalences and implications in compound statements are tricky business. But as long as you're crystal clear on your hypothesis and conclusions, you're good to go.

I said in the beginning,
> When I say "Pythagorean Theorem holds", I don't mean it applies. I mean that it is true.

Indeed, the implication $r \implies s$ is true. But for a triangle, if $r$ doesn't hold, I can't really do much with it, can I? The hypothesis doesn't hold, so the theorem doesn't *apply*.

Alright this one has gone on long enough. Seeya next.

</span>