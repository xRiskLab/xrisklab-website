---
layout: default
title: "Research & Publications"
---

<section class="research-hero">
  <div class="container">
    <h1 class="research-title">Research & Publications</h1>
    <p class="research-subtitle">Academic contributions to machine learning, statistics, and risk management</p>
  </div>
</section>

<section class="publications-section">
  <div class="container">
    <div class="publications-grid">
      
      <div class="publication-card glass-surface-hover featured">
        <div class="publication-type">Preprint</div>
        <h3>An Information-Theoretic Framework for Credit Risk Modeling: Unifying Industry Practice with Statistical Theory for Fair and Interpretable Scorecards</h3>
        <p class="publication-authors">Agus Sudjianto, Denis Burakov</p>
        <p class="publication-venue">arXiv preprint, September 2025</p>
        <p class="publication-abstract">We establish a unified information-theoretic framework revealing Weight of Evidence (WoE), Information Value (IV), and Population Stability Index (PSI) as instances of classical information divergences. Through the delta method applied to WoE transformations, we derive standard errors for IV and PSI, enabling formal hypothesis testing and probabilistic fairness constraints for the first time in credit risk modeling.</p>
        <div class="publication-links">
          <a href="/assets/papers/2509.09855v1.pdf" class="btn btn-primary btn-sm" target="_blank">📄 PDF</a>
          <a href="https://arxiv.org/abs/2509.09855" class="btn btn-secondary btn-sm" target="_blank">arXiv</a>
          <a href="https://github.com/asudjianto-xml/Information-Theoretic-for-Credit-Modeling" class="btn btn-outline btn-sm" target="_blank">💻 Code</a>
          <a href="#" class="btn btn-outline btn-sm" onclick="togglePDFViewer('pdf-2509'); return false;">👁️ Preview</a>
        </div>
        <div id="pdf-2509" class="pdf-viewer" style="display: none;">
          <iframe src="/assets/papers/2509.09855v1.pdf" width="100%" height="600px" style="border: 1px solid var(--border-glass); border-radius: 12px; margin-top: 16px;"></iframe>
        </div>
      </div>

      <div class="publication-card glass-surface-hover">
        <div class="publication-type">Technical Report</div>
        <h3>Weight of Evidence (WOE), Log Odds, and Standard Errors</h3>
        <p class="publication-authors">Denis Burakov</p>
        <p class="publication-venue">xRiskLab Technical Report, 2024</p>
        <p class="publication-abstract">Comprehensive methodology for computing standard errors for Weight of Evidence (WOE) values, with practical implementations.</p>
        <div class="publication-links">
          <a href="/assets/papers/woe_standard_errors.pdf" class="btn btn-primary btn-sm" target="_blank">📄 PDF</a>
          <a href="https://github.com/xRiskLab/fastwoe" class="btn btn-outline btn-sm" target="_blank">💻 Code</a>
          <a href="#" class="btn btn-outline btn-sm" onclick="togglePDFViewer('pdf-woe'); return false;">👁️ Preview</a>
        </div>
        <div id="pdf-woe" class="pdf-viewer" style="display: none;">
          <iframe src="/assets/papers/woe_standard_errors.pdf" width="100%" height="600px" style="border: 1px solid var(--border-glass); border-radius: 12px; margin-top: 16px;"></iframe>
        </div>
      </div>

    </div>
  </div>
</section>

