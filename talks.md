---
layout: default
title: Talks
---

<style>
.talks-container {
    max-width: 750px;
    margin: 0 auto;
}

.talk-item {
    padding: 1em 0;
    border-bottom: 1px solid #e2e8f0;
    transition: background 0.2s;
}

.talk-item:hover {
    background: #f8fafc;
    margin: 0 -1em;
    padding: 1em;
    border-radius: 8px;
    border-bottom-color: transparent;
}

.talk-item:last-child {
    border-bottom: none;
}

.talk-header {
    display: flex;
    align-items: center;
    gap: 0.8em;
    margin-bottom: 0.4em;
}

.talk-badge {
    display: inline-block;
    padding: 0.2em 0.6em;
    border-radius: 4px;
    font-size: 0.7em;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.03em;
    flex-shrink: 0;
}

.talk-badge.mit {
    background: #a31f34;
    color: white;
}

.talk-badge.pharmads {
    background: #1a365d;
    color: white;
}

.talk-badge.acm {
    background: #0277bd;
    color: white;
}

.talk-badge.falan {
    background: #2e7d32;
    color: white;
}

.talk-year {
    font-size: 0.8em;
    color: #94a3b8;
}

.talk-title {
    font-weight: 600;
    color: #1a365d;
    margin-bottom: 0.3em;
    font-size: 0.95em;
}

.talk-title a {
    color: #1a365d;
    text-decoration: none;
}

.talk-title a:hover {
    text-decoration: underline;
}

.talk-title a::after {
    content: " ↗";
    font-size: 0.8em;
    color: #94a3b8;
}

.talk-venue {
    font-size: 0.85em;
    color: #64748b;
    margin-bottom: 0.3em;
}

.talk-description {
    font-size: 0.85em;
    color: #64748b;
    margin-top: 0.5em;
    line-height: 1.5;
}

@media (max-width: 600px) {
    .talk-header {
        flex-wrap: wrap;
    }
}
</style>

<div class="talks-container">

<div class="talk-item">
    <div class="talk-header">
        <span class="talk-badge pharmads">PharmaDS</span>
        <span class="talk-year">2026</span>
    </div>
    <div class="talk-title"><a href="https://phds.nestat.org/index.html" target="_blank" rel="noopener"> Identifying High-Risk Asthma Patient Subgroups using Explanation-Guided Clustering</a></div>
    <div class="talk-venue">Pharmaceutical Data Science Conference</div>
    <div class="talk-description">Presented methods on subgroup detection when developing ML models for acute asthma exacerbation risk prediction to inform precision medicine strategies.</div>
</div>

<div class="talk-item">
    <div class="talk-header">
        <span class="talk-badge mit">MIT NEWDIGS</span>
        <span class="talk-year">2020–2021</span>
    </div>
    <div class="talk-title">Using RWD and ML to predict rheumatoid arthritis treatment response: Anti-TNF vs JAK Inhibitors</div>
    <div class="talk-venue">MIT NEWDIGS Design Lab Speaker</div>
    <div class="talk-description">Presented ML models predicting treatment response in rheumatoid arthritis using real-world claims data to inform biologic treatment selection.</div>
</div>

<div class="talk-item">
    <div class="talk-header">
        <span class="talk-badge acm">ACM CHIL</span>
        <span class="talk-year">2020</span>
    </div>
    <div class="talk-title"><a href="https://slideslive.com/38931925/automated-clinical-concept-mapping-using-snomed?ref=search-presentations-automated+clinical+concept" target="_blank" rel="noopener">Clinical data interoperability using SNOMED</a></div>
    <div class="talk-venue">ACM Conference on Health, Inference, and Learning</div>
    <div class="talk-description">Bridging ICD-9 and ICD-10 via SNOMED graph traversal and NLP for clinical concept stability.</div>
</div>

<div class="talk-item">
    <div class="talk-header">
        <span class="talk-badge falan">FALAN</span>
        <span class="talk-year">October 2016</span>
    </div>
    <div class="talk-title">The effects of experience on brain myelination: mechanisms and implications</div>
    <div class="talk-venue">Federation of Latin American and Caribbean Neuroscience Societies · Buenos Aires, Argentina</div>
    <div class="talk-description">Reviewed mechanisms of experience-dependent myelination and implications for brain plasticity and learning.</div>
</div>

</div>
