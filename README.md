# Awesome Robot Social Navigation [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

This repo keeps track of the historical and recent advances in robot social navigation/crowd navigation/navigation in dynamic or human environments.

- **I'm actively developing this list, if you would like to contribute or spot any error, please open a pull request!**
- For viewers' convenience, the links of papers first prioritize their websites, and then the free preprints if they are publicly available. 
- Some papers belong to more than one category, I only link them on their first appearance. 

------
## Table of Content
  * [Surveys](#surveys)
  * [Datasets and Benchmarks](#datasets-and-benchmarks)
    + [Real-world Datasets](#real-world-datasets)
    + [Simulated Datasets and Benchmarks](#simulated-datasets-and-benchmarks)
  * [Methods](#methods)
    + [Model-based Methods](#model-based-methods)
    + [Learning-based Methods](#learning-based-methods)
      - [Supervised Learning](#supervised-learning)
      - [Reinforcement Learning](#reinforcement-learning)
  * [Environment Models](#environment-models)
  * [User Studies](#user-studies)
  * [Recent Workshops](#workshops)

------
## Surveys
- [Human-aware robot navigation: A survey](https://www.sciencedirect.com/science/article/abs/pii/S0921889013001048), Robotics and Autonomous Systems 2013.
- [Core Challenges of Social Robot Navigation: A Survey](https://dl.acm.org/doi/full/10.1145/3583741), THRI 2023.
- [Principles and guidelines for evaluating social robot navigation algorithms](https://arxiv.org/pdf/2306.16740), arXiv 2023.
- [A Survey on Socially Aware Robot Navigation: Taxonomy and Future Challenges](https://arxiv.org/abs/2311.06922), IJRR 2024.
- [Conflict Avoidance in Social Navigation—a Survey](https://dl.acm.org/doi/full/10.1145/3647983), THRI 2024.
- [Bridging Requirements, Planning, and Evaluation: A Review of Social Robot Navigation](https://www.mdpi.com/1424-8220/24/9/2794), Sensors 2024.
- [Characterizing the Complexity of Social Robot Navigation Scenarios](https://arxiv.org/abs/2405.11410), arXiv 2024.

------
## Datasets and Benchmarks
Note that lots of datasets or benchmarks are proposed as a part of individual papers. Here I did not include them, and only list works that solely focus on datasets or benchmarks.
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
- [TBD Pedestrian Dataset](https://arxiv.org/abs/2309.17187), ICRA 2024. 

### Simulators & Simulated Datasets
**Review**: [A Review of Software for Crowd Simulation](https://urban-analytics.github.io/dust/docs/ped_sim_review.pdf).

- 2D simulators
  - [CrowdNav](https://github.com/vita-epfl/CrowdNav)
    - Extension with static obstacles, SFM human agents, and [Stable Baselines 3](https://stable-baselines3.readthedocs.io/en/master/) support: [CrowdSimPlus](https://github.com/sepsamavi/safe-interactive-crowdnav?tab=readme-ov-file#crowdsimplus-simulator).
  - [SocNav1: A Dataset to Benchmark and Learn Social Navigation Conventions](https://github.com/gnns4hri/SocNav1), MDPI 2019.
  - [SocNav2](https://github.com/jginesclavero/social_nav2)
  - [SocNavBench: A Grounded Simulation Testing Framework for Evaluating Social Navigation](https://github.com/CMU-TBD/SocNavBench), THRI 2022.
- 3D simulators
  - [Pedsim-ROS](https://github.com/srl-freiburg/pedsim_ros)
  - [AI Habitat 3.0](https://aihabitat.org/habitat3/)
  - [iGibson](https://github.com/StanfordVL/iGibsonChallenge2021)
  - [gym_ped_sim](https://github.com/onlytailei/gym_ped_sim)
  - [Social Environment for Autonomous Navigation (SEAN) 2.0](https://sean.interactive-machines.com/)
  - [HuNavSim: A ROS 2 Human Navigation Simulator for Benchmarking Human-Aware Robot Navigation](https://arxiv.org/pdf/2305.01303), RAL 2023.
  - [Arena-Rosnav 3.0: A Comprehensive Development and Benchmarking Platform for Navigation](https://github.com/Arena-Rosnav), RSS 2024.
  - [Arena 4.0: A Comprehensive ROS2 Development and Benchmarking Platform for Human-centric Navigation Using Generative-Model-based Environment Generation](https://arxiv.org/pdf/2409.12471), arXiv 2024.
------
## Methods
### Model-based Methods
#### Velocity obstacle approaches (RVO, ORCA, etc)
- [Motion Planning in Dynamic Environments using Velocity Obstacles](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=d8315aaef1544046a184f7ad8252cf1de0def800), IJRR 1998.
- [Reciprocal Velocity Obstacles for Real-Time Multi-Agent Navigation](https://gamma.cs.unc.edu/RVO/), ICRA 2008.
- [Generalized Velocity Obstacles](http://gamma-web.iacs.umd.edu/NHRVO/WilkieIROS09.pdf), IROS 2009.
- [Optimal Reciprocal Collision Avoidance for Multi-Agent Navigation](https://emotion.inrialpes.fr/fraichard/safety2010/10-vandenberg-etal-icraw.pdf), [website](https://gamma.cs.unc.edu/ORCA/), ICRA 2010.
- [Reciprocal n-Body Collision Avoidance](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=0595d16fca09a3979ccd2222b094e4b72755e780), Robotics Research 2011.
- [The Hybrid Reciprocal Velocity Obstacle](https://gamma.cs.unc.edu/HRVO/), T-RO 2011.
- [V-RVO: Decentralized Multi-Agent Collision Avoidance using Voronoi Diagrams and Reciprocal Velocity Obstacles](https://arxiv.org/abs/2102.13281), IROS 2021.
- ORCA for non-holonomic robots:
  - (ORCA-DD) [Smooth and Collision-Free Navigation for Multiple Robots Under Differential-Drive Constraints](https://gamma.cs.unc.edu/ORCA-DD/), IROS 2010. 
  - (Non-holomomic ORCA) [Optimal Reciprocal Collision Avoidance for Multiple Non-Holonomic Robots](https://www.research-collection.ethz.ch/bitstream/handle/20.500.11850/63793/eth-7722-01.pdf?sequence=1), Distributed Autonomous Robotic Systems 2013.

#### [ROS navigation stack](http://robotics.stanford.edu/~ang/papers/icraoss09-ROS.pdf)
- (DWA) [The Dynamic Window Approach to Collision Avoidance](https://www.ri.cmu.edu/pub_files/pub1/fox_dieter_1997_1/fox_dieter_1997_1.pdf), Robotics and Automation Magazine 1997.
- (TEB) [Time Elastic Band Planner](https://wiki.ros.org/teb_local_planner), paper series 2012-2017.
  - (Human-aware TEB) [Human-Aware Navigation Planner for Diverse Human-Robot Contexts](https://arxiv.org/abs/2106.09971), IROS 2021.

#### Model Predictive Control (MPC)
- [Model Predictive Contouring Control for Collision Avoidance in Unstructured Dynamic Environments](https://github.com/tud-amr/amr-lmpcc), RA-L 2019.
- [Anticipatory Navigation in Crowds by Probabilistic Prediction of Pedestrian Future Movements](https://ieeexplore.ieee.org/document/9561022), ICRA 2021.
- [Collision Avoidance in Tightly-Constrained Environments without Coordination: a Hierarchical Control Approach](https://sites.google.com/berkeley.edu/sg-control), ICRA 2021.
- [Group-based Motion Prediction for Navigation in Crowded Environments](https://proceedings.mlr.press/v164/wang22e.html), CoRL 2021.
- [Integrating Predictive Motion Uncertainties with Distributionally Robust Risk-Aware Control for Safe Robot Navigation in Crowds](https://arxiv.org/abs/2403.05081), ICRA 2024.
- [SICNav: Safe and Interactive Crowd Navigation Using Model Predictive Control and Bilevel Optimization](http://sepehr.fyi/projects/sicnav/), arXiv 2023.
- [Multi-Robot Cooperative Navigation in Crowds: A Game-Theoretic Learning-Based Model Predictive Control Approach](https://arxiv.org/abs/2310.06964), ICRA 2024.

#### Potential Field & Force-based Methods
- (Social Force) [Social Force Model for Pedestrian Dynamics](https://arxiv.org/abs/cond-mat/9805244), Physics Review 1995.
- [Robot Companion: A Social-Force based approach with Human Awareness-Navigation in Crowded Environments](https://digital.csic.es/bitstream/10261/96448/4/Robot%20companion.pdf), IROS 2013.
- [Socially-Aware Reactive Obstacle Avoidance Strategy Based on Limit Cycle](https://ieeexplore.ieee.org/abstract/document/9013059), RA-L 2020.

#### Game Theory
- [Mixed-Strategy Nash Equilibrium for Crowd Navigation](https://arxiv.org/abs/2403.01537), arXiv 2024.

#### Gaussian Mixture Models (GMM)
- [Socially-Aware Navigation Planner Using Models of Human-Human Interaction](https://rrl.cse.unr.edu/media/documents/2017/sebastian-SAN-ROMAN.pdf), RO-MAN 2017.

#### Topological Braids
- [Social Momentum: Design and Evaluation of a Framework for Socially Competent Robot Navigation](https://dl.acm.org/doi/10.1145/3495244), THRI 2022.

### Learning-based Methods

#### Supervised Learning
- [Deep-Learned Collision Avoidance Policy for Distributed Multi-Agent Navigation](https://arxiv.org/abs/1609.06838), RA-L 2017.
- [Socially Compliant Navigation through Raw Depth Inputs with Generative Adversarial Imitation Learning](https://arxiv.org/abs/1710.02543), ICRA 2018.
- [Deep local trajectory replanning and control for robot navigation](https://arxiv.org/abs/1905.05279), ICRA 2019.
- [Towards Safe Navigation Through Crowded Dynamic Environments](https://sites.temple.edu/trail/files/2021/11/XieXinDamesIROS2021.pdf), IROS 2021.
- [Towards Imitation Learning in Real World Unstructured Social Mini-Games in Pedestrian Crowds](https://arxiv.org/abs/2405.16439), arXiv 2024.
- [SACSoN: Scalable Autonomous Control for Social Navigation](https://sites.google.com/view/SACSoN-review), RA-L 2023.
- [SocialGAIL: Faithful Crowd Simulation for Social Robot Navigation](https://ieeexplore.ieee.org/document/10610371), ICRA 2024.

#### Reinforcement Learning
- Using detected pedestrian states as input
  - (CADRL) [Decentralized noncommunicating multiagent collision avoidance with deep reinforcement learning](https://arxiv.org/abs/1609.07845), ICRA 2017.
  - [Socially aware motion planning with deep reinforcement learning](https://arxiv.org/abs/1703.08862), IROS 2017.
  - (LSTM-RL) [Motion Planning Among Dynamic, Decision-Making Agents with Deep Reinforcement Learning](https://arxiv.org/abs/1805.01956), IROS 2018.
  - (OM-SARL) [Crowd-robot interaction: Crowd-aware robot navigation with attention-based deep reinforcement learning](https://arxiv.org/abs/1809.08835), ICRA 2019.
  - [Robot Navigation in Crowds by Graph Convolutional Networks with Attention Learned from Human Gaze](https://arxiv.org/abs/1909.10400), RA-L 2020.
  - [Decentralized structural-RNN for robot crowd navigation with deep reinforcement learning](https://sites.google.com/illinois.edu/crowdnav-dsrnn/home), ICRA 2021.
- Using raw sensor data as input
  - [Towards Optimally Decentralized Multi-Robot Collision Avoidance via Deep Reinforcement Learning](https://arxiv.org/abs/1709.10082), ICRA 2018.
  - [Distributed Multi-Robot Collision Avoidance via Deep Reinforcement Learning for Navigation in Complex Scenarios](https://sites.google.com/view/hybridmrca), IJRR 2020.
  - [Learning Local Planners for Human-aware Navigation in Indoor Environments](http://ras.papercept.net/images/temp/IROS/files/0122.pdf), IROS 2020.
  - [Robot Navigation in Constrained Pedestrian Environments using Reinforcement Learning](https://arxiv.org/abs/2010.08600), ICRA 2021.
  - [Towards Multi-Modal Perception-Based Navigation: A Deep Reinforcement Learning Method](https://ieeexplore.ieee.org/document/9372890), RA-L 2021.
- Combining human trajectory prediction and robot planning
  - (RGL) [Relational Graph Learning for Crowd Navigation](https://arxiv.org/abs/1909.13165), IROS 2020.
  - [DenseCAvoid: Real-time Navigation in Dense Crowds using Anticipatory Behaviors](https://arxiv.org/abs/2002.03038), ICRA 2020.
  - [Socially Aware Crowd Navigation with Multimodal Pedestrian Trajectory Prediction for Autonomous Vehicles](https://arxiv.org/abs/2011.11191), ITSC 2020.
  - [Intent-Aware Pedestrian Prediction for Adaptive Crowd Navigation](https://intuitivecomputing.github.io/publications/2020-icra-katyal.pdf), ICRA 2020.
  - [Path Planning in Dynamic Environments using Generative RNNs and Monte Carlo Tree Search](https://arxiv.org/abs/2001.11597), ICRA 2020.
  - [Mobile Robot Navigation Using Learning-Based Method Based on Predictive State Representation in a Dynamic Environment](https://robotics.ait.kyushu-u.ac.jp/kurazume/papers/MatsumotoSII22.pdf), IEEE SII 2022.
  - [Intention Aware Robot Crowd Navigation with Attention-Based Interaction Graph](https://sites.google.com/view/intention-aware-crowdnav/home), ICRA 2023.
  - [Stranger Danger! Identifying and Avoiding Unpredictable Pedestrians in RL-based Social Robot Navigation](https://people.eecs.berkeley.edu/~prabal/pubs/papers/pohland24stranger.pdf), arXiv 2024. 
- Constrained crowd navigation with both humans and obstacles
  - [Robot Navigation in Crowded Environments Using Deep Reinforcement Learning](https://ras.papercept.net/images/temp/IROS/files/0386.pdf), IROS 2020. 
  - DenseCAvoid, ICRA 2020.
  - Robot Navigation in Constrained Pedestrian Environments using Reinforcement Learning, ICRA 2021.
  - [NavRep: Unsupervised Representations for Reinforcement Learning of Robot Navigation in Dynamic Human Environments](https://arxiv.org/abs/2012.04406), ICRA 2021.
  - [DRL-VO: Learning to Navigate Through Crowded Dynamic Scenes Using Velocity Obstacles](https://github.com/TempleRAIL/drl_vo_nav), T-RO 2023.
  - [Sample-Efficient Learning-Based Dynamic Environment Navigation With Transferring Experience From Optimization-Based Planner](https://ieeexplore.ieee.org/document/10552894), RA-L 2024.
- Reward function design
  - [Human-Inspired Multi-Agent Navigation using Knowledge Distillation](https://github.com/xupei0610/KDMA), IROS 2021.
  - [DWA-RL: Dynamically Feasible Deep Reinforcement Learning Policy for Robot Navigation among Mobile Obstacles](https://ieeexplore.ieee.org/document/9561462), ICRA 2021.
  - [DRL-VO](https://github.com/TempleRAIL/drl_vo_nav), T-RO 2023.
  - [Intention Aware Robot Crowd Navigation with Attention-Based Interaction Graph](https://arxiv.org/pdf/2203.01821), ICRA 2023.

#### Foundation Models for Social Navigation
- [SRLM: Human-in-Loop Interactive Social Robot Navigation with Large Language Model and Deep Reinforcement Learning](https://arxiv.org/abs/2403.15648), arXiv 2024.
- [Socially Aware Robot Navigation through Scoring Using Vision-Language Models](https://arxiv.org/abs/2404.00210), arXiv 2024.
- [GSON: A Group-based Social Navigation Framework with Large Multimodal Model](https://arxiv.org/pdf/2409.18084), arXiv 2024.
------
## Environment Models
### Pedestrian Behavior Modeling
**Review**: [A review on crowd simulation and modeling](https://www.sciencedirect.com/science/article/abs/pii/S1524070320300242), Graphical Models 2020.
- [Modeling Cooperative Navigation in Dense Human Crowds](https://arxiv.org/abs/1705.06201), ICRA 2017.
- [From Crowd Simulation to Robot Navigation in Crowds](https://inria.hal.science/hal-02461493/file/root.pdf), RA-L 2020.
- [Group Split and Merge Prediction With 3D Convolutional Networks](https://ieeexplore.ieee.org/abstract/document/8972421), RA-L 2020.

### Map Generation of Dynamic Scenes
- (SNGNN2D) [Generation of Human-aware Navigation Maps using Graph Neural Networks](https://arxiv.org/abs/2011.05180), International Conference on Innovative Techniques and Applications of Artificial Intelligence 2021.
- [Stochastic Occupancy Grid Map Prediction in Dynamic Scenes](https://arxiv.org/abs/2210.08577), CoRL 2023.

------
## User Studies
- Social Momentum, THRI 2022.
- [How Do Robot Experts Measure the Success of Social Robot Navigation?](https://dl.acm.org/doi/10.1145/3610978.3640636), HRI 2024.

------
## Workshops
- [Social Robot Navigation: Advances and Evaluation](https://seanavbench.interactive-machines.com/), ICRA 2022.
- [The 2nd Workshop on Social Robot Navigation: Advances and Evaluation](https://seanavbench23.pages.dev/), IROS 2023.
- [The Last-Mile Robotics Workshop: Envisioning Effective, Sustainable and Human-Centric Delivery](https://www.lastmilerobotics.dfl.ae/), IROS 2023.
- [Unsolved Problems in Social Robot Navigation](https://unsolvedsocialnav.org/), RSS 2024.

------
## References
Part of this repo is adapted from the literature review of the following papers/repos:
- S. Liu, P. Chang, W. Liang, N. Chakraborty, and K. Driggs-Campbell, "[Decentralized Structural-RNN for Robot Crowd Navigation with Deep Reinforcement Learning]()," in IEEE International Conference on Robotics and Automation (ICRA), 2023, pp. 3517-3524.
- S. Liu, P. Chang, Z. Huang, N. Chakraborty, K. Hong, W. Liang, D. Livingston McPherson, J. Geng, and K. Driggs-Campbell, "[Intention Aware Robot Crowd Navigation with Attention-Based Interaction Graph]()," in IEEE International Conference on Robotics and Automation (ICRA), 2021, pp. 12015-12021.
- H. Karnan, A. Nair, X. Xiao, G. Warnell, S. Pirk, A. Toshev, J. Hart, J. Biswas, and P. Stone, "[Socially CompliAnt Navigation Dataset (SCAND): A Large-Scale Dataset Of Demonstrations For Social Navigation]()," IEEE Robotics and Automation Letters, vol. 7, no. 4, pp. 11807-11814, 2022.
- Z. Xie and P. Dames, "[DRL-VO: Learning to Navigate Through Crowded Dynamic Scenes Using Velocity Obstacles]()," IEEE Transactions on Robotics, vol. 39, no. 4, pp. 2700-2719, 2023.
- [learning-based-navigation-list](https://github.com/CUN-bjy/learning-based-navigation-papers/), Github.
