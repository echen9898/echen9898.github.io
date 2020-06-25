---
layout: post
title: "Safe Simulation to Real World Transfer for an RL Agent"
image: "/assets/profiles/blind_spots.jpg"
date: 2019-10-30
skills: "ROS, Python, C++, Linux, reinforcement learning"
---

___

<p>&nbsp;</p>

**Resources: [code](https://github.com/echen9898/safe_rl){:target="_blank"}**

<p>&nbsp;</p>

This project was completed with [Ramya Ramakrishnan](https://people.csail.mit.edu/ramyaram/){:target="_blank"} for the [Interactive Robotics Group](https://interactive.mit.edu/){:target="_blank"} at MIT. As the field of artificial intelligence progresses, many intelligent robots are being trained in simulation environments before being tested in the real world. While many simulation environments are incredibly realistic, it will always be difficult to fully replicate real world conditions. Small discrepancies between training and testing environments can lead to dangerous behavioral mistakes when a robot is deployed. This is an implementation of a system that is trained to detect situations where a discrepancy between simulation and the real world occurs. These situations are called "blind spots", and this project is based on the papers that outline this issue: [1](http://interactive.mit.edu/sites/default/files/documents/Ramakrishnan_AAAI_2019.pdf){:target="_blank"}, [2](http://erichorvitz.com/JAIR_sim_to_real_transfer.pdf){:target="_blank"}. Once a blind spot is detected, the robot can ask for human intervention instead of taking a potentially dangerous action. The demo below shows a car that's trained to drive towards an orange cone. In a real world scenario, a "dangerous" red block might be present that wasn't accounted for when training in simulation. Now, the agent drives directly towards the red cone. In the demo below, the agent identifies the situation as a blind spot and asks for human intervention. The human operator steers the car left and the car resumes autonomous control and drives to the cone. This experiment simplified the environment in order to provide proof of concept. 

For future work, the system needs to be refined and tested on a larger scale robotic system with a more complex environment. This will inevitably reveal flaws in the system that will need to be resolved before it can be applied practically. Additionally, figuring out how to model and incorporate human feedback in the finetuning phase could be interesting. Modeling the optimization intentions of a human is a potentially difficult inverse reinforcement learning problem that could be studied at a simpler level by building on this approach. Because the robot already has a functional policy and can classify blindspots, figuring out human intention from the corrective actions supplied might be easier than starting from scratch with no policy and no classifier.



<img src="/assets/2019-10-30/demo.gif" alt="Safe RL demo" class="center blog_post_body"> 
