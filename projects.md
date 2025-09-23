---------

layout: default

title: "Projects"layout: defaultlayout: default

---

title: "Projects"title: "Projects"

<section class="projects-hero">

  <div class="container">------

    <h1 class="projects-title">Open Source Projects</h1>

    <p class="projects-subtitle">Advanced machine learning libraries for risk management and interpretable AI</p>

  </div>

</section><section class="projects-hero"><section class="projects-hero">



<section class="projects-section">  <div class="container">  <div class="container">

  <div class="container">

    <div class="projects-grid">    <h1 class="projects-title">Open Source Projects</h1>    <h1 class="projects-title">Open Source Projects</h1>

      {% for project in site.projects %}

      <div class="project-card glass-surface-hover{% if project.featured %} featured{% endif %}">    <p class="projects-subtitle">Advanced machine learning libraries for risk assessment and interpretable AI</p>    <p class="projects-subtitle">Advanced machine learning libraries for risk assessment and interpretable AI</p>

        {% if project.image %}

        <div class="project-image">  </div>  </div>

          <img src="{{ project.image }}" alt="{{ project.title }}" loading="lazy">

          {% if project.featured %}</section></section>

          <div class="project-overlay">

            <span class="badge badge-featured">Featured</span>

          </div>

          {% endif %}<section class="projects-section"><section class="projects-section">

        </div>

        {% endif %}  <div class="container">  <div class="container">

        <div class="project-content">

          <div class="project-header">    <div class="projects-grid">    <div class="projects-grid">

            <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>

            <div class="project-badges">      {% for project in site.projects %}      <div class="project-card glass-surface-hover featured">

              {% for tag in project.tags limit:2 %}

              <span class="badge {% cycle 'badge-primary', 'badge-secondary' %}">{{ tag }}</span>      <div class="project-card glass-surface-hover{% if project.featured %} featured{% endif %}">        <div class="project-image">

              {% endfor %}

            </div>        {% if project.image %}          <img src="/assets/images/projects/fastwoe-workflow.png" alt="FastWoe Workflow Diagram" loading="lazy">

          </div>

          <p>{{ project.description }}</p>        <div class="project-image">          <div class="project-overlay">

          <div class="project-footer">

            <div class="project-links">          <img src="{{ project.image }}" alt="{{ project.title }}" loading="lazy">            <span class="badge badge-featured">Featured</span>

              <a href="{{ project.github }}" class="btn btn-outline btn-sm">GitHub</a>

              {% if project.pypi %}          {% if project.featured %}          </div>

              <a href="{{ project.pypi }}" class="btn btn-secondary btn-sm">PyPI</a>

              {% endif %}          <div class="project-overlay">        </div>

            </div>

          </div>            <span class="badge badge-featured">Featured</span>        <div class="project-content">

        </div>

      </div>          </div>          <div class="project-header">

      {% endfor %}

    </div>          {% endif %}            <h3><a href="/fastwoe/">FastWoe</a></h3>

  </div>

</section>        </div>            <div class="project-badges">



<section class="projects-contribute">        {% endif %}              <span class="badge badge-primary">Scikit-learn</span>

  <div class="container">

    <div class="contribute-content">        <div class="project-content">              <span class="badge badge-secondary">Statistics</span>

      <h2>Contribute to xRiskLab</h2>

      <p>Our projects are open source and community-driven. We welcome contributions from developers, data scientists, and researchers who share our vision of interpretable machine learning.</p>          <div class="project-header">            </div>

      <div class="contribute-buttons">

        <a href="https://github.com/xRiskLab" class="btn btn-primary">View on GitHub</a>            <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>          </div>

        <a href="/contact/" class="btn btn-secondary">Get in Touch</a>

      </div>            <div class="project-badges">          <p>Lightweight Weight of Evidence encoding with comprehensive statistics and inference capabilities. Built for fast, efficient feature engineering in credit scoring and risk modeling.</p>

    </div>

  </div>              {% for tag in project.tags limit:2 %}          <div class="project-features">

