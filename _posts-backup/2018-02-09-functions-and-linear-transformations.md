---
layout: post
title: "Functions and linear transformations"
date: 2018-02-09
use_math: true
---

These notes are taken from [Khan Academy's Matrix Transformations: Functions and Linear Transformations](https://www.khanacademy.org/math/linear-algebra/matrix-transformations#linear-transformations).

## A more formal understanding of functions

Range is the subset of co-domain that the function actually maps to.

\begin{align} \label{1}
	f : X \rightarrow Y
\end{align}
The equation \ref{1} implies that set $$X$$ is domain, set $$Y$$ is co-domain, and set $Y$ is the range.

\begin{align} \label{2}
f : \mathbb{R} \rightarrow \mathbb{R}
\end{align}
The equation \ref{2} implies that $$\mathbb{R}$$ is domain, $\mathbb{R}$ is co-domain, and $\mathbb{R}$ is the range.

\begin{align} \label{3}
	f(x) =x^2
\end{align}
The equation \ref{3} implies that $$x$$ is domain, $$x^2$$ is co-domain, and $$x^2$$ is the range.


\begin{align} \label{4}
	f:\mathbb{R^2} \rightarrow \mathbb{R}
\end{align}
The equation \ref{4} implies that $$\mathbb{R^2}$$ is domain, $$\mathbb{R}$$ is co-domain, and $$\mathbb{R}$$ is the range.

\begin{align} \label{5}
	g(x_1, x_2) = 2
\end{align}
The equation  \ref{5} implies that $$(x_1, x_2)$$ is domain, $$2$$ is co-domain, and $$2$$ is the range.

\begin{align} \label{6}
	h(x_1, x_2) = (x_1 + x_2, x_2 - x_1, x_2x_1)
\end{align}
The equation \ref{6} implies that $$(x_1, x_2)$$ is domain, $$(x_1 + x_2, x_2 - x_1, x_2x_1)$$ is co-domain, and $$(x_1 + x_2, x_2 - x_1, x_2x_1)$$ is the range.

If $$x_1 = 2$ and $x_2 = 3$$, then

\begin{align} \label{7}
	h(2, 3) = (5, 1, 6)
\end{align}
The equation \ref{7} implies that $$(2, 3)$$ is domain, $$(5, 1, 6)$$ is co-domain, and $$(5, 1, 6)$$ is the range.

## Vector transformations

Vectors are members of some set.

\begin{align} \label{8}
	f:X \rightarrow Y
\end{align}
The equation \ref{8} implies that set $$X$$ is mapped to set $$Y$$.

\begin{align} \label{9}
	\vec{x} \in \mathbb{R}^n
\end{align}
The equation \ref{9} explains that $$\vec{x}$$ belongs to $$n$$-dimensional real coordinate space. 

\begin{align} \label{10}
	f : \mathbb{R}^n \rightarrow \mathbb{R}^m
\end{align}
The equation \ref{10} states that $$n$$-dimensional real coordinate space is mapped to $$m$$-dimensional real coordinate space. A regular arrow represents a set is being represented by another set. Also, it means that vectors are valid elements of sets.

\begin{align} \label{11}
	f : x \mapsto x^2
\end{align}
The equation \ref{11} states that $$x$$ is mapped to $$x^2$$. An arrow with vertical line represents a function definition. Also, it means that functions are mapping between elements of sets. Thus, we can have functions of vectors.

\begin{align} \label{12}
	f : (x_1, x_2, x_3) = (x_1 + 2x_2, 3x_3)
\end{align}
The equation \ref{12} can be represented by equation \ref{11}.

\begin{align} \label{13}
	f : \mathbb{R}^3 \rightarrow \mathbb{R}^2
\end{align}
The equation \ref{13} means that three-dimensional real coordinate space is mapped to two-dimensional real coordinate space.

\begin{align} \label{14}
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
The equation \ref{14} shows another representation of equation \ref{13}.


Transformation is a function operating on vectors. It is called transformation because we are transforming one vector to another.

\begin{align} \label{15}
	T : \mathbb{R}^3 \rightarrow \mathbb{R}^2
\end{align}
The equation \ref{15} means that three-dimensional real coordinate space is transformed to two-dimensional real coordinate space.

\begin{align} \label{16}
	T : (x_1, x_2, x_3) \rightarrow (x_1 + 2x_2, 3x_3)
\end{align}
The equation \ref{16} means that $$(x_1, x_2, x_3)$$ is transformed into $$(x_1 + 2x_2, 3x_3)$$.

## Linear transformations

\begin{align} \label{17}
	\vec{a}, \vec{b} \in \mathbb{R}^n
\end{align}

\begin{align} \label{18}
	T(\vec{a} + \vec{b}) = T(\vec{a}) + T(\vec{b})
\end{align}

\begin{align} \label{19}
	T(c\vec{a}) = c T(\vec{a})
\end{align}

The equations \ref{17}, \ref{18}, and \ref{19} support the basis of linear transformation.

\begin{align} \label{20}
	T:\mathbb{R}^2 \rightarrow \mathbb{R}^2
\end{align}

\begin{align} \label{21}
	T(x_1, x_2) = T(x_1 + x_2, 3x_1)
\end{align}

\begin{align} \label{22}
	T 
	\begin{pmatrix} 
		\begin{bmatrix}
			x_1 \\\
			x_2
		\end{bmatrix} 
	\end{pmatrix} 
	= 
	\begin{bmatrix}
		x_1 + x_2 \\\
		3x_1
	\end{bmatrix} 
\end{align}

\begin{align} \label{23}
	T: 
	\begin{pmatrix} 
		\begin{bmatrix}
			x_1 \\\
			x_2
		\end{bmatrix} 
	\end{pmatrix} 
	\mapsto 
	\begin{bmatrix}
		x_1 + x_2 \\\
		3x_1
	\end{bmatrix} 
\end{align}

The equations \ref{20}, \ref{21}, \ref{22}, and \ref{23} support the linear transformation from two-dimensional real coordinate space to two-dimensional real coordinate space.

\begin{align} \label{24}
	\vec{a} = 
	\begin{bmatrix}
		a_1 \\\
		a_2
	\end{bmatrix}
	, \vec{b} = 
	\begin{bmatrix}
		b_1 \\\
		b_2
	\end{bmatrix} 
\end{align}

\begin{align} \label{25}
	\vec{a} + \vec{b} = 
	\begin{bmatrix}
		a_1 + b_1 \\\
		a_2 + b_2
	\end{bmatrix} 
\end{align}

\begin{align} \label{26}
	T(\vec{a} + \vec{b}) = T 
	\begin{pmatrix} 
		\begin{bmatrix}
			a_1 + b_1 \\\
			a_2 + b_2
		\end{bmatrix} 
	\end{pmatrix} 
	= 
	\begin{bmatrix}
		a_1 + a_2 + b_1 + b_2 \\\
		3a_1 + 3b_2
	\end{bmatrix} 
\end{align}

The equations \ref{24}, \ref{25}, and \ref{26} support linear transformation. The equation \ref{26} is the transformed equation by sustituting \ref{24} to equation \ref{17} and left side of equation \ref{18}. 

Likewise,

\begin{align} \label{27}
	T(\vec{a}) = 
	\begin{pmatrix} 
		\begin{bmatrix}
			a_1 \\\
			a_2
		\end{bmatrix} 
	\end{pmatrix} 
	= 
	\begin{bmatrix}
		a_1 + a_2 \\\
		3a_1
	\end{bmatrix} 
\end{align}

\begin{align} \label{28}
	T(\vec{b}) = 
	\begin{pmatrix} 
		\begin{bmatrix}
			b_1 \\\
			b_2
		\end{bmatrix} 
	\end{pmatrix} 
	= 
	\begin{bmatrix}
		b_1 + b_2 \\\
		3b_1
	\end{bmatrix} 
\end{align}

\begin{align} \label{29}
	T(\vec{a}) + T(\vec{b}) = 
	\begin{bmatrix}
		a_1 + a_2 + b_1 + b_2 \\\
		3a_1 + 3b_1
	\end{bmatrix} 
\end{align}

The equations \ref{27}, \ref{28}, and \ref{29} demonstrate linear transformation. The equation \ref{29} is the transformed equation by sustituting \ref{27} and \ref{28} to right side of equation \ref{18}. It shows that equation \ref{29} is the same as equation \ref{26}.


Also,

\begin{align} \label{30}
	c(\vec{a}) =
	\begin{bmatrix}
		ca_1 \\\
		ca_2
	\end{bmatrix}
\end{align}

\begin{align} \label{31}
	T(c\vec{a}) = T 
	\begin{pmatrix}
		\begin{bmatrix}
			ca_1 + ca_2 \\\
			3ca_1
		\end{bmatrix}
	\end{pmatrix} 
	= c 
	\begin{bmatrix}
		a_1 + a_2 \\\
		a_1
	\end{bmatrix}
\end{align}

The equations \ref{30} and \ref{31} demonstrate proof of equation \ref{19}.

Therefore, equation \ref{21} is a linear transformation or LT.

\begin{align} \label{32}
	T \begin{pmatrix}
		\begin{bmatrix}
			x_1 \\\
			x_2
		\end{bmatrix}
	\end{pmatrix}
	= c 
	\begin{bmatrix}
		x_1^2 \\\
		0
	\end{bmatrix}
\end{align}

\begin{align} \label{33}
	T(c\vec{a}) \neq c^2 T(\vec{a})
\end{align}

The equation \ref{32} is not a linear transformation because it results to equation \ref{33}.


## Visualizing linear transformations

The word "transformation" can be best visualized by imagining that the line can be stretched, compressed, or rotated like a spring or slinky.

\begin{align} \label{34}
	f(x + y) = f(x) + f(y)
\end{align}

\begin{align} \label{35}
	f(cx) = cf(x)
\end{align}

A linear transform is a function $$f(x)$$ that satisfies two properties: \ref{33} and \ref{34}, where $$f$$ is a function of vectors.

A two-dimensional linear transformation is a special kind of function which takes in a two-dimensional vector $$\begin{bmatrix} x \\ y \end{bmatrix}$$ and outputs another two-dimensional vector.

\begin{align} \label{36}
	f(\textbf{v} + \textbf{w}) = f(\textbf{v}) + f(\textbf{w})
\end{align}

\begin{align} \label{37}
	f(c\textbf{v}) = cf(\textbf{v})
\end{align}

A linear transformation is two-dimensional if it satisfies two properties: \ref{36} and \ref{37}, where $$\textbf{v}$$ and $$\textbf{w}$$ are vectors.

A transformation is linear if it follows a geometric rule: The origin must remain fixed, and all lines must remain lines.

<!--## Matrix from visual representation of transformation-->

## Matrix vector products as linear transformations

\begin{align} \label{38}
	A =
	\begin{bmatrix}
		\vec{v_1} & \vec{v_2} & ... & \vec{v_n}
	\end{bmatrix}
\end{align}


\begin{align} \label{39}
	T: \mathbb{R}^n \rightarrow \mathbb{R}^m
\end{align}

\begin{align} \label{40}
	T(\vec{x}) = \textbf{A} \vec{x}
\end{align}



## Linear transformations as matrix vector products

## Image of a subset under a transformation

## im$\textrm{(}$T$\textrm{)}$: Image of a transformation

## Preimage and kernel example

## Sums and scalar multiples of linear transformations

## More on matrix addition and scalar multiplication




<!--## Linear transformation examples

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

To be continued...-->