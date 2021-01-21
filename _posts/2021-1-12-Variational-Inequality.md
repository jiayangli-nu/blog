---
layout: post
title: Variational Inequality
---

***Classcial Results and New Insights***


**Variational inequality** (VI) was first proposed as a tool to study partial differential equations in the 1960s. Subsequently, researchers began to realize that it could also be a powerful tool for various problems in operations research, economics and engineering.

Actually, when I started to learn about it, I thought this topic was a little bit outdated. However, after looking deep into VI, I realized it still could be a powerful tool for my research. Meanwhile, recent advances in machine learning could also help us understand more about VI. Therefore, I decided to write this blog to provide a documentation and unification of some fundamental concepts about VI. Specifically, we will mainly focus on the following questions.

1. **Formulation**: What is VI?
2. **Algorithm**: How to solive it?
3. **Differentiation**: How to differentiate through it?

This outline is in line with some classic textbooks, while I also want to add some new materials besides those classical results in the textbooks, especially how VI is related to today's research topic.


{: class="table-of-content"}
* TOC
{:toc}


## 1. Formulation

Given a set $$\mathcal{X} \subseteq \mathbb R^n$$ and a function $$F: \mathcal{X} \to \mathbb R^n$$, a (finite-dimensional) VI problem $$(F, \mathcal{X})$$ is to find $$x^* \in \mathcal{X}$$ such that

$$
    \left< F(x^*),  x - x^*  \right> \geq 0, \quad \forall~x \in \mathcal{X}.
    \tag{1}
$$

Before further introducing any properties of VI, I think it would be better to first have some examples. 

### VI and Optimization

Given a set $$\mathcal{X} \subseteq \mathbb R^n$$ and a differentiable function $$f: \mathcal{X} \to \mathbb R$$. Consider the following optimization problem $$(f, \mathcal{X})$$:

$$
\begin{aligned}
	\min_{x \in \mathcal{X}}~~&f(x) \\
	\text{s.t.}~~&x \in \mathcal{X}
\end{aligned}
\tag{2}
$$

First, let's review the concepts of **feasible direction** and **descent direction**. At a feasible point $$\bar{x} \in \mathcal{X}$$,

* The cone of feasible directions $$\mathcal{F}_{\bar{x}}$$ is defined as

$$\left{d \neq 0: f(\bar{x} + \tau d) \in \mathcal{X}, \quad \forall \tau \in [0, \bar{\tau}] \right}$$

* The cone of descent direction $$\mathcal{D}_{\bar{x}}$$ is defined as

$$\left{d \neq 0: f(\bar{x} + \tau d) < f(\bar{x}), \quad \forall \tau \in [0, \bar{\tau}]\right}$$

If $x^*$ is a local minimizer of $(2)$,

**Proposition**: If $$\mathcal{X}$$ is convex, any local minimizer $$x^*$$ of an optimization problem $$(f, \mathcal{X})$$ is a solution to a VI problem $$(\nabla f, \mathcal{X})$$.



### VI and Game Theory


## 2. Algorithm

## 3. Differentiation
