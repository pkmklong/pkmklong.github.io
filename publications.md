---
layout: default
title: Publications
---

<style>
/* Publications-specific styles */
.publications-header {
    text-align: center;
    margin-bottom: 50px;
    padding-bottom: 30px;
    border-bottom: 1px solid #e5e5e5;
}

.publications-header h1 {
    font-size: 2.2rem;
    font-weight: 300;
    color: #2c3e50;
    margin-bottom: 8px;
}

.publications-header p {
    font-size: 1.1rem;
    color: #666;
    font-weight: 300;
}

.section-header {
    font-size: 1.5rem;
    font-weight: 300;
    color: #2c3e50;
    margin: 40px 0 25px 0;
    padding-bottom: 10px;
    border-bottom: 2px solid #3498db;
}

.publications-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 25px;
    margin-bottom: 40px;
}

.publication-tile {
    background: white;
    border: 1px solid #e5e5e5;
    border-radius: 8px;
    padding: 25px;
    transition: all 0.2s ease;
    text-decoration: none;
    color: inherit;
    display: block;
    position: relative;
}

.publication-tile:hover {
    border-color: #3498db;
    box-shadow: 0 4px 12px rgba(52, 152, 219, 0.1);
    transform: translateY(-2px);
    text-decoration: none;
    color: inherit;
}

.external-link-icon {
    position: absolute;
    top: 15px;
    right: 15px;
    color: #999;
    font-size: 0.9rem;
}

.publication-tile:hover .external-link-icon {
    color: #3498db;
}

.tile-category {
    font-size: 0.8rem;
    color: #3498db;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    margin-bottom: 12px;
}

.tile-title {
    font-size: 1.1rem;
    font-weight: 400;
    color: #2c3e50;
    margin-bottom: 12px;
    line-height: 1.4;
}

.tile-description {
    font-size: 0.9rem;
    color: #666;
    line-height: 1.5;
    margin-bottom: 15px;
}

.tile-meta {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 0.8rem;
    color: #999;
    padding-top: 12px;
    border-top: 1px solid #f0f0f0;
}

.journal-name {
    font-weight: 500;
    color: #666;
}

/* Category-specific colors */
.tile-healthcare .tile-category { color: #e74c3c; }
.tile-healthcare:hover { border-color: #e74c3c; box-shadow: 0 4px 12px rgba(231, 76, 60, 0.1); }

.tile-neuroscience .tile-category { color: #9b59b6; }
.tile-neuroscience:hover { border-color: #9b59b6; box-shadow: 0 4px 12px rgba(155, 89, 182, 0.1); }

.nav-link {
    display: inline-block;
    margin-top: 30px;
    color: #3498db;
    text-decoration: none;
    font-size: 0.9rem;
    padding: 8px 0;
    border-bottom: 1px solid transparent;
    transition: border-color 0.2s ease;
}

.nav-link:hover {
    border-bottom-color: #3498db;
}

@media (max-width: 768px) {
    .publications-grid {
        grid-template-columns: 1fr;
        gap: 20px;
    }
    
    .publications-header h1 {
        font-size: 1.8rem;
    }
    
    .publication-tile {
        padding: 20px;
    }
}
</style>
<div class="publications-header">
    <p>Selected publications and patents spanning applied machine learning in healthcare and a decade of neuroscience and cancer research. Full record on <a href="https://scholar.google.com/citations?user=Xg4y16YAAAAJ&hl=en" target="_blank" rel="noopener">Google Scholar</a>.</p>
</div>

<!-- Healthcare AI & Applied ML -->
<h2 class="section-header">Applied ML in Healthcare</h2>
<div class="publications-grid">
    {% assign healthcare_pubs = site.publications | where_exp: "item", "item.path contains 'healthcare_ai'" %}
    {% assign healthcare_sorted = healthcare_pubs | sort: "year" | reverse %}
    {% for publication in healthcare_sorted %}
        <a href="{{ publication.external_url | default: '#' }}" target="_blank" rel="noopener" class="publication-tile tile-healthcare">
            <span class="external-link-icon">↗</span>
            <div class="tile-category">{{ publication.type | capitalize }}</div>
            <h3 class="tile-title">{{ publication.title }}</h3>
            <p class="tile-description">{{ publication.description }}</p>
            <div class="tile-meta">
                <span class="journal-name">{{ publication.journal | default: publication.venue }}</span>
                <span>{{ publication.year }}</span>
            </div>
        </a>
    {% endfor %}
</div>
<!-- Neuroscience -->
<h2 class="section-header">Neuroscience & Cancer Research</h2>
<div class="publications-grid">
    {% assign neuro_pubs = site.publications | where_exp: "item", "item.path contains 'neuroscience'" %}
    {% assign neuro_sorted = neuro_pubs | sort: "year" | reverse %}
    {% for publication in neuro_sorted %}
        <a href="{{ publication.external_url | default: '#' }}" target="_blank" rel="noopener" class="publication-tile tile-neuroscience">
            <span class="external-link-icon">↗</span>
            <div class="tile-category">{{ publication.type | capitalize }}</div>
            <h3 class="tile-title">{{ publication.title }}</h3>
            <p class="tile-description">{{ publication.description }}</p>
            <div class="tile-meta">
                <span class="journal-name">{{ publication.journal }}</span>
                <span>{{ publication.year }}</span>
            </div>
        </a>
    {% endfor %}
</div>
<a href="{{ "/" | relative_url }}" class="nav-link">← Back to Main Profile</a>
