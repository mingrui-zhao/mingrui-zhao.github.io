---
layout: post
title: Getting familiar with mathematical abstraction
date: 2024-07-24
description: a quick exercise to know math
tags: math
categories: math-tutorial
related_posts: false
---

When I started university math courses, I quickly realized that high school only reveals a small part of Mathematics. During my high school years, I considered myself "good" at math, excelling at number crunching, vector calculations, and function integrations and differentiations. However, I soon understood that these skills are merely tools that anyone can master or let computers handle. The true essence of Mathematics lies in abstraction—the ability to rigorously think, approach, and solve problems.

In my third year of university, I decided to pursue a double degree in Mathematical Sciences, which was quite overwhelming. I enjoyed math but struggled to excel, believing that others were more naturally gifted and destined to succeed. Reflecting on my undergraduate years, I now realize that while there are indeed gifted individuals, the majority of those who excel in math are the ones who grasp the essence of mathematical thinking early and commit to practicing it. As I move toward graduate school, I have come to appreciate the importance of mathematical thinking even more. If I could redo my math undergraduate years, I'd really hope someone could explain how the world of math changes at higher levels. Here, I believe one simple math question can reveal some of the beauty of mathematics.
## Prove $$\sqrt{2}$$ is irrational

Before I became familiar with mathematical thinking, I might have attempted to prove this statement as follows (and that's exactly how I did my first term math assignments):

1. Consider some examples of irrational numbers, such as $$pi$$ and $$\sqrt{5}$$.
2. Identify their common properties, such as having non-repeating, never-ending decimal digits.
3. Try to show that $$\sqrt{2}$$ follows a similar pattern by calculating its digits and observing the lack of a repeating pattern.

While this approach might convince oneself, it is insufficient to convince others. It is impossible to list all decimal digits of $$\sqrt{2}$$
  to prove its irrationality. Instead, I will present a cohesive proof and hope to illustrate the elegance of mathematical thinking.

### Proof by Contradiction: Suppose $$\sqrt{2}$$ is rational.
**Definition:A real number $$n$$ is rational if it can be written as $$p/q$$ with for integer $$p,q$$ and $$p,q$$ co-prime.**

Suppose $$\sqrt{2}$$ is rational, then $$\sqrt{2}=\frac{p}{q}$$ for some $$p,q\in \mathbb{N}$$

Squaring both end, we get
\begin{equation}
2 = \frac{p^2}{q^2}
\end{equation}

Thus
\begin{equation}
p^2 = 2q^2
\end{equation}

Now, we see $$p^2$$ must be an even number, as there is a $$2$$ on the right hand side. If $$p^2$$ is an even square, what does it imply on $$p$$? 

If $$p$$ is odd, let $$p=2x+1$$ for some integer $$x$$, then 

$$p^2=4x^2+4x+1$$ 

which is even+even+odd=odd. 

Therefore, an odd $$p$$ can not lead to an even $$p^2$$, so $$p$$ must be even (Try forward prove this property - an even $$p$$ lead to an even square).

Here we proved

**Lemma: If $$p^2$$ is even, then $$p$$ is also even**.

Since $$p$$ is even, let $$p=2y$$ for some integer $$y$$. Then $$p^2=4y^2$$ and $$q^2=\frac{1}{2}p^2=2y^2$$.

Immediately we see that this implies $$q^2$$ is an even number, and hence by the Lemma $$q$$ is even.

The overall proof lead to the statement that both $$p,q$$ are even, so they can not be co-prime, violating the definition of a rational number. 

A contradiction is found, thus $$\sqrt{2}$$ is irrational.

## Takeaways
I hope this simple exercise can be a good demo of how mathematical proof works -- a playground with sole logics and derivations. Though it is only an entry-level math problem, it has provided me a lot of insights in dealing other math problems -- mentality-wise. The important part is not how we acknowledged tha irrationality of $$\sqrt{2}$$, but how we come up with the idea of proof by contradiction, work around the definition and to proceed with thinking of parity properties. If you have not done this before, it is not easy as it looks. Try proving $$\sqrt{5}$$ is irrational for fun!