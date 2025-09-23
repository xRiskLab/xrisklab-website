---
layout: default
title: "Contact"
---

<section class="contact-hero">
  <div class="container">
    <h1 class="contact-title">Get in Touch</h1>
    <p class="contact-subtitle">Ready to transform your risk assessment models? We'd love to hear from you.</p>
  </div>
</section>

<section class="contact-content">
  <div class="container">
    <div class="contact-grid">
      <div class="contact-info">
        <div class="contact-section glass-surface">
          <h2>Contact Information</h2>
          <div class="contact-items">
            <div class="contact-item">
              <div class="contact-icon">📧</div>
              <div class="contact-details">
                <h3>Email</h3>
                <p><a href="mailto:contact@xrisklab.ai">contact@xrisklab.ai</a></p>
                <small>We typically respond within 24 hours</small>
              </div>
            </div>
            
            <div class="contact-item">
              <div class="contact-icon">💬</div>
              <div class="contact-details">
                <h3>GitHub Discussions</h3>
                <p><a href="https://github.com/xRiskLab" target="_blank">github.com/xRiskLab</a></p>
                <small>Join our community discussions and get help</small>
              </div>
            </div>
            
            <div class="contact-item">
              <div class="contact-icon">🐛</div>
              <div class="contact-details">
                <h3>Bug Reports</h3>
                <p><a href="https://github.com/xRiskLab" target="_blank">Report Issues</a></p>
                <small>Found a bug? Let us know on GitHub</small>
              </div>
            </div>
          </div>
        </div>

        <div class="contact-section glass-surface">
          <h2>What We Can Help With</h2>
          <ul class="help-list">
            <li><strong>Technical Support:</strong> Get help with implementation and troubleshooting</li>
            <li><strong>Custom Solutions:</strong> Discuss tailored solutions for your specific needs</li>
            <li><strong>Training & Consulting:</strong> Learn best practices for interpretable ML</li>
            <li><strong>Partnership Opportunities:</strong> Explore collaboration possibilities</li>
            <li><strong>Feature Requests:</strong> Suggest new features and improvements</li>
          </ul>
        </div>

        <div class="contact-section glass-surface">
          <h2>Community</h2>
          <p>Join our growing community of data scientists, risk managers, and ML practitioners working on interpretable machine learning solutions.</p>
          
          <div class="community-links">
            <a href="https://github.com/xRiskLab" class="community-link glass-surface-hover" target="_blank">
              <div class="community-icon">📚</div>
              <div>
                <h4>GitHub</h4>
                <p>Explore our open-source projects</p>
              </div>
            </a>
            
            <a href="https://github.com/xRiskLab" class="community-link glass-surface-hover" target="_blank">
              <div class="community-icon">💡</div>
              <div>
                <h4>Discussions</h4>
                <p>Join technical discussions</p>
              </div>
            </a>
            
            <a href="https://github.com/xRiskLab" class="community-link glass-surface-hover" target="_blank">
              <div class="community-icon">🤝</div>
              <div>
                <h4>Contributing</h4>
                <p>Contribute to our projects</p>
              </div>
            </a>
          </div>
        </div>
      </div>

      <div class="contact-form-section">
        <div class="contact-form glass-surface">
          <h2>Send us a Message</h2>
          <p>Have a specific question or project in mind? We'd love to hear about it.</p>
          
          <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="form">
            <div class="form-group">
              <label for="name">Name *</label>
              <input type="text" id="name" name="name" required>
            </div>
            
            <div class="form-group">
              <label for="email">Email *</label>
              <input type="email" id="email" name="email" required>
            </div>
            
            <div class="form-group">
              <label for="company">Company/Organization</label>
              <input type="text" id="company" name="company">
            </div>
            
            <div class="form-group">
              <label for="subject">Subject *</label>
              <select id="subject" name="subject" required>
                <option value="">Select a topic</option>
                <option value="technical-support">Technical Support</option>
                <option value="custom-solution">Custom Solution</option>
                <option value="training-consulting">Training & Consulting</option>
                <option value="partnership">Partnership Opportunity</option>
                <option value="feature-request">Feature Request</option>
                <option value="other">Other</option>
              </select>
            </div>
            
            <div class="form-group">
              <label for="message">Message *</label>
              <textarea id="message" name="message" rows="6" required placeholder="Tell us about your project, questions, or how we can help..."></textarea>
            </div>
            
            <button type="submit" class="btn btn-primary">Send Message</button>
          </form>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
.contact-hero {
  background: transparent;
  padding: 80px 0 40px;
  text-align: center;
}

.contact-title {
  font-size: clamp(2.5rem, 6vw, 3.5rem);
  font-weight: 700;
  margin-bottom: 24px;
  color: var(--text-primary);
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.contact-subtitle {
  font-size: clamp(1.125rem, 3vw, 1.375rem);
  color: var(--text-secondary);
  max-width: 700px;
  margin: 0 auto;
  line-height: 1.5;
}

.contact-content {
  padding: 80px 0;
}

.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px;
  max-width: 1200px;
  margin: 0 auto;
}