</section>

              <span class="badge {% cycle 'badge-primary', 'badge-secondary' %}">{{ tag }}</span>            <ul>

<style>

.projects-hero {              {% endfor %}              <li>✨ Efficient WOE encoding algorithms</li>

  background: transparent;

  padding: 80px 0 40px;            </div>              <li>📊 Statistical significance testing</li>

  text-align: center;

}          </div>              <li>🔍 Information Value calculations</li>



.projects-title {          <p>{{ project.description }}</p>              <li>⚡ High-performance implementation</li>

  font-size: clamp(2.5rem, 6vw, 3.5rem);

  font-weight: 700;          <div class="project-footer">            </ul>

  margin-bottom: 24px;

  color: var(--text-primary);            <div class="project-links">          </div>

  background: var(--primary-gradient);

  -webkit-background-clip: text;              <a href="{{ project.github }}" class="btn btn-outline btn-sm">GitHub</a>          <div class="project-footer">

  -webkit-text-fill-color: transparent;

  background-clip: text;              {% if project.pypi %}            <div class="project-links">

}

              <a href="{{ project.pypi }}" class="btn btn-secondary btn-sm">PyPI</a>              <a href="https://github.com/xRiskLab/fastwoe" class="btn btn-outline btn-sm">GitHub</a>

.projects-subtitle {

  font-size: clamp(1.125rem, 3vw, 1.375rem);              {% endif %}              <a href="https://pypi.org/project/fastwoe/" class="btn btn-secondary btn-sm">PyPI</a>

  color: var(--text-secondary);

  max-width: 700px;            </div>              <a href="/assets/papers/fastwoe-statistical-inference-2023.pdf" class="btn btn-research btn-sm">📄 Paper</a>

  margin: 0 auto;

  line-height: 1.5;          </div>            </div>

}

        </div>          </div>

.projects-section {

  padding: 80px 0;      </div>        </div>

}

      {% endfor %}      </div>

.projects-grid {

  display: grid;    </div>

  grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));

  gap: 32px;  </div>      <div class="project-card glass-surface-hover">

}

</section>        <div class="project-header">

.project-card {

  background: var(--surface-glass);          <h3><a href="/woeboost/">WoeBoost</a></h3>

  backdrop-filter: var(--blur-amount);

  -webkit-backdrop-filter: var(--blur-amount);<section class="projects-contribute">          <div class="project-badges">

  border: 1px solid var(--border-glass);

  border-radius: 20px;  <div class="container">            <span class="badge badge-primary">Machine Learning</span>

  padding: 0;

  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);    <div class="contribute-content">            <span class="badge badge-secondary">Interpretability</span>

  position: relative;

  overflow: hidden;      <h2>Contribute to xRiskLab</h2>          </div>

  display: flex;

  flex-direction: column;      <p>Our projects are open source and community-driven. We welcome contributions from developers, data scientists, and researchers who share our vision of interpretable machine learning.</p>        </div>

  height: 100%;

}      <div class="contribute-buttons">        <p>Interpretable gradient boosting with WOE-based scoring for high-stakes domains. Combines the power of XGBoost with the interpretability requirements of regulated industries.</p>



.project-card.featured {        <a href="https://github.com/xRiskLab" class="btn btn-primary">View on GitHub</a>        <div class="project-features">

  border-color: var(--accent-blue);

  background: rgba(0, 122, 255, 0.08);        <a href="/contact/" class="btn btn-secondary">Get in Touch</a>          <ul>

}

      </div>            <li>🎯 WOE-based feature transformations</li>

.project-card::before {

  content: '';    </div>            <li>� Model interpretability tools</li>

  position: absolute;

  top: 0;  </div>            <li>📈 Performance optimization</li>

  left: 0;

  right: 0;</section>            <li>⚖️ Regulatory compliance features</li>

  height: 1px;

  background: var(--primary-gradient);          </ul>

  transform: translateX(-100%);

  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);<style>        </div>

  z-index: 2;

}.projects-hero {        <div class="project-footer">



.project-card:hover::before {  background: transparent;          <div class="project-links">

  transform: translateX(0);

}  padding: 80px 0 40px;            <a href="https://github.com/xRiskLab/woeboost" class="btn btn-outline btn-sm">GitHub</a>



.project-card:hover {  text-align: center;            <a href="https://pypi.org/project/woeboost/" class="btn btn-secondary btn-sm">PyPI</a>

  transform: translateY(-8px);

  background: var(--surface-glass-hover);}          </div>

  box-shadow: var(--shadow-glass);

}        </div>



