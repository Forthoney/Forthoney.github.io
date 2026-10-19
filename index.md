---
title: "Seong-Heon Jung"
permalink:  
layout: home
image: assets/nyu2025.JPG
image_alt: "A photo of Seong-Heon Jung in a blue sweater"
---
I am a first-year PhD student in parallel programming languages at New York University (Courant).

I currently work on **space-safe parallel programming**: parallel programs that only incur a predictable and bounded memory overhead.
Without thoughtful design, parallel programs can undergo a superlinear space blowup, meaning a P processor run may use more than P times the memory of a single-threaded run.
This results in higher memory usage of course, and sometimes even worse performance (cache misses, etc.).

I tackle this challenge from both practice and theory.
* Practice: [reasoning/profiling tools](https://dl.acm.org/doi/10.1145/3816782.3819212) for analyzing the worst-case space usage of off-the-shelf parallel programs.
* Theory: verifiably space-safe parallel programming primitives such as schedulers and memory allocators.

I am advised by [Prof. Sam Westrick](https://cs.nyu.edu/~shw8119/).
During my undergrad, I was advised by [Prof. Nikos Vasilakis](https://nikos.vasilak.is) at Brown University.

This site is built with a Jekyll theme I published myself, [consolo](https://github.com/Forthoney/consolo).
