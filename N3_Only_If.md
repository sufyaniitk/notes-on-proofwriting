<span style='font-family: Calibri serif'>

## 3 - 'If and only if' statements

</span>

---

<span style='font-family: Bahnschrift'>

This discussion will be less analysing a proof, more talking about a class of problems and a brief glance into mathematical logic.

---

You have already encountered mathematical reasoning, probably in the form of Boolean Algebra - how to negate expressions, how to take conjunctions (AND) and disjunctions (OR), de Morgan's laws, distributing a connective over another, etc.

The very same operations can be done for mathematical statements. A mathematical statement is any statement that can be assigned a value of `True` or `False`. This value may depend on your initial assumptions. In fact, a theorem in Mathematical Logic tells us that if we begin with a set of statements each assigned a value, and consider all statements that can be constructed by repeatedly appending `AND` and `NOT` to the original set, the value of each of these statements is non-ambiguous. i.e, it can be determined uniquely from the values of the original statements.

This may seem inconsequential, and for the most part obvious, but it has bizarre consequences when applied to some exotic statements. For example, accepting the Axiom of Choice leads to the Banach-Tarski paradox; rejecting it leads to a vector space with 2 basis sets of differing cardinalities. In fact, without choice, we cannot even assign every set a cardinality.

All of this was unnecessary discourse to pique your interests and get your mind geared toward logic. What I want to talk about is 'if and only if' statements. You may have encountered the term in some problems, asking you to prove something happens if and only if (or iff) something else happens.

---

The term I prefer is 'logically equivalent'. i.e., as far as your building blocks are concerned, two logically equivalent statements are virtually indistinguishable. If one of them is true, the other must be so. If one of them is false, the other must be so.

That covers the definition - statements that are true together and false together. Intuitively, it doesn't matter what information you're given. If you're given any one of them, you can immediately conclude the other.

Compare this to an implication. Given a statement $p \implies q$, and if you're given the statement $p$, then you can immediately conclude $q$, but not vice versa. Similarly, if you're given $\neg q$ (ie, $q$ did not happen) then you can conclude $\neg p$ (indeed, $p$ could not have happened, otherwise $q$ would have happened), but again, not vice versa.

In case of logical equivalence, given either, I can conclude the other. Given the negation of either, I can conclude the negation of the other. That is to say, $p \implies q$ and $q \implies p$ both hold.


This gives us two things - a shorthand $p \iff q$ for logical equivalence, and a way of proving it. To show two statements are logically equivalent, it suffices to show they imply each other.

As a matter of fact, you use equivalent statements all the time! A few examples I can think of off the top of my head:

- A matrix has an inverse and it has a nonzero determinant
- A triangle is equiangular and it is equilateral
- A triangle is right-angled and it satisfies the Pythagorean Theorem
- An integer is even, and the square of that integer is even
- A matrix is invertible and it has a unique solution for every corresponding system of equations

You have encountered, and used, these logical equivalences *multiple* times. If any one statement holds, its analogue does. If any one statement fails, its analogue does. We will spend time proving a few of these and looking at some techniques in the process.

---

The term 'if and only if' comes from a recognition of sufficient and necessary conditions.

Suppose the implication $p \implies q$ holds. Then I can say $q$ happens if $p$ happens, and it should make sense to you. Here, we call $p$ a *sufficient* condition for $q$ to happen. i.e, $p$ can 'trigger' $q$ so to say. However, $q$ may have other triggers - so it is not necessary that if $q$ happens $p$ must have happened. Say, if it rains, the ground is wet. But if the ground is wet, it could be from a pipe burst.

However, I can *also* say that $p$ happens **only if** $q$ happens - i.e., if $\neg q$ happens, $p$ cannot happen at all. In this case we call $q$ a *necessary* condition for $p$ to happen - i.e, $q$ must happen for $p$ to happen, but it doesn't guarantee that $p$ will happen. i.e, if the ground is not wet, it is not possible that it has rained. But again, if the ground is wet, you can't conclude that it has rained.

In case of logical equivalences, both conditions are sufficient and necessary for each other. They happen *if and only if* the other happens.

---

This was content you should otherwise be familiar with. I put this in to get you into gear for the next discussion, where we will look at a new proving technique.

And I'll do something weird - I'll "prove" a proving technique, but without making it complicated.

Make sure you know most of what's going on here. If not, take a refresher on logic. My personal favorite suggestion is the first chapter from Goodaire and Parmenter's text, *Discrete Mathematics with Graph Theory*.

</span>