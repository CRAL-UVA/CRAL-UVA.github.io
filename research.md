---
title: Research
permalink: /research/
---

<!-- ### About us -->
<!-- <center> 
  <h2>Towards <span style="color:#E57200;">Human-Like</span> <span style="color:#232D4B;">Mobility</span> and <span style="color:#232D4B;">Autonomy</span> for Robots in the Real World</h2> 
</center> -->

<center> 
  <h2> <span style="color:#232D4B;">Towards <span style="color:#E57200;">Human-Like</span> Mobility and Autonomy for Robots in the Real World</span></h2> 
</center>

<br><br>

1. **How do robots take risks in real world environments?** Can robots overtake people in crowds? Can robots clean your house when guests are coming over in the next 10 minutes? In this research, we are currently solving risk-aware mobility and autonomy as a spatio-temporal optimization problem.<br><br>
2.	**How do robots respect social norms around people?** Can robots understand people--what they're doing and why? what they're about to do? and what is the best way to respond to different people in different contexts? We are currently exploring this problem using VLMs and LLMs.<br><br>
3.	**How do robots recover and learn from failures?** Can robots learn from their past experiences and generalize to ones in real world contexts? What is the minimum amount of experiences needed? What is the nature of such experiences? What is the optimal representation of such experiences? We are currently solvng this problem using in-context reinforcement learning.




<!-- The development of mobile service robots can be divided into two distinct golden eras. First, the "Don't Go There" era (1962–2010), where service robots were confined to cages, with any form of human-robot interaction strictly prohibited. Second, the "Get Out Of The Way" era (2011–2021), where the robots freed from their cages, yet humans were still advised to avoid any direct interaction with them. Today, we are entering a third era (2022–present), where advances in engineering and artificial intelligence (AI) have made it possible for robots to co-exist with humans. From on-road traffic to pedestrian sidewalks, from hospitals and airports to our homes, from warehouses to university campuses, these service robots have the potential to improve people's everyday lives. -->

<!-- Our longstanding goal is to unlock the full potential of mobile service robots in the real world so that they can perform tasks as efficiently as we can. We envision a new paradigm, which we call *Human-Like Mobility*, that enable robots to navigate in complex human environments, not just safely, but also confidently, gracefully, and in an agile manner. -->

<!-- ### Research -->

<!-- <iframe width="360" height="180" src="https://www.youtube.com/embed/t4tkCCIGXRU?autoplay=1&mute=1&loop=1&playlist=t4tkCCIGXRU" title="" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe><iframe width="360" height="180" src="https://www.youtube.com/embed/0Zjmm31b1fI?autoplay=1&mute=1&loop=1&playlist=0Zjmm31b1fI" title="Rethinking Social Robot Navigation: Leveraging the Best of Two Worlds" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe> -->

<!-- <br>

#### *Confident* and *Agile*, but *Safe* Multi-Robot Navigation in Complex Human Environments

<div style="display: flex; justify-content: center;">
  <img src="https://maicbf.github.io/static/images/ours_trajectory_16_agents_empty_itr_06_fps_10_trailing_random.gif" width="400"/>
  <img src="https://maicbf.github.io/static/images/maze_2.gif" width="400"/>
</div>


Humans are safe, but at the same time, move confidently with grace and agility in order to be efficient and comfortable. For example, a more impatient individual will overtake a slow-moving group in front and squeeze through narrow gaps even if it means means light contact with other people or objects. Robots today sacrifice efficiency for safety, and cannot be fully deployed in complex human environments. <br> -->

<!-- We work on developing multi-robot algorithms and systems that simultaneously give liveness, agility, and safety guarantees in fully decentralized settings in unstructured environments. We routinely work in the sub-areas of optimal control, machine learning, and reinforcement learning, and testing out our ideas both in simulation as well as on real physical robots.

<u>Some active projects are</u>:
1. **Non-Conservative Barrier Functions (NCBFs)**: Given as input local state-based observations or high-level camera/lidar observation, we develop a new type of CBFs to combine safety, agility, and liveness in a unified CBF. This CBF is then added as a filter to any off-the-shelf planner.
2.	**Physics informed neural Social Mini-Game solvers**: Currently, we assume a fixed dynamic model for which we design new controllers. But what if the dynamic model itself looks different in social navigation ? We use Physics-informed NNs to learn the dynamics model and then develop new controllers for them.
3.	**Multi-agent RL**: We will extend safe RL theory to incorporate safety and agility in RL.


