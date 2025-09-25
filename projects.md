---
layout: default
title: "Projects"
---

<section class="projects-section">
  <div class="container">
    <h1 class="projects-title">Open Source Projects</h1>
    <p class="projects-subtitle">
      Advanced machine learning libraries for risk management and interpretable AI.
    </p>

    <div class="projects-grid">
      {% for project in site.projects %}
      <div class="project-card{% if project.featured %} featured{% endif %}">
        
        {% if project.image %}
        <div class="project-image">
          <img src="{{ project.image }}" alt="{{ project.title }}" loading="lazy">
          {% if project.featured %}
          <div class="project-overlay">
            <span class="badge badge-featured">Featured</span>
          </div>
          {% endif %}
        </div>
        {% else %}
        <!-- fallback placeholder -->
        <div class="project-image project-placeholder">
          <span>{{ project.title }}</span>
        </div>
        {% endif %}

        <div class="project-content">
          <div class="project-header">
            <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
          </div>

          <div class="project-badges">
            {% for tag in project.tags limit:2 %}
            <span class="badge {% cycle 'badge-primary', 'badge-secondary' %}">{{ tag }}</span>
            {% endfor %}
          </div>

          <p>{{ project.description }}</p>

          {% if project.features %}
          <div class="project-features">
            <ul>
              {% for feature in project.features %}
              <li>{{ feature }}</li>
              {% endfor %}
            </ul>
          </div>
          {% endif %}

          <div class="project-footer">
            <div class="project-links">
              {% if project.github %}
              <a href="{{ project.github }}" class="btn btn-outline btn-sm">GitHub</a>
              {% endif %}
              {% if project.pypi %}
              <a href="{{ project.pypi }}" class="btn btn-secondary btn-sm">PyPI</a>
              {% endif %}
              {% if project.paper %}
              <a href="{{ project.paper }}" class="btn btn-research btn-sm">📄 Paper</a>
              {% endif %}
            </div>
          </div>
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</section>

<section class="projects-contribute">
  <div class="container">
    <div class="contribute-content">
      <h2>Contribute to xRiskLab</h2>
      <p>
        Our projects are open source and community-driven. We welcome contributions from developers,
        data scientists, and researchers who share our vision of interpretable machine learning.
      </p>
      <div class="contribute-buttons">
        <a href="https://github.com/xRiskLab" class="btn btn-primary">View on GitHub</a>
        <a href="/contact/" class="btn btn-secondary">Get in Touch</a>
      </div>
    </div>
  </div>
</section>

<style>
.projects-section {
  padding: 80px 0;
}

.projects-title {
  font-size: clamp(2.5rem, 6vw, 3.5rem);
  font-weight: 700;
  margin-bottom: 24px;
  text-align: center;
  color: var(--text-primary);
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.projects-subtitle {
  font-size: clamp(1.125rem, 3vw, 1.375rem);
  color: var(--text-secondary);
  text-align: center;
  max-width: 700px;
  margin: 0 auto 40px;
  line-height: 1.5;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 24px;
  margin-top: 40px;
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
}

.project-card {
  background: var(--surface-glass);
  backdrop-filter: var(--blur-amount);
  -webkit-backdrop-filter: var(--blur-amount);
  border: 1px solid var(--border-glass);
  border-radius: 20px;
  padding: 0;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  height: 100%;
}

.project-card.featured {
  border-color: var(--accent-blue);
  background: rgba(0, 122, 255, 0.08);
}

.project-card:hover {
  transform: translateY(-8px);
  background: var(--surface-glass-hover);
  box-shadow: var(--shadow-glass);
}

.project-image {
  position: relative;
  width: 100%;
  height: 200px;
  overflow: hidden;
  border-radius: 20px 20px 0 0;
}

.project-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  display: block;
}

.project-card:hover .project-image img {
  transform: scale(1.05);
}

.project-placeholder {
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #222, #444);
  color: var(--text-secondary);
  font-weight: 600;
  font-size: 1.2rem;
}

.project-overlay {
  position: absolute;
  top: 16px;
  right: 16px;
  z-index: 2;
}

.project-content {
  padding: 24px;
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}

.project-header h3 {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 12px;
  color: var(--text-primary);
  line-height: 1.3;
}

.project-header h3 a {
  color: inherit;
  text-decoration: none;
  transition: all 0.3s ease;
}

.project-card:hover .project-header h3 {
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.project-badges {
  display: flex;
  gap: 6px;
  flex-wrap: wrap;
  margin-bottom: 16px;
}

.badge {
  padding: 4px 12px;
  border-radius: 12px;
  font-size: 12px;
  font-weight: 500;
}

.badge-primary {
  background: rgba(0, 122, 255, 0.15);
  color: var(--accent-blue);
  border: 1px solid rgba(0, 122, 255, 0.2);
}

.badge-secondary {
  background: rgba(88, 86, 214, 0.15);
  color: var(--accent-purple);
  border: 1px solid rgba(88, 86, 214, 0.2);
}

.badge-featured {
  background: rgba(255, 45, 146, 0.15);
  color: var(--accent-pink);
  border: 1px solid rgba(255, 45, 146, 0.2);
  font-weight: 600;
}

.project-content p {
  color: var(--text-secondary);
  margin-bottom: 16px;
  line-height: 1.5;
  font-size: 14px;
  flex-grow: 1;
}

.project-features ul {
  list-style: none;
  padding: 0;
  margin: 0 0 20px 0;
}

.project-features li {
  color: var(--text-secondary);
  font-size: 14px;
  margin-bottom: 8px;
}

.project-footer {
  margin-top: auto;
}

.project-links {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
}

.btn-sm {
  padding: 8px 16px;
  font-size: 13px;
  border-radius: 8px;
}

.btn-research {
  background: rgba(255, 149, 0, 0.15);
  color: var(--text-primary);
  border: 1px solid rgba(255, 149, 0, 0.2);
}

.projects-contribute {
  background: var(--surface-glass);
  backdrop-filter: var(--blur-amount);
  -webkit-backdrop-filter: var(--blur-amount);
  border: 1px solid var(--border-glass);
  border-radius: 20px;
  margin: 40px auto;
  max-width: 800px;
  padding: 48px 32px;
  text-align: center;
}

.contribute-content h2 {
  font-size: 2rem;
  font-weight: 600;
  margin-bottom: 20px;
  color: var(--text-primary);
}

.contribute-content p {
  color: var(--text-secondary);
  margin-bottom: 32px;
  line-height: 1.6;
  font-size: 16px;
}

.contribute-buttons {
  display: flex;
  gap: 16px;
  justify-content: center;
  flex-wrap: wrap;
}

@media (min-width: 1200px) {
  .projects-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
    gap: 20px;
    margin-top: 32px;
  }

  .project-content {
    padding: 20px;
  }

  .contribute-buttons {
    flex-direction: column;
    align-items: center;
  }

  .projects-contribute {
    margin: 40px 16px;
    padding: 32px 24px;
  }
}
</style>
