---
title: Social Mini-Games
permalink: /social-mini-games/
description: Research at CRΔL on multi-robot navigation in social mini-games — control, planning, AI, and the datasets and simulators that support them.
---

<div class="rl-title">
  <span class="rl-sub">Research</span>
  <h2>Social Mini-Games</h2>
</div>

<div class="rl-figure rl-figure-top">
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 134" role="img" aria-labelledby="smgSceneTitle smgSceneDesc" font-family="'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif">
  <title id="smgSceneTitle">Three social mini-games</title>
  <desc id="smgSceneDesc">Three social mini-games side by side: a doorway, a corridor, and an intersection. In each one, two robots approach a shared piece of space that only one of them can use at a time, and their paths conflict.</desc>

  <defs>
    <marker id="smgArrowO" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="5" markerHeight="5" orient="auto-start-reverse">
      <path d="M0 0 L10 5 L0 10 z" fill="#E57200"/>
    </marker>
    <marker id="smgArrowN" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="5" markerHeight="5" orient="auto-start-reverse">
      <path d="M0 0 L10 5 L0 10 z" fill="#232D4B" fill-opacity="0.55"/>
    </marker>
  </defs>

  <!-- doorway -->
  <g transform="translate(6,2)">
    <path d="M150 12 V48 M150 68 V104" fill="none" stroke="#232D4B" stroke-opacity="0.42" stroke-width="3.5" stroke-linecap="round"/>
    <path d="M47 44 C92 44 116 52 140 56" fill="none" stroke="#E57200" stroke-width="2" marker-end="url(#smgArrowO)"/>
    <path d="M47 78 C92 78 116 68 140 63" fill="none" stroke="#232D4B" stroke-opacity="0.55" stroke-width="2" marker-end="url(#smgArrowN)"/>
    <circle cx="36" cy="44" r="6.5" fill="#E57200"/>
    <circle cx="36" cy="78" r="6.5" fill="#232D4B" fill-opacity="0.7"/>
    <text x="93" y="124" text-anchor="middle" font-size="10.5" fill="#232D4B">doorway</text>
  </g>

  <!-- corridor -->
  <g transform="translate(222,2)">
    <path d="M10 24 H190 M10 86 H190" fill="none" stroke="#232D4B" stroke-opacity="0.42" stroke-width="3.5" stroke-linecap="round"/>
    <path d="M39 44 H118" fill="none" stroke="#E57200" stroke-width="2" marker-end="url(#smgArrowO)"/>
    <path d="M161 66 H82" fill="none" stroke="#232D4B" stroke-opacity="0.55" stroke-width="2" marker-end="url(#smgArrowN)"/>
    <circle cx="28" cy="44" r="6.5" fill="#E57200"/>
    <circle cx="172" cy="66" r="6.5" fill="#232D4B" fill-opacity="0.7"/>
    <text x="100" y="124" text-anchor="middle" font-size="10.5" fill="#232D4B">corridor</text>
  </g>

  <!-- intersection -->
  <g transform="translate(438,2)">
    <path d="M8 24 H84 M124 24 H192 M8 58 H84 M124 58 H192 M84 4 V24 M84 58 V78 M124 4 V24 M124 58 V78" fill="none" stroke="#232D4B" stroke-opacity="0.42" stroke-width="3.5" stroke-linecap="round"/>
    <path d="M41 41 H74" fill="none" stroke="#E57200" stroke-width="2" marker-end="url(#smgArrowO)"/>
    <path d="M104 25 V52" fill="none" stroke="#232D4B" stroke-opacity="0.55" stroke-width="2" marker-end="url(#smgArrowN)"/>
    <circle cx="30" cy="41" r="6.5" fill="#E57200"/>
    <circle cx="104" cy="14" r="6.5" fill="#232D4B" fill-opacity="0.7"/>
    <text x="100" y="124" text-anchor="middle" font-size="10.5" fill="#232D4B">intersection</text>
  </g>
</svg>
</div>

<div class="rl-lede" markdown="0">
<p class="rl-lead">A <a class="rl-term" href="#smg-trivia" title="Where the term comes from"><em>social mini-game</em></a> (SMG) is a short, local interaction in a physically constrained environment in which a few agents (robots and/or humans) compete for a shared space that only one of them can use at a time (e.g. going through doorways, narrow hallways, unsignalized intersections etc.). SMGs exhibit high agency where small actions can significantly change the interaction dynamics, coordination requirements, and potential for deadlocks.</p>

<p>SMGs can be formalized as a multi-agent variation of a spatially constrained, time-optimal, motion planning problem in which a frequent failure mode is the freezing robot problem in which robots stop moving because every available motion looks unsafe.</p>

