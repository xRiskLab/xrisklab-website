---
layout: default
title: "About xRiskLab"
---

<div class="about-page">
  <div class="container">
    <div class="about-hero">
      <h1>About xRiskLab</h1>
      <p class="lead">We're pioneering the future of interpretable machine learning for risk management and credit scoring.</p>
    </div>

    <div class="about-content">
      <div class="about-section">
        <h2>Our Mission</h2>
        <p>At xRiskLab, we believe that advanced machine learning should be both powerful and interpretable. Our mission is to bridge the gap between cutting-edge AI capabilities and the transparency requirements of high-stakes domains like finance, healthcare, and regulatory compliance.</p>
        
        <p>We develop open-source tools that enable data scientists and risk managers to build models that not only perform exceptionally but also explain their decisions in clear, actionable terms.</p>
      </div>

      <div class="about-section">
        <h2>Our Expertise</h2>
        <div class="expertise-grid">
          <div class="expertise-item glass-surface">
            <h3>🎯 Credit Scoring</h3>
            <p>Advanced scorecard boosting, WOE-based models, and interpretable gradient boosting for financial institutions.</p>
          </div>
          <div class="expertise-item glass-surface">
            <h3>🔍 Interpretable AI</h3>
            <p>Transparent machine learning solutions with statistical rigor and confidence intervals for decision-making.</p>
          </div>
          <div class="expertise-item glass-surface">
            <h3>⚡ High Performance</h3>
            <p>Production-scale algorithms optimized for speed and scalability in enterprise environments.</p>
          </div>
          <div class="expertise-item glass-surface">
            <h3>📊 Statistical Inference</h3>
            <p>Rigorous statistical methods with uncertainty quantification and standard error calculations.</p>
          </div>
        </div>
      </div>

      <div class="about-section">
        <h2>Our Approach</h2>
        <p>We combine deep expertise in machine learning with a strong foundation in statistical theory. Our tools are built on principles that ensure:</p>
        
        <ul class="approach-list">
          <li><strong>Interpretability:</strong> Every model decision can be explained and validated</li>
          <li><strong>Statistical Rigor:</strong> Proper uncertainty quantification and confidence intervals</li>
          <li><strong>Production Ready:</strong> Optimized for real-world deployment and scalability</li>
          <li><strong>Open Source:</strong> Transparent, community-driven development</li>
          <li><strong>Industry Standards:</strong> Compliance with regulatory requirements and best practices</li>
        </ul>
      </div>

      <div class="about-section">
        <h2>Why xRiskLab?</h2>
        <p>Traditional machine learning approaches often create "black box" models that are difficult to interpret and validate. In high-stakes domains like credit risk, this creates significant challenges for model validation, regulatory compliance, and business understanding.</p>
        
        <p>Our solutions address these challenges by providing:</p>
        
        <div class="benefits-grid">
          <div class="benefit-item">
            <div class="benefit-icon">🔬</div>
            <h4>Scientific Foundation</h4>
            <p>Built on rigorous statistical theory and peer-reviewed research</p>
          </div>
          <div class="benefit-item">
            <div class="benefit-icon">🛠️</div>
            <h4>Practical Tools</h4>
            <p>Easy-to-use Python libraries that integrate with existing workflows</p>
          </div>
          <div class="benefit-item">
            <div class="benefit-icon">📈</div>
            <h4>Proven Results</h4>
            <p>Demonstrated improvements in model performance and interpretability</p>
          </div>
          <div class="benefit-item">
            <div class="benefit-icon">🤝</div>
            <h4>Community Support</h4>
            <p>Active development and support from the open-source community</p>
          </div>
        </div>
      </div>

      <div class="about-section">
        <h2>Get Started</h2>
        <p>Ready to transform your risk management models? Explore our projects and start building more interpretable, powerful machine learning solutions today.</p>
        
        <div class="cta-buttons">
          <a href="/projects/" class="btn btn-primary">Explore Projects</a>
          <a href="/contact/" class="btn btn-secondary">Get in Touch</a>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
.about-page {
  background: transparent;
  min-height: 100vh;
  padding: 40px 0;
}

.about-hero {
  text-align: center;
  margin-bottom: 80px;
  padding: 40px 0;
}

.about-hero h1 {
  font-size: clamp(2.5rem, 6vw, 3.5rem);
  font-weight: 700;
  margin-bottom: 24px;
  color: var(--text-primary);
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.lead {
  font-size: clamp(1.125rem, 3vw, 1.375rem);
  color: var(--text-secondary);
  max-width: 700px;
  margin: 0 auto;
  line-height: 1.5;
}

.about-content {
  max-width: 900px;
  margin: 0 auto;
}

.about-section {
  margin-bottom: 80px;
}

.about-section h2 {
  font-size: 2rem;
  font-weight: 600;
  margin-bottom: 24px;
  color: var(--text-primary);
}

.about-section p {
  color: var(--text-secondary);
  margin-bottom: 24px;
  line-height: 1.7;
  font-size: 16px;
}

.expertise-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 24px;
  margin-top: 32px;
}

.expertise-item {
  padding: 32px;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.expertise-item:hover {
  transform: translateY(-4px);
  background: var(--surface-glass-hover);
}

.expertise-item h3 {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 16px;
  color: var(--text-primary);
}

.expertise-item p {
  color: var(--text-secondary);
  margin-bottom: 0;
  font-size: 15px;
}

.approach-list {
  list-style: none;
  padding: 0;
}

.approach-list li {
  background: var(--surface-glass);
  border: 1px solid var(--border-glass);
  border-radius: 12px;
  padding: 24px;
  margin-bottom: 16px;
  color: var(--text-secondary);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.approach-list li:hover {
  background: var(--surface-glass-hover);
  transform: translateX(8px);
}

.approach-list li strong {
  color: var(--accent-blue);
  font-weight: 600;
}

.benefits-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 32px;
  margin-top: 32px;
}

.benefit-item {
  text-align: center;
  padding: 32px 16px;
}

.benefit-icon {
  font-size: 48px;
  margin-bottom: 16px;
  filter: grayscale(1);
  transition: filter 0.3s ease;
}

.benefit-item:hover .benefit-icon {
  filter: grayscale(0);
}

.benefit-item h4 {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 16px;
  color: var(--text-primary);
}

.benefit-item p {
  color: var(--text-secondary);
  margin-bottom: 0;
  font-size: 15px;
}

.cta-buttons {
  display: flex;
  gap: 16px;
  justify-content: center;
  flex-wrap: wrap;
  margin-top: 32px;
}

@media (max-width: 768px) {
  .about-hero h1 {
    font-size: 2.5rem;
  }
  
  .lead {
    font-size: 1.125rem;
  }
  
  .expertise-grid,
  .benefits-grid {
    grid-template-columns: 1fr;
  }
  
  .cta-buttons {
    flex-direction: column;
    align-items: center;
  }

  .expertise-item,
  .benefit-item {
    padding: 24px;
  }
}
</style>
