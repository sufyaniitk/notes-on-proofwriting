<span style='font-family: Calibri serif;'>

## Antecedents and Consequents

</span>

---

<span style='font-family: Bahnschrift;'>

Now that you are familiar with if and only if statements and contrapositives, it is time to revisit the first problem we completed, but a modified version.

The modification I'm making is both to the problem and the way it's phrased. We will have a look at antecedents and consequents, and how to correctly recognise them.

Given an implication $p \implies q$, we call the statement $p$ the *antecedent*, or more colloquially, the *hypothesis*. On the other hand, the statement $q$ is called the *consequent*, or the *conclusion*.

Naturally, when you set out to prove something, you should have clarity on what the hypothesis is and what the conclusion should be.

My favorite example of even the best students confusing the two comes from the 2020 INMO Problem 2:

Suppose $P(x)$ is a polynomial with real coefficients satisfying the condition 

$$
P(\cos\theta + \sin\theta) = P(\cos\theta - \sin\theta)
$$

for every real $\theta$. Prove that $P(x)$ can be expressed in the form 

$$
P(x) = a_0 + a_1(1-x^2)^2 + a_2(1-x^2)^4 + ... + a_n(1-x^2)^{2n}
$$

for some real numbers $a_0, a_1, ..., a_n$ and some nonnegative $n$

---

The HBCSE, every year, releases a document outlining common mistakes made by students in the examination. For this problem, the most common error made by students (selected for the INMO, mind you) was to *prove the implication in the opposite direction.* They started with suppoing $P(x)$ had the given form, and showed that $P(\cos\theta + \sin\theta) = P(\cos\theta - \sin\theta)$ must hold.

Having followed the discussion on implications and contrapositives and sufficient and necessary conditions and so many more things, you should be able to see that a mistake like this is absolutely inexcusable at best.

So let's have a look at the original problem, `Ctrl+C Ctrl+V`'d from `N1`.

**Q. Show that the square of an even number is even.**

Take some time and recognise the antecedent and consequent.

Ready? The antecedent is `a number n is even`. The consequent is `the number n^2 is even`.

Note the appearance of a new variable $n$ which was not originally stated in the problem. You could say my recognition of the antecedent and consequent is imprecise. To which I will respond the problem was originally imprecisely stated as to not intimidate you.

A correct, more sound statement would be **Q. Given an integer $n$, show that if $n$ is even, then $n^2$ is even**

Both $p$ and $q$ are *laid out for you*. $p$ here is `an integer n is even` and $q$ is `n^2 is even`. **This will not always be the case**. Branches of mathematics, such as the arithmetic of integers, are too ubiquitous for detail to be necessary. Similarly, you may find ill-stated problems in the middle chapters of some textbooks. But, it is expected of you to extract the $p$s and the $q$s correctly when that happens, because by that time, the author expects you to have developed familiarity with the subject. Discussion for later.

---

Let's have a look at the modified problem now.

**Q. Show that an integer is even if and only if its square is even**

Obviously, this is a bi-implication. Try and recognise the antecedents and consequents of both of them.

A useful trick is to look at the `if` and the `only if` seperately. If you want to show $p \text{ if and only if } q$, then we show both $p \text{ if } q$ and $p \text{ only if } q$. Notice that $p \text{ if } q$ is the implication $q \implies p$, NOT the opposite. Much the same, $p \text{ only if } q$ is the implication $p \implies q$, NOT the opposite.

So in our original problem, **an integer is even only if its square is even** has antecedent `an integer n is even` and consequent `n^2 is even`

What about the opposite? **an integer is even if its square is even**, or that **its square is even implies an integer is even**. 

The antecedent appears to be `its square is even`. Whose square? Similarly the consequent appears to be `an integer is even`. Just any integer?

We have to infer from context. The context can be the implication itself or its converse. Again, the problem is ill-posed, but we're supposed to connect the dots.

The antecedent here would be `an integer of the form n^2 is even` and the consequent would be `n is even`. That is much more precise.

---

I advice you to read through the previous section again and internalise this notion of extracting mathematical statements, even from ill-posed problems. I'll try to be as precise as possible from now on, but when I'm not, its your duty to pick up the pieces.

</span>