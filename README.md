# Awesome Robot Social Navigation [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
This repo keeps track of the historical and recent advances in robot social navigation/crowd navigation/navigation in dynamic or human environments.

- **I'm actively developing this list, if you would like to contribute or spot any error, please open a pull request!**
- For viewers' convenience, the links of papers first prioritize their websites, and then the free preprints if they are publicly available. 

## Table of Content
 [Awesome Robot Social Navigation](#awesome-robot-social-navigation)
  * [Surveys](#surveys)
  * [Datasets and Benchmarks](#datasets-and-benchmarks)
    + [Real-world Datasets](#real-world-datasets)
    + [Simulated Datasets and Benchmarks](#simulated-datasets-and-benchmarks)
  * [Methods](#methods)
    + [Model-based Methods](#model-based-methods)
    + [Learning-based Methods](#learning-based-methods)
      - [Supervised Learning](#supervised-learning)
      - [Reinforcement Learning](#reinforcement-learning)
  * [Pedestrian Behavior Modeling](#human-behavior-modelling)
  * [User studies](#user-studies)


## Surveys
- [Core Challenges of Social Robot Navigation: A Survey](https://dl.acm.org/doi/full/10.1145/3583741), THRI 2023.
- [A Survey on Socially Aware Robot Navigation: Taxonomy and Future Challenges](https://arxiv.org/abs/2311.06922), IJRR 2024.
- [Conflict Avoidance in Social Navigation—a Survey](https://dl.acm.org/doi/full/10.1145/3647983), THRI 2024.

## Datasets and Benchmarks
### Real-world Datasets
- [Experimental Analysis of Sample-Based Maps for Long-Term SLAM](https://journals.sagepub.com/doi/10.1177/0278364908096286), IJRR 2009.
- [Long-term experiments with an adaptive spherical view representation for navigation in changing environments](https://www.researchgate.net/publication/215639692_Long-Term_Experiments_with_an_Adaptive_Spherical_View_Representation_for_Navigation_in_Changing_Environments), Robotics and Automation Systems 2011.
- [Tracking People in 3D Using a Bottom-Up Top-Down Detector](http://www2.informatik.uni-freiburg.de/~spinello/spinelloICRA11.pdf), ICRA 2011.
- [Localization and navigation of the CoBots over long-term deployments](https://scholarworks.umass.edu/cgi/viewcontent.cgi?article=2327&context=cs_faculty_pubs), IJRR 2013.
- (NCLT) [University of Michigan North Campus Long-Term Vision and Lidar Dataset](https://robots.engin.umich.edu/nclt/), IJRR 2010.
- (L-CAS) [Online Learning for Human Classification in 3D LiDAR-based Tracking](https://lcas.lincoln.ac.uk/wp/research/data-sets-software/l-cas-3d-point-cloud-people-dataset/), IROS 2017.
- (JDRB) [JackRabbot Dataset and Benchmark](https://jrdb.erc.monash.edu/), paper series 2021-2023. 
- [SocNavBench: A Grounded Simulation Testing Framework for Evaluating Social Navigation](https://github.com/CMU-TBD/SocNavBench), THRI 2022.
- [THOR and THOR-Magni](http://thor.oru.se/), RA-L 2020 and arXiv 2022.
- (SCAND) [Socially CompliAnt Navigation Dataset](https://www.cs.utexas.edu/~xiao/SCAND/SCAND.html), RA-L 2022.
- (MuSoHu) [Toward Human-Like Social Robot Navigation: A Large-Scale, Multi-Modal, Social Human Navigation Dataset](https://cs.gmu.edu/~xiao/Research/MuSoHu/), IROS 2023.

### Simulated Datasets and Benchmarks
**Review**: [A Review of Software for Crowd Simulation](https://urban-analytics.github.io/dust/docs/ped_sim_review.pdf).
- [CrowdNav](https://github.com/vita-epfl/CrowdNav).
- [SocNav1: A Dataset to Benchmark and Learn Social Navigation Conventions](https://github.com/gnns4hri/SocNav1), MDPI 2019.
- [SocNavBench: A Grounded Simulation Testing Framework for Evaluating Social Navigation](https://github.com/CMU-TBD/SocNavBench), THRI 2022.
- [Pedsim-ROS](https://github.com/srl-freiburg/pedsim_ros).

## Methods
### Model-based Methods
#### Velocity obstacle approaches (RVO, ORCA, etc)
- [Reciprocal Velocity Obstacles for Real-Time Multi-Agent Navigation](https://gamma.cs.unc.edu/RVO/), ICRA 2008.
- [Optimal Reciprocal Collision Avoidance for Multi-Agent Navigation](https://emotion.inrialpes.fr/fraichard/safety2010/10-vandenberg-etal-icraw.pdf), [website](https://gamma.cs.unc.edu/ORCA/), ICRA 2010.
- [Reciprocal n-Body Collision Avoidance](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=0595d16fca09a3979ccd2222b094e4b72755e780), Robotics Research 2011.
- [The Hybrid Reciprocal Velocity Obstacle](https://gamma.cs.unc.edu/HRVO/), T-RO 2011.

#### [ROS navigation stack](http://robotics.stanford.edu/~ang/papers/icraoss09-ROS.pdf)
- (DWA) [The Dynamic Window Approach to Collision Avoidance](https://www.ri.cmu.edu/pub_files/pub1/fox_dieter_1997_1/fox_dieter_1997_1.pdf), Robotics and Automation Magazine 1997.
- (TEB) [Time Elastic Band Planner](https://wiki.ros.org/teb_local_planner), paper series 2012-2017.

#### MPC
- [Integrating Predictive Motion Uncertainties with Distributionally Robust Risk-Aware Control for Safe Robot Navigation in Crowds](https://arxiv.org/abs/2403.05081), ICRA 2024.

#### Force-based Methods
- (Social Force) [Social Force Model for Pedestrian Dynamics](https://arxiv.org/abs/cond-mat/9805244), Physics Review 1995.

#### Game Theory
- [Mixed-Strategy Nash Equilibrium for Crowd Navigation](https://arxiv.org/abs/2403.01537), arXiv 2024.

### Learning-based Methods

#### Supervised Learning
#### Reinforcement Learning
- Combining human trajectory prediction and robot planning
  - (RGL) [Relational Graph Learning for Crowd Navigation](https://arxiv.org/abs/1909.13165), IROS 2020.
  - [DenseCAvoid: Real-time Navigation in Dense Crowds using Anticipatory Behaviors](https://arxiv.org/abs/2002.03038), ICRA 2020.
  - [Socially Aware Crowd Navigation with Multimodal Pedestrian Trajectory Prediction for Autonomous Vehicles](https://arxiv.org/abs/2011.11191), ITSC 2020.
  - [Intent-Aware Pedestrian Prediction for Adaptive Crowd Navigation](https://intuitivecomputing.github.io/publications/2020-icra-katyal.pdf), ICRA 2020.
  - [Path Planning in Dynamic Environments using Generative RNNs and Monte Carlo Tree Search](https://arxiv.org/abs/2001.11597), ICRA 2020.
  - [Mobile Robot Navigation Using Learning-Based Method Based on Predictive State Representation in a Dynamic Environment](https://robotics.ait.kyushu-u.ac.jp/kurazume/papers/MatsumotoSII22.pdf), IEEE SII 2022.
  - [ntention Aware Robot Crowd Navigation with Attention-Based Interaction Graph](https://sites.google.com/view/intention-aware-crowdnav/home), ICRA 2023.
  - [Stranger Danger! Identifying and Avoiding Unpredictable Pedestrians in RL-based Social Robot Navigation](https://people.eecs.berkeley.edu/~prabal/pubs/papers/pohland24stranger.pdf), arXiv 2024. 


## Pedestrian Behavior Modelling
**Review**: [A review on crowd simulation and modeling](https://www.sciencedirect.com/science/article/abs/pii/S1524070320300242), Graphical Models 2020.
- [Modeling Cooperative Navigation in Dense Human Crowds](https://arxiv.org/abs/1705.06201), ICRA 2017.

## User Studies
- [How Do Robot Experts Measure the Success of Social Robot Navigation?](https://dl.acm.org/doi/10.1145/3610978.3640636), HRI 2024.