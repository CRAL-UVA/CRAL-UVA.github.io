---
title: Autonomous Driving
permalink: /autonomous-driving/
description: Research at CRΔL on autonomous driving in dense, heterogeneous, and unstructured traffic — tracking, prediction, behavior modeling, planning, datasets, and AI.
---

<div class="rl-title">
  <span class="rl-sub">Research</span>
  <h2>Autonomous Driving</h2>
</div>

<div class="rl-lede" markdown="0">
<p>Autonomous driving works reasonably well when traffic is orderly and the environment is structured. It works far less well when these assumptions do not hold. CRΔL's work targets the latter case where traffic is dense, heterogeneous, and unstructured. This setting enhances the long-tail problem in autonomous driving.</p>
</div>

<div class="rl-figure">
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 350" role="img" aria-labelledby="adFigTitle adFigDesc" font-family="'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif">
  <title id="adFigTitle">The driving pipeline for dense, heterogeneous, unstructured traffic</title>
  <desc id="adFigDesc">A road scene at the top holds cars, buses, scooters, a rickshaw, cyclists, and pedestrians packed together and ignoring the lane line. Below it, a four-stage pipeline runs from tracking, to trajectory prediction, to behavior modeling, to planning and navigation. A dashed path bypasses the middle stages and feeds the scene straight into planning, labelled as end-to-end AI. A base layer of datasets and simulation supports the whole pipeline.</desc>

  <defs>
    <marker id="adArrow" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="5.5" markerHeight="5.5" orient="auto-start-reverse">
      <path d="M0 0 L10 5 L0 10 z" fill="#232D4B" fill-opacity="0.5"/>
    </marker>
    <marker id="adArrowO" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="5.5" markerHeight="5.5" orient="auto-start-reverse">
      <path d="M0 0 L10 5 L0 10 z" fill="#E57200"/>
    </marker>
  </defs>

  <!-- the scene -->
  <text x="12" y="20" font-size="10" font-weight="600" letter-spacing="1.7" fill="#949bab">DENSE &#183; HETEROGENEOUS &#183; UNSTRUCTURED</text>
  <rect x="10" y="30" width="620" height="76" rx="7" fill="#f4f7fb" stroke="#232D4B" stroke-opacity="0.14"/>
  <path d="M24 68 H616" stroke="#232D4B" stroke-opacity="0.18" stroke-width="2" stroke-dasharray="11 9"/>

  <g fill="#232D4B">
    <rect x="34" y="46" width="64" height="19" rx="3" fill-opacity="0.78"/>
    <rect x="120" y="74" width="42" height="15" rx="3" fill-opacity="0.55"/>
    <rect x="196" y="44" width="40" height="15" rx="3" fill-opacity="0.55"/>
    <rect x="252" y="72" width="58" height="18" rx="3" fill-opacity="0.68"/>
    <rect x="360" y="70" width="26" height="18" rx="5" fill-opacity="0.6"/>
    <rect x="414" y="46" width="42" height="15" rx="3" fill-opacity="0.55"/>
    <rect x="548" y="76" width="44" height="15" rx="3" fill-opacity="0.55"/>
    <rect x="500" y="42" width="34" height="13" rx="3" fill-opacity="0.45"/>
  </g>
  <g fill="#E57200">
    <rect x="174" y="82" width="17" height="8" rx="2"/>
    <rect x="322" y="50" width="17" height="8" rx="2"/>
    <rect x="466" y="86" width="17" height="8" rx="2"/>
    <rect x="590" y="50" width="15" height="7" rx="2"/>
    <circle cx="282" cy="52" r="4.5"/>
    <circle cx="404" cy="94" r="4.5"/>
    <circle cx="516" cy="66" r="4.5"/>
  </g>

  <path d="M121 108 V128" fill="none" stroke="#232D4B" stroke-opacity="0.5" stroke-width="2" marker-end="url(#adArrow)"/>

  <!-- the pipeline -->
  <g>
    <rect x="58" y="134" width="126" height="62" rx="7" fill="#ffffff" stroke="#232D4B" stroke-opacity="0.2"/>
    <text x="121" y="164" text-anchor="middle" font-size="11.5" font-weight="600" fill="#232D4B">Tracking</text>
    <text x="121" y="181" text-anchor="middle" font-size="9" fill="#8a91a0">DensePeds &#183; RoadTrack</text>
  </g>
  <path d="M186 165 H198" fill="none" stroke="#232D4B" stroke-opacity="0.5" stroke-width="2" marker-end="url(#adArrow)"/>

  <g>
    <rect x="204" y="134" width="126" height="62" rx="7" fill="#ffffff" stroke="#232D4B" stroke-opacity="0.2"/>
    <text x="267" y="164" text-anchor="middle" font-size="11.5" font-weight="600" fill="#232D4B">Prediction</text>
    <text x="267" y="181" text-anchor="middle" font-size="9" fill="#8a91a0">TraPHic &#183; RobustTP</text>
  </g>
  <path d="M332 165 H344" fill="none" stroke="#232D4B" stroke-opacity="0.5" stroke-width="2" marker-end="url(#adArrow)"/>

  <g>
    <rect x="350" y="134" width="126" height="62" rx="7" fill="#ffffff" stroke="#232D4B" stroke-opacity="0.2"/>
    <text x="413" y="164" text-anchor="middle" font-size="11.5" font-weight="600" fill="#232D4B">Behavior</text>
    <text x="413" y="181" text-anchor="middle" font-size="9" fill="#8a91a0">CMetric &#183; GraphRQI</text>
  </g>
  <path d="M478 165 H490" fill="none" stroke="#232D4B" stroke-opacity="0.5" stroke-width="2" marker-end="url(#adArrow)"/>

  <g>
    <rect x="496" y="134" width="126" height="62" rx="7" fill="#ffffff" stroke="#232D4B" stroke-opacity="0.2"/>
    <text x="559" y="164" text-anchor="middle" font-size="11.5" font-weight="600" fill="#232D4B">Planning</text>
    <text x="559" y="181" text-anchor="middle" font-size="9" fill="#8a91a0">iPLAN &#183; B-GAP</text>
  </g>

  <!-- the AI shortcut -->
  <path d="M34 108 C20 160 20 232 74 232 L486 232 C528 232 550 226 559 202"
        fill="none" stroke="#E57200" stroke-width="2" stroke-dasharray="7 5" marker-end="url(#adArrowO)"/>
  <text x="300" y="252" text-anchor="middle" font-size="10.5" fill="#E57200">AI &#183; end-to-end policies that skip the middle</text>

  <!-- the base layer -->
  <g stroke="#E57200" stroke-opacity="0.45" stroke-width="2" fill="none">
    <path d="M121 274 V264" marker-end="url(#adArrowO)"/>
    <path d="M267 274 V264" marker-end="url(#adArrowO)"/>
    <path d="M413 274 V264" marker-end="url(#adArrowO)"/>
    <path d="M559 274 V264" marker-end="url(#adArrowO)"/>
  </g>
  <rect x="10" y="280" width="620" height="58" rx="7" fill="#fdf4ec" stroke="#E57200" stroke-opacity="0.35"/>
  <rect x="10" y="280" width="4" height="58" rx="2" fill="#232D4B" fill-opacity="0.6"/>
  <text x="30" y="306" font-size="12.5" font-weight="600" fill="#232D4B">Datasets &amp; Simulation</text>
  <text x="30" y="324" font-size="10" fill="#6b7280">METEOR &#183; DAVE &#183; B-GAP &#8212; traffic this messy has to be recorded and simulated first</text>
