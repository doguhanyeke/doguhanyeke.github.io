---
title: "Adversarial Robotics"
layout: blog
permalink: /blogs/adversarial-robotics/
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
    line-height: 1.5;
}

.page__content .blog-date {
    font-size: 1em;
    color: #7a8288;
    margin-bottom: 1em;
}

.page__content .blog-section {
    margin-bottom: 1.5em;
}

.page__content .blog-section-title {
    font-size: 1.2em;
    font-weight: bold;
    margin-bottom: 0.8em;
    color: #494e52;
}

.page__content .read-time {
    font-size: 1em;
    color: #7a8288; 
    margin-top: 1em;
    margin-bottom: 1.5em;
}

.page__content .read-time-icon {
    margin-right: 0.2em;
}

.page__content p {
    font-size: 1.2em !important;
    line-height: 1.6 !important;
}

.page__content ul,
.page__content li {
    font-size: 1em !important;
    line-height: 1.5 !important;
}
</style>

<div class="blog-section">
    <p>Systematic threat modeling for LLM-controlled robotics.</p>
    <p>Adversaries can influence or control multiple components across the perception–planning–actuation stack. Below is a concise model that distinguishes the robotics setting from conventional chatbot jailbreaks and outlines capabilities and defenses.</p>

    <div class="blog-section-title">Why robotics jailbreaks are different</div>
    <ul>
        <li><strong>Physical actions matter</strong>: What seems “safe” in chat can be unsafe when executed by an embodied robot. A prompt that is benign in text may cause hazardous motion.</li>
        <li><strong>Multimodal inputs</strong>: Beyond text, robots process vision (images/video) and audio (voice→text). Attacks can exploit these additional channels.</li>
        <li><strong>Context dependence</strong>: Safety depends on state and surroundings. Accelerating is fine on an empty path but unsafe with an obstacle ahead.</li>
    </ul>

    <div class="blog-section-title">Attacker inputs</div>
    <ul>
        <li><strong>World perturbations</strong>: Modify the environment or sensors (camera/LiDAR) to mislead perception.</li>
        <li><strong>Adversarial instructions</strong>: Craft text or voice prompts (voice→text) to elicit harmful plans.</li>
    </ul>

    <div class="blog-section-title">Attacker capabilities</div>
    <ul>
        <li><strong>Black-box</strong>: Issue voice/text commands and observe behavior; no access to internal model outputs.</li>
        <li><strong>Gray-box</strong>: Read LLM/VLM outputs (e.g., reasoning traces) but cannot modify the model.</li>
        <li><strong>White-box</strong>: Access to architecture and weights; can tailor gradient-based or prompt-internal attacks.</li>
    </ul>

    <div class="blog-section-title">Defense surfaces</div>
    <ul>
        <li><strong>Input</strong>: Sanitize and rewrite user instructions; filter or verify sensor inputs before planning.</li>
        <li><strong>Model</strong>: Use robust system prompts; fine-tune for safety and constraint adherence (e.g., RLHF, DPO).</li>
        <li><strong>Post-filtering</strong>: Validate and constrain plans/actions with safety checks before execution; provide enforceable guarantees.</li>
    </ul>
</div>