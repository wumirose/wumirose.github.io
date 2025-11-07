<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Olawumi Olasunkanmi - Computer Science PhD Candidate</title>
  <style>
    body {
      font-family: Arial, Helvetica, sans-serif;
      line-height: 1.6;
      color: #2C3E50;
      margin: 0;
      padding: 0;
      background-color: #FAFBFC;
    }
    
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 20px;
    }
    
    /* Hero Section */
    .hero {
      background: linear-gradient(135deg, #4B9CD3 0%, #357ABD 100%);
      color: white;
      padding: 60px 20px;
      text-align: center;
      margin-top: 80px;
    }
    
    .hero h1 {
      font-size: 42px;
      margin: 0 0 10px 0;
    }
    
    .hero p {
      font-size: 20px;
      margin: 5px 0;
    }
    
    /* Section Styling */
    .section {
      background: white;
      margin: 30px 0;
      padding: 40px;
      border-radius: 12px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.08);
    }
    
    .section h2 {
      color: #357ABD;
      font-size: 28px;
      margin-top: 0;
      padding-bottom: 10px;
      border-bottom: 3px solid #4B9CD3;
    }
    
    /* Card Grid */
    .card-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      margin-top: 20px;
    }
    
    .card {
      background: #F8F9FA;
      padding: 25px;
      border-radius: 10px;
      border-left: 4px solid #4B9CD3;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    
    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 16px rgba(75, 156, 211, 0.2);
    }
    
    .card h3 {
      color: #357ABD;
      margin-top: 0;
      font-size: 22px;
    }
    
    /* Quick Links */
    .quick-links {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      margin-top: 20px;
    }
    
    .quick-link {
      background: #4B9CD3;
      color: white;
      padding: 12px 24px;
      border-radius: 8px;
      text-decoration: none;
      transition: all 0.3s;
      display: inline-block;
    }
    
    .quick-link:hover {
      background: #357ABD;
      transform: translateY(-2px);
      box-shadow: 0 4px 12px rgba(75, 156, 211, 0.3);
    }
    
    /* Skills Badges */
    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 15px;
    }
    
    .skill-badge {
      background: #E8F4F8;
      color: #357ABD;
      padding: 8px 16px;
      border-radius: 20px;
      font-size: 14px;
      font-weight: 500;
    }
    
    /* Call-to-Action Box */
    .cta-box {
      background: linear-gradient(135deg, #E8F4F8 0%, #D0E8F5 100%);
      padding: 30px;
      border-radius: 12px;
      border: 2px solid #4B9CD3;
      text-align: center;
      margin-top: 30px;
    }
    
    .cta-box h3 {
      color: #357ABD;
      margin-top: 0;
    }
    
    /* Footer */
    footer {
      background: #2C3E50;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 50px;
    }
    
    @media (max-width: 768px) {
      .hero h1 { font-size: 32px; }
      .section { padding: 25px; }
      .card-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

[Your Navbar Here]

<!-- Hero Section -->
<div class="hero">
  <h1>Olawumi Roseline Olasunkanmi</h1>
  <p>Doctoral Candidate in Computer Science</p>
  <p>University of North Carolina at Chapel Hill</p>
  <p style="margin-top: 15px;">🎓 Expected Graduation: May 2026</p>
</div>

<div class="container">
  
  <!-- About Me Section -->
  <div class="section">
    <h2>About Me</h2>
    <p style="font-size: 18px; line-height: 1.8;">
      I am seeking a <strong>teaching-focused faculty position</strong> at universities or 
      liberal arts colleges beginning Fall 2026. My research focuses on explainable AI for 
      biomedical knowledge graphs, and I have extensive experience teaching computer science 
      to diverse learners across 300+ students in Nigerian and American educational systems.
    </p>
    
    <div class="quick-links">
      <a href="/teaching" class="quick-link">📚 Teaching Experience</a>
      <a href="/research" class="quick-link">🔬 Research & Publications</a>
      <a href="/awards" class="quick-link">🏆 Awards & Recognition</a>
      <a href="/associations" class="quick-link">👥 Professional Service</a>
    </div>
  </div>
  
  <!-- Education Section -->
  <div class="section">
    <h2>Education</h2>
    <div class="card-grid">
      <div class="card">
        <h3>Ph.D. in Computer Science</h3>
        <p><strong>University of North Carolina at Chapel Hill</strong></p>
        <p>Expected: May 2026</p>
        <p style="margin-top: 10px; color: #7F8C8D;">
          <strong>Dissertation:</strong> Knowledge Graph Augmentation with Data Integration 
          and Explainable Edge Inference
        </p>
        <p style="color: #7F8C8D;">
          <strong>Advisors:</strong> Stanley Ahalt & Harlin Lee
        </p>
      </div>
      
      <div class="card">
        <h3>M.Sc. in Computer Science</h3>
        <p><strong>University of North Carolina at Chapel Hill</strong></p>
        <p>May 2023</p>
      </div>
      
      <div class="card">
        <h3>B.Tech in Computer Science</h3>
        <p><strong>Ladoke Akintola University of Technology, Nigeria</strong></p>
        <p>First Class Honors (GPA: 4.52/5.00)</p>
        <p>2017</p>
      </div>
    </div>
  </div>
  
  <!-- Teaching Highlight -->
  <div class="section">
    <h2>Teaching at a Glance</h2>
    <p style="font-size: 18px;"><strong>300+ students taught</strong> across programming, 
    data structures, data science, and machine learning</p>
    
    <div style="margin-top: 20px;">
      <h3 style="color: #357ABD;">Teaching Philosophy</h3>
      <ul style="font-size: 16px; line-height: 1.8;">
        <li><strong>Relevance drives engagement</strong> — Anchoring abstract concepts in real-world applications</li>
        <li><strong>Inclusion requires intentional design</strong> — Creating multiple entry points for diverse learners</li>
        <li><strong>Productive struggle builds confidence</strong> — Scaffolding challenges to support growth</li>
      </ul>
    </div>
    
    <a href="/teaching" class="quick-link" style="margin-top: 20px;">Learn more about my teaching →</a>
  </div>
  
  <!-- Research Highlight -->
  <div class="section">
    <h2>Research Highlights</h2>
    <p style="font-size: 18px;">Focus: Explainable AI for Biomedical Knowledge Graphs</p>
    
    <div class="card-grid">
      <div class="card">
        <h3>ROBOKOP</h3>
        <p>Developing explainable AI methods for biomedical knowledge discovery with the 
        NIH Biomedical Data Translator Consortium</p>
      </div>
      
      <div class="card">
        <h3>RELATE</h3>
        <p>Building NLP tools for automated relation extraction from biomedical literature 
        using large language models</p>
      </div>
      
      <div class="card">
        <h3>EDGAR</h3>
        <p>Explainable Enrichment-Driven Graph Reasoner for drug repurposing in large 
        knowledge graphs</p>
      </div>
    </div>
    
    <a href="/research" class="quick-link" style="margin-top: 20px;">View full research & publications →</a>
  </div>
  
  <!-- Technical Skills -->
  <div class="section">
    <h2>Technical Skills</h2>
    <div style="margin-bottom: 15px;">
      <strong style="color: #357ABD;">Programming Languages:</strong>
      <div class="skills">
        <span class="skill-badge">Python</span>
        <span class="skill-badge">R</span>
        <span class="skill-badge">SQL</span>
        <span class="skill-badge">JavaScript</span>
        <span class="skill-badge">PHP</span>
      </div>
    </div>
    
    <div style="margin-bottom: 15px;">
      <strong style="color: #357ABD;">ML/AI Frameworks:</strong>
      <div class="skills">
        <span class="skill-badge">PyTorch</span>
        <span class="skill-badge">TensorFlow</span>
        <span class="skill-badge">scikit-learn</span>
        <span class="skill-badge">Keras</span>
      </div>
    </div>
    
    <div style="margin-bottom: 15px;">
      <strong style="color: #357ABD;">Data Science:</strong>
      <div class="skills">
        <span class="skill-badge">pandas</span>
        <span class="skill-badge">NumPy</span>
        <span class="skill-badge">NetworkX</span>
        <span class="skill-badge">Neo4j</span>
      </div>
    </div>
  </div>
  
  <!-- Call to Action -->
  <div class="cta-box">
    <h3>Interested in Discussing Opportunities?</h3>
    <p style="font-size: 18px;">I'm happy to discuss teaching opportunities, research 
    collaborations, or computer science education.</p>
    <a href="mailto:roolasunkanmi@unc.edu" class="quick-link" style="margin-top: 15px;">
      📧 Contact Me
    </a>
  </div>
  
</div>

<footer>
  <p>© 2025 Olawumi Olasunkanmi | Last Updated: November 2025</p>
</footer>

</body>
</html>
