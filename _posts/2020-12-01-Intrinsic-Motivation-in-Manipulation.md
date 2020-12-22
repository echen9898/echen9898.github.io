---
layout: post
title: "Study of Intrinsic Motivation in the Context of Robotic Push Tasks"
rank: 1
image: "/assets/profiles/fetch.png"
date: 2020-12-01
skills: "Pytorch"
---

___

<p>&nbsp;</p>

**Resources: [code](https://github.com/echen9898/curiosity_baselines/tree/881_project){:target="_blank"}, [report]({% link /assets/2020-12-01/6.881 Report.pdf %}){:target="_blank"}, [video](https://www.youtube.com/watch?v=lYg7b6BWSGk&t=7s){:target="_blank"}**

<p>&nbsp;</p>

[6.881 (Robotic Manipulation)](http://manipulation.csail.mit.edu/Fall2020/){:target="_blank"} is a graduate class at MIT taught by Prof. Tedrake that explores robot manipulation from perception to planning. For the final project, [Isaac](http://www.isaacperper.com/){:target="_blank"}, [Michael](https://www.linkedin.com/in/michael-hiebert-a12b1414a/){:target="_blank"} and I studied the limits of two intrinsic motivation methods ([ICM](https://pathak22.github.io/noreward-rl/resources/icml17.pdf){:target="_blank"}, [Disagreement](https://pathak22.github.io/exploration-by-disagreement/){:target="_blank"}) on a variety of simple block pushing tasks. While PPO augmented with ICM successfully showed improvements over standard PPO in a variety of scenarios, we were particularly interested in exploring the limits of ICM's inverse model in the context of various action discretizations, and comparing the method to Disagreement when action noise was applied. In the future given more time, it would be interesting to investigate ICM on more complex manipulation tasks, and expand to a multi-task setting. It would also be cool to see how the inverse model scales to a continuous action space, and see if these methods scale to real robots. For more details on the results checkout the report and the video above.

<img src="/assets/2020-12-01/heatmaps.png" alt="Heatmaps" class="center blog_post_body"> 