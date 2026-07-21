---
layout: default
---

<style>
/* Compact vertical spacing */
h2 { margin-top: 1.8em !important; margin-bottom: 0.8em !important; font-size: 1.3em !important; color: #1a365d !important; }
h3 { margin-top: 1em !important; margin-bottom: 0.2em !important; font-size: 1.05em !important; }
p { margin-bottom: 0.8em !important; }
li { margin-bottom: 0.4em !important; }
ul { margin-bottom: 1em !important; }
hr { margin: 1.5em 0 !important; }

/* Homepage introduction */
.home-hero {
    display: grid;
    grid-template-columns: minmax(0, 1fr) 180px;
    gap: 2em;
    align-items: center;
    margin: 2em 0 1.5em;
}

.home-hero h2 {
    margin-top: 0 !important;
    font-size: 1.65em !important;
    line-height: 1.25;
}

.home-hero p {
    max-width: 58ch;
}

.profile-picture {
    width: 180px !important;
    height: 180px !important;
    object-fit: cover;
    border-radius: 8px !important;
    box-shadow: 0 4px 12px rgba(0,0,0,0.15) !important;
    margin: 0 !important;
}

.hero-links {
    display: flex;
    gap: 1em;
    margin-top: 1.2em;
}

.hero-links a {
    display: inline-block;
    padding: 0.45em 0.8em;
    border: 1px solid #0077be;
    border-radius: 5px;
    text-decoration: none;
}

.hero-links a:first-child {
    background: #0077be;
    color: #fff;
}

.track-record {
    margin: 1.5em 0 2em;
    padding: 1em 0;
    border-top: 1px solid #e2e8f0;
    border-bottom: 1px solid #e2e8f0;
    color: #475569;
}

.focus-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 0;
    margin: 1em 0 2em;
}

.focus-item {
    padding: 0 1.2em;
}

.focus-item:first-child {
    padding-left: 0;
}

.focus-item + .focus-item {
    border-left: 1px solid #e2e8f0;
}

.focus-item h3 {
    margin-top: 0 !important;
}

.focus-item p {
    color: #475569;
    font-size: 0.92em;
}

.current-interests {
    border-left: 3px solid #0077be;
    padding-left: 1em;
    margin: 1em 0 2em;
}

/* Featured Work Grid */
.featured-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.2em;
    margin-bottom: 1em;
}

.featured-item {
    display: flex;
    gap: 0.8em;
    padding: 0.8em;
    border-radius: 8px;
    background: #f8fafc;
    border: 1px solid #e2e8f0;
    text-decoration: none;
    color: inherit;
    transition: all 0.2s ease;
}

.featured-item:hover {
    background: #fff;
    border-color: #cbd5e1;
    box-shadow: 0 4px 12px rgba(0,0,0,0.08);
    transform: translateY(-2px);
}

.featured-item img {
    width: 100px;
    height: 70px;
    object-fit: cover;
    object-position: top left;
    border-radius: 4px;
    flex-shrink: 0;
}

.featured-info {
    display: flex;
    flex-direction: column;
    gap: 0.25em;
    min-width: 0;
}

.featured-title {
    font-weight: 600;
    font-size: 0.95em;
    color: #1a365d;
}

.featured-blurb {
    font-size: 0.8em;
    color: #64748b;
    line-height: 1.4;
}

.featured-source {
    font-size: 0.75em;
    color: #64748b;
    margin-top: auto;
}

.see-more-links {
    display: flex;
    gap: 2em;
    justify-content: center;
    margin-top: 0.5em;
    margin-bottom: 1.5em;
}

.see-more-links a {
    color: #2c5282;
    text-decoration: none;
    font-size: 0.9em;
}

.see-more-links a:hover {
    text-decoration: underline;
}

/* Responsive */
@media (max-width: 768px) {
    .home-hero {
        grid-template-columns: 1fr;
        gap: 1.2em;
        margin-top: 1.5em;
    }
    .home-hero .profile-picture {
        width: 130px !important;
        height: 130px !important;
        margin: 0 auto !important;
    }
    .focus-grid {
        grid-template-columns: 1fr;
    }
    .focus-item,
    .focus-item:first-child {
        padding: 0.8em 0;
    }
    .focus-item + .focus-item {
        border-left: 0;
        border-top: 1px solid #e2e8f0;
    }
    .featured-grid {
        grid-template-columns: 1fr;
    }
    .featured-item img {
        width: 80px;
        height: 56px;
    }
}
</style>

