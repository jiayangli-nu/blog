---
layout: post
title: Variational Inequality
---

***Classcial Results and New Insights***


**Variational inequality** (VI) was first proposed as a tool to study partial differential equations in the 1960s. Subsequently, researchers began to realize that it could also be a powerful tool for various problems in operations research, economics and engineering.

Actually, when I started to learn about it, I thought this topic was a little bit outdated. However, after looking deep into VI, I realized it still could be a powerful tool for my research. Meanwhile, recent advances in machine learning could also help us understand more about VI. Therefore, I decided to write this blog to provide a documentation and unification of some fundamental concepts about VI. Specifically, we will mainly focus on the following questions.

1. **Formulation**: What is VI?
2. **Algorithm**: How to solive it?
3. **Differentiability**: How to differentiate through it?

This outline is in line with some classic textbooks, while I also want to add some new materials besides those classical results in the textbooks, especially how VI is related to today's research topic.


{: class="table-of-content"}
* TOC
{:toc}


## 1. Formulation

Given a set $$\mathcal{X} \subseteq \mathbb R^n$$ and a function $$F: \mathcal{X} \to \mathbb R^n$$, a (finite-dimensional) VI problem $$(F, \mathcal{X})$$ is to find $$x^* \in \mathcal{X}$$ such that

$$
    \left< F(x^*),  x - x^*  \right> \geq 0, \quad \forall~x \in \mathcal{X}.
    \tag{1}
    \label{eq:1}
$$

Before further introducing any properties of VI, I think it would be better to first have some examples. 

### VI and Optimization

Given a set $$\mathcal{X} \subseteq \mathbb R^n$$ and a *continuously differentiable* function $$f: \mathcal{X} \to \mathbb R$$. Consider the following optimization problem $$(f, \mathcal{X})$$:

$$
\begin{aligned}
	\min_{x \in \mathcal{X}}~~&f(x) \\
	\text{s.t.}~~&x \in \mathcal{X}
\end{aligned}
\tag{2}
\label{eq:2}
$$

First, let's review the concepts of **feasible direction** and **descent direction**. At a feasible point $$\bar{x} \in \mathcal{X}$$,

* A vector $$d \in \mathbb R^n$$, $$d \neq 0$$ is a feasible direction, if there exists $$\bar{\tau} > 0$$, s.t.

$$f(\bar{x} + \tau d) \in \mathcal{X}, \quad \forall \tau \in [0, \bar{\tau}].$$

* A vector $$d \in \mathbb R^n$$, $$d \neq 0$$ is a descent direction, if there exists $$\bar{\tau} > 0$$, s.t.

$$f(\bar{x} + \tau d) < f(\bar{x}), \quad \forall \tau \in [0, \bar{\tau}].$$

Using these concepts, we can directly formulate an optimziation problem to a VI problem when $$\mathcal{X}$$ is convex.

**Proposition 1.1**: If $$\mathcal{X}$$ is convex, any local minimizer $$x^*$$ of the optimization problem $$(f, \mathcal{X})$$ is a solution to a VI problem $$(\nabla f, \mathcal{X})$$.

***Proof.*** Since $$\mathcal{X}$$ is convex, the cone of feasible directions at $$x^*$$ is 

$$\mathcal{F}_{x^*} = \left\{d = x - x^*, x \in \mathcal{X} \right\}.$$

Since $$f$$ is continuously differentiable, the cone of descent directions at $$x^*$$ is  (<span style="color:red">Here the continuity of $$\nabla f$$ is important!</span>)

$$\mathcal{D}_{x^*} = \left\{d = x - x^*, \left<\nabla f(x^*), x - x^* \right> < 0 \right\}.$$


If $$x^*$$ is a local minimizer, then $$\mathcal{F}_{x^*} \cap \mathcal{D}_{x^*} = \emptyset$$, or equivalently

$$\left<\nabla f(x^*), x - x^*\right> \geq 0, \forall x \in \mathcal{X},$$

i.e. every feasible direction is not a descent direction. $$\blacksquare$$

The converse is also true when $$f$$ is convex on $$\mathcal{X}$$. 

**Proposition 1.2**: If $$f$$ is convex, any solution $$x^*$$ to the VI problem $$(\nabla f, \mathcal{X})$$ is a global minimizer of the optimization problem $$(f, \mathcal{X})$$.

***Proof.*** Since $$f$$ is convex, 

$$f(x) \geq f(x^*) + \left<\nabla f(x^*), x - x^*\right> \geq f(x^*), \quad \forall x \in \mathcal{X}. \blacksquare $$

These two propositions establish the equivalence between VI and convex optimization. 

**Comment.** Formulating an optimization problem as a VI problem is extremly straightforward. However, one may ask: why bother? We already know almost everything about convex optimization. So, let's move to the next part to see why VI is useful.



### VI and Nash Equilibrium

Consider a game $$(\mathcal N, \mathcal{A}, u)$$ played by a set of agents $$\mathcal N$$, where each agent $$i \in \mathcal N$$ selects an *action* $$a_i \in \mathcal A_i$$ to minimize its disutility and each player's disutility is determined by a function

$$u_i: \mathcal A = \prod_{i \in \mathcal N} \mathcal{A}_i\to \mathbb R$$.

The outcome of a game can be predicted by its **Nash equilibrium**. Can VI become a powerful tool to analyze Nash equilibrium? Let's see some examples.

**Example 1.1 (Continuous Game)** When the action set $$\mathcal{A}_i$$ is continuous for all $$i$$, we call it a continuous game. If agents play pure strategies to minimize their disutilities, $$a^* \in \mathcal A$$ is a Nash equilibrium if

$$
    u_i(a_i^*, a_{-i}^*) = \min_{a_i \in \mathcal{A}_i} u_i(a_i, a_{-i}^*), \quad \forall i \in \mathcal{N}.
$$

We also assume that $$u_i$$ is continuously differentiable and write $$v_i(a) = \nabla_{a_i} u_i(a)$$.
Specifically, if $$\mathcal{A}_i$$ is closed and convex for all $$i$$, then a Nash equilibrium $$a^*$$ is the solution to 


The converse also holds if for all $$i \in \mathcal{N}$$, $$u_i$$ is convex in $$a_i$$ for all $$a_{-i} \in \prod_{j \neq i} \mathcal{A}_j$$.

**Example 1.2 (Finite Game)**

**Example 1.3 (Population Game)**



### VI and Reinforcement Learning

### Fixed-Point Formulation


## 2. Algorithm

## 3. Differentiability