</svg>
<p class="rl-figcaption">Each stage below is a section on this page. The dashed path is the newer question we are testing: how much of the pipeline can a large model replace, and at what cost?</p>
</div>

<div class="rl-section">
<span class="rl-kicker">01</span>
<h3>Tracking</h3>
<p>Everything downstream depends on knowing where the other agents are, and dense traffic is close to the worst case for a tracker. Agents are small, they occlude each other constantly, and a scooter and a bus do not move alike. A tracker that treats every detection as an independent box loses agents exactly when the scene is most crowded.</p>
<p>Our answer is to put the interaction model inside the tracker, so that the behavior causing the occlusion also helps resolve it.</p>

<ul class="rl-papers">
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/IROS40897.2019.8968470">DensePeds</a>
    <span class="rl-venue">IROS 2019</span>
    <p>Tracks pedestrians in dense crowds using a motion model of how people actually avoid each other (Front-RVO) rather than generic constant-velocity assumptions. The same collision avoidance that creates the occlusions becomes the prior that recovers from them.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/ICRA40945.2020.9196612">RoadTrack</a>
    <span class="rl-venue">ICRA 2020</span>
    <p>Extends the idea to road agents of very different sizes and dynamics sharing the same space, and runs in real time on video from a moving vehicle.</p>
  </li>