<section class="industry-section">
  <div class="container">
    <h2 class="section-title">Industry Insights & Collaborations</h2>
    <div class="insights-grid">
      
      <div class="insight-card glass-surface-hover">
        <div class="insight-type">Industry Article</div>
        <h3>Beyond Credit Scoring: A Decision-Making Framework for Profitable Lending</h3>
        <p class="insight-description">Exploring advanced machine learning techniques and their applications in modern lending decisions, focusing on interpretable AI and regulatory compliance.</p>
        <div class="insight-links">
          <a href="https://taktile.com/articles/beyond-the-credit-score-modern-decision-making-for-profitable-lending" class="btn btn-primary btn-sm" target="_blank">� Read Article</a>
        </div>
      </div>

      <div class="insight-card glass-surface-hover">
        <div class="insight-type">Academic Affiliation</div>
        <h3>University of Edinburgh Business School</h3>
        <p class="insight-description">External Affiliate at the Credit Research Centre, contributing to research in credit risk management and interpretable machine learning methods for financial applications.</p>
        <div class="insight-links">
          <a href="https://www.crc.business-school.ed.ac.uk/about/external-affiliates" class="btn btn-primary btn-sm" target="_blank">🎓 View Profile</a>
        </div>
      </div>

    </div>
  </div>
</section>

<section class="contact-research-section">
  <div class="container">
    <div class="research-contact-card glass-surface">
      <h2>Research Collaboration & Inquiries</h2>
      <p>Interested in collaborating on research projects or discussing applications of interpretable machine learning in your organization?</p>
      <div class="research-contact-buttons">
        <a href="mailto:contact@xrisklab.ai" class="btn btn-primary">📧 Get in Touch</a>
        <a href="/contact/" class="btn btn-secondary">Contact Form</a>
      </div>
    </div>
  </div>
</section>



<style>
.research-hero {
  background: transparent;
  padding: 80px 0 40px;
  text-align: center;
}

.research-title {
  font-size: clamp(2.5rem, 6vw, 3.5rem);
  font-weight: 700;
  margin-bottom: 24px;
  color: var(--text-primary);
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.research-subtitle {
  font-size: clamp(1.125rem, 3vw, 1.375rem);
  color: var(--text-secondary);
  max-width: 700px;
  margin: 0 auto;
  line-height: 1.5;
}

.publications-section {
  padding: 80px 0;
}

.publications-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  gap: 32px;
  margin-bottom: 80px;
}

.publication-card {
  background: var(--surface-glass);
  backdrop-filter: var(--blur-amount);
  -webkit-backdrop-filter: var(--blur-amount);
  border: 1px solid var(--border-glass);
  border-radius: 20px;
  padding: 32px;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.publication-card.featured {
  border-color: var(--accent-blue);
  background: rgba(0, 122, 255, 0.08);
}

.publication-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: var(--primary-gradient);
  transform: translateX(-100%);
  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}

.publication-card:hover::before {
  transform: translateX(0);
}

.publication-card:hover {
  transform: translateY(-8px);
  background: var(--surface-glass-hover);
  box-shadow: var(--shadow-glass);
}

.publication-type {
  display: inline-block;
  background: rgba(0, 122, 255, 0.15);
  color: var(--accent-blue);
  padding: 6px 12px;
  border-radius: 12px;
  font-size: 12px;
  font-weight: 600;
  margin-bottom: 16px;
  border: 1px solid rgba(0, 122, 255, 0.2);
}

.publication-card h3 {
  font-size: 1.375rem;
  font-weight: 600;
  margin-bottom: 12px;
  color: var(--text-primary);
  line-height: 1.3;
}

.publication-authors {
  color: var(--accent-purple);
  font-weight: 500;
  margin-bottom: 8px;
  font-size: 14px;
}

.publication-venue {
  color: var(--text-secondary);
  font-style: italic;
  margin-bottom: 16px;
  font-size: 14px;
}

.publication-abstract {
  color: var(--text-secondary);
  line-height: 1.6;
  margin-bottom: 24px;
  font-size: 15px;
}

.publication-links {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
}

.industry-section {
  padding: 40px 0 80px;
  background: rgba(0, 122, 255, 0.02);
  border-radius: 20px;
  margin: 40px 0;
}

.insights-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 32px;
}

.insight-card {
  background: var(--surface-glass);
  backdrop-filter: var(--blur-amount);
  -webkit-backdrop-filter: var(--blur-amount);
  border: 1px solid var(--border-glass);
  border-radius: 20px;
  padding: 32px;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.insight-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: var(--primary-gradient);
  transform: translateX(-100%);
  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}

