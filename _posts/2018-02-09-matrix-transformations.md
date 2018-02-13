---
layout: post
title: "Matrix Transformations"
date: 2018-02-09
use_math: true
---

These notes are taken from [Khan Academy](https://www.khanacademy.org/math/linear-algebra/matrix-transformations#linear-transformations).


## Functions and linear transformations

### A more formal understanding of functions

Range is the subset of co-domain that the function actually maps to.

\begin{align} 
\label{a}
f : X 
\rightarrow 
Y
\end{align}
The equation \ref{a} implies that set $X$ is domain, set $Y$ is co-domain, and set $Y$ is the range.

\begin{align} 
\label{f}
f : \mathbb{R} 
\rightarrow 
\mathbb{R}
\end{align}
The equation \ref{f} implies that $\mathbb{R}$ is domain, $\mathbb{R}$ is co-domain, and $\mathbb{R}$ is the range.

\begin{align} 
\label{b}
f(x)
=
x^2
\end{align}
The equation \ref{b} implies that $x$ is domain, $x^2$ is co-domain, and $x^2$ is the range.


\begin{align} 
\label{g}
f:\mathbb{R^2} \rightarrow \mathbb{R}
\end{align}
The equation \ref{g} implies that $\mathbb{R^2}$ is domain, $\mathbb{R}$ is co-domain, and $\mathbb{R}$ is the range.

\begin{align} 
\label{c}
g(x_1, x_2) 
= 
2
\end{align}
The equation  \ref{c} implies that $x_1, x_2$ is domain, $2$ is co-domain, and $2$ is the range.

\begin{align} 
\label{d}
h(x_1, x_2) 
= 
(x_1 + x_2, x_2 - x_1, x_2x_1)
\end{align}
The equation \ref{d} implies that $(x_1, x_2)$ is domain, $(x_1 + x_2, x_2 - x_1, x_2x_1)$ is co-domain, and $(x_1 + x_2, x_2 - x_1, x_2x_1)$ is the range.

If $x_1 = 2$ and $x_2 = 3$, then
\begin{align} 
\label{e}
h(2, 3) = (5, 1, 6)
\end{align}
The equation \ref{e} implies that $(2, 3)$ is domain, $(5, 1, 6)$ is co-domain, and $(5, 1, 6)$ is the range.

### Vector transformations

Vectors are members of some set.

\begin{align} 
\label{h}
f:X \rightarrow Y
\end{align}
The equation \ref{h} implies that set $X$ is mapped to set $Y$.


\begin{align} \label{i}
\vec{x} \in \mathbb{R}^n
\end{align}
The equation \ref{i} explains that $\vec{x}$ belongs to $n$-dimensional real coordinate space. 

\begin{align} \label{j}
f : \mathbb{R}^n
\rightarrow
\mathbb{R}^m
\end{align}
The equation \ref{j} states that $n$-dimensional real coordinate space is mapped to $m$-dimensional real coordinate space. A regular arrow represents a set is being represented by another set. Also, it means that vectors are valid elements of sets.

\begin{align} 
\label{k}
f : x
\mapsto
x^2
\end{align}
The equation \ref{k} states that $x$ is mapped to $x^2$. An arrow with vertical line represents a function definition. Also, it means that functions are mapping between elements of sets. Thus, we can have functions of vectors.

\begin{align} 
\label{l}
f : (x_1, x_2, x_3)
=
(x_1 + 2x_2, 3x_3)
\end{align}
The equation \ref{l} can be represented by equation \ref{m}.

\begin{align} 
\label{m}
f : \mathbb{R}^3
\rightarrow
\mathbb{R}^2
\end{align}
The equation \ref{m} means that 3-dimensional real coordinate space is mapped to 2-dimensional real coordinate space.

\begin{align} 
\label{n}
f :
\begin{pmatrix}
\begin{bmatrix}
x_1 \\\
x_2 \\\
x_3
\end{bmatrix}
\end{pmatrix}
=
\begin{bmatrix}
x_1 + 2x_2 \\\
3x_3
\end{bmatrix}
\end{align}
The equation \ref{n} shows another representation of equation \ref{k}.

## Linear transformation examples

To be continued...

## Transformations and matrix multiplication

To be continued...

## Inverse functions and transformations

To be continued...

## Finding inverses and determinants

To be continued...

## More determinant depth

To be continued...

## Transpose of a matrix

To be continued...