.project-image {.projects-title {      </div>

  position: relative;

  width: 100%;  font-size: clamp(2.5rem, 6vw, 3.5rem);

  height: 200px;

  overflow: hidden;  font-weight: 700;      <div class="project-card glass-surface-hover">

  border-radius: 20px 20px 0 0;

}  margin-bottom: 24px;        <div class="project-header">



.project-image img {  color: var(--text-primary);          <h3><a href="/xbooster/">xBooster</a></h3>

  width: 100%;

  height: 100%;  background: var(--primary-gradient);          <div class="project-badges">

  object-fit: cover;

  transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);  -webkit-background-clip: text;            <span class="badge badge-primary">XGBoost</span>

}

  -webkit-text-fill-color: transparent;            <span class="badge badge-secondary">CatBoost</span>

.project-card:hover .project-image img {

  transform: scale(1.05);  background-clip: text;          </div>

}

}        </div>

.project-overlay {

  position: absolute;        <p>Comprehensive scorecard framework for XGBoost and CatBoost with SQL deployment capabilities. Streamlines model development from training to production deployment.</p>

  top: 16px;

  right: 16px;.projects-subtitle {        <div class="project-features">

  z-index: 2;

}  font-size: clamp(1.125rem, 3vw, 1.375rem);          <ul>



.project-content {  color: var(--text-secondary);            <li>🚀 End-to-end model pipeline</li>

  padding: 32px;

  display: flex;  max-width: 700px;            <li>� SQL code generation</li>

  flex-direction: column;

  flex-grow: 1;  margin: 0 auto;            <li>📊 Model monitoring tools</li>

}

  line-height: 1.5;            <li>� Production deployment</li>

.project-header {

  margin-bottom: 20px;}          </ul>

}

        </div>

.project-header h3 {

  font-size: 1.5rem;.projects-section {        <div class="project-footer">

  font-weight: 600;

  margin-bottom: 12px;  padding: 80px 0;          <div class="project-links">

  color: var(--text-primary);

  transition: all 0.3s ease;}            <a href="https://github.com/xRiskLab/xBooster" class="btn btn-outline btn-sm">GitHub</a>

}

            <a href="https://pypi.org/project/xbooster/" class="btn btn-secondary btn-sm">PyPI</a>

.project-header h3 a {

  color: inherit;.projects-grid {          </div>

  text-decoration: none;

  transition: all 0.3s ease;  display: grid;        </div>

}

  grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));      </div>

.project-card:hover .project-header h3 {

  background: var(--primary-gradient);  gap: 32px;

  -webkit-background-clip: text;

  -webkit-text-fill-color: transparent;}      <div class="project-card glass-surface-hover">

  background-clip: text;

}        <div class="project-header">



.project-badges {.project-card {          <h3><a href="/projects/fisher-scoring/">Fisher Scoring</a></h3>

  display: flex;

  gap: 8px;  background: var(--surface-glass);          <div class="project-badges">

  flex-wrap: wrap;

}  backdrop-filter: var(--blur-amount);            <span class="badge badge-primary">Statistics</span>



.badge {  -webkit-backdrop-filter: var(--blur-amount);            <span class="badge badge-secondary">Machine Learning</span>

  padding: 4px 12px;

  border-radius: 12px;  border: 1px solid var(--border-glass);          </div>

  font-size: 12px;

  font-weight: 500;  border-radius: 20px;        </div>

}

  padding: 0;        <p>Efficient implementation of Fisher's scoring algorithm for maximum likelihood estimation with numerical optimization and convergence diagnostics.</p>

.badge-primary {

  background: rgba(0, 122, 255, 0.15);  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);        <div class="project-features">

  color: var(--accent-blue);

  border: 1px solid rgba(0, 122, 255, 0.2);  position: relative;          <ul>

}

  overflow: hidden;            <li>📈 MLE optimization</li>