<p class="rl-pull">Humans solve SMGs quickly, without speaking and usually without slowing down much. We want robots to do the same, and we want to be able to prove that they will.</p>

<p class="rl-openlabel">The following are some exciting open problems in robotics and autonomy towards solving SMGs:</p>

<ol class="rl-open">
  <li><span class="rl-q">What sort of guarantees can we give to SMG solvers?</span> e.g. safety? goal-reaching (task completion)? realtime? min-time? robustness/generalizability? scalability? And to what extent do we need to relax the taxonomy/assumptions to ensure these guarantees?</li>
  <li><span class="rl-q">What role does physical AI play in solving SMGs</span> and how do we integrate reasoning and classical control-theoretic approaches in a closed-loop feedback mechanism, especially when solving SMGs with underactuated systems like humanoid robots?</li>
  <li><span class="rl-q">What does it take to solve SMGs that involve humans?</span> How can SMG solvers take human irrationality into account? Also, how do we trade off between social compliance and safety around humans?</li>
  <li><span class="rl-q">Is there a unifying connection between different approaches to solving SMGs?</span> for example, can MARL, MAPF, dynamic game theory, and trajectory optimization be reduced to a &ldquo;master&rdquo; algorithm?</li>
</ol>

<div class="rl-trivia-row">
<aside class="rl-trivia" id="smg-trivia">
<span class="rl-trivia-label">Fun Trivia</span>
<p>The term &ldquo;Social Mini-Game&rdquo; was coined by Prof. Joydeep Biswas. Prof. Chandra was a postdoc in Joydeep&rsquo;s lab (2022-24) and was the lead researcher on SMGs. Since then, Prof. Chandra:</p>
<ol class="rl-trivia-list">
  <li>Published two journal research papers on SMGs which (1) establish the problem formally and (2) survey the literature on multi-robot systems in the context of SMGs.</li>
  <li>Designed the first graduate level course focusing on SMGs.</li>
  <li>Established a program that currently conducts active research in SMGs at four<span class="rl-nowrap">&nbsp;levels.&nbsp;<svg class="rl-pointer" viewBox="0 0 46 14" aria-hidden="true" focusable="false"><path d="M1 7 H33" fill="none" stroke="#E57200" stroke-width="2" stroke-linecap="round"/><path d="M31 1.5 L42 7 L31 12.5 Z" fill="#E57200"/></svg></span></li>
</ol>
</aside>

<div class="rl-stack" role="img" aria-label="The four levels we work at: AI at the top, then planning, then control, all resting on a foundation of datasets, simulators, and surveys.">
<span class="rl-stack-label" aria-hidden="true">How CRΔL solves SMG problems</span>
<div class="rl-stack-cards" aria-hidden="true">
  <div class="rl-level">
    <span class="rl-level-name">AI</span>
    <span class="rl-level-note">vision-language models and LLM dialogue read the context</span>
  </div>
  <span class="rl-level-link"></span>
  <div class="rl-level">
    <span class="rl-level-name">Planning</span>
    <span class="rl-level-note">games, auctions, and inverse RL decide who goes first</span>
  </div>
  <span class="rl-level-link"></span>
  <div class="rl-level">
    <span class="rl-level-name">Control</span>
    <span class="rl-level-note">barrier functions keep robots safe and still moving</span>
  </div>
  <span class="rl-level-link"></span>
  <div class="rl-level">
    <span class="rl-level-name">Datasets &#183; Simulators &#183; Surveys</span>
    <span class="rl-level-note">definitions, benchmarks, and open code</span>
  </div>
</div>
<!-- <p class="rl-figcaption">The three method layers all rest on the shared definitions, benchmarks, and code at the base.</p> -->
</div>
</div>

<div class="rl-section">
<span class="rl-kicker">01</span>
<h3>Control</h3>
<!-- <p>Control is where safety and liveness objectives collide. A controller has to guarantee that robots never collide with an obstacle, and also that they never enter a deadlock. The second guarantee is the hard one, because the standard tool for the first &mdash; the control barrier function &mdash; is precisely what makes robots freeze in tight spaces. Give every robot the same safety margin in a doorway and the safest option for all of them is to wait.</p> -->
<!-- <p>Our approach is to make the barrier itself adaptive. Rather than a fixed margin that everyone respects equally, the margin shifts with the situation, so one robot gives way slightly and the group keeps moving. The resulting controllers are safe, deadlock-free, and fully decentralized: no robot has to talk to any other.</p> -->

