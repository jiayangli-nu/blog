---
layout: post
title: Variational Inequality Theory
---

In 1966, variational inequality (VI) was first proposed as a tool in the study of partial differential equations. Subsequently, researchers began to realize that it could also be a powerful tool for various problems in operations research, economics and also engineering. When I started to learn about it, I thought this topic was a little bit outdated. However, after looking deep into VI, I found that it still could be a powerful tool for my research. Meanwhile, recent advances in machine learning could also help us understand more about VI. Therefore, I decided to write this blog to provide a documentation and unification of some fundamental concepts about VI. Specifically, we will mainly focus on the following questions.

1. What kinds of problems can be formulated as VI?
2. How to find the solution to a VI problem?
3. How to differentiate through a VI problem?

This outline is generally in line with most classic textbooks. The primary goal of this post is to provide a  



{: class="table-of-content"}
* TOC
{:toc}


## 1. What is VI?

Given a set $$\mathcal{Z} \subseteq \mathbb R^n$$ and a function $$F: \mathcal{Z} \to \mathbb R^n$$, a VI problem $$(F, \mathcal{Z})$$ is to find $$z^* \in \mathcal{Z}$$ such that

$$
    \left< F(z^*),  z - z^*  \right> \geq 0, \quad \text{for all}~z \in \mathcal{Z}.
$$



### VI and Optimization
### VI and Game Theory


## 2. Algorithm
