<span style='font-family: Calibri serif;'>

## 13 - Common Induction Mistakes

</span>

---
<span style='font-family: Bahnschrift;'>

Not so much 'mistakes' as it is an example of the kind of mistake I pointed out at the end of the last discussion. Let's have a look.

---

<span style='font-family: Calibri serif;'>

#### All horses are the same color

</span>

Let $P(n)$ denote the statement: `given a collection of n horses, all horses in the collection have the same color`

**Claim.** $P(n)$ is true for every $n \geq 1$

**Proof.** (Base Case) Let $n = 1$. Then every horse in a $1$ horse collection has the same color is trivial.

(IH) Suppose $P(m)$ holds for some $m$, i.e, given *any* collection of $m$ horses, they all have the same color.

(Completion) Consider a collection of $m+1$ horses. By IH, $a_1, a_2, \dots, a_m$ have the same color. By IH again, $a_{2}, a_{3}, \dots, a_{m+1}$ have the same color.

Clearly, $a_m$ and $a_{m+1}$ thus have the same color. $\square$

---

Where did I go wrong? Well, my process relies on removing one horse from the set and considering the colors of the remaining horses. However, this process *fails* when proving $P(2)$ from $P(1)$ because when you remove just the one horse, there's nothing left.

Let's have a look at one final example for induction.

<span style='font-family: Calibri serif;'>

#### Small offset

</span>

Suppose you set out to show that $\sum_{k=1}^{n} = \dfrac{n^2+n+2}{2}$. If you checked that $f(n+1) = f(n) + (n+1)$, you would find that equality holds and make your conclusion.

Where you would go wrong, however, is checking the base case. You never light your string of crackers on fire, you just check that burning one will ignite the next.

Light the fire. *Check the base case*. That's all.

</span> 