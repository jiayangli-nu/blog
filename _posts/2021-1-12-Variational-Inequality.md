---
layout: post
title: Variational Inequality Theory
---

Variational inequality (VI) theory was first introduced in the study of partial differential equations (PDE) in 1966. In the past decades, researchers unveiled that it could be a powerful tool for the study of problems in operations research, economics and also engineering. When I started to learn about it, I thought this topic was a little bit outdated. But after looking deep into VI, I realized that it could still be extremely useful in today's research on game theory and machine learning. Therefore, I decided to write this blog post to provide a documentation and unification of some fundamental concepts in VI theory. Specifically, we will mainly focus on the following questions.

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
