---
layout: default
title: "Contact"
---

<div class="contact-page">
  <div class="container">
    <div class="contact-hero">
      <h1>Get in Touch</h1>
      <p class="lead">Ready to transform your risk assessment models? We'd love to hear from you.</p>
    </div>

    <div class="contact-content">
      <div class="contact-info">
        <div class="contact-section">
          <h2>Contact Information</h2>
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

        <div class="contact-section">
          <h2>What We Can Help With</h2>
          <ul class="help-list">
            <li><strong>Technical Support:</strong> Get help with implementation and troubleshooting</li>
            <li><strong>Custom Solutions:</strong> Discuss tailored solutions for your specific needs</li>
            <li><strong>Training & Consulting:</strong> Learn best practices for interpretable ML</li>
            <li><strong>Partnership Opportunities:</strong> Explore collaboration possibilities</li>
            <li><strong>Feature Requests:</strong> Suggest new features and improvements</li>
          </ul>
        </div>

        <div class="contact-section">
          <h2>Community</h2>
          <p>Join our growing community of data scientists, risk managers, and ML practitioners working on interpretable machine learning solutions.</p>
          
          <div class="community-links">
            <a href="https://github.com/xRiskLab" class="community-link" target="_blank">
              <div class="community-icon">📚</div>
              <div>
                <h4>GitHub</h4>
                <p>Explore our open-source projects</p>
              </div>
            </a>
            
            <a href="https://github.com/xRiskLab" class="community-link" target="_blank">
              <div class="community-icon">💡</div>
              <div>
                <h4>Discussions</h4>
                <p>Join technical discussions</p>
              </div>
            </a>
            
            <a href="https://github.com/xRiskLab" class="community-link" target="_blank">
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
        <div class="contact-form">
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
</div>

<style>
.contact-page {
  background: #0a0a0a;
  min-height: 100vh;
  padding: 2rem 0;
}

.contact-hero {
  text-align: center;
  margin-bottom: 4rem;
  padding: 2rem 0;
}

.contact-hero h1 {
  font-size: 3rem;
  font-weight: 700;
  margin-bottom: 1rem;
  color: #ffffff;
}

.lead {
  font-size: 1.25rem;
  color: #cccccc;
  max-width: 600px;
  margin: 0 auto;
}

.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  max-width: 1200px;
  margin: 0 auto;
}

.contact-section {
  margin-bottom: 3rem;
}

.contact-section h2 {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 1.5rem;
  color: #20c997;
}

.contact-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  margin-bottom: 2rem;
  padding: 1.5rem;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 12px;
}

.contact-icon {
  font-size: 2rem;
  flex-shrink: 0;
}

.contact-details h3 {
  font-size: 1.125rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  color: #ffffff;
}

.contact-details p {
  margin-bottom: 0.5rem;
}

.contact-details a {
  color: #20c997;
  text-decoration: none;
}

.contact-details a:hover {
  color: #17a2b8;
}

.contact-details small {
  color: #888888;
  font-size: 0.875rem;
}

.help-list {
  list-style: none;
  padding: 0;
}

.help-list li {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 8px;
  padding: 1.5rem;
  margin-bottom: 1rem;
  color: #cccccc;
}

.help-list li strong {
  color: #20c997;
}

.community-links {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.community-link {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1.5rem;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 12px;
  text-decoration: none;
  color: inherit;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.community-link:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(32, 201, 151, 0.2);
}

.community-icon {
  font-size: 2rem;
  flex-shrink: 0;
}

.community-link h4 {
  font-size: 1.125rem;
  font-weight: 600;
  margin-bottom: 0.25rem;
  color: #20c997;
}

.community-link p {
  color: #cccccc;
  margin: 0;
  font-size: 0.875rem;
}

.contact-form {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 12px;
  padding: 2rem;
}

.contact-form h2 {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 1rem;
  color: #20c997;
}

.contact-form p {
  color: #cccccc;
  margin-bottom: 2rem;
}

.form {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.form-group {
  display: flex;
  flex-direction: column;
}

.form-group label {
  font-weight: 500;
  margin-bottom: 0.5rem;
  color: #ffffff;
}

.form-group input,
.form-group select,
.form-group textarea {
  padding: 0.75rem;
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 8px;
  background: rgba(255, 255, 255, 0.05);
  color: #ffffff;
  font-family: inherit;
  font-size: 1rem;
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #20c997;
  box-shadow: 0 0 0 2px rgba(32, 201, 151, 0.2);
}

.form-group input::placeholder,
.form-group textarea::placeholder {
  color: #888888;
}

.form-group textarea {
  resize: vertical;
  min-height: 120px;
}

@media (max-width: 768px) {
  .contact-hero h1 {
    font-size: 2rem;
  }
  
  .lead {
    font-size: 1.125rem;
  }
  
  .contact-content {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  
  .contact-item {
    flex-direction: column;
    text-align: center;
  }
  
  .community-links {
    flex-direction: column;
  }
}
</style>
