<span style='font-family: Calibri'>

## 1 - Definitions and Direct Proofs

</span>

---

<span style='font-family: Bahnschrift;'>

A *definition* is a way of assigning names to mathematical objects for simplicity. For instance, we use the phrase *"function from set A to set B"* to mean *"A subset* $f$ *of the Cartesian Product* $A \times B$ *such that for every* $a \in A$ *there is a* $b \in B$ *with* $(a,b) \in f$, *and if* $(a, b_1) \in f$, $(a, b_2) \in f$ *then* $b_1 = b_2$"

Now we used the terms *Cartesian Product* and *subset* which further have their own definitions. If we replace those in the definition for a function, and then replace the definiton of a function in that for say, a differentiable function, then things get very complicated very fast.

This is a point of confusion for a lot of people. Problems that ask you to prove something "obvious" are asking you to check whether the given definitions hold within context.

</span>

---

<span style='font-family: Calibri'>

### An example

</span>

<span style='font-family: Bahnschrift;'>

**Q. Show that the square of an even number is even.**

This may seem obvious to you. Just take an even number, square it, and you get another even number. Things that seem obvious usually present you a direct line of sight. The proof technique used here is a *Direct Proof*. You start with what's given (an even number) and after a few steps, you conclude with what's required (the square being an even number).

Note that to start with an even number, I first have to know what an even number is. Similarly, To check whether the number I have obtained after squaring is even, I have to once again know what an even number is. This is where the **definition** of an even number kicks in. To check whether a number is even, I check if it satisfies the **definition** of an even number. You know it, but I like being pedantic so

**Definition. Even Integer** An integer $n$ is called *even* if for some integer $m$, $n = 2m$.
(Note we take for granted the definition of an integer)

Now that I know what an even integer (number) is, I'm ready to write the proof.

**Proof.** Let $n$ be an even integer. (<- 1. starting with what's given)

Then, $n = 2m$ for some integer $m$ (<- 2. using the definition)

Thus, $n^2 = (2m)^2 = 4m^2$ (<- 3. intermediate step, depends on problem)

Thus, $n^2 = 2(2m^2)$ (<- 4. key insight to the problem)

i.e. there is an integer $m' = 2m^2$ for which $n^2 = 2m'$ (<- 5. restating my conclusion in terms of the definition)

Therefore, $n^2$ is even. $\square$

---

I want to point out a few things here. Note in step 2, I appear to have created a new variable, $m$, out of thin air. That is not the case. The existence of such an $m$ is guaranteed by the definition. Further, note that I have *specified* in step 2 that $m$ is an integer, even though it may feel like I didn't need to.

If I don't specify that, then I have failed to use the definition correctly. **Always specify everything**. In more complicated problems, this could become a cause of error.

Step 3 is algebraic manipulation. I want you to note I'm borrowing properties of integers when I say $(ab)^2 = a^2b^2$ (this does not hold in matrices, for example). Although **ideally I should specify this**, it is not really necessary because of two reasons:

i) multiplication of integers is something very, very basic, and does not really require clarification (ie, you don't need to specify you're using the commutativity of integer multiplication. You can just do it).
ii) It is abundantly clear from context what you're doing

Again, in more complicated problems, you may have a much longer step 3 or multiple step 3s. That is, you have rephrased what you're given in more mathematical terms, and are now working toward the conclusion. This may mean adding and subtracting the same quantity, considering a subset, exploiting some property etc (we'll see examples). But the overall motive is try to work towards what you want to conclude.

Step 4 is the "key idea" so to say, that you can factor out a 2 from the value of $n^2$. *This essentially completes the problem*. BUT; for that to work, you *have* to be assured that $2m^2$ **is an integer**. This is why we specify that $m$ is an integer in step 2; because $2m^2$ being an integer follows directly from $m$ being an integer.

If we leave out that specification, ie if we say $n$ is even if $n = 2m$; not only have we used the definition wrong, but we cannot conclude $2m^2$ is an integer with just the information we have, and thus we cannot make our final conclusion.

Of course, depending on the problem, you may have *multiple* step 3s and step 4s. You may need to make multiple adjustments and you may need to have multiple insights that fit together nicely. What I'm saying is not all direct proofs are this simple, but *they are still direct*. Your proof may be much more complex, but the steps I've outlined are broad classifications of what you'll be doing.

What's left is step 5. You would very often see proofs omit this step and just stop at $n^2 = 2m'$ but I've left it in for clarity. In step 5, I take my conclusion $n^2 = 2m'$, and I write it in a way that looks more or less like the definition. I'm assuring myself that yes, there *is* an integer $m'$ for which $n^2 = 2m'$. And by definition, whenever that happens, I can say $n^2$ is even.

---

The overarching goal of this doc specifically was to introduce you to how definitions work and the overall structure of direct proofs. There are a lot more logical nuances to this discussion, but I'm omitting them at the risk of infodumpimg. We will cover them slowly over these notes, but I'm not guaranteeing self-sufficiency.

Read the simple 5 line proof again and again and really try to grasp what is going on. In the next doc, I'll point out a logical nuance in this proof and tackle a canonical example in real analysis - that the limit of a sum sequence is the sum of individual limits.

</span>