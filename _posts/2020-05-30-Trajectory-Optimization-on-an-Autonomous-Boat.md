---
layout: post
title: "Trajectory Optimization on an Autonomous Boat"
image: "/assets/profiles/boat.png"
date: 2020-05-30
skills: "Drake, Python, Optimization"
---

___

<p>&nbsp;</p>

**Resources: [code](https://github.com/echen9898/docking){:target="_blank"}, [report]({% link /assets/2020-05-30/6.832 Report.pdf %}){:target="_blank"}, [video](https://www.youtube.com/watch?v=8AD0oO6Yoag){:target="_blank"}**

<p>&nbsp;</p>

[6.832 (Underactuated Robotics)](http://underactuated.csail.mit.edu/Spring2020/index.html){:target="_blank"} is a graduate class at MIT that explores nonlinear control of various robotic system. For the final project, [Isaac](http://www.isaacperper.com/){:target="_blank"} and I derived the planar dynamics of a simple motorboat and successfully generated paths with moving obstacles in a variety of current flows using trajectory optimization. The project was implemented using [Drake](https://drake.mit.edu/){:target="_blank"}, and we experimented with both [Snopt](https://ccom.ucsd.edu/~optimizers/solvers/snopt/){:target="_blank"} and [Ipopt](https://github.com/coin-or/Ipopt){:target="_blank"} solvers. For a detailed description of the dynamics and the optimization formulation, checkout the report or video above.

Given the same optimization formulation, each of these solvers produced very similar solutions for simple scenarios but diverged in more complex current fields. While the success of either method is dependant on the current field, any obstacles, and your desired start and goal configurations, we found that in a large majority of situations the Drake implementation of Ipopt performed better than the Drake implementation of Snopt. Below is an example of a simple trajectory returned by Ipopt.

<img src="/assets/2020-05-30/whirlpool.png" alt="Whirlpool trajectory" class="center blog_post_body"> 

By adding constraints on the boats distance from obstacles Ipopt is able to generate smooth paths through both static and moving obstacles, as shown below.

<img src="/assets/2020-05-30/obstacles.png" alt="Trajectory with obstacles" class="center blog_post_body">

While we did experiment with costs on fuel consumption and distance covered, even relatively simple formulations with constraints on the boats dynamics and torques resulted in reasonably efficient trajectories like the docking maneuver pictured here.

<img src="/assets/2020-05-30/docking.png" alt="Docking maneuver" class="center blog_post_body">

This project was only a few weeks long, and there are definitely a variety of interesting directions to pursue further. We hope to get around to working on those a bit more.