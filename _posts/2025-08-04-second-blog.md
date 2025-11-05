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
                    <td>2025-04-17</td>
                    <td>Conseca</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">https://arxiv.org/abs/2501.17070</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-03-26</td>
                    <td>ShieldAgent</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">https://arxiv.org/abs/2503.22738</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2024-09-18</td>
                    <td>AirGapAgent</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">https://arxiv.org/abs/2405.05175</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-11-09</td>
                    <td>RoboPair</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">https://arxiv.org/pdf/2410.13691</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-03-10</td>
                    <td>RoboGuard</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">https://arxiv.org/abs/2503.07885</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-07-31</td>
                    <td>CEE</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">https://arxiv.org/html/2504.13201v2</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-09-27</td>
                    <td>J-DAPT</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">https://www.arxiv.org/abs/2509.23281</a></td>
                    <td class="code-cell">null</td>
                </tr>
                <tr>
                    <td>2025-08-23</td>
                    <td>TocTou</td>
                    <td>Author Name et.al.</td>
                    <td><a href="#">https://arxiv.org/abs/2508.17155</a></td>
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