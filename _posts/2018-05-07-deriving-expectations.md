---
layout: post
title: "Deriving expectations"
date: 2018-05-07
use_math: true
---

Using mathematical equations, show that for a random variable $X$ with variance $Var(X)$, 

$Var(X) = \left<X^2\right> - \left<X\right>^2$.

This is my solution.

Using $E()$ instead of $\left< \right>$:

$Var(X) = E[(X + E(X))^2]$

$Var(X) = E[X^2 -2E(X)X + E(X)^2]$

$Var(X) = E(X^2) -2E(X)E(X) + E(X)^2$

$Var(X) = E(X^2) -2E(X)^2 + E(X)^2$

$Var(X) = E(X^2) -E(X)^2$

Thus,

$Var(X) = \left<X^2\right> - \left<X\right>^2$