.badge-secondary {

  background: rgba(88, 86, 214, 0.15);  display: flex;            <li>⚡ Fast convergence</li>

  color: var(--accent-purple);

  border: 1px solid rgba(88, 86, 214, 0.2);  flex-direction: column;            <li>🔬 Statistical rigor</li>

}

  height: 100%;            <li>📊 Diagnostic tools</li>

.badge-featured {

  background: rgba(255, 45, 146, 0.15);}          </ul>

  color: var(--accent-pink);

  border: 1px solid rgba(255, 45, 146, 0.2);        </div>

  font-weight: 600;

}.project-card.featured {        <div class="project-footer">



.project-card p {  border-color: var(--accent-blue);          <div class="project-links">

  color: var(--text-secondary);

  margin-bottom: 24px;  background: rgba(0, 122, 255, 0.08);            <a href="https://github.com/xRiskLab/fisher-scoring" class="btn btn-outline btn-sm">GitHub</a>

  line-height: 1.6;

  font-size: 15px;}            <a href="https://pypi.org/project/fisher-scoring/" class="btn btn-secondary btn-sm">PyPI</a>

  flex-grow: 1;

}          </div>



.project-footer {.project-card::before {        </div>

  margin-top: auto;

}  content: '';      </div>



.project-links {  position: absolute;

  display: flex;

  gap: 12px;  top: 0;      <div class="project-card glass-surface-hover">

  flex-wrap: wrap;

}  left: 0;        <div class="project-header">



.btn-sm {  right: 0;          <h3><a href="/projects/pearsonify/">Pearsonify</a></h3>

  padding: 8px 16px;

  font-size: 13px;  height: 1px;          <div class="project-badges">

  border-radius: 8px;

}  background: var(--primary-gradient);            <span class="badge badge-primary">Correlation</span>



.projects-contribute {  transform: translateX(-100%);            <span class="badge badge-secondary">Analysis</span>

  background: var(--surface-glass);

  backdrop-filter: var(--blur-amount);  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);          </div>

  -webkit-backdrop-filter: var(--blur-amount);

  border: 1px solid var(--border-glass);  z-index: 2;        </div>

  border-radius: 20px;

  margin: 40px auto;}        <p>Advanced correlation analysis and data transformation toolkit using Pearson correlation methods and statistical techniques for data science workflows.</p>

  max-width: 800px;

  padding: 48px 32px;        <div class="project-features">

  text-align: center;

}.project-card:hover::before {          <ul>



.contribute-content h2 {  transform: translateX(0);            <li>📊 Correlation analysis</li>

  font-size: 2rem;

  font-weight: 600;}            <li>🔄 Data transformation</li>

  margin-bottom: 20px;

  color: var(--text-primary);            <li>📈 Statistical methods</li>

}

.project-card:hover {            <li>🎯 Feature selection</li>

.contribute-content p {

  color: var(--text-secondary);  transform: translateY(-8px);          </ul>

  margin-bottom: 32px;

  line-height: 1.6;  background: var(--surface-glass-hover);        </div>

  font-size: 16px;

}  box-shadow: var(--shadow-glass);        <div class="project-footer">



.contribute-buttons {}          <div class="project-links">

  display: flex;

  gap: 16px;            <a href="https://github.com/xRiskLab/pearsonify" class="btn btn-outline btn-sm">GitHub</a>

  justify-content: center;

  flex-wrap: wrap;.project-image {            <a href="https://pypi.org/project/pearsonify/" class="btn btn-secondary btn-sm">PyPI</a>

}

  position: relative;          </div>

@media (max-width: 768px) {

  .projects-grid {  width: 100%;        </div>

    grid-template-columns: 1fr;

    gap: 24px;  height: 200px;      </div>

  }

  overflow: hidden;

  .contribute-buttons {

    flex-direction: column;  border-radius: 20px 20px 0 0;      <div class="project-card glass-surface-hover">

    align-items: center;

  }}        <div class="project-header">



  .projects-contribute {          <h3><a href="/projects/rf-explainer/">RF Explainer</a></h3>

    margin: 40px 16px;

    padding: 32px 24px;.project-image img {          <div class="project-badges">

  }

}  width: 100%;            <span class="badge badge-primary">Scikit-learn</span>

</style>
  height: 100%;            <span class="badge badge-secondary">Random Forest</span>

  object-fit: cover;          </div>

  transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);        </div>

}        <p>Comprehensive interpretability tools for Random Forest models with feature importance analysis and model explanation capabilities for ML transparency.</p>

        <div class="project-features">

