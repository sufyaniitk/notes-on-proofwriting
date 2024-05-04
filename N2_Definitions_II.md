<span style='font-family: Calibri'>

## 2 - More on Definitions and Direct Proofs

</span>

---

<span style='font-family: Bahnschrift;'>

In the previous discussion we saw a proof for the fact that the square of an even number is even. This "obvious" fact was proven with the help of the definition of an even number - a gateway from our understanding to precise, rigorous statements.

For this discussion I want to revisit the proof and point out a nuance. Albeit seemingly insignficant, the word "any" holds a lot of weight in the problem, and we will see how it affects our approach.

Other than that, we will have a look at another proof, one you may be familiar with from Real Analysis. This will lead us to another approach to proofs, but all in due time. <!-- I want to point out the whole if a then b requires argument/construction thing with this. Also quantifiers. -->

---

<span style='font-family: Calibri'>

### A revisit to squaring numbers

</span>

In the stated problem, I want you to focus on the word *"an"*. Show that the square of *an* even number is even.

Suppose I were to rewrite the problem. Show that the square of $2$ is even. Or $22$. Or $46$. Or $8937508$. "Easy", you'll say. Just square the number and it'll come out to be even.

But the task that we're handed is different. You're given an *arbitrary* even number. You have absolutely no clue how many digits it has, what it looks like, so you can't just square it and call it a day.

No, you have to work harder. You have to think about what an even number actually is. "A number of the form $2m$ with $m$ an integer" [notice the specification]). You have to square it and then show that the resulting number is again of the same form. Only then do you get your reward.

Point of emphasis - when given something *general* - you have to think about what more fundamental properties the object has, rather than the object itself. When I'm completing the proof, I'm **not** thinking about a specific even number, I'm starting with some property that *all* even numbers have, so that my proof is airtight.

You have to pay attention to these small things. I'll try to point out as many as possible, but it is equally your duty to be on the lookout.

---

<span style='font-family: Calibri'>

### Sum of sequences

</span>

There is a very high likelihood that you know what a sequence of real numbers is; and that if two sequences are such that $ \{ a_n \} _n \rightarrow A$ and $ \{ b_n \} _n \rightarrow B$, then the sequence given by their sum has the property $ \{ a_n + b_n \} _n \rightarrow A + B$

Just for clarity, $ \{ a_n \} _n \rightarrow A$ signifies that the sequence $ \{ a_n \}$ converges to the number $A$.

Consider, then, the following problem.

**Q. Given two convergent sequences, show that the sequence formed by adding their terms converges to the sum of the limits.**

Again, a direct proof. Given something holds, verify something else holds. But ITS SO OBVIOUS! WHAT ELSE COULD IT BE!

What do we do when we have to verify something obvious? We verify the definition. What is the definition of a sequence converging somewhere?

Well, I could write out

$$
\forall \space \varepsilon > 0 \space \exists \space N \in \mathbb N, \space n \geq N \implies |a_n - A| < \varepsilon
$$

but it makes no sense.

Or, I could be gentle, and write out

**Definition. Convergence of a Sequence** Say a sequence $ \{ a_n \} $ converges to $A$ if for every $\varepsilon > 0$, some infinite tail of the sequence falls within $\varepsilon$ distance of $A$.

Much cleaner, much more intuitive without the unnecessary symbols. Given a positive number $\varepsilon$, all points of the sequence beyond some $N$ fall within $\varepsilon$ distance of the limit. That gives you a much clearer picture than whatever unholy amalgamation of symbols I wrote above.

So, just knowing the definition sometimes isn't enough. You really have to know what it's trying to convey.

Now that I have the definition, I can complete steps 1 and 2 of the overall outline.

1. Start with what's given
1. Use definitions

So, our proof starts somewhat like

Let $ \{ a_n \} \rightarrow A$ and $ \{ b_n \} \rightarrow B$. Then, given $\epsilon_1, \epsilon_2 > 0$ there are natural numbers $N_1, N_2$ such that $n \geq N_1 \implies |a_n - A| < \epsilon_1$, and $n \geq N_2 \implies |b_n - B| < \epsilon_2$

Step 3 is to start working towards what you want. I want to show that given an $\epsilon > 0$, the existence of an $N$ such that $n \geq N \implies |(a_n + b_n) - (A + B)| < \epsilon$

So let $\epsilon > 0$ be given. Notice the LHS of the above inequality. If we apply the triangle inequality to this, we get $|(a_n + b_n) - (A+B)| \leq |a_n - A| + |b_n - B|$. This accounts for step 3. Use what you're given (all numbers involved are real and thus the triangle inequality applies) to make things easy.

What have I made easy here? Well, two things. First, if I can bound the RHS by $\epsilon$, I'm done.

Second, I ALREADY have bounds on the RHS. Given any $\epsilon_1, \epsilon_2$, I can always bound the RHS by $\epsilon_1 + \epsilon_2$ by taking the $\text{max}$ of the corresponding $N_1$ and $N_2$.

So all I need is a clever choice of $\epsilon_1$ and $\epsilon_2$ that bounds the RHS by $\epsilon$. This is step 4. Be clever with your simplified system and you're done.

If I can get $\epsilon_1$ and $\epsilon_2$ to sum to $\epsilon$, I'm done. Which leads to the natural choice of $\dfrac \epsilon 2$. This concludes step 4.

The final step is to establish the existence of $N$ for the given $\epsilon$. Well, choose $N_1$ and $N_2$ so that they satisfy the definition of convergence of $a_n$ and $b_n$ with $\dfrac \epsilon 2$ in place of $\epsilon$. Choosing the max of these $N_1$ and $N_2$ as $N$ satisfies the inequality in step 3 and hence the required inequality.

---

See if you can write the proof now. A rough sketch is given.

**Proof.** Let $\{a_n\} \rightarrow A$ and $\{b_n\} \rightarrow B$. Then, given $\epsilon_1, \epsilon_2 > 0$ there are natural numbers $N_1, N_2$ such that $n \geq N_1 \implies |a_n - A| < \epsilon_1$, and $n \geq N_2 \implies |b_n - B| < \epsilon_2$

Let $\epsilon > 0$ be given. Let $\epsilon_1 = \epsilon_2 = \dfrac \epsilon 2$. Since $\dfrac \epsilon 2 > 0$, there are naturals $N_3$ and $N_4$ such that $n \geq N_3 \implies |a_n - A| < \dfrac \epsilon 2$ and $n \geq N_4 \implies |b_n - B| < \dfrac \epsilon 2$.

Let $N = \text{max}(N_3, \space N_4)$. Then for $n \geq N$, both above inequalities are satisfied.

Finally consider

$$
|(a_n + b_n) - (A + B)| \\
\leq |a_n - A| + |b_n - B| \\
\leq (\text{if } n \geq N) \space \dfrac \epsilon 2 + \dfrac \epsilon 2 \\
= \epsilon
$$

Hence for $n \geq N$, the defining inequality holds. Thus $\{a_n + b_n\} \rightarrow A + B$ $\square$

---

Go through the proof. Understand where steps 1 - 5 show up (it may not be in order). If I'm introducing a new variable, understand where it's coming from. Try to understand why $\dfrac \epsilon 2$ is the natural choice and not, say, $1$ and $\epsilon - 1$.

Once you're ready, move on to the next doc.
</span>