.insight-card:hover::before {
  transform: translateX(0);
}

.insight-card:hover {
  transform: translateY(-8px);
  background: var(--surface-glass-hover);
  box-shadow: var(--shadow-glass);
}

.insight-type {
  display: inline-block;
  background: rgba(88, 86, 214, 0.15);
  color: var(--accent-purple);
  padding: 6px 12px;
  border-radius: 12px;
  font-size: 12px;
  font-weight: 600;
  margin-bottom: 16px;
  border: 1px solid rgba(88, 86, 214, 0.2);
}

.insight-card h3 {
  font-size: 1.375rem;
  font-weight: 600;
  margin-bottom: 16px;
  color: var(--text-primary);
  line-height: 1.3;
}

.insight-description {
  color: var(--text-secondary);
  line-height: 1.6;
  margin-bottom: 24px;
  font-size: 15px;
}

.insight-links {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
}

.contact-research-section {
  padding: 40px 0;
}

.research-contact-card {
  background: var(--surface-glass);
  backdrop-filter: var(--blur-amount);
  -webkit-backdrop-filter: var(--blur-amount);
  border: 1px solid var(--border-glass);
  border-radius: 20px;
  padding: 48px;
  text-align: center;
  max-width: 600px;
  margin: 0 auto;
}

.research-contact-card h2 {
  font-size: 1.75rem;
  font-weight: 600;
  margin-bottom: 16px;
  color: var(--text-primary);
}

.research-contact-card p {
  color: var(--text-secondary);
  margin-bottom: 32px;
  line-height: 1.6;
  font-size: 16px;
}

.research-contact-buttons {
  display: flex;
  gap: 16px;
  justify-content: center;
  flex-wrap: wrap;
}

.pdf-viewer {
  margin-top: 16px;
  transition: all 0.3s ease;
}

.pdf-viewer iframe {
  border: 1px solid var(--border-glass);
  border-radius: 12px;
  background: var(--background-secondary);
}

.presentations-section {
  padding: 40px 0 80px;
}

.presentations-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 24px;
}

.presentation-card {
  background: var(--surface-glass);
  backdrop-filter: var(--blur-amount);
  -webkit-backdrop-filter: var(--blur-amount);
  border: 1px solid var(--border-glass);
  border-radius: 16px;
  padding: 24px;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.presentation-card:hover {
  transform: translateY(-4px);
  background: var(--surface-glass-hover);
}

.presentation-card h4 {
  font-size: 1.125rem;
  font-weight: 600;
  margin-bottom: 8px;
  color: var(--text-primary);
}

.presentation-venue {
  color: var(--text-secondary);
  margin-bottom: 16px;
  font-size: 14px;
  font-style: italic;
}

.presentation-links {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
}

.btn-sm {
  padding: 6px 12px;
  font-size: 12px;
  border-radius: 8px;
}

@media (max-width: 768px) {
  .publications-grid {
    grid-template-columns: 1fr;
    gap: 24px;
  }

  .insights-grid {
    grid-template-columns: 1fr;
    gap: 24px;
  }

  .presentations-grid {
    grid-template-columns: 1fr;
  }

  .publication-card,
  .insight-card,
  .presentation-card,
  .research-contact-card {
    padding: 24px;
  }

  .publication-links,
  .insight-links,
  .presentation-links,
  .research-contact-buttons {
    justify-content: center;
  }

  .research-contact-buttons {
    flex-direction: column;
    align-items: center;
  }
}
</style>

<script>
function togglePDFViewer(viewerId) {
  const viewer = document.getElementById(viewerId);
  if (viewer.style.display === 'none' || viewer.style.display === '') {
    viewer.style.display = 'block';
    viewer.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
  } else {
    viewer.style.display = 'none';
  }
}
</script>