.project-card:hover .project-image img {          <ul>

  transform: scale(1.05);            <li>🌲 Random Forest analysis</li>

}            <li>🔍 Model explainability</li>

            <li>📊 Feature importance</li>

.project-overlay {            <li>📈 Visualization tools</li>

  position: absolute;          </ul>

  top: 16px;        </div>

  right: 16px;        <div class="project-footer">

  z-index: 2;          <div class="project-links">

}            <a href="https://github.com/xRiskLab/rf-explainer" class="btn btn-outline btn-sm">GitHub</a>

            <a href="https://pypi.org/project/rf-explainer/" class="btn btn-secondary btn-sm">PyPI</a>

.project-content {          </div>

  padding: 32px;        </div>

  display: flex;      </div>

  flex-direction: column;    </div>

  flex-grow: 1;  </div>

}</section>



.project-header {<section class="projects-contribute">

  margin-bottom: 20px;  <div class="container">

}    <div class="contribute-content">

      <h2>Contribute to xRiskLab</h2>

.project-header h3 {      <p>Our projects are open source and community-driven. We welcome contributions from developers, data scientists, and researchers who share our vision of interpretable machine learning.</p>

  font-size: 1.5rem;      <div class="contribute-buttons">

  font-weight: 600;        <a href="https://github.com/xRiskLab" class="btn btn-primary">View on GitHub</a>

  margin-bottom: 12px;        <a href="/contact/" class="btn btn-secondary">Get in Touch</a>

  color: var(--text-primary);      </div>

  transition: all 0.3s ease;    </div>

}  </div>

</section>

.project-header h3 a {

  color: inherit;<style>

  text-decoration: none;.projects-hero {

  transition: all 0.3s ease;  background: transparent;

}  padding: 80px 0 40px;

  text-align: center;

.project-card:hover .project-header h3 {}

  background: var(--primary-gradient);

  -webkit-background-clip: text;.projects-title {

  -webkit-text-fill-color: transparent;  font-size: clamp(2.5rem, 6vw, 3.5rem);

  background-clip: text;  font-weight: 700;

}  margin-bottom: 24px;

  color: var(--text-primary);

.project-badges {  background: var(--primary-gradient);

  display: flex;  -webkit-background-clip: text;

  gap: 8px;  -webkit-text-fill-color: transparent;

  flex-wrap: wrap;  background-clip: text;

}}



.badge {.projects-subtitle {

  padding: 4px 12px;  font-size: clamp(1.125rem, 3vw, 1.375rem);

  border-radius: 12px;  color: var(--text-secondary);

  font-size: 12px;  max-width: 700px;

  font-weight: 500;  margin: 0 auto;

}  line-height: 1.5;

}

.badge-primary {

  background: rgba(0, 122, 255, 0.15);.projects-section {

  color: var(--accent-blue);  padding: 80px 0;

  border: 1px solid rgba(0, 122, 255, 0.2);}

}

.projects-grid {

.badge-secondary {  display: grid;

  background: rgba(88, 86, 214, 0.15);  grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));

  color: var(--accent-purple);  gap: 32px;

  border: 1px solid rgba(88, 86, 214, 0.2);}

}