</ul>
</div>

<div class="rl-section">
<span class="rl-kicker">02</span>
<h3>Trajectory Prediction</h3>
<p>Once you can see the agents, you need to know where they are going. In dense traffic that answer depends far more on the neighbors than on the road geometry, which inverts the usual assumption of lane-based predictors. A scooter two meters to the right constrains you more than the entire lane ahead.</p>

<ul class="rl-papers">
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/CVPR.2019.00868">TraPHic</a>
    <span class="rl-venue">CVPR 2019</span>
    <p>Weights each neighbor by how much it actually constrains the ego agent instead of treating everything within a radius equally, and weights heterogeneous agents differently because a bus and a bicycle impose different costs.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1145/3359999.3360495">RobustTP</a>
    <span class="rl-venue">ACM CSCS 2019</span>
    <p>Predicts end to end from raw sensor input, so the predictor absorbs the tracker's noise rather than assuming it was handed clean trajectories. Accuracy measured against ground-truth trajectories overstates what a predictor actually delivers inside a real stack.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/LRA.2020.3004794">Forecasting Trajectory and Behavior with Spectral Clustering in Graph-LSTMs</a>
    <span class="rl-venue">RA-L 2020</span>
    <p>Predicts where an agent will go and what kind of driver it is at the same time. The two help each other: knowing a driver is aggressive sharpens the trajectory, and the trajectory is the only evidence available for the label.</p>
  </li>
</ul>
</div>

<div class="rl-section">
<span class="rl-kicker">03</span>
<h3>Planning and Navigation</h3>
<p>A planner in dense traffic cannot wait for a gap, because in this kind of traffic the gap is produced by the merge rather than preceding it. It has to reason about what the other drivers will concede, which makes planning here close to the <a href="{{ site.baseurl }}/social-mini-games">social mini-games</a> work on the other research page.</p>

<ul class="rl-papers">
  <li>
    <a class="rl-name" href="https://proceedings.mlr.press/v229/wu23b.html">iPLAN: Intent-Aware Planning via Distributed Multi-Agent RL</a>
    <span class="rl-venue">CoRL 2023</span>
    <p>Each agent infers its neighbors' intent from their observed trajectories and plans against that estimate, instead of assuming that everyone shares a policy or a set of rules.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/LRA.2022.3152594">B-GAP</a>
    <span class="rl-venue">RA-L 2022</span>
    <p>Most driving simulators generate well-behaved traffic, so policies trained in them are only ever tested against drivers who yield. B-GAP generates behavior-rich traffic with a controllable mix of aggressive and conservative drivers, and trains navigation policies in it.</p>
  </li>
</ul>
</div>

<div class="rl-section">
<span class="rl-kicker">04</span>
<h3>Behavior Modeling</h3>
<p>"Aggressive" and "conservative" are useful words, but a planner needs a number, computed in real time, from data it already has. We build driver behavior measures out of the geometry of the interaction itself rather than out of hand-labeled video.</p>
<p>The common thread is a graph: agents are nodes, and the fact that one agent has to react to another is an edge. Most of what we want to say about behavior turns out to be a statement about that graph.</p>

