---
layout: default
title: Model Card
---

<style>
/* Model Card Styles */
.model-card {
    max-width: 900px;
    margin: 0 auto;
}

.mc-header {
    text-align: center;
    margin-bottom: 1.2em;
    padding-bottom: 0.8em;
    border-bottom: 2px solid #e2e8f0;
}

.mc-header h1 {
    font-size: 1.6em;
    color: #1a365d;
    margin-bottom: 0.2em;
    font-weight: 700;
}

.mc-header .tagline {
    color: #64748b;
    font-size: 0.95em;
    margin-bottom: 0.4em;
}

.mc-header .version {
    display: inline-block;
    background: #1a365d;
    color: #fff;
    font-size: 0.7em;
    padding: 0.15em 0.5em;
    border-radius: 4px;
    font-family: monospace;
}

.mc-section {
    margin-bottom: 1.5em;
}

.mc-section h2 {
    font-size: 0.95em;
    color: #1a365d;
    margin-bottom: 0.6em;
    padding-bottom: 0.3em;
    border-bottom: 1px solid #e2e8f0;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.05em;
}

/* Leadership Quadrant */
.quadrant-container {
    display: flex;
    justify-content: center;
    margin: 1.5em 0 0.5em;
}

.quadrant {
    position: relative;
    width: 280px;
    height: 280px;
    border: 2px solid #cbd5e1;
    border-radius: 8px;
    background: #fff;
}

.quadrant-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    height: 100%;
}

.quadrant-cell {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 1em;
    text-align: center;
    border: 1px solid #e2e8f0;
}

.quadrant-cell .label {
    font-weight: 600;
    font-size: 0.95em;
    color: #1e40af;
    margin-bottom: 0.3em;
}

.quadrant-cell .desc {
    font-size: 0.75em;
    color: #64748b;
}

.quadrant-marker {
    position: absolute;
    width: 14px;
    height: 14px;
    background: rgba(234, 88, 12, 0.7);
    border: 2px solid rgba(255,255,255,0.8);
    border-radius: 50%;
    box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    top: 53%;
    left: 72%;
    transform: translate(-50%, -50%);
    z-index: 10;
}

.quadrant-axes {
    position: absolute;
    width: 100%;
    height: 100%;
    pointer-events: none;
}

.axis-label {
    position: absolute;
    font-size: 0.7em;
    color: #94a3b8;
    text-transform: uppercase;
    letter-spacing: 0.05em;
}

.axis-label.top { top: -20px; left: 50%; transform: translateX(-50%); }
.axis-label.bottom { bottom: -20px; left: 50%; transform: translateX(-50%); }
.axis-label.left { left: -60px; top: 50%; transform: translateY(-50%) rotate(-90deg); }
.axis-label.right { right: -60px; top: 50%; transform: translateY(-50%) rotate(90deg); }

/* Training Data Cards */
.training-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1em;
}

.training-card {
    background: #fff;
    border: 1px solid #e2e8f0;
    border-radius: 8px;
    padding: 0.8em;
}

.training-card h3 {
    font-size: 0.75em;
    color: #64748b;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    margin-bottom: 0.6em;
    padding-bottom: 0.3em;
    border-bottom: 1px solid #e2e8f0;
}

.training-card table {
    width: 100%;
    font-size: 0.8em;
}

.training-card td {
    padding: 0.25em 0;
    vertical-align: top;
}

.training-card td:first-child {
    font-weight: 600;
    color: #475569;
    width: 35%;
}

.training-card td:last-child {
    color: #64748b;
}

/* Feature Importance */
.feature-chart {
    background: #fff;
    border: 1px solid #e2e8f0;
    border-radius: 8px;
    padding: 0.8em;
}

.feature-row {
    display: flex;
    align-items: center;
    margin-bottom: 0.5em;
}

.feature-row:last-child {
    margin-bottom: 0;
}

.feature-label {
    width: 150px;
    font-size: 0.8em;
    color: #475569;
    flex-shrink: 0;
}

.feature-bar-container {
    flex: 1;
    height: 18px;
    background: #f1f5f9;
    border-radius: 4px;
    margin-right: 0.8em;
    overflow: hidden;
}

.feature-bar {
    height: 100%;
    background: linear-gradient(90deg, #3b82f6, #1d4ed8);
    border-radius: 4px;
}

.feature-value {
    width: 35px;
    font-size: 0.8em;
    font-weight: 600;
    color: #1e40af;
    text-align: right;
}

.feature-desc {
    font-size: 0.7em;
    color: #94a3b8;
    margin-left: 150px;
    margin-top: -0.3em;
    margin-bottom: 0.4em;
}

/* Model Comparison */
.model-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 0.8em;
}

.model-card-item {
    background: #fff;
    border: 1px solid #e2e8f0;
    border-radius: 8px;
    padding: 0.8em;
    transition: all 0.2s;
}