.project-card {

.badge-featured {  background: var(--surface-glass);

  background: rgba(255, 45, 146, 0.15);  backdrop-filter: var(--blur-amount);

  color: var(--accent-pink);  -webkit-backdrop-filter: var(--blur-amount);

  border: 1px solid rgba(255, 45, 146, 0.2);  border: 1px solid var(--border-glass);

  font-weight: 600;  border-radius: 20px;

}  padding: 0;

  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);

.project-card p {  position: relative;

  color: var(--text-secondary);  overflow: hidden;

  margin-bottom: 24px;  display: flex;

  line-height: 1.6;  flex-direction: column;

  font-size: 15px;  height: 100%;

  flex-grow: 1;}

}

.project-card.featured {

.project-footer {  border-color: var(--accent-blue);

  margin-top: auto;  background: rgba(0, 122, 255, 0.08);

}}



.project-links {.project-card::before {

  display: flex;  content: '';

  gap: 12px;  position: absolute;

  flex-wrap: wrap;  top: 0;

}  left: 0;

  right: 0;

.btn-sm {  height: 1px;

  padding: 8px 16px;  background: var(--primary-gradient);

  font-size: 13px;  transform: translateX(-100%);

  border-radius: 8px;  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);

}  z-index: 2;

}

.projects-contribute {

  background: var(--surface-glass);.project-card:hover::before {

  backdrop-filter: var(--blur-amount);  transform: translateX(0);

  -webkit-backdrop-filter: var(--blur-amount);}

  border: 1px solid var(--border-glass);

  border-radius: 20px;.project-card:hover {

  margin: 40px auto;  transform: translateY(-8px);

  max-width: 800px;  background: var(--surface-glass-hover);

  padding: 48px 32px;  box-shadow: var(--shadow-glass);

  text-align: center;}

}

.project-image {

.contribute-content h2 {  position: relative;

  font-size: 2rem;  width: 100%;

  font-weight: 600;  height: 200px;

  margin-bottom: 20px;  overflow: hidden;

  color: var(--text-primary);  border-radius: 20px 20px 0 0;

}}



.contribute-content p {.project-image img {

  color: var(--text-secondary);  width: 100%;

  margin-bottom: 32px;  height: 100%;

  line-height: 1.6;  object-fit: cover;

  font-size: 16px;  transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);

}}



.contribute-buttons {.project-card:hover .project-image img {

  display: flex;  transform: scale(1.05);

  gap: 16px;}

  justify-content: center;

  flex-wrap: wrap;.project-overlay {

}  position: absolute;

  top: 16px;

@media (max-width: 768px) {  right: 16px;

  .projects-grid {  z-index: 2;

    grid-template-columns: 1fr;}

    gap: 24px;

  }.project-content {

  padding: 32px;

  .contribute-buttons {  display: flex;

    flex-direction: column;  flex-direction: column;

    align-items: center;  flex-grow: 1;

  }}



  .projects-contribute {.project-header {

    margin: 40px 16px;  margin-bottom: 20px;

    padding: 32px 24px;}

  }

}.project-header h3 {

</style>  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 12px;
  color: var(--text-primary);
  transition: all 0.3s ease;
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
  gap: 8px;
  flex-wrap: wrap;
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

.project-card p {
  color: var(--text-secondary);
  margin-bottom: 24px;
  line-height: 1.6;
  font-size: 15px;
  flex-grow: 1;
}

.project-features {
  margin-bottom: 24px;
}

.project-features ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.project-features li {
  color: var(--text-secondary);
  font-size: 14px;
  padding: 8px 0;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
  transition: color 0.3s ease;
}

.project-features li:last-child {
  border-bottom: none;
}

.project-features li:hover {
  color: var(--text-primary);
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
  background: rgba(175, 82, 222, 0.15);
  color: var(--accent-pink);
  border: 1px solid rgba(175, 82, 222, 0.3);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.btn-research:hover {
  background: rgba(175, 82, 222, 0.25);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(175, 82, 222, 0.3);
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

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
    gap: 24px;
  }

  .project-card {
    padding: 24px;
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
