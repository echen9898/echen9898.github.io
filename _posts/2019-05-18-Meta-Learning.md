---
layout: post
title: "Meta-learning Algorithms"
rank: 3
image: "/assets/profiles/meta.png"
date: 2019-05-18
skills: "Python, PyTorch, image processing"
---

___

<p>&nbsp;</p>
**Resources: [code](https://github.com/qwellens/meta_learning_project){:target="_blank"}, [report](/assets/2019-05-18/882_Report.pdf){:target="_blank"}**
<p>&nbsp;</p>

[6.882 (Advanced Topics in AI: Embodied Intelligence)](https://phillipi.github.io/6.882/2019/){:target="_blank"} is a graduate course at MIT that covers a variety of topics at the intersection of artificial intelligence and robotics. One of these topics is meta-learning, which seeks to enable sample efficient learning by optimizing experiment metadata. The algorithms analyzed in this project do this by learning a set of initial network weights that make it easy to finetune the model on subsequent tasks. For our final project, we compared our own meta-learning algorithm called Reptile against two common meta-learning algorithms - MAML and Insect. Reptile is similar to MAML with the exception that it does not use a double gradient method to compute the backward pass in the outer loop, and does not require minibatch test data for each task. According to the [MAML paper](https://arxiv.org/pdf/1703.03400.pdf){:target="_blank"}, the double gradient makes the network computation approximately 33% slower. In order to see if the relative complexity of MAML and Insect yield significant gains, we tested all three approaches on time-series regression and image classification tasks. While we did not cover more complex tasks like reinforcement learning scenarios where MAML might well outperform Reptile by taking full advantage of its additional complexity, the simpler regression results shown below seem to indicate that MAML's complexity might not be necessary on all tasks. Additional experiments would be needed to fully understand the drawbacks and make more conclusive performance comparisons.

<img src="/assets/2019-05-18/regression_results.png" alt="Regression experiment results" class="center blog_post_body">