.model-card-item:hover {
    box-shadow: 0 4px 12px rgba(0,0,0,0.08);
}

.model-card-item .model-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 0.4em;
}

.model-card-item .model-name {
    font-weight: 600;
    color: #1e40af;
    font-size: 0.9em;
}

.model-card-item .fit-badge {
    font-size: 0.65em;
    padding: 0.15em 0.4em;
    border-radius: 4px;
    background: #f1f5f9;
    color: #64748b;
}

.model-card-item p {
    font-size: 0.75em;
    color: #64748b;
    margin-bottom: 0.3em;
}

.model-card-item .strengths {
    color: #059669;
}

.model-card-item .weaknesses {
    color: #dc2626;
}

/* Regularization */
.regularization-box {
    background: linear-gradient(135deg, #f0fdf4 0%, #dcfce7 100%);
    border: 1px solid #86efac;
    border-radius: 8px;
    padding: 0.8em;
}

.regularization-box ul {
    list-style: none;
    font-size: 0.75em;
    padding: 0;
    margin: 0;
}

.regularization-box li {
    padding: 0.2em 0;
    color: #475569;
}

.regularization-box li strong {
    color: #166534;
}

/* Limitations */
.limitations-box {
    background: #fff;
    border: 1px solid #fecaca;
    border-left: 4px solid #ef4444;
    border-radius: 8px;
    padding: 0.8em;
}

.limitations-box ul {
    list-style: none;
    font-size: 0.75em;
    color: #64748b;
    padding: 0;
    margin: 0;
}

.limitations-box li {
    padding: 0.2em 0;
}

.limitations-box li::before {
    content: "⚠ ";
    color: #ef4444;
}

/* Intended Use */
.use-cases {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4em;
}

.use-tag {
    background: #eff6ff;
    color: #1e40af;
    padding: 0.3em 0.6em;
    border-radius: 20px;
    font-size: 0.75em;
    border: 1px solid #bfdbfe;
}

/* Responsive */
@media (max-width: 700px) {
    .training-grid, .model-grid {
        grid-template-columns: 1fr;
    }
    .quadrant {
        width: 240px;
        height: 240px;
    }
    .quadrant-cell .label {
        font-size: 0.8em;
    }
    .quadrant-cell .desc {
        font-size: 0.65em;
    }
    .quadrant-marker {
        top: 53%;
        left: 72%;
        width: 10px;
        height: 10px;
    }
    .feature-label {
        width: 100px;
    }
    .feature-desc {
        margin-left: 100px;
    }
}
</style>

<div class="model-card">
    
<!-- Header -->
<header class="mc-header">
    <h1>Model Card: Patrick Long</h1>
    <div class="tagline">Healthcare AI • Neuroscience • Leadership</div>
    <span class="version">v2025.1</span>
</header>

<!-- Leadership Style -->
<section class="mc-section">
    <h2>Leadership Style</h2>
    <div class="quadrant-container">
        <div class="quadrant">
            <div class="quadrant-axes">
                <span class="axis-label top">Task Oriented</span>
                <span class="axis-label bottom">People Oriented</span>
                <span class="axis-label left">Introvert</span>
                <span class="axis-label right">Extrovert</span>
            </div>
            <div class="quadrant-grid">
                <div class="quadrant-cell">
                    <span class="label">Analyzer</span>
                    <span class="desc">Introverted, Task-oriented</span>
                </div>
                <div class="quadrant-cell">
                    <span class="label">Director</span>
                    <span class="desc">Extroverted, Task-oriented</span>
                </div>
                <div class="quadrant-cell">
                    <span class="label">Collaborator</span>
                    <span class="desc">Introverted, People-oriented</span>
                </div>
                <div class="quadrant-cell">
                    <span class="label">Promoter</span>
                    <span class="desc">Extroverted, People-oriented</span>
                </div>
            </div>
            <div class="quadrant-marker"></div>
        </div>
    </div>
</section>

<!-- Training Data -->
<section class="mc-section">
    <h2>Training Data</h2>
    <div class="training-grid">
        <div class="training-card">
            <h3>Academia</h3>
            <table>
                <tr><td>PhD</td><td>Neuroscience, University of Vermont</td></tr>
                <tr><td>Postdoc</td><td>Harvard Medical School, University of Michigan Medical School</td></tr>
                <tr><td>Domain</td><td>Brain development, myelination, glioblastoma</td></tr>
                <tr><td>Methods</td><td>Molecular biology, translational research</td></tr>
            </table>
        </div>
        <div class="training-card">
            <h3>Industry</h3>
            <table>
                <tr><td>Current</td><td>Director, AI Engineering @ IQVIA</td></tr>
                <tr><td>Team</td><td>Global team (US, UK, India)</td></tr>
                <tr><td>Domain</td><td>Real-world data (claims, EHR)</td></tr>
                <tr><td>Therapeutics</td><td>Rare disease, oncology, metabolic, CNS</td></tr>
                <tr><td>Prior</td><td>Tech transfer, biotech consulting</td></tr>
            </table>
        </div>
    </div>
</section>

<!-- Feature Importance -->
<section class="mc-section">
    <h2>Feature Importance</h2>
    <div class="feature-chart">
        <div class="feature-row">
            <span class="feature-label">Scientific Thinking</span>
            <div class="feature-bar-container">
                <div class="feature-bar" style="width: 100%;"></div>
            </div>
            <span class="feature-value">0.30</span>
        </div>
        <div class="feature-desc">First-principles reasoning, mechanistic understanding</div>
        
        <div class="feature-row">
            <span class="feature-label">Applied Healthcare ML</span>
            <div class="feature-bar-container">
                <div class="feature-bar" style="width: 83%;"></div>
            </div>
            <span class="feature-value">0.25</span>
        </div>
        <div class="feature-desc">Predictive models on real-world clinical data</div>
        
        <div class="feature-row">
            <span class="feature-label">RWD Intuition</span>
            <div class="feature-bar-container">
                <div class="feature-bar" style="width: 67%;"></div>
            </div>
            <span class="feature-value">0.20</span>
        </div>
        <div class="feature-desc">Understanding the data generating process</div>
        
        <div class="feature-row">
            <span class="feature-label">Leadership</span>
            <div class="feature-bar-container">
                <div class="feature-bar" style="width: 50%;"></div>
            </div>
            <span class="feature-value">0.15</span>
        </div>
        <div class="feature-desc">Team building, cross-functional influence</div>
        
        <div class="feature-row">
            <span class="feature-label">Neuroscience Domain</span>
            <div class="feature-bar-container">
                <div class="feature-bar" style="width: 33%;"></div>
            </div>
            <span class="feature-value">0.10</span>
        </div>
        <div class="feature-desc">Expertise in life science and translational research</div>
    </div>
</section>

<!-- Model Architecture Comparison -->
<section class="mc-section">
    <h2>Model Architecture Comparison</h2>
    <div class="model-grid">
        <div class="model-card-item">
            <div class="model-header">
                <span class="model-name">🔮 Transformer/LLM</span>
            </div>
            <p class="strengths">Attends to context across multiple levels: individual, team, business, culture; draws on wide experience (bench → tech transfer → applied AI)</p>
            <p class="weaknesses">Diplomatic tendencies may soften directness; can be verbose</p>
        </div>
        
        <div class="model-card-item">
            <div class="model-header">
                <span class="model-name">🌲 XGBoost</span>
            </div>
            <p class="strengths">Iterative self-improvement; learns from mistakes; sees value in marginal gains</p>
            <p class="weaknesses">Builds intuition through practice rather than upfront; needs to see things play out</p>
        </div>
        
        <div class="model-card-item">
            <div class="model-header">
                <span class="model-name">🕸️ GNN (Graph Neural Network)</span>
            </div>
            <p class="strengths">Relational understanding; leverages connections between people, teams, stakeholders for better outcomes</p>
            <p class="weaknesses">Sensitive to network effects; consensus-building can slow decision-making</p>
        </div>
        
        <div class="model-card-item">
            <div class="model-header">
                <span class="model-name">📈 Linear Regression</span>
            </div>
            <p class="strengths">Reduces complexity for explainability; prioritizes actionable insights</p>
            <p class="weaknesses">Effectiveness varies by context (heteroscedastic); simplicity may mask overconfidence</p>
        </div>
    </div>
</section>

<!-- Regularization -->
<section class="mc-section">
    <h2>Regularization</h2>
    <div class="regularization-box">
        <ul>
            <li><strong>L1 (Sparsity):</strong> Scientific training grounds me in mechanistic thinking, focusing on what's clinically meaningful vs. noise</li>
            <li><strong>L2 (Smoothing):</strong> Working across clinical domains prevents over-specialization</li>
            <li><strong>Dropout:</strong> Rotating across therapeutic areas, methods, and the pre-clinical to clinical spectrum</li>
        </ul>
    </div>
</section>

<!-- Known Limitations -->
<section class="mc-section">
    <h2>Known Limitations</h2>
    <div class="limitations-box">
        <ul>
            <li>Benefits from experienced peers to escape local minima</li>
            <li>May require explicit negative feedback; implicit signals sometimes dropped</li>
            <li>Converges iteratively; flexibility can come at the cost of long-term directional certainty</li>
            <li>Context window limitations on administrative tasks</li>
        </ul>
    </div>
</section>

<!-- Intended Use Cases -->
<section class="mc-section">
    <h2>Best Deployed For</h2>
    <div class="use-cases">
        <span class="use-tag">Building ML teams</span>
        <span class="use-tag">Translating technical ↔ business</span>
        <span class="use-tag">Clinical domain + ML integration</span>
        <span class="use-tag">Patient identification models</span>
    </div>
</section>

</div>
