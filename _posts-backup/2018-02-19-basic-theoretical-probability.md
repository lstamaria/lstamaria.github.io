---
layout: post
title: "Basic theoretical probability"
date: 2018-02-19
use_math: true
---

These notes are taken from [Khan Academy's Probability: Basic Theoretical Probability](https://www.khanacademy.org/math/statistics-probability/probability-library/basic-theoretical-probability/v/basic-probability).

## Intro to theoretical probability

\begin{align} \label{1}
	P(H) = \frac{1}{2} = 50%
\end{align}

The equation \ref{1} shows the probability of flipping heads of a coin.

\begin{align} \label{2}
	P(1) = \frac{1}{6}
\end{align}

The equation \ref{2} shows the probability of getting 1 after rolling a die.

\begin{align} \label{3}
	P(1 \textrm{ or } 6) = \frac{2}{6} = \frac{1}{3}
\end{align}

The equation \ref{3} shows the probability of getting 1 or 6 after rolling a die.

\begin{align} \label{4}
	P(2 \textrm{ and }  3) = \frac{0}{6}
\end{align}

The equation \ref{4} shows the probability of getting 2 and 3 after rolling a die.

\begin{align} \label{5}
	P( \textrm{even}) = \frac{3}{6} = \frac{1}{2}
\end{align}

The equation \ref{5} shows the probability of getting an even number such as 2, 4, or 6 after rolling a die.


## Probability: the basics

Probability is how likely something is to happen. 

Statistics is the analysis of events governed by probability.

The best example for understanding probability is flipping a coin.

\begin{align} \label{6}
	P(\textrm{condition}) = \frac{\textrm{# of possibilities that meets condition}} {\textrm{# of equally likely possibilities}}
\end{align}

The equation \ref{6} shows general formula of probability.

The probability of an event can only be between 0 and 1. It can also be written as a percentage.

The probability of an event $$A$$ is written as $$P(A)$$.

If $$P(A) > P(B)$$, then event A has higher chance of occuring than B.

If $$P(A) = P(B)$$, then events A and B are equally likely to occur.


## Simple probability: yellow marble

Problem: Find the probability of pulling a yellow marble from a bag with 3 yellow, 2 red, 2 green, and 1 blue.

Answer:

\begin{align} \label{7}
	P(\textrm{yellow}) = \frac{3} {3 + 2 + 2 + 1} = \frac{3} {8} 
\end{align}

The equation \ref{7} shows the probability of pulling a yellow marble from a bag of marbles.


## Simple probability: non-blue marble

Problem: We have a bag with 9 red marbles, 2 blue marbles, and 3 green marbles in it. What is the probability of randomly selecting a non-blue marble from the bag?

Answer:

\begin{align} \label{8}
	P(\textrm{blue}) = \frac{2} {9 + 2 + 3}  = \frac{1} {7} 
\end{align}

\begin{align} \label{9}
	P(\textrm{non-blue}) = 1 - \frac{1} {7}	= \frac{6} {7} 
\end{align}

The equations \ref{8} and \ref{9} show the probability of pulling a non-blue marble from a bag of marbles.

Problem: If a number is randomly chosen from the following list, what is the probability that the number is a multiple of 5?

32, 49, 30, 55, 56, 28, 50, 40, 40, 45, 3, 25

Answer:

\begin{align} \label{10}
	P(\textrm{multiple of 5}) = \frac{7} {12}
\end{align}

The equation \ref{10} shows the probability of getting a multiple of 5 from a set of numbers.

Problem: The circumference of a circle is 36$$\pi$$. Contained in that circle is a smaller circle with are 16$$\pi$$. A point is selected at random from the inside the larger circle. What is the probability that the point also lies in the smaller circle?

Answer:

\begin{align} \label{11}
	P(\textrm{point in smaller circle}) = \frac{\textrm{area of smaller circle}} {\textrm{area of bigger circle}}
\end{align}

\begin{align} \label{12}
	P(\textrm{point in smaller circle}) = \frac{16\pi} {324\pi} = \frac {4} {81}
\end{align}

The equations \ref{11} and \ref{12} show the probability of getting a point that lies in both smaller circle and bigger circle.

## Intuitive sense of probabilities

Another best example for understanding probability is rolling a die.

\begin{align} \label{13}
	P(\textrm{rolling} \leq 2) = \frac{2}{6} = \frac {1} {3}
\end{align}

The equations \ref{13} shows the probability of rolling less than or equal to 2. 

\begin{align} \label{14}
	P(\textrm{rolling} \geq 3) = \frac{4}{6} = \frac {2} {3}
\end{align}

The equations \ref{14} shows the probability of rolling greater than or equal to 3. 

The equation \ref{14} has greater probability than equation \ref{13}. This means that rolling greater than or equal 3 is more likely to happen than rolling less than or equal to 3.

\begin{align} \label{15}
	P(\textrm{rolling} 7) = \frac{0}{6} = 0 or 0\%
\end{align}

The equations \ref{15} shows the probability of rolling 7. This means that the event is *impossible to happen*.

\begin{align} \label{16}
	P(\textrm{rolling any from 1 to 6}) = \frac{6}{6} = 1 or 100\%
\end{align}

The equations \ref{15} shows the probability of rolling any from 1 to 6. This means that the event is *going to happen*.

## The Monty Hall problem

Monty Hall is the host of Let's Make A Deal with three doors that hide one major prize and two silly rewards. The goal is to find the door that hides the major prize. Switching is allowed after seeing the item hidden on the first door.

\begin{align} \label{17}
	P(\textrm{win}) = \frac{1}{3}
\end{align}

\begin{align} \label{18}
	P(\textrm{lose}) = \frac{2}{3} 
\end{align}

The equation \ref{17} shows the probability of winning if you don't switch. The equation \ref{18} shows the probability of losing if you don't switch.


\begin{align} \label{19}
	P(\textrm{win}) = \frac{2}{3}
\end{align}

\begin{align} \label{20}
	P(\textrm{lose}) = \frac{1}{3} 
\end{align}

The equation \ref{19} shows the probability of winning if you switch. The equation \ref{20} shows the probability of losing if you switch.