#### *Next-Gen Socially Compliant* Multi-Robot Navigation in Complex Human Environments
<div style="display: flex; justify-content: center; align-items: center; gap: 10px;">
<iframe src="https://myuva-my.sharepoint.com/personal/aar8xx_virginia_edu/_layouts/15/embed.aspx?UniqueId=c7857167-ecee-4acd-8902-6faab24f6b7c" width="600" height="300" frameborder="0" scrolling="no" allowfullscreen title="vlmreasoning"></iframe>
  <iframe src="https://myuva-my.sharepoint.com/personal/aar8xx_virginia_edu/_layouts/15/embed.aspx?UniqueId=f6e53a62-496d-4b5c-8673-cf3c7b37492e" width="200" height="200" frameborder="0" scrolling="no" allowfullscreen title="VLMVideo"></iframe> -->
<!-- </div>


Recent advances in robot learning, large vision-language models, and transformer-based architectures have made it possible for robots to interact with humans via complex natural language instructions. We are leveraging these ideas with the goal of building a next-generation paradigm for human-robot interaction where humans can interact with robots seamlessly and perform complex tasks via mind and body gestures.

At the same time, we are designing algorithms for robots to understand human intent. As humans, we always infer other people's intent without them ever having to verbally indicate so. For instance, we can tell a person's state of mind, simply from their style of walking, their gestures, their facial expressions, etc. Can we leverage these non-verbal cues for social robot navigation? 

<u>Some active projects are</u>:
1.	**Implicit Reasoning via Trajectory Prediction**: Given lidar pointcloud as input, we will do 3D object (maybe even pose) tracking and get the trajectories. Then, use transformer architecture networks to predict future trajectories and poses. An encoder-decoder network will take these predictions and the decoder will generate control inputs for the ego-agent.
2.	**Explicit Reasoning via Cost Map learning**: Use trajectory data to learn a social cost map over a geometric cost map that is provided by standard off the shelf planners like Move base. We will learn the cost map and the resulting planner in an end-to-end fashion
3.	**Explicit Reasoning via Inverse Reinforcement Learning**: Collect trajectory data, then use IRL to learn reward functions of all agents in scene. We will compute a control input by maximizing the reward function. -->
<!-- 4.	**Explicit Reasoning via Analytical Reasoning**: Given the trajectory input, use closed form solutions to generate behavior labels (discrete or continuous) that can then be supplied to a high level planner followed by a low level planner.
5.	**Explicit Reasoning via Vision-Language Models**: VLMs will take in the camera, lidar and prompt as input, and output a high level text-based plan for what the robot should do in the current social context. This high level plan is then followed by the low level motion controller.


#### Autonomous Driving *in Dense, Heterogeneous, and Chaotic Environments*

<div style="display: flex; justify-content: center;">
  <div style="text-align: center; margin-right: 10px;">
    <iframe src="https://myuva-my.sharepoint.com/personal/aar8xx_virginia_edu/_layouts/15/embed.aspx?UniqueId=d1ae93c2-b86f-458f-a8ea-40a6e7b30dcc" width="300" height="300" frameborder="0" scrolling="no" allowfullscreen title="traffic-baseline"></iframe>
    <p>Baseline Traffic Model</p>
  </div>
  <div style="text-align: center;">
    <iframe src="https://myuva-my.sharepoint.com/personal/aar8xx_virginia_edu/_layouts/15/embed.aspx?UniqueId=eb856f66-1ffc-4957-b582-2bee4d26de0c" width="300" height="300" frameborder="0" scrolling="no" allowfullscreen title="traffic-ours"></iframe>
    <p>Our Traffic Model</p>
  </div>
</div>


Over the past decade, we have made immense progress in autonomous driving in developed nations like U.S.A, Europe, UK, etc. But we are still far from achieving the same success in developing nations like India, where the traffic is far denser, far more heterogeneous, and far more chaotic. Our research focuses on developing autonomous driving and ADAS for traffic in these regions.

<u>Some active projects are</u>
1. **Off-road autonomous racing** -->