.contact-section {
  backdrop-filter: var(--blur-amount);
  -webkit-backdrop-filter: var(--blur-amount);
  border-radius: 20px;
  padding: 32px;
  margin-bottom: 32px;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.contact-section h2 {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 24px;
  color: var(--text-primary);
}

.contact-items {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.contact-item {
  display: flex;
  align-items: flex-start;
  gap: 16px;
  padding: 20px;
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 12px;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.contact-item:hover {
  background: rgba(255, 255, 255, 0.05);
  transform: translateY(-2px);
}

.contact-icon {
  font-size: 32px;
  flex-shrink: 0;
  filter: grayscale(1);
  transition: filter 0.3s ease;
}

.contact-item:hover .contact-icon {
  filter: grayscale(0);
}

.contact-details h3 {
  font-size: 1.125rem;
  font-weight: 600;
  margin-bottom: 8px;
  color: var(--text-primary);
}

.contact-details p {
  margin-bottom: 8px;
  color: var(--text-secondary);
}

.contact-details a {
  color: var(--accent-blue);
  text-decoration: none;
  transition: color 0.3s ease;
}

.contact-details a:hover {
  color: var(--accent-purple);
}

.contact-details small {
  color: var(--text-tertiary);
  font-size: 13px;
}

.help-list {
  list-style: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.help-list li {
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 12px;
  padding: 20px;
  color: var(--text-secondary);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  line-height: 1.6;
}

.help-list li:hover {
  background: rgba(255, 255, 255, 0.05);
  transform: translateX(4px);
}

.help-list li strong {
  color: var(--accent-blue);
  font-weight: 600;
}

.contact-section p {
  color: var(--text-secondary);
  margin-bottom: 24px;
  line-height: 1.6;
}

.community-links {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.community-link {
  display: flex;
  align-items: center;
  gap: 16px;
  padding: 20px;
  background: var(--surface-glass);
  backdrop-filter: var(--blur-amount);
  -webkit-backdrop-filter: var(--blur-amount);
  border: 1px solid var(--border-glass);
  border-radius: 12px;
  text-decoration: none;
  color: inherit;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.community-link:hover {
  transform: translateY(-4px);
  background: var(--surface-glass-hover);
  box-shadow: var(--shadow-glass);
}

.community-icon {
  font-size: 32px;
  flex-shrink: 0;
  filter: grayscale(1);
  transition: filter 0.3s ease;
}

.community-link:hover .community-icon {
  filter: grayscale(0);
}

.community-link h4 {
  font-size: 1.125rem;
  font-weight: 600;
  margin-bottom: 4px;
  color: var(--text-primary);
}

.community-link p {
  color: var(--text-secondary);
  margin: 0;
  font-size: 14px;
}

.contact-form {
  backdrop-filter: var(--blur-amount);
  -webkit-backdrop-filter: var(--blur-amount);
  border-radius: 20px;
  padding: 32px;
  position: sticky;
  top: 120px;
}

.contact-form h2 {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 16px;
  color: var(--text-primary);
}

.contact-form > p {
  color: var(--text-secondary);
  margin-bottom: 32px;
  line-height: 1.6;
}

.form {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.form-group {
  display: flex;
  flex-direction: column;
}

.form-group label {
  font-weight: 500;
  margin-bottom: 8px;
  color: var(--text-primary);
  font-size: 14px;
}

.form-group input,
.form-group select,
.form-group textarea {
  padding: 12px 16px;
  border: 1px solid var(--border-glass);
  border-radius: 12px;
  background: rgba(255, 255, 255, 0.05);
  color: var(--text-primary);
  font-family: inherit;
  font-size: 15px;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--accent-blue);
  box-shadow: 0 0 0 3px rgba(0, 122, 255, 0.1);
  background: rgba(255, 255, 255, 0.08);
}

.form-group input::placeholder,
.form-group textarea::placeholder {
  color: var(--text-tertiary);
}

.form-group textarea {
  resize: vertical;
  min-height: 120px;
  line-height: 1.5;
}

.form-group select {
  cursor: pointer;
}

/* Custom select arrow for consistency */
.form-group select {
  appearance: none;
  background-image: url('data:image/svg+xml;charset=US-ASCII,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="%23999"><path d="M8 12L2 6h12z"/></svg>');
  background-repeat: no-repeat;
  background-position: right 12px center;
  background-size: 12px;
  padding-right: 40px;
}

@media (max-width: 768px) {
  .contact-grid {
    grid-template-columns: 1fr;
    gap: 32px;
  }
  
  .contact-form {
    position: static;
  }
  
  .contact-item {
    flex-direction: column;
    text-align: center;
    gap: 12px;
  }
  
  .community-links {
    gap: 12px;
  }

  .contact-section {
    padding: 24px;
  }

  .contact-form {
    padding: 24px;
  }
}

@media (max-width: 480px) {
  .contact-section {
    padding: 20px;
  }

  .contact-form {
    padding: 20px;
  }

  .contact-item {
    padding: 16px;
  }

  .community-link {
    padding: 16px;
  }

  .help-list li {
    padding: 16px;
  }
}
</style>