<ul class="rl-papers">
  <li>
    <a class="rl-name" href="https://doi.org/10.1007/s10514-025-10194-8">Deadlock-free, Safe, and Decentralized Multi-Robot Navigation via Discrete-Time CBFs</a>
    <span class="rl-venue">Autonomous Robots 2025</span>
    <p>Our main result on this question. We formulate social mini-games in discrete time and derive barrier functions that certify collision avoidance and rule out deadlock at the same time, with no communication between robots.</p>
  </li>
  <li>
    <a class="rl-name" href="https://arxiv.org/abs/2412.04659">LiveNet</a>
    <span class="rl-venue">L4DC 2025</span>
    <p>A single neural controller that handles safety, liveness, and robustness together, and that intervenes on the nominal plan as little as it can. The robot deviates only where the interaction actually requires it.</p>
    <p class="rl-extra"><a href="https://livenet-uva.github.io/">project page</a></p>
  </li>
  <li>
    <a class="rl-name" href="https://arxiv.org/abs/2503.13098">LivePoint</a>
    <span class="rl-venue">Under Review</span>
    <p>Takes the same guarantees to high-dimensional inputs. The controller runs directly on dense observations instead of a clean state estimate, and stays fully decentralized in cluttered environments.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/ICRA55743.2025.11128344">MA-ICBF: Decentralized Safe and Scalable Multi-Agent Control under Limited Actuation</a>
    <span class="rl-venue">ICRA 2025</span>
    <p>Real robots have bounded actuators, and most safety guarantees quietly assume they do not. This work learns neural integral control barrier functions that respect input limits, and scales to large teams.</p>
    <p class="rl-extra"><a href="https://maicbf.github.io/">project page</a></p>
  </li>
  <li>
    <a class="rl-name" href="https://arxiv.org/abs/2511.14024">FACA: Fair and Agile Multi-Robot Collision Avoidance with Dynamic Priorities</a>
    <span class="rl-venue">Preprint</span>
    <p>Yielding is also a fairness problem. If the controller always picks the same robot to give way, the team is still safe, but one robot pays for everyone else's progress. FACA assigns priorities that change over time, so the cost of yielding is spread across the team without giving up agility. It is the control-side answer to the question <a href="#ai">GameChat</a> asks in language.</p>
  </li>
</ul>
</div>

<div class="rl-section">
<span class="rl-kicker">02</span>
<h3>Planning</h3>
<!-- <p>Planning answers a different question. Not how to move safely, but <em>who goes first</em>. Once you accept that the other agents are self-interested &mdash; a person in a hurry takes the doorway and does not wait to be assigned a slot &mdash; ordering stops being a scheduling problem and becomes a game.</p> -->
<!-- <p>We model these situations as games and solve for equilibria that are efficient and that each agent has an incentive to follow.</p> -->

<ul class="rl-papers">
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/LRA.2023.3265169">SocialMAPF</a>
    <span class="rl-venue">RA-L 2023</span>
    <p>Classical multi-agent path finding assumes agents execute whatever plan they are handed. SocialMAPF drops that assumption: agents are strategic, so we compute an ordering each agent has an incentive to follow, fast enough to run online.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/LRA.2022.3144516">GamePlan</a>
    <span class="rl-venue">RA-L 2022</span>
    <p>Game-theoretic ordering for human drivers at intersections, roundabouts, and merges. Priority is settled by an auction among the drivers rather than by a central authority, which is closer to how these situations actually resolve.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/ICRA46639.2022.9811865">Game-Theoretic Planning among Risk-Aware Human Drivers</a>
    <span class="rl-venue">ICRA 2022</span>
    <p>Humans differ in how much risk they will take, and a planner that assumes the average human fails against the tails. We make risk preference an explicit parameter of the game, so the robot's plan degrades gracefully when the other driver is more aggressive than expected.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/ITSC55140.2022.9921968">GameOpt</a>
    <span class="rl-venue">ITSC 2022</span>
    <p>Real-time priority assignment and control at unsignalized intersections with mixed traffic, where no signal exists to impose an order and the agents must find one themselves.</p>
  </li>
  <li>
    <a class="rl-name" href="https://arxiv.org/abs/2405.16430">GameOpt+</a>
    <span class="rl-venue">MRS 2025</span>
    <p>Adds fuel efficiency to the objective. Ordering that is optimal for throughput is not automatically optimal for energy, and at an intersection the gap between the two is measurable.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/IROS60139.2025.11247542">Multi-Agent Inverse RL in Real-World Unstructured Pedestrian Crowds</a>
    <span class="rl-venue">IROS 2025</span>
    <p>All of the above needs reward functions, and hand-designing them is guesswork. Here we recover them from real pedestrian crowds instead &mdash; a multi-agent inverse RL problem in which none of the behavior is labeled and the crowd is genuinely unstructured.</p>
  </li>
</ul>
</div>

