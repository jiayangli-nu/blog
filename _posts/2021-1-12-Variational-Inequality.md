---
layout: post
title: Variational Inequality Theory
---

Variational inequality (VI) was first proposed as a tool to study partial differential equations in the 1960s. Subsequently, researchers began to realize that it could also be a powerful tool for various problems in operations research, economics and engineering.

Actually, when I started to learn about it, I thought this topic was a little bit outdated. However, after looking deep into VI, I realized it still could be a powerful tool for my research. Meanwhile, recent advances in machine learning could also help us understand more about VI. Therefore, I decided to write this blog to provide a documentation and unification of some fundamental concepts about VI. Specifically, we will mainly focus on the following questions.

1. What is VI?
2. How to solive it?
3. How to differentiate through it?

This outline is in line with some classic textbooks, while I also want to add some new materials besides those well-known results in the textbooks, especially how VI is related to today's research topic.



{: class="table-of-content"}
* TOC
{:toc}


## 1. What is VI?

Given a set $$\mathcal{X} \subseteq \mathbb R^n$$ and a function $$F: \mathcal{X} \to \mathbb R^n$$, a (finite-dimensional) VI problem $$(F, \mathcal{X})$$ is to find $$x^* \in \mathcal{X}$$ such that

$$
    \left< F(x^*),  x - x^*  \right> \geq 0, \quad \forall~x \in \mathcal{X}.
$$

Before introducing any properties of VI, I think it would be better to first have some examples. 

### VI and Optimization

The first example is that optimization problems can be naturally fomulated as VI problems. Let's consider the following problem:

$$
\begin{aligned}
	\min_{x \in \mathcal{X}}~~&f(x) \\
	\text{s.t.}~~&x \in \mathcal{X}
\end{aligned}
$$



### VI and Game Theory


## 2. Algorithm