<ul class="rl-papers">
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/IROS45743.2020.9341720">CMetric</a>
    <span class="rl-venue">IROS 2020</span>
    <p>Defines driver behavior through centrality on the traffic interaction graph. A driver that many others must react to is, by that measure, aggressive, and the measure is computable from trajectories alone.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/ICRA40945.2020.9196751">GraphRQI</a>
    <span class="rl-venue">ICRA 2020</span>
    <p>Classifies driver behavior from the spectrum of that same graph, which gives a classifier fast enough to run alongside the planner rather than offline.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/TITS.2021.3130218">Using Graph-Theoretic Machine Learning to Predict Human Driver Behavior</a>
    <span class="rl-venue">IEEE T-ITS 2022</span>
    <p>The journal treatment that pulls the graph-theoretic line together and tests it across datasets, with the analysis the conference papers had no room for.</p>
  </li>
  <li>
    <a class="rl-name" href="https://arxiv.org/abs/2405.05354">Transfer-LMR</a>
    <span class="rl-venue">Preprint</span>
    <p>The behaviors that matter most are the ones you have least data for. This work recognizes heavy-tail driving behavior across diverse traffic scenarios by transferring from the common cases into the rare ones.</p>
  </li>
</ul>
</div>

<div class="rl-section">
<span class="rl-kicker">05</span>
<h3>Datasets and Simulation</h3>
<p>Dense, unstructured traffic was under-represented in public driving data for a long time, which meant that methods built for it could not be compared. We record and release the traffic we actually want to solve, and pay particular attention to the rare events, because those are the ones that decide whether a system is deployable.</p>

<ul class="rl-papers">
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/ICRA48891.2023.10161281">METEOR</a>
    <span class="rl-venue">ICRA 2023</span>
    <p>A dense, heterogeneous, and unstructured traffic dataset annotated specifically for rare behaviors: the pedestrian crossing mid-block, the animal on the road, the scooter coming the wrong way down the lane.</p>
  </li>
  <li>
    <a class="rl-name" href="https://arxiv.org/abs/2412.20042">DAVE</a>
    <span class="rl-venue">IV 2026</span>
    <p>A video dataset built around vulnerable road users, with atomic visual element annotations, in environments where their behavior is genuinely hard to anticipate.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/LRA.2022.3152594">B-GAP</a>
    <span class="rl-venue">RA-L 2022</span>
    <p>Listed above under planning, and just as much a simulation contribution: it is how we generate the aggressive drivers that the datasets only capture occasionally.</p>
  </li>
</ul>
</div>

<div class="rl-section">
<span class="rl-kicker">06</span>
<h3>AI</h3>
<p>The pipeline above is modular and you can inspect every stage, which is the argument for it. The argument against it is that errors compound across four stages, and each stage is tuned on a different objective than the one that matters. Large models offer to collapse the whole thing into one policy.</p>
<p>We are testing that claim rather than assuming it, and reporting the cases where it does not hold.</p>

<ul class="rl-papers">
  <li>
    <a class="rl-name" href="https://arxiv.org/abs/2511.12751">Are LLMs The Way Forward? LLM-Guided RL for Decentralized Autonomous Driving</a>
    <span class="rl-venue">ICRA 2026</span>
    <p>A case study rather than a proposal. We put an LLM in the loop of a decentralized driving policy and report where it helps and where it only adds cost.</p>
  </li>
  <li>
    <a class="rl-name" href="https://arxiv.org/abs/2511.12755">Prompt-Driven Domain Adaptation for End-to-End Driving via In-Context RL</a>
    <span class="rl-venue">Preprint</span>
    <p>Adapts an end-to-end driving policy to a new domain through prompting and in-context reinforcement learning instead of retraining, which is the property that would make deployment across regions practical.</p>
  </li>
</ul>
</div>

{% include research-nav.html label="More research at CRΔL" %}