<div class="rl-section" id="ai">
<span class="rl-kicker">03</span>
<h3>AI</h3>
<!-- <p>Safety and ordering are still not enough. The right answer in a hallway depends on things a controller cannot observe: who is carrying something heavy, who is on a deadline, who has the harder time stopping and starting again. That information is semantic, and it is exactly what large vision and language models are good at supplying.</p> -->
<!-- <p>Our position is that these models should inform the controller, not replace it. The guarantee keeps coming from the barrier function or the game; the model only supplies the context that sets its parameters.</p> -->

<ul class="rl-papers">
  <li>
    <a class="rl-name" href="https://arxiv.org/abs/2603.21142">Dynamic Control Barrier Function Regulation with Vision-Language Models</a>
    <span class="rl-venue">Under Review</span>
    <p>A VLM watches the scene and tunes the barrier function online. The safety certificate still comes from the CBF; the model only decides how conservative to be, and does it fast enough to stay in the control loop.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1109/MRS66243.2025.11357267">GameChat</a>
    <span class="rl-venue">MRS 2025</span>
    <p>Robots negotiate in natural language. Each robot runs its own LLM, they exchange a short dialogue about whose task is more urgent, and they agree on an order. The outcome is socially optimal rather than merely collision-free: a robot with nothing to deliver yields to one that is running late. GameChat argues for priority in language; <a href="https://arxiv.org/abs/2511.14024">FACA</a> enforces it in the controller and keeps it fair over repeated encounters.</p>
    <p class="rl-extra"><a href="https://gamechat-uva.github.io/">project page</a></p>
  </li>
</ul>
</div>

<div class="rl-section">
<span class="rl-kicker">04</span>
<h3>Datasets, Simulators, and Surveys</h3>
<!-- <p>None of this is worth much if no one else can reproduce it, and for a long time social navigation had no shared definition of what it was even trying to do. A good part of our effort goes into the common infrastructure: the taxonomy, the evaluation protocol, the simulator, and the code.</p> -->

<ul class="rl-papers">
  <li>
    <a class="rl-name" href="https://doi.org/10.1007/s10514-026-10251-w">Multi-Robot Navigation in Social Mini-Games: Definitions, Taxonomy, and Algorithms</a>
    <span class="rl-venue">Autonomous Robots 2026</span>
    <p>Where the term comes from, what counts as one, and how the existing algorithms relate to each other. This is the best single entry point to everything on this page.</p>
    <p class="rl-extra"><a href="https://socialminigames.github.io/">project page</a> <a href="https://arxiv.org/abs/2508.13459">arXiv</a></p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1145/3700599">Principles and Guidelines for Evaluating Social Robot Navigation Algorithms</a>
    <span class="rl-venue">ACM THRI 2025</span>
    <p>A community effort across more than twenty groups on what social navigation should be measured against. Much of the disagreement in the field turns out to be disagreement about metrics.</p>
  </li>
  <li>
    <a class="rl-name" href="https://doi.org/10.1609/aaai.v38i21.30562">SocialGym 2.0</a>
    <span class="rl-venue">AAAI 2024</span>
    <p>A simulator for multi-robot learning and navigation in shared human spaces, built so that policies can be trained and compared on the same scenarios.</p>
  </li>
  <li>
    <a class="rl-name" href="https://github.com/CRAL-UVA/SMGLib">SMGLib</a>
    <span class="rl-venue">Open Source</span>
    <p>Our open implementation of the social mini-game scenarios and the baselines that solve them. We use it in our own papers and in the graduate multi-robot navigation course.</p>
  </li>
</ul>
</div>

<script>
// In-page links scroll to their target without leaving the fragment in the URL,
// so a refresh reloads /social-mini-games/ at the top rather than jumping back.
(function () {
  var motion = window.matchMedia('(prefers-reduced-motion: reduce)');

  function flash(el) {
    el.classList.add('rl-flash');
    window.setTimeout(function () { el.classList.remove('rl-flash'); }, 2200);
  }

  function clearHash() {
    if (window.history && history.replaceState) {
      history.replaceState(null, '', window.location.pathname + window.location.search);
    }
  }

  document.addEventListener('click', function (e) {
    var link = e.target && e.target.closest ? e.target.closest('a[href^="#"]') : null;
    if (!link || link.getAttribute('href') === '#') return;

    var target = document.getElementById(link.getAttribute('href').slice(1));
    if (!target) return;

    e.preventDefault();
    target.scrollIntoView({ behavior: motion.matches ? 'auto' : 'smooth', block: 'start' });
    flash(target);
    clearHash();
  });

  // Arriving on a link that already carries a fragment: let the browser do its
  // jump, then drop the fragment so a refresh behaves like a plain visit.
  if (window.location.hash.length > 1) {
    var landed = document.getElementById(window.location.hash.slice(1));
    if (landed) {
      flash(landed);
      window.setTimeout(clearHash, 0);
    }
  }
})();
</script>