<section class="home-hero">
  <div>
    <h2>Technical leadership for machine learning on real-world healthcare data</h2>
    <p>I lead the design and delivery of healthcare machine learning work, from cohort and outcome definition through model development, validation, and deployment for large-scale patient identification. My focus includes disease detection, progression, patient outcomes, and clinically meaningful patient subgroups.</p>
    <p>This work draws on deep experience with claims and EHR data, along with my training as a neuroscientist and cancer biologist.</p>
    <div class="hero-links">
      <a href="#selected-work">Selected work</a>
      <a href="{{ '/contact' | relative_url }}">Contact</a>
    </div>
  </div>
  <img class="profile-picture" src="{{ '/assets/images/photo_3.jpg' | relative_url }}" alt="Patrick Long">
</section>

<p class="track-record">My teams and I have delivered more than 50 end-to-end predictive modeling studies. Each had its own study design, cohort and outcome definitions, validation plan, and requirements for use at scale. My public work includes 15+ publications across healthcare ML, neuroscience, and cancer biology, plus 3 healthcare AI patents.</p>

## How I Work

<div class="focus-grid">
  <div class="focus-item">
    <h3>Machine learning methodology</h3>
    <p>I work across gradient boosting, clustering, NLP, transformers, and agentic systems. The method follows the question, the data, and the decision it needs to support.</p>
  </div>
  <div class="focus-item">
    <h3>Real-world data</h3>
    <p>Claims and EHR data reflect care delivery, coding, access, and missingness. Understanding that data-generating process is part of the modeling work.</p>
  </div>
  <div class="focus-item">
    <h3>Scientific context</h3>
    <p>My training in neuroscience and cancer biology helps me connect model design to disease mechanism, progression, and clinical meaning.</p>
  </div>
</div>

## Current Technical Interests

<div class="current-interests">
  <p>I look for practical uses of transformers, deep learning, and LLM-based workflows in healthcare analysis. I am especially interested in methods that improve analytical capability or remove manual work. The goal is to match the method to the data, clinical question, and operating constraints.</p>
  <p><strong>Recent public work:</strong> Explanation-guided clustering for high-risk asthma subgroups, presented at PharmaDS 2026, and a related study published in <em>BMJ Health & Care Informatics</em> in 2025.</p>
</div>

## Selected Work {#selected-work}

<div class="featured-grid">
  <a class="featured-item" href="https://informatics.bmj.com/content/32/1/e101282" target="_blank" rel="noopener">
    <img src="{{ '/assets/images/articles/bmj-hci-asthma-2025.png' | relative_url }}" alt="Asthma ML paper" loading="lazy">
    <div class="featured-info">
      <div class="featured-title">Asthma Subgroup Discovery</div>
      <div class="featured-blurb">Predictive modeling and explanation-guided clustering with longitudinal claims data to identify high-risk asthma subgroups.</div>
      <div class="featured-source">BMJ Health & Care Informatics, 2025</div>
    </div>
  </a>
  
  <a class="featured-item" href="https://informatics.bmj.com/content/29/1/e100510.info" target="_blank" rel="noopener">
    <img src="{{ '/assets/images/articles/bmj-hci-nash-2022.png' | relative_url }}" alt="NASH ML paper" loading="lazy">
    <div class="featured-info">
      <div class="featured-title">NASH Detection Model</div>
      <div class="featured-blurb">Machine learning approach using prescription and claims data for non-alcoholic steatohepatitis detection.</div>
      <div class="featured-source">BMJ Health & Care Informatics, 2022</div>
    </div>
  </a>
  
  <a class="featured-item" href="https://pmc.ncbi.nlm.nih.gov/articles/PMC4261922/" target="_blank" rel="noopener">
    <img src="{{ '/assets/images/articles/science-myelin-2014.png' | relative_url }}" alt="Science paper" loading="lazy">
    <div class="featured-info">
      <div class="featured-title">To Learn is to Myelinate</div>
      <div class="featured-blurb">A perspective on how learning drives myelin plasticity in the adult brain and changes white matter.</div>
      <div class="featured-source">Science, 2014</div>
    </div>
  </a>
  
  <a class="featured-item" href="https://dl.acm.org/doi/10.1145/3368555.3384453" target="_blank" rel="noopener">
    <div class="featured-info">
      <div class="featured-title">Clinical Concept Mapping with SNOMED</div>
      <div class="featured-blurb">An NLP and graph traversal method for mapping between ICD editions through a stable clinical ontology.</div>
      <div class="featured-source">ACM CHIL, 2020 · US Patent 11,960,456</div>
    </div>
  </a>
</div>

<div class="see-more-links">
  <a href="{{ '/publications' | relative_url }}">More publications →</a>
  <a href="{{ '/tutorials' | relative_url }}">More educational apps →</a>
</div>

Interested in healthcare machine learning, real-world data, or scientific collaboration? [Get in touch]({{ '/contact' | relative_url }}).
