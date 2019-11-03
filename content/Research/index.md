---
title: Research Summary
summary: Here we describe how to add a page to your site.
date: "2018-06-28T00:00:00Z"

reading_time: false  # Show estimated reading time?
share: false  # Show social sharing links?
profile: false  # Show author profile?
comments: false  # Show comments?

# Optional header image (relative to `static/img/` folder).
header:
  caption: ""
  image: "image.jpg"
---

My research areas involve the following areas:

* Artificial intelligence (AI) for active physical systems
* Deep reinforcement learning (DRL) algorithms
* Mathematical models for high dimensional stochastic systems
* AI for Finanical engineering
* Chemical physics for active physical system

## Deep reinforcement learning algorithms

Sustantial efforts are generally required to training a deep reinforcement learning (DRL) neural network to learn robust, competitive policies for high-dimensional, temporally-extended, and sparse rewward control tasks. Still, training process is prone to diverge and learned policies can be inferior. The lack of interpretation and transparency in various end-to-end DRL prevents efficent diagnoise and remediation. Aiming to bring DRL to real-world applications and to impact broader research areas beyond traditional AI field (i.e., robotics, games) , I am interested in developping novel architectures and training algorithms that enables DRL to produce stable, robust, intepretable control policies.

 


## AI for colloidal robots
{{< figure library="true" src="robot/AIicon.png" title="" lightbox="true" >}}

Equipping micro-/nanoscale colloidal robots with artificial intelligence such that they can efficiently navigate in unknown complex environments could dramatically impact their use in emerging applications like precision surgery and targeted drug delivery. Here we develop a model-free deep reinforcement learning algorithm that can train colloidal robots to learn effective navigation strategies in unknown environments with random obstacles. We employed a deep neural network archecture that enables the robot to mimic animal navigation decision-making by directly processing raw sensor input and decomposing long-range navigations to short-range ones. We show that trained robot agents learn to make navigation decisions regarding both obstacle avoidance and travel time minimization, based solely on local sensory inputs without prior knowledge of the global environment. Such agents with biologically inspired mechanisms can acquire competitive navigation capabilities in large-scale, complex environments containing obstacles of diverse shapes, sizes, and configurations. This study illustrates the potential of artificial intelligence to enable colloidal robots in extensive applications.


## AI for colloidal robots
{{< figure library="true" src="robot/multiRobotCancer2.png" title="" lightbox="true" >}}

The majority of deaths associated with cancer are caused by the migration of cancer cells into various primary organs. In the migration process, more formally known as metastasis, cancer cells travel through the blood or lymph systems, eventually forming new tumors in other vital organs. 
A promising solution to the stop the millions of cancer cells from migrating to other sites is to introducing millions of micro-robots that are capable of intercepting and erasing the cancer cells when they travel through blood or lymph vessels. These micro-robots are capable of identifying and delivering drugs to the targeted cancer cells, while circumventing other normal cells, for example, red cells in blood stream. 
However, the path to the targeted cancel cells are confronted with navigation challenges including long-distance travel in the blood vessel, unknown or spatiotemporally changing environment abundant with other normal cells, and additional time and fuel constraints. If we consider the fact that 50% of the vessel space are taken by red cells that are travelling as well, the process is like chasing a running car while playing dodgeball.   
Deep reinforcement learning – a subfield of Artificial Intelligence, provides a deep neural network architecture that aims to minimally mimic the animal navigation decision-making system. This Artificial Intelligence method enables micro-robot agents to navigate through the complicated environment of blood cells and successfully deliver drugs to the targeted cancer cells.


{{< relref "project/multiagentdrl" >}}











