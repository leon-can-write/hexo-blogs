---
title: Dataming1
date: 2020/5/7 11:49
toc: true
categories:
- courses
tags:
- data mining
- bayers
---



# Bayes’ Theorem

**The conditional probability** is given as follows:
$$
P(A|B)=P(A,B)/P(B)
$$
$P(A|B)$ means the probability of $A$ given $B$ has happened.

$P(A, B)$ means the probability that both $A, B$ happen at the same time.

But if $A, B$ are independent, then probability of $A$ does not depend on $B$,  that is $P(A|B)=P(A)$,  then we have $P(A, B)=P(A)P(B)$. 

Hence we have the **bayers’ theorem**:
$$
P(A|B) = \frac{P(B|A)P(A)}{P(B)}
$$
WWe have names for the terms in the theorem:

| Term     | Name       |
| -------- | ---------- |
| $P(A|B)$ | posterior  |
| $P(B|A)$ | likelihood |
| $P(A)$   | prior      |

We will have a quick walk through on what these names mean.



Suppose someone knock at the door when we are having a class, are they a man or a woman? If there are more women in the school, then we will have more confident in saying the one at the door is a woman than a man.

Our speculation is based on **priori**, and a formal definition of that is given as follows:
$$
\text{A priori (prior) is probability of the state of nature.}
$$




We can use other information to heWlp us recognize the gender of the one at the door, like their clothing, their appearance etc.

$P(A|B_{man}) \& P(A|B_{woman})$ helps us to tell the difference between appearance of man and woman. So the **likelihood** is defined as:
$$
\text{Likelihood is a measurement or feature} \\ \text{on the state if the nature.}
$$
