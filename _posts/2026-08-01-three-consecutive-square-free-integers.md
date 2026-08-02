---
layout: post
title: "Three Consecutive Square-Free Integers, Infinitely Often"
date: 2026-08-01
description: "A short density argument showing that infinitely many triples of consecutive integers are square-free."
categories: mathematics
related_posts: false
---

A positive integer is **square-free** if it is not divisible by the
square of any prime. Call a positive integer $a$ **simple** if

$$
a,\qquad a+1,\qquad a+2
$$

are all square-free.

Are there infinitely many simple integers?

The answer is yes, and there is a short proof using only the density of
the square-free integers.

*This argument was originally written in December 2022 and published here in August 2026.*

## The proof

Any triple of three consecutive square-free integers must be of the form

$$
4n+1,\qquad 4n+2,\qquad 4n+3.
$$

Indeed, every other triple of three consecutive integers contains a
multiple of $4$, which cannot be square-free.

Suppose, for contradiction, that only finitely many of these triples are
entirely square-free. Then, for every sufficiently large $n$, at least
one of

$$
4n+1,\qquad 4n+2,\qquad 4n+3
$$

is not square-free.

The integer $4n$ is also not square-free. Therefore, every sufficiently
large block

$$
\{4n,4n+1,4n+2,4n+3\}
$$

contains at most two square-free integers.

Let $Q(x)$ denote the number of square-free positive integers not
exceeding $x$. Our assumption would imply

$$
Q(x)\leq \frac{x}{2}+O(1).
$$

However, the square-free integers have natural density

$$
\lim_{x\to\infty}\frac{Q(x)}{x}
=
\frac{6}{\pi^2}
>
\frac12.
$$

This is a contradiction. Hence there are infinitely many triples of
consecutive square-free integers. \(\square\)

## A quantitative consequence

The same proof gives more than infinitude.

Let $G(N)$ be the number of $n\in\{0,\ldots,N-1\}$ such that

$$
4n+1,\qquad 4n+2,\qquad 4n+3
$$

are all square-free.

A good block contains three square-free integers, while every other
block contains at most two. Consequently,

$$
Q(4N)\leq 2N+G(N).
$$

Since

$$
Q(4N)=\frac{24}{\pi^2}N+o(N),
$$

we obtain

$$
\liminf_{N\to\infty}\frac{G(N)}{N}
\geq
\frac{24}{\pi^2}-2
\approx 0.4317.
$$

Thus the proof actually establishes that such triples have positive
lower density among the possible triples \((4n+1,4n+2,4n+3)\).

## The original note

I found this argument in December 2022 while solving Bilkent University's
Problem of the Month. The photograph below is my original handwritten
solution from that time.

![My original handwritten solution, December 2022]({{ '/assets/img/squarefree_triples_proof.jpeg' | relative_url }})

## Note on priority

I found this argument independently, but the result and the proof are
not new. Essentially the same density argument had appeared previously,
and substantially stronger asymptotic results on patterns of square-free
integers are classical.

## References

- [MathOverflow: Are there infinitely many triples of consecutive square-free integers?](https://mathoverflow.net/questions/59741/are-there-infinitely-many-triples-of-consecutive-square-free-integers)
- [Bilkent Problem of the Month, December 2022](https://w3.bilkent.edu.tr/bilkent/problem-of-the-month-december-2022/)
- Leon Mirsky, “Arithmetical Pattern Problems Relating to Divisibility by \(r\)th Powers.”
