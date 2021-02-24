---
title: The starter's pack for Schroedinger's Smoke
date: 2020/10/7 20:41
toc: true
categories:
- courses
tags:
- graphics
---



I was always fascinated by the mysterious properties of smoke. I read the paper Schroedinger's Smoke. It took a entirely different perspective on smoke simulation -- Quantum Mechanics. It was frustrating to read to be honest for the excessive amount of prerequisites. The article aims to provide some background so the paper would be much readable.



## Fluid Simulation Methods

There are 2 genres of approaches to attack fluid simulation, grid-based (the Eulerian Specification) and particle-based (the Lagrangian specification). The Eulerian specification would try to understand fluid motion at a fixed location. The Lagrangian Specification would follow a certain particle, as it moves across space. Intuitively, Lagrangian method could be quite computationally expensive. With particles interacting with each other, the complexity would rise to $O(N^2)$. Eulerian specification, however, would be easier to compute. The quality of simulation depends on the granularity of the grid[^lag] . According to the author of Shroedinger's Smoke, Eulerian specification also suffers from loss of vortex. But their method would help them migitate the problem.

[^lag]: https://en.wikipedia.org/wiki/Lagrangian_and_Eulerian_specification_of_the_flow_field



## Quantum Machenics (QMs)

### Wave functions

The author of the paper assumes we understand QMs. It is definetly not the case when I first read it. 

This chapter would quickly walk through concepts of QMs that would help us understand jargon in the paper.



Let's start with one of the simplest simple harmonics. The formula for simple harmonics is as follows:

$$
\phi(x, t) = cos(\frac{2\pi}{\lambda}x-\omega t).
$$



But physicists have found that the wave function in the complex domain can better describe the properties of waves, so we use this expression to express the properties of waves, I will color it so it would be more easy to read. The image is shown in **Fig. 1**:


$$
\phi(x, t) = \textcolor{#990011}{\text{cos}}(\frac{2\pi}{\lambda}x-\omega t)+i\textcolor{#110099}{\text{sin}}(\frac{2\pi}{\lambda}x-\omega t)
$$

We can abbreviate the **wave function** in an exponential form:
$$
e^{ix} = \textcolor{#990011}{\text{cos}}x + \textcolor{#110099}{\text{sin}}x\\
\phi(x, t) = e^{i(\frac{2\pi}{\lambda}x-\omega t)}
$$



### Wave-particle duality

