---
layout: post
title: VI: Classical Results and New Insights
---

**Variational inequality** (VI) was first proposed as a tool to study partial differential equations in the 1960s. Subsequently, researchers began to realize that it could also be a powerful tool for various problems in operations research, economics and engineering.

Actually, when I started to learn about it, I thought this topic was a little bit outdated. However, after looking deep into VI, I realized it still could be a powerful tool for my research. Meanwhile, recent advances in machine learning could also help us understand more about VI. Therefore, I decided to write this blog to provide a documentation and unification of some fundamental concepts about VI. Specifically, we will mainly focus on the following questions.

1. **Formulation**: What is VI?
2. **Algorithm**: How to solive it?
3. **Differentiability**: How to differentiate through it?

This outline is in line with some classic textbooks, while I also want to add some new materials besides those classical results in the textbooks, especially how VI is related to today's research topic.


{: class="table-of-content"}
* TOC
{:toc}


## 1. What is VI?

Given a set $$\mathcal{X} \subseteq \mathbb R^n$$ and a function $$F: \mathcal{X} \to \mathbb R^n$$, a (finite-dimensional) VI problem $$(F, \mathcal{X})$$ is to find $$x^* \in \mathcal{X}$$ such that

$$
    \left< F(x^*),  x - x^*  \right> \geq 0, \quad \forall~x \in \mathcal{X}.
$$

Before further introducing any properties of VI, I think it would be better to first have some examples. 

### VI and Optimization

Given a set $$\mathcal{X} \subseteq \mathbb R^n$$ and a differentiable function $$f: \mathcal{X} \to \mathbb R$$. Consider the following optimization problem:

$$
\begin{aligned}
	\min_{x \in \mathcal{X}}~~&f(x) \\
	\text{s.t.}~~&x \in \mathcal{X}
\end{aligned}
$$

First, let's review the concepts of **feasible direction** and **descent direction**. At a feasible point $$\bar{x} \in \mathcal{X}$$,

* A vector $$d$$ is a feasible direction, if there exists a scalar $$\bar{\tau}$$ such that $$f(\bar{x} + \tau d) < f(\bar{x})$$
* If

**Proposition**: If $$\mathcal{X}$$ is



### VI and Game Theory


## 2. How to solve it?

## 3. How to differentiate through it?
