<span style='font-family: Calibri serif;'>

## 9 - Without Loss to Generality

</span>

<span style='font-family: Bahnschrift;'>

Alright, here's the deal. After all of that development, for the final discussion or two, I'll just throw examples and highlight some points of emphasis.

These will be things we have already discussed, just a new set of examples for you to ponder.

---

Consider the following problem:

**Q. A triangle has two equal sides iff the opposing angles are equal**

Welp, you know it's time for the picture.

![](/files/N9_1.png)

$(\rightarrow)$ We want to show that if two sides are equal, so are their opposing angles. There's 3 sides in a triangle, and hence $\binom{3}{2} = 3$ ways to pick a pair of sides. So what do we do, write 3 seperate proofs?

No. We state that *without loss in generality, assume* $|\omega_0\omega_1| = |\omega_2\omega_0| = a$. If that happens, let $\omega_0M$ be the perpendicular from $\omega_0$ to $\omega_1\omega_2$. Then, we have right triangles $\omega_0M\omega_2$ and $\omega_0M\omega_1$, both are right angled (and hence we can use the Pythagorean Theorem)

Thus, $|\omega_0M|^2 + |M\omega_2|^2 = a^2 = |M\omega_1|^2 + |\omega_0M|^2$. Thus $|M\omega_2| = |M\omega_1|$. Hence by $SSS$, we conclude $\Delta\omega_0M\omega_2 \cong \Delta\omega_0M\omega_1$ and thus $\angle\omega_2 = \angle\omega_1$. $\square$.


Points of emphasis -
1. We used the Pythagorean Theorem and $SSS$ criterion in our proof, therefore, by nature, *they are part of our hypothesis*. Within any set of predefined axioms; theorems (or statements that have already been shown to be true) can be used no problem. We explored this in the last discussion.

1. We can't just say *without loss in/of generality* (oft abbreviated $\text{WLOG}$ or $\text{WLG}$) and move on. One has to specify why their chosen specific case covers all the general cases.
    
    - In this case, our specific choice implies all possible cases because if some other pair had equal lengths, a simple relabeling, and reproducing the given proof completes the proof. You have to be sure that the proof you're giving for the specific case can be reproduced for other cases.

1. Here it should be clear what the phrase "without loss in generality" means. We focus on a specific case and claim that it completes the proof. Overall, it would appear that we have only proven the specific case, but we actually prove the statement in its entirety, i.e., *no generalisation is lost*

This should help you understand $\text{WLG}$ proofs and recognise where you might have to use one.

---

$(\leftarrow)$ Suppose without loss in generality $\alpha_1 = \alpha_2$. Assume the side lengths to be $a_0, a_1, a_2$. Now we'll pull out the cosine rule, and solve for values of $a_1^2$ and $a_2^2$

$a_1^2 = a_0^2 + a_2^2 - 2a_0a_2\cos\alpha_1$

$a_2^2 = a_0^2 + a_1^2 - 2a_0a_1\cos\alpha_2$

Subtracting the 2 equations, and using $\alpha_1 = \alpha_2$, we get $a_1^2 - a_2^2 = a_2^2 - a_1^2$ giving $a_1 = a_2$, $\text{QED}$

Once again, we have taken the cosine rule as a part of our hypothesis, thus emphasizing once again what statments you assume true have an impact on what inferences you can make. Note the use of another WLG argument here.

Let's have a look at another example.

---

So, we saw for $n = 3$, an $n$ sided polygon is equiangular if and only if it is equilateral. Consider, then, this extension of the problem:

**Q. Prove or disprove - for every** $n \geq 3$ **, an** $n$ **sided regular polygon is equiangular if and only if it is equilateral**

A *prove or disprove* problem. Figure out whether the statement holds or not, and then prove your point.

Well, I say the statement is false. It claims the equivalence for every $n \geq 3$, but I say the equivalence doesn't hold for $n = 4$. Rhombuses are equilateral but not equiangular, and rectangles are equiangular but not equilateral.

Thus equiangular and equilateral are not true/false together at $n = 4$, therefore the equivalence doesn't hold for $n = 4$. And thus the "for every $n \geq 3$" part of our statement fails to hold.

Producing an example for which a *forall* statement fails to hold is called a *counterexample*. The mere existence of that counterexample is enough to disprove any forall statement.

In our example, rhombuses are the counterexample to `all equilateral 4-gons are equiangular`, rectangles are the counterexample to `all equiangular 4-gons are equilateral`. Overall, $n = 4$ is a counterexample to `for n >= 3, n-gons are equiangular iff equilateral`

---

The last section, I'm trying to point you to the simple fact that the negation of a statement $\forall q, P(q)$ is $\exists q, \neg P (q)$. i.e., negating "for all $q$, $P(q)$ holds" gives "there exists a $q$ such that $P(q)$ is false".

Thus, existence of a $q$ for which $P(q)$ is false *disproves* the statement "for every $q$, $P(q)$ holds". Similarly, if for every $q$ you can show $P(q)$ holds, then you have just disproved "there is a $q$ for which $\neg P(q)$ is true".

</span>