---
title: Research
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

## Research Areas

* [Applied AI Algorithms for Intelligent Micro/Nano-Robot Systems](#robotAI)
	- [Single-agent Systems](#robotAI-SingleAgent)
	- [Multi-agent Systems (2D)](#robotAI-MultiAgent2D)
	- [Multi-agent Systems (3D)](#robotAI-MultiAgent3D)
	- [Distributed Multi-agent Systems](#robotAI-DistributedMultiAgent)
* [Deep reinforcement learning algorithms](#AIAlgo)
* [Applied optimal control and estimation in stochastic systems](#StochSystem)
* [Novel simulation algorithms for stochastic physical systems](#SimulationAlgo)
* [Modeling stochastic physical systems](#StochPhysicalSystem)

### Intelligent Micro/Nano-Robot Systems
{{< figure library="true" src="robot/AIicon2.png" title="" lightbox="true" >}}
#### Single-agent System<a name="robotAI-SingleAgent"></a>

{{< youtube b8yFWW_sRZU >}}



Equipping micro-/nanoscale colloidal robots with artificial intelligence such that they can efficiently navigate in unknown complex environments could dramatically impact their use in emerging applications like precision surgery and targeted drug delivery. Here we develop a model-free deep reinforcement learning algorithm that can train colloidal robots to learn effective navigation strategies in unknown environments with random obstacles. We employed a deep neural network archecture that enables the robot to mimic animal navigation decision-making by directly processing raw sensor input and decomposing long-range navigations to short-range ones. We show that trained robot agents learn to make navigation decisions regarding both obstacle avoidance and travel time minimization, based solely on local sensory inputs without prior knowledge of the global environment. Such agents with biologically inspired mechanisms can acquire competitive navigation capabilities in large-scale, complex environments containing obstacles of diverse shapes, sizes, and configurations. This study illustrates the potential of artificial intelligence to enable colloidal robots in extensive applications.
{{< figure library="true" src="robot/DRLInterpretation.jpg" title="" lightbox="true" >}}

Read more: \
* Micro/Nano Motor Navigation and Localization via Deep Reinforcement Learning \
<u>Y Yang</u>, M Bevan, B Li ***Advanced Theory and Simulations (2020)***[[Web]](https://onlinelibrary.wiley.com/doi/full/10.1002/adts.202000034){{% staticref "files/MicroNano Motor Navigation and Localization via Deep Reinforcement Learning.pdf" "newtab" %}} [PDF]{{% /staticref %}} \
* Efficient Navigation of Colloidal Robots in an Unknown Environment via Deep Reinforcement Learning\
<u>Y Yang</u>, B Li, M Bevan ***Advanced Intelligent Systems (2019)*** [[Web]](https://aip.scitation.org/doi/pdf/10.1063/1.5126201) {{% staticref "files/Yang, Bevan, Li - 2019 - Efficient Navigation of Colloidal Robots in an Unknown Environment via Deep Reinforcement Learning.pdf" "newtab" %}} [PDF]{{% /staticref %}}


#### Multi-agent System in 2D <a name="robotAI-MultiAgent2D"></a>

Controlling active colloidal particle swarms could enable useful microscopic functions in emerging applications at the interface of nanotechnology and robotics. Here, we present a computational study of controlling self-propelled colloidal particle propulsion speeds to cooperatively capture and transport cargo particles, which otherwise produce random dispersions. By sensing swarm and cargo coordinates, each particle’s speed is actuated according to a control policy based on multiagent assignment and path planning strategies that navigate stochastic particle trajectories to targets around cargo. Colloidal swarms are shown to dynamically cage cargo at their center via inward radial forces while simultaneously translating via directional forces. Speed, power, and efficiency of swarm tasks display emergent coupled dependences on swarm size and pair interactions and approach asymptotic limits indicating near-optimal performance. This scheme exploits unique interactions and stochastic dynamics in colloidal swarms to capture and transport microscopic cargo in a robust, stable, error-tolerant, and dynamic manner.

{{< figure library="true" src="robot/antMultiagent_demo.jpg" title="" lightbox="true" >}}



{{< youtube ofibeCz5QM4 >}}

Read more: \
* Cargo Capture and Transport via Colloidal Swarms \
<u>Y Yang</u>, M Bevan ***Science Advances (2020)***[[Web]](https://advances.sciencemag.org/content/6/4/eaay7679){{% staticref "files/cargo capture and transport via colloidal swarms.pdf" "newtab" %}} [PDF]{{% /staticref %}}


#### Multi-agent System in 3D <a name="robotAI-MultiAgent3D"></a>
Designing intelligent nano-robots that can autonomously navigate in complex and crowded environments such as tissues and blood vessels can offer tremendous possibilities in biomedical applications. Here we report a hierarchical control scheme that enables a nano-robot to efficiently navigate in a blood environment. Our control scheme consists of a high-level controller setting short-ranged dynamic targets to guide the robot to follow a desired path and a low-level deep reinforcement learning controller (DRL) responsible for navigating towards to these dynamic guiding targets. The DRL controller minimally mimics the visual navigation of intelligent species and maps a coarse 3D sensation of the robot’s local environment to control decisions. From extensive navigation data,  the DRL controller is capable of learning competitive, robust, generalizable navigation strategies in free space and in confined environments with red blood cells. Once deployed in blood vessels, the controlled robot can efficiently navigate in blood vessels with different concentrations, vessel size, and RBC configurations. This study identifies the key elements in designing control systems for autonomous nanorobots and illustrates the potential of artificial intelligence for biomedical applications.
{{< figure library="true" src="robot/robotBloodDemo.jpg" title="" lightbox="true" >}}



#### Distributed Multi-agent System<a name="robotAI-DistributedMultiAgent"></a>
Assembly large number (>1000) of colloidal robots into ordered structures can enable applications not attainable in small colloids systems (<100), yet on the other hand poses challenges of developing robust and efficient coordination and control strategies.  Here we report a decentralized and asynchronized control strategy that can enable thousands of colloidal robots to precisely assemble into predefined shapes and perform in-place shape transformations. This is enabled by equipping individual robot with the capability to make decisions on sequential assembly order and navigation through complex environments formed during assembly processes. Using deep reinforcement learning, distributed intelligent robot agents are trained to learn hierarchical navigation strategy across different length scales based on local sensor information at different granularity. Our results demonstrate a flexible and scalable algorithmic framework to control a large number of colloidal robots collective assembly behavior in a robust, error-tolerant, reconfigurable manner.
{{< figure library="true" src="robot/LargeScaleRobotAssembly.jpg" title="" lightbox="true" >}}




### Deep reinforcement learning algorithms<a name="AIAlgo"></a>


Deep reinforcement learning for high dimensional, hierarchical control tasks usually requires the use of complex neural networks as functional approximators, which can lead to inefficiency, instability and even divergence in the training process. Here, we introduce stacked deep Q learning (SDQL), a flexible modularized deep reinforcement learning architecture, that can enable finding of optimal control policy of control tasks consisting of multiple linear stages in a stable and efficient way. SDQL exploits the linear stage structure by approximating the Q function via a collection of deep Q sub-networks stacking along an axis marking the stage-wise progress of the whole task. By back-propagating the learned state values from later stages to earlier stages, all sub-networks co-adapt to maximize the total reward of the whole task, although each sub-network is responsible for learning optimal control policy for its own stage. This modularized architecture offers considerable flexibility in terms of environment and policy modeling, as it allows choices of different state spaces, action spaces, reward structures, and Q networks for each stage, Further, the backward stage-wise training procedure of SDQL can offers additional transparency, stability, and flexibility to the training process, thus facilitating model fine-tuning and hyper-parameter search. We demonstrate that SDQL is capable of learning competitive strategies for problems with characteristics of high-dimensional state space, heterogeneous action space(both discrete and continuous), multiple scales, and sparse and delayed rewards.
{{< figure library="true" src="DRLAlgorithms/Architecutre.png" title="" lightbox="true" >}}

Read more: \
* A Deep Reinforcement Learning Architecture for Multi-stage Optimal Control \
<u>Y Yang</u> ***Preprint (2019)***[[Web]](https://arxiv.org/abs/1911.10684){{% staticref "files/A Deep Reinforcement Learning Architecture for Multi-stage Optimal Control.pdf" "newtab" %}} [PDF]{{% /staticref %}}

### Applied optimal control and estimation in stochastic systems<a name="StochSystem"></a>
Perfectly ordered states are targets in diverse molecular to microscale systems involving, for example, atomic clusters, protein folding, protein crystallization, nanoparticle superlattices, and colloidal crystals. However, there is no obvious approach to control the assembly of perfectly ordered global free energy minimum structures; near-equilibrium assembly is impractically slow, and faster out-of-equilibrium processes generally terminate in defective states. Here, we demonstrate the rapid and robust assembly of perfect crystals by navigating kinetic bottlenecks using closed-loop control of electric field mediated crystallization of colloidal particles. An optimal policy is computed with dynamic programming using a reaction coordinate based dynamic model. By tracking real-time stochastic particle configurations and adjusting applied fields via feedback, the evolution of unassembled particles is guided through polycrystalline states into single domain crystals. This approach to controlling the assembly of a target structure is based on general principles that make it applicable to a broad range of processes from nano- to microscales (where tuning a global thermodynamic variable yields temporal control over thermal sampling of different states via their relative free energies).
{{< figure library="true" src="optimalColloidalAssembly/optimalColloidalAssembly.jpg" title="" lightbox="true" >}}


Read more:\

* An M-Estimator for Reduced-Rank High-Dimensional Linear Dynamical System Identification. \\
S Chen, K Liu, <u>Y Yang</u>, Y Xu, S Lee, M Lindquist, BS Caffo, JT Vogelstein. ***Pattern recognition letters (2017)***  [[Web]](https://www.sciencedirect.com/science/article/pii/S0167865516303671)  {{% staticref "files/An M-estimator for reduced-rank system identification.pdf" "newtab" %}} [PDF]{{% /staticref %}} \
* Optimal Feedback Controlled Assembly of Perfect Crystals. \
X Tang\*, B Rupp\*, <u>Y Yang</u>\*, TD Edwards, MA Grover, MA Bevan. (\*Equal Contribution) ***ACS nano (2016)*** [[Web]](https://pubs.acs.org/doi/abs/10.1021/acsnano.6b02400) {{% staticref "files/Optimal Feedback Controlled Assembly of Perfect Crystals.pdf" "newtab" %}} [PDF]{{% /staticref %}} \
* Dynamic Colloidal Assembly Pathways via Low Dimensional Models. \
<u>Y Yang</u>, R Thyagarajan, DM Ford, MA Bevan. ***The Journal of chemical physics (2016)***  [[Web]](https://aip.scitation.org/doi/abs/10.1063/1.4951698) {{% staticref "files/Dynamic colloidal assembly pathways via low dimensional models.pdf" "newtab" %}} [PDF]{{% /staticref %}} \
* Controlling Assembly of Colloidal Particles into Structured Objects: Basic Strategy and A Case Study \\
MA Bevan, DM Ford, MA Grover, B Shapiro, D Maroudas, <u>Y Yang</u>, et al. ***Journal of Process Control (2015)***  [[Web]](https://www.sciencedirect.com/science/article/pii/S0959152414002959)   {{% staticref "files/Controlling assembly of colloidal particles into structured objectsl.pdf" "newtab" %}} [PDF]{{% /staticref %}}


### Noval simulation algorithms for stochastic physical systems<a name="SimulationAlgo"></a>


Colloidal rod diffusion near a wall is modeled and simulated based on a constrained Stokesian dynamic model of chains-of-spheres. By modeling colloidal rods as chains-of-spheres, complete diffusion tensors are computed for colloidal rods in bulk media and near interfaces, including hydrodynamic interactions, translation-rotation coupling, and all diffusion modes in the particle and lab frames. Simulated trajectories based on the chain-of-spheres diffusion tensor are quantified in terms of typical experimental quantities such as mean squared positional and angular displacements as well as autocorrelation functions. Theoretical expressions are reported to predict measured average diffusivities as well as the crossover from short-time anisotropic translational diffusion along the rod’s major axis to isotropic diffusion. Diffusion modes are quantified in terms of closed form empirical fits to model results to aid their use in interpretation and prediction of experiments involving colloidal rod diffusion in interfacial and confined systems.

Brownian dynamics of colloidal particles on complex curved surfaces has found important applications in diverse physical, chemical, and biological processes. However, most Brownian dynamics simulation algorithms focus on relatively simple curved surfaces that can be analytically parameterized. In this work, we develop an algorithm to enable Brownian dynamics simulation on extremely complex curved surfaces. We approximate complex curved surfaces with triangle mesh surfaces and employ a novel scheme to perform particle simulation on these triangle mesh surfaces. Our algorithm computes forces and velocities of particles in global coordinates but updates their positions in local coordinates, which combines the strengths from both global and local simulation schemes. We benchmark the proposed algorithm with theory and then simulate Brownian dynamics of both single and multiple particles on torus and knot surfaces. The results show that our method captures well diffusion, transport, and crystallization of colloidal particles on complex surfaces with nontrivial topology. This study offers an efficient strategy for elucidating the impact of curvature, geometry, and topology on particle dynamics and microstructure formation in complex environments.

{{< figure library="true" src="simulation/BrownianManifold.jpg" title="" lightbox="true" >}}

Read more:\
* Interfacial Colloidal Rod Dynamics: Coefficients, Simulations, and Analysis\
<u>Y Yang</u>, MA Bevan ***The Journal of chemical physics (2017)*** [[Web]](https://aip.scitation.org/doi/10.1063/1.4995949) {{% staticref "files/Interfacial colloidal rod dynamics Coefficients, simulations,.pdf" "newtab" %}} [PDF]{{% /staticref %}} \
* A Simulation Algorithm for Brownian Dynamics on Complex Curved Surfaces\
<u>Y Yang</u>, B Li ***The Journal of chemical physics (2019)*** [[Web]](https://aip.scitation.org/doi/pdf/10.1063/1.5126201) {{% staticref "files/Yang, Li - 2019 - A Simulation Algorithm for Brownian Dynamics on Complex Curved Surfaces.pdf" "newtab" %}} [PDF]{{% /staticref %}}


### Modeling stochastic physical systems<a name="StochPhysicalSystem"></a>
Colloidal rod diffusion near a wall is modeled and simulated based on a constrained Stokesian dynamic model of chains-of-spheres. By modeling colloidal rods as chains-of-spheres, complete diffusion tensors are computed for colloidal rods in bulk media and near interfaces, including hydrodynamic interactions, translation-rotation coupling, and all diffusion modes in the particle and lab frames. Simulated trajectories based on the chain-of-spheres diffusion tensor are quantified in terms of typical experimental quantities such as mean squared positional and angular displacements as well as autocorrelation functions. Theoretical expressions are reported to predict measured average diffusivities as well as the
crossover from short-time anisotropic translational diffusion along the rod’s major axis to isotropic diffusion. Diffusion modes are quantified in terms of closed form empirical fits to model results to aid their use in interpretation and prediction of experiments involving colloidal rod diffusion in interfacial and confined systems. 
{{< figure library="true" src="physicalSystem/physicalSystemModeling.jpg" title="" lightbox="true" >}}


Read more:\
* Colloidal Crystal Grain Boundary Formation and Motion. \
TD Edwards\*, <u>Y Yang</u>\*, DJ Beltran-Villegas, MA Bevan. (\*Equal Contribution) ***Nature Scientific reports (2014)*** [[Web]](https://www.nature.com/articles/srep06132) {{% staticref "files/Colloidal crystal grain boundary formation and motion.pdf" "newtab" %}} [PDF]{{% /staticref %}} \
* Collective oscillation in dense suspension of self-propelled chiral rods \
Y Liu, <u>Y Yang</u>, B Li, XQ Feng ***Soft matter (2019)***  [[Web]](https://pubs.rsc.org/en/content/articlelanding/2019/sm/c9sm00159j/unauth#!divAbstract)  {{% staticref "files/Liu et al. - 2019 - Collective oscillation in dense suspension of self-propelled chiral rods.pdf" "newtab" %}} [PDF]{{% /staticref %}} \
* Energy Landscapes for Ellipsoids in Non-uniform AC Electric Fields\
I Torres-Díaz, B Rupp, <u>Y Yang</u>, MA Bevan ***Soft matter (2018)***  [[Web]](https://pubs.rsc.org/en/content/articlelanding/2018/sm/c7sm02287e/unauth#!divAbstract)  {{% staticref "files/Energy landscapes for ellipsoids in non-uniform.pdf" "newtab" %}} [PDF]{{% /staticref %}} \
* Interfacial Colloidal Rod Dynamics: Coefficients, Simulations, and Analysis\\
<u>Y Yang</u>, MA Bevan ***The Journal of chemical physics (2017)*** [[Web]](https://aip.scitation.org/doi/abs/10.1063/1.4995949) {{% staticref "files/Interfacial colloidal rod dynamics Coefficients, simulations,.pdf" "newtab" %}} [PDF]{{% /staticref %}} \
* Interfacial and Confined Colloidal Rod Diffusion \
JL Bitter, <u>Y Yang</u>, G Duncan, H Fairbrother, MA Bevan. ***Langmuir (2017)*** [[Web]](https://pubs.acs.org/doi/abs/10.1021/acs.langmuir.7b01704) {{% staticref "files/Interfacial and Confined Colloidal Rod Diffusion.pdf" "newtab" %}} [PDF]{{% /staticref %}} \
* Reconfigurable Multi-scale Colloidal Assembly on Excluded Volume Patterns. \
TD Edwards, <u>Y Yang</u>, WN Everett, MA Bevan. ***Nature Scientific reports (2015)***  [[Web]](https://www.nature.com/articles/srep13612)  {{% staticref "files/Reconfgurable multi-scale colloidal assembly on excluded volume patterns.pdf" "newtab" %}} [PDF]{{% /staticref %}} \
* Modeling Depletion Mediated Colloidal Assembly on Topographical Patterns. \
<u>Y Yang</u>, TD Edwards, MA Bevan. ***Journal of colloid and interface science(2015)*** [[Web]](https://www.sciencedirect.com/science/article/pii/S0021979714009461)   {{% staticref "files/Modeling depletion mediated colloidal assembly on topographical.pdf" "newtab" %}} [PDF]{{% /staticref %}}



