---
title: "Research Testbeds"
layout: single
permalink: /testbeds/
author_profile: true
classes: wide
---

<style>
.page__title {
    color: #494e52 !important;
    font-weight: bold;
}

.page__content {
   font-size: 1em;
   color: #494e52;
}

.testbed-intro {
   font-size: 1em;
   color: #494e52;
   margin-bottom: 2em;
}

.testbed-item {
   font-size: 1em;
   color: #494e52;
   margin-bottom: 1.5em;
}

.testbed-title {
   font-size: 1.2em;
   font-weight: bold;
   color: #494e52;
   margin-bottom: 1em;
}

h1.page__title {
    color: #494e52 !important;
    font-weight: bold;
}

.page__title.p-name {
    color: #494e52 !important;
    font-weight: bold;
}

.page__title a {
    color: #494e52 !important;
    text-decoration: none;
}
</style>

<div class="testbed-intro">
In addition to publishing research papers, I contribute to the development of realistic testbeds and digital twins to bridge theoretical insights with practical applications. My work spans critical domains, including water treatment plants, chemical plants, and multi-robot swarm navigation and communication. These efforts focus on enhancing system resilience, mitigating vulnerabilities, and closing the sim-to-real gap in industrial control systems (ICS) and cyber-physical systems (CPS).
</div>

<div class="testbed-item">
<div class="testbed-title">
ICS testbed on minimega [<a href="https://www.sandia.gov/">Sandia</a> partnership]
</div>
</div>
<p align="center" style="margin-top: 10px; margin-bottom: 10px;">
<img src="/assets/images/sandia2.jpg" height="150" width="300">
<br>
</p>
<div class="testbed-intro">
I led a collaborative project with Sandia National Labs to deploy and test cyber emulation tools on SOL4CE (Scalable Open Laboratory for Cyber Experimentation). Our team developed virtual environments for analyzing industrial control systems, focusing on two key case studies: a chemical plant simulator and manufacturing plants. We successfully identified and demonstrated critical vulnerabilities, including sensor spoofing attacks and control channel exploits. The project utilized Sceptre, a framework combining Minimega for VM orchestration and Phenix for configuration management. By implementing these testbeds in a controlled virtual environment, we enabled safe testing of security scenarios without risking physical infrastructure. This work advances our understanding of ICS vulnerabilities while providing a platform for future cybersecurity research and training.
<br>
[<a href="https://www.cerias.purdue.edu/research/projects/home/detail/339/deploying_cyber_emulation_modeling_and_analysis_tools_on_the_sol4ce">Project</a>]
</div>

<div class="testbed-item">
<div class="testbed-title">
Chemical Plant and Water Treatment Plant [<a href="https://action.ucsb.edu/">NSF ACTION GATE</a>]
</div>
</div>
<div style="display: flex; justify-content: space-between; margin: 20px 0;">
  <div style="width: 48%;">
      <video width="100%" height="300" controls preload="auto" poster="/assets/images/image1.png">
          <source src="/assets/images/video1.mp4" type="video/mp4">
      </video>
      <p align="center" style="color: #494e52;">Attack Agent</p>
  </div>
  <div style="width: 48%;">
      <video width="100%" height="300" controls preload="auto" poster="/assets/images/image2.png">
          <source src="/assets/images/video2.mp4" type="video/mp4">
      </video>
      <p align="center" style="color: #494e52;">Defense Agent</p>
  </div>
</div>
<div class="testbed-intro">
In collaboration with researchers at UCSB and Purdue, I led the development of GATE, an AWS-based test environment for evaluating industrial control systems (ICS) security research. GATE features a digital twin of two critical components: a chemical plant simulating hazardous exothermic reactions, and a water treatment plant with PLC-controlled water purification processes. Our team created an environment that enables researchers to safely validate attack detection mechanisms, test defense strategies, and evaluate security tools in a controlled setting that accurately replicates real industrial processes.
</div>

<div class="testbed-item">
<div class="testbed-title">
Distributed Robot Swarm Simulation [<a href="https://www.purdue.edu/computes/aida3/">AIDA3</a>]
</div>
</div>
<p align="center" style="margin-top: 10px; margin-bottom: 10px;">
<img src="/assets/images/swarm.jpg" height="300" width="600">
<br>
</p>
<div class="testbed-intro">
We developed a distributed robot swarm simulation framework by extending a single-UAV simulator to support multi-robot systems. The framework integrates Gazebo's physics engine with PX4 Autopilot, enabling high-fidelity physics simulation with accurate sensor noise, dynamics, and environmental interactions. Our implementation uses ROS topics for inter-robot communication and adds support for dynamic waypoints using multiple collision avoidance algorithms. Written in Python and C++, the framework effectively simulates environmental changes, vehicle dynamics, and real-time communication between robots in swarm scenarios.
</div>