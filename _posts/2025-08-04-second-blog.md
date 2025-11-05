---
title: "Breaking LLM Agents"
layout: blog
permalink: /blogs/llm-agents/
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

.page__content .blog-image {
    text-align: center;
    margin: 1.5em 0;
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
    <p>As LLM agents spread into products and embodied systems, security and privacy risks grow in both scope and impact. Below is a concise field note on threats, defenses, and representative references for agentic systems across chat and robotics.</p>

    <div class="blog-section-title">Papers published in this domain</div>
    
    <style>
    .papers-table {
        width: 100%;
        max-width: 100%;
        border-collapse: collapse;
        margin: 1.5em 0;
        background-color: #2d2d2d;
        color: #ffffff;
        font-size: 0.95em;
        table-layout: fixed;
    }
    
    .papers-table th {
        background-color: #1a1a1a;
        color: #ffffff;
        padding: 12px 15px;
        text-align: left;
        font-weight: bold;
        border-bottom: 2px solid #444;
    }
    
    .papers-table th.sortable {
        cursor: pointer;
        user-select: none;
        position: relative;
    }
    
    .papers-table th.sortable:hover {
        background-color: #252525;
    }
    
    .papers-table th.sortable .sort-arrow {
        display: inline-block;
        margin-left: 5px;
        font-size: 0.8em;
        color: #888;
        transition: color 0.2s;
    }
    
    .papers-table th.sortable:hover .sort-arrow {
        color: #ffffff;
    }
    
    .papers-table th.sortable.sorted-asc .sort-arrow::after {
        content: "▲";
        color: #4a9eff;
    }
    
    .papers-table th.sortable.sorted-desc .sort-arrow::after {
        content: "▼";
        color: #4a9eff;
    }
    
    .papers-table th.sortable .sort-arrow::after {
        content: "⇅";
    }
    
    .papers-table th:nth-child(1) {
        width: 12%;
    }
    
    .papers-table th:nth-child(2) {
        width: 15%;
    }
    
    .papers-table th:nth-child(3) {
        width: 18%;
    }
    
    .papers-table th:nth-child(4) {
        width: 40%;
    }
    
    .papers-table th:nth-child(5) {
        width: 10%;
    }
    
    .papers-table td {
        padding: 12px 15px;
        border-bottom: 1px solid #444;
        word-wrap: break-word;
        overflow-wrap: break-word;
    }
    
    .papers-table td:nth-child(1) {
        width: 12%;
    }
    
    .papers-table td:nth-child(2) {
        width: 15%;
    }
    
    .papers-table td:nth-child(3) {
        width: 18%;
    }
    
    .papers-table td:nth-child(4) {
        width: 40%;
    }
    
    .papers-table td:nth-child(5) {
        width: 10%;
    }
    
    .papers-table td:last-child {
        padding-right: 15px;
    }
    
    .papers-table a {
        color: #4a9eff;
        text-decoration: underline;
        word-break: break-all;
    }
    
    .papers-table tr:hover {
        background-color: #3a3a3a;
    }
    
    .papers-table a:hover {
        color: #6bb3ff;
    }
    
    .papers-table .code-cell {
        color: #888;
    }
    
    .papers-table-wrapper {
        width: 100%;
        max-width: 100%;
        overflow-x: auto;
        margin: 1.5em 0;
        box-sizing: border-box;
    }
    </style>
    
    <div class="papers-table-wrapper">
        <table class="papers-table">
            <thead>
                <tr>
                    <th class="sortable" id="sort-date">Publish Date<span class="sort-arrow"></span></th>
                    <th>Title</th>
                    <th>Authors</th>
                    <th>PDF</th>
                    <th>Code</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>2025-01-28</td>
                    <td>Context is Key for Agent Security</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2501.17070">2501.17070</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-03-26</td>
                    <td>ShieldAgent: Shielding Agents via Verifiable Safety Policy Reasoning</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2503.22738">2503.22738</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-05-08</td>
                    <td>AirGapAgent: Protecting Privacy-Conscious Conversational Agents</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2405.05175">2405.05175</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-10-17</td>
                    <td>RoboPair</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2410.13691">2410.13691</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-03-10</td>
                    <td>RoboGuard</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2503.07885">2503.07885</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-04-15</td>
                    <td>CEE</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2504.13201">2504.13201</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-09-27</td>
                    <td>Preventing Robotic Jailbreaking via Multimodal Domain Adaptation</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2509.23281">2509.23281</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-08-23</td>
                    <td>Mind the Gap: Time-of-Check to Time-of-Use Vulnerabilities in LLM-Enabled Agents</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2508.17155">2508.17155</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-03-28</td>
                    <td>JailbreakBench</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2404.01318">2404.01318</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-02-06</td>
                    <td>HarmBench: A Standardized Evaluation Framework for Automated Red Teaming and Robust Refusal</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2402.04249">2402.04249</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-05-13</td>
                    <td>RobustNav</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2106.04531">2405.07890</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-11-04</td>
                    <td>AgentHarm</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2410.09024">2410.09024</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-10-09</td>
                    <td>ST-WebAgentBench: A Benchmark for Evaluating Safety and Trustworthiness in Web Agents</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2410.06703">2410.06703</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-09-09</td>
                    <td>AbstentionBench: Reasoning LLMs Fail on Unanswerable Questions</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2409.05678">2409.05678</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-08-19</td>
                    <td>ARE Meta</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2408.09876">2408.09876</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-08-23</td>
                    <td>Mind the Gap: Time-of-Check to Time-of-Use Vulnerabilities in LLM-Enabled Agents</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2508.17155">2508.17155</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-06-08</td>
                    <td>Adversarial Attacks on Robotic Vision Language Action Models</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2406.05432">2406.05432</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-07-18</td>
                    <td>TAP</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">TBD</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-07-02</td>
                    <td>GCG</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2307.15043">2307.15043</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-04-17</td>
                    <td>TurkingBench</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2403.11905">2404.11234</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-03-14</td>
                    <td>Google's Approach to Protecting Privacy In the Age of AI</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://research.google/pubs/googles-approach-to-protecting-privacy-in-the-age-of-ai/">Link</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-09-27</td>
                    <td>Securing MCP-based Agent Workflows</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">TBD</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-05-27</td>
                    <td>Dolphins</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://research.nvidia.com/labs/avg/publication/ma.cao.etal.arxiv2023/">Link</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-08-16</td>
                    <td>Sound Image Perturb</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">TBD</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-10-04</td>
                    <td>Multimodal Adv Training</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">TBD</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-07-02</td>
                    <td>BrowserArena: Evaluating LLM Agents on Real-World Web Navigation Tasks</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2407.02421">2407.02421</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-03-07</td>
                    <td>Chatbot Arena: An Open Platform for Evaluating LLMs by Human Preference</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2403.04132">2403.04132</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-09-30</td>
                    <td>CHAI: Command Hijacking against embodied AI</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2510.00181">2510.00181</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-09-29</td>
                    <td>SecInfer: Preventing Prompt Injection via Inference-time Scaling</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2509.24967">2509.24967</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-10-01</td>
                    <td>WAInjectBench: Benchmarking Prompt Injection Detections for Web Agents</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2510.01354">2510.01354</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-09-09</td>
                    <td>Adversarial Attacks on Robotic Vision Language Action Models</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2506.03350">2409.05678</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-08-30</td>
                    <td>OmniVLA: An Omni-Modal Vision-Language-Action Model for Robot Navigation</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">TBD</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-07-11</td>
                    <td>NaviLA</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">TBD</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-12-04</td>
                    <td>Emerging Risks from Embodied AI Require Urgent Policy Action</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2509.00117">2509.00117</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-06-20</td>
                    <td>RoboCop: A Robust Zero-Day Cyber-Physical Attack Detection Framework for Robots</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://ieeexplore.ieee.org/document/10802522">2406.14789</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-11-10</td>
                    <td>RoboGuardZ: A Scalable Zero-Shot Framework for Detecting Zero-Day Malware in Robots</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://beerkay.github.io/papers/Berkay2024RoboGuardzIROS.pdf">Link</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-03-11</td>
                    <td>Google Semantic Safety</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2503.08663">2503.08663</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-09-05</td>
                    <td>Vision-Language-Action Models for Robotics: A Review Towards Real-World Applications</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">TBD</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-03-18</td>
                    <td>GROOT1</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2503.14734">2503.14734</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-08-06</td>
                    <td>Simulation Control Visual SysID</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">TBD</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-09-25</td>
                    <td>Can AI Perceive Physical Danger and Intervene?</td>
                    <td>Author Name et.al.</td>
                    <td><a href="https://arxiv.org/abs/2509.21651">2509.21651</a></td>
                    <td class="code-cell">null</td>
                </tr>
            </tbody>
        </table>
    </div>
    
    <script>
    (function() {
        const sortHeader = document.getElementById('sort-date');
        const table = document.querySelector('.papers-table');
        const tbody = table.querySelector('tbody');
        let sortDirection = 'desc'; // Start with descending (newest first)
        
        // Set initial sort to descending
        sortHeader.classList.add('sorted-desc');
        sortTable();
        
        sortHeader.addEventListener('click', function() {
            // Toggle sort direction
            sortDirection = sortDirection === 'asc' ? 'desc' : 'asc';
            
            // Update header classes
            sortHeader.classList.remove('sorted-asc', 'sorted-desc');
            sortHeader.classList.add(sortDirection === 'asc' ? 'sorted-asc' : 'sorted-desc');
            
            // Sort the table
            sortTable();
        });
        
        function sortTable() {
            const rows = Array.from(tbody.querySelectorAll('tr'));
            
            rows.sort((a, b) => {
                const dateA = a.cells[0].textContent.trim();
                const dateB = b.cells[0].textContent.trim();
                
                if (sortDirection === 'asc') {
                    return dateA.localeCompare(dateB);
                } else {
                    return dateB.localeCompare(dateA);
                }
            });
            
            // Remove all rows and re-add them in sorted order
            rows.forEach(row => tbody.removeChild(row));
            rows.forEach(row => tbody.appendChild(row));
        }
    })();
    </script>
</div>