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

/* Top-right floating profile picture */
.profile-picture {
    float: right !important;
    width: 180px !important;
    height: 180px !important;
    border-radius: 8px !important;
    box-shadow: 0 4px 12px rgba(0,0,0,0.15) !important;
    margin: 0 0 1.5em 2em !important;
    clear: right !important;
}

/* About section layout */
.about-content {
    overflow: hidden;
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
    color: #94a3b8;
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
    .featured-grid {
        grid-template-columns: 1fr;
    }
    .featured-item img {
        width: 80px;
        height: 56px;
    }
    .profile-picture {
        float: none !important;
        display: block !important;
        margin: 1em auto !important;
        width: 150px !important;
        height: 150px !important;
    }
}
</style>

<img class="profile-picture" src="{{ '/assets/images/photo_3.jpg' | relative_url }}" alt="Patrick Long">

Hi, I'm Patrick. I lead teams building healthcare ML solutions to find patients with rare or under-diagnosed diseases who may benefit from available treatments, using claims and EHR data.

My through line is combining science and tech to improve health: a decade as a neuroscientist at the bench (molecular biology, developmental neurobiology, cancer therapeutics), then tech transfer evaluating early-stage medical inventions like clinical decision support tools, digital health platforms, and therapeutics. Since then I've been building healthcare ML solutions on real-world data, from problem framing through deployment, with 50+ predictive models deployed at scale.

15+ publications and 3 patents in healthcare AI. In my free time I build [educational apps]({{ '/tutorials' | relative_url }}) about biology, AI/ML, and system design.

**Recent:** Presented at the Pharmaceutical Data Science Conference (PharmaDS 2026) · New paper on asthma subgroup discovery in *BMJ Health & Care Informatics* (2025)

## Featured Work

<div class="featured-grid">
  <a class="featured-item" href="https://informatics.bmj.com/content/32/1/e101282" target="_blank" rel="noopener">
    <img src="{{ '/assets/images/articles/bmj-hci-asthma-2025.png' | relative_url }}" alt="Asthma ML paper" loading="lazy">
    <div class="featured-info">
      <div class="featured-title">Asthma Subgroup Discovery</div>
      <div class="featured-blurb">ML-driven patient clustering using longitudinal claims data to identify high-risk asthma phenotypes.</div>
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
      <div class="featured-blurb">How learning drives myelin plasticity in the adult brain—linking neural activity to white matter changes.</div>
      <div class="featured-source">Science, 2014</div>
    </div>
  </a>
  
  <a class="featured-item" href="https://www.healthcareaiprimer.com/" target="_blank" rel="noopener">
    <img src="{{ '/assets/images/articles/og-image.jpg' | relative_url }}" alt="Healthcare AI Primer" loading="lazy">
    <div class="featured-info">
      <div class="featured-title">Healthcare AI Primer</div>
      <div class="featured-blurb">Study notes on ML and real-world data across drug discovery, clinical trials, and regulatory science.</div>
      <div class="featured-source">Live Project</div>
    </div>
  </a>
</div>

<div class="see-more-links">
  <a href="{{ '/publications' | relative_url }}">More publications →</a>
  <a href="{{ '/tutorials' | relative_url }}">More educational apps →</a>
</div>

Working on something at the intersection of healthcare and AI, or interested in collaborating? [Get in touch]({{ '/contact' | relative_url }}).
