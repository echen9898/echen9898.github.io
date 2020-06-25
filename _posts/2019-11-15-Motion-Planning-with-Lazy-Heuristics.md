---
layout: post
title: "Dynamic Motion Planning using Lazy Heuristics"
image: "/assets/profiles/lazy_planning.jpg"
date: 2019-11-15
skills: "Julia"
---

___

<p>&nbsp;</p>

**Resources: [code](https://github.com/echen9898/Lazy_LPA){:target="_blank"}**

<p>&nbsp;</p>

This project implements A`*` and LPA`*` planning algorithms in Julia. [LPA`*`](https://en.wikipedia.org/wiki/Lifelong_Planning_A*){:target="_blank"} is an incremental planning algorithm that can adapt to environmental changes without having to recalculate the entire graph. This implementation of LPA`*` is slightly different from the original version in that it uses a lazy heuristic to save resources when updating the g-values before each consecutive search. This cuts down on the number of costly edge evaluations the algorithm needs to perform even further. The image below shows nodes and edges evaluated lazily in dark blue, and edges evaluated by the original algorithm in light blue.

<img src="/assets/2019-11-15/plan.png" alt="LPA* Plan" class="center blog_post_body"> 
