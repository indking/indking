<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Nikhil Kawade - Elite Software Architect & Innovation Leader</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=JetBrains+Mono:wght@400;500;600&display=swap');
  
  *, *::before, *::after {
    box-sizing: border-box;
  }
  
  :root {
    --primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    --secondary-gradient: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
    --tech-gradient: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
    --dark-gradient: linear-gradient(135deg, #0c0c0c 0%, #1a1a1a 50%, #2d2d2d 100%);
    --accent-color: #00ff88;
    --text-primary: #ffffff;
    --text-secondary: #b0b0b0;
    --glass-bg: rgba(255, 255, 255, 0.1);
    --glass-border: rgba(255, 255, 255, 0.2);
  }
  
  body {
    margin: 0; 
    padding: 0; 
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    background: var(--dark-gradient);
    color: var(--text-primary);
    overflow-x: hidden;
    min-height: 100vh;
    position: relative;
  }
  
  /* Animated Background */
  .bg-animation {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 0;
    overflow: hidden;
  }
  
  .floating-shapes {
    position: absolute;
    width: 100%;
    height: 100%;
  }
  
  .shape {
    position: absolute;
    background: linear-gradient(45deg, rgba(79, 172, 254, 0.1), rgba(0, 242, 254, 0.1));
    border-radius: 50%;
    animation: float 20s infinite ease-in-out;
  }
  
  .shape:nth-child(1) { width: 80px; height: 80px; top: 20%; left: 10%; animation-delay: 0s; }
  .shape:nth-child(2) { width: 120px; height: 120px; top: 60%; left: 80%; animation-delay: 5s; }
  .shape:nth-child(3) { width: 60px; height: 60px; top: 80%; left: 20%; animation-delay: 10s; }
  .shape:nth-child(4) { width: 100px; height: 100px; top: 30%; left: 70%; animation-delay: 15s; }
  
  @keyframes float {
    0%, 100% { transform: translateY(0px) rotate(0deg); opacity: 0.3; }
    50% { transform: translateY(-20px) rotate(180deg); opacity: 0.8; }
  }
  
  .container {
    max-width: 1200px;
    width: 100%;
    margin: 0 auto;
    padding: 2rem;
    position: relative;
    z-index: 1;
  }
  
  /* Hero Section */
  .hero {
    text-align: center;
    padding: 4rem 0;
    position: relative;
  }
  
  .hero::before {
    content: '';
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 200px;
    height: 200px;
    background: radial-gradient(circle, rgba(0, 255, 136, 0.3) 0%, transparent 70%);
    border-radius: 50%;
    z-index: -1;
  }
  
  .profile-card {
    background: var(--glass-bg);
    backdrop-filter: blur(20px);
    border: 1px solid var(--glass-border);
    border-radius: 24px;
    padding: 3rem;
    margin-bottom: 3rem;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
    position: relative;
    overflow: hidden;
  }
  
  .profile-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--accent-color), transparent);
  }
  
  .avatar-container {
    margin: 0 auto 2rem;
    width: 200px;
    height: 200px;
    perspective: 1000px;
    position: relative;
  }
  
  .avatar-sphere {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    background: linear-gradient(45deg, #4facfe, #00f2fe);
    box-shadow:
      inset 0 0 20px rgba(79, 172, 254, 0.8),
      0 0 40px rgba(0, 242, 254, 0.4),
      0 20px 40px rgba(0, 0, 0, 0.3);
    transform-style: preserve-3d;
    transition: all 0.3s ease;
    position: relative;
    z-index: 1;
    animation: pulse 4s ease-in-out infinite;
  }
  
  @keyframes pulse {
    0%, 100% { box-shadow: inset 0 0 20px rgba(79, 172, 254, 0.8), 0 0 40px rgba(0, 242, 254, 0.4), 0 20px 40px rgba(0, 0, 0, 0.3); }
    50% { box-shadow: inset 0 0 20px rgba(79, 172, 254, 1), 0 0 60px rgba(0, 242, 254, 0.8), 0 20px 40px rgba(0, 0, 0, 0.3); }
  }
  
  .avatar-photo {
    position: absolute;
    top: 10px;
    left: 10px;
    width: 180px;
    height: 180px;
    border-radius: 50%;
    object-fit: cover;
    border: 3px solid rgba(255, 255, 255, 0.3);
    filter: drop-shadow(0 10px 20px rgba(0, 0, 0, 0.5));
    z-index: 2;
  }
  
  .title {
    font-size: 3.5rem;
    font-weight: 900;
    margin-bottom: 1rem;
    background: linear-gradient(135deg, #ffffff, #4facfe, #00f2fe);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-shadow: 0 0 30px rgba(79, 172, 254, 0.5);
    animation: titleGlow 3s ease-in-out infinite alternate;
  }
  
  @keyframes titleGlow {
    from { filter: drop-shadow(0 0 10px rgba(79, 172, 254, 0.5)); }
    to { filter: drop-shadow(0 0 20px rgba(0, 242, 254, 0.8)); }
  }
  
  .subtitle {
    font-size: 1.5rem;
    font-weight: 600;
    color: var(--accent-color);
    margin-bottom: 1rem;
    animation: fadeInUp 1s ease 0.5s both;
  }
  
  .description {
    font-size: 1.1rem;
    color: var(--text-secondary);
    max-width: 600px;
    margin: 0 auto 2rem;
    line-height: 1.6;
    animation: fadeInUp 1s ease 0.7s both;
  }
  
  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  
  /* Stats Section */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    margin: 3rem 0;
  }
  
  .stat-card {
    background: var(--glass-bg);
    backdrop-filter: blur(20px);
    border: 1px solid var(--glass-border);
    border-radius: 16px;
    padding: 2rem;
    text-align: center;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
  }
  
  .stat-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
    transition: left 0.5s ease;
  }
  
  .stat-card:hover::before {
    left: 100%;
  }
  
  .stat-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
    border-color: var(--accent-color);
  }
  
  .stat-number {
    font-size: 2.5rem;
    font-weight: 800;
    color: var(--accent-color);
    margin-bottom: 0.5rem;
    font-family: 'JetBrains Mono', monospace;
  }
  
  .stat-label {
    font-size: 1rem;
    color: var(--text-secondary);
    font-weight: 500;
  }
  
  /* Tech Stack */
  .tech-section {
    margin: 4rem 0;
  }
  
  .section-title {
    font-size: 2.5rem;
    font-weight: 800;
    text-align: center;
    margin-bottom: 3rem;
    background: linear-gradient(135deg, #ffffff, #4facfe);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  
  .tech-categories {
    display: grid;
    gap: 2rem;
  }
  
  .tech-category {
    background: var(--glass-bg);
    backdrop-filter: blur(20px);
    border: 1px solid var(--glass-border);
    border-radius: 16px;
    padding: 2rem;
    transition: all 0.3s ease;
  }
  
  .tech-category:hover {
    transform: translateY(-2px);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
  }
  
  .category-title {
    font-size: 1.3rem;
    font-weight: 700;
    margin-bottom: 1.5rem;
    color: var(--accent-color);
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  
  .tech-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
    gap: 1.5rem;
    justify-items: center;
    align-items: center;
  }
  
  .tech-item {
    position: relative;
    transition: all 0.3s ease;
    cursor: pointer;
  }
  
  .tech-item img {
    width: 60px;
    height: 60px;
    object-fit: contain;
    filter: drop-shadow(0 4px 8px rgba(0, 0, 0, 0.3));
    transition: all 0.3s ease;
    border-radius: 8px;
    background: white;
    padding: 8px;
  }
  
  .tech-item:hover img {
    transform: scale(1.2) rotate(5deg);
    filter: drop-shadow(0 8px 16px rgba(79, 172, 254, 0.6));
  }
  
  .tech-item::after {
    content: attr(data-name);
    position: absolute;
    bottom: -30px;
    left: 50%;
    transform: translateX(-50%);
    background: rgba(0, 0, 0, 0.8);
    color: white;
    padding: 4px 8px;
    border-radius: 4px;
    font-size: 0.8rem;
    white-space: nowrap;
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.3s ease;
  }
  
  .tech-item:hover::after {
    opacity: 1;
  }
  
  /* GitHub Stats */
  .github-stats {
    margin: 4rem 0;
    text-align: center;
  }
  
  .stats-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
  }
  
  .github-stats img {
    max-width: 100%;
    height: auto;
    border-radius: 12px;
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
    transition: all 0.3s ease;
  }
  
  .github-stats img:hover {
    transform: scale(1.02);
    box-shadow: 0 12px 35px rgba(79, 172, 254, 0.3);
  }
  
  /* Contact Section */
  .contact-section {
    margin: 4rem 0;
    text-align: center;
  }
  
  .contact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
  }
  
  .contact-item {
    background: var(--glass-bg);
    backdrop-filter: blur(20px);
    border: 1px solid var(--glass-border);
    border-radius: 12px;
    padding: 1.5rem;
    text-decoration: none;
    color: var(--text-primary);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
  }
  
  .contact-item::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 2px;
    background: var(--tech-gradient);
    transform: scaleX(0);
    transition: transform 0.3s ease;
  }
  
  .contact-item:hover::before {
    transform: scaleX(1);
  }
  
  .contact-item:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
    border-color: var(--accent-color);
  }
  
  .contact-icon {
    font-size: 2rem;
    margin-bottom: 0.5rem;
    color: var(--accent-color);
  }
  
  .contact-label {
    font-weight: 600;
    margin-bottom: 0.25rem;
  }
  
  .contact-value {
    font-size: 0.9rem;
    color: var(--text-secondary);
  }
  
  /* Activity Graph */
  .activity-section {
    margin: 4rem 0;
    text-align: center;
  }
  
  .activity-graph {
    background: var(--glass-bg);
    backdrop-filter: blur(20px);
    border: 1px solid var(--glass-border);
    border-radius: 16px;
    padding: 2rem;
    margin-top: 2rem;
    overflow: hidden;
  }
  
  /* Responsive Design */
  @media (max-width: 768px) {
    .container {
      padding: 1rem;
    }
    
    .title {
      font-size: 2.5rem;
    }
    
    .subtitle {
      font-size: 1.2rem;
    }
    
    .tech-grid {
      grid-template-columns: repeat(auto-fill, minmax(60px, 1fr));
      gap: 1rem;
    }
    
    .tech-item img {
      width: 50px;
      height: 50px;
    }
    
    .stats-grid {
      grid-template-columns: 1fr;
      gap: 1rem;
    }
  }
  
  /* Animations */
  @keyframes slideInLeft {
    from { opacity: 0; transform: translateX(-50px); }
    to { opacity: 1; transform: translateX(0); }
  }
  
  @keyframes slideInRight {
    from { opacity: 0; transform: translateX(50px); }
    to { opacity: 1; transform: translateX(0); }
  }
  
  .slide-in-left {
    animation: slideInLeft 0.8s ease forwards;
  }
  
  .slide-in-right {
    animation: slideInRight 0.8s ease forwards;
  }
  
  /* Scrollbar Styling */
  ::-webkit-scrollbar {
    width: 8px;
  }
  
  ::-webkit-scrollbar-track {
    background: #1a1a1a;
  }
  
  ::-webkit-scrollbar-thumb {
    background: var(--accent-color);
    border-radius: 4px;
  }
  
  ::-webkit-scrollbar-thumb:hover {
    background: #00cc6a;
  }
</style>
</head>
<body>
  <div class="bg-animation">
    <div class="floating-shapes">
      <div class="shape"></div>
      <div class="shape"></div>
      <div class="shape"></div>
      <div class="shape"></div>
    </div>
  </div>

  <div class="container">
    <!-- Hero Section -->
    <section class="hero">
      <div class="profile-card">
        <div class="avatar-container">
          <div class="avatar-sphere" id="avatarSphere">
            <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/4fbec4c9-41fc-450a-8542-64f0e658e75d.png" alt="Nikhil Kawade" class="avatar-photo" />
          </div>
        </div>
        
        <h1 class="title">Nikhil Kawade</h1>
        <p class="subtitle">🚀 Elite Software Architect & Innovation Leader</p>
        <p class="description">
          Transforming complex challenges into elegant solutions through cutting-edge technology and innovative thinking. 
          Passionate about building scalable systems, leading high-performance teams, and driving digital transformation.
        </p>
        
        <div class="contact-grid">
          <a href="https://github.com/indking" class="contact-item" target="_blank">
            <div class="contact-icon">🐙</div>
            <div class="contact-label">GitHub</div>
            <div class="contact-value">@indking</div>
          </a>
          <a href="https://indking.in" class="contact-item" target="_blank">
            <div class="contact-icon">🌐</div>
            <div class="contact-label">Portfolio</div>
            <div class="contact-value">indking.in</div>
          </a>
          <a href="mailto:contact@indking.in" class="contact-item">
            <div class="contact-icon">✉️</div>
            <div class="contact-label">Email</div>
            <div class="contact-value">Let's Connect</div>
          </a>
          <a href="https://linkedin.com/in/indking" class="contact-item" target="_blank">
            <div class="contact-icon">💼</div>
            <div class="contact-label">LinkedIn</div>
            <div class="contact-value">Professional Network</div>
          </a>
        </div>
      </div>
    </section>

    <!-- Stats Section -->
    <section class="stats-section">
      <div class="stats-grid">
        <div class="stat-card slide-in-left">
          <div class="stat-number">8+</div>
          <div class="stat-label">Years of Excellence</div>
        </div>
        <div class="stat-card slide-in-left">
          <div class="stat-number">50+</div>
          <div class="stat-label">Projects Delivered</div>
        </div>
        <div class="stat-card slide-in-right">
          <div class="stat-number">20+</div>
          <div class="stat-label">Technologies Mastered</div>
        </div>
        <div class="stat-card slide-in-right">
          <div class="stat-number">100%</div>
          <div class="stat-label">Client Satisfaction</div>
        </div>
      </div>
    </section>

    <!-- Tech Stack Section -->
    <section class="tech-section">
      <h2 class="section-title">🛠️ Technology Arsenal</h2>
      
      <div class="tech-categories">
        <div class="tech-category">
          <h3 class="category-title">💻 Programming Languages</h3>
          <div class="tech-grid">
            <div class="tech-item" data-name="Java">
              <img src="https://cdn.worldvectorlogo.com/logos/java-4.svg" alt="Java" />
            </div>
            <div class="tech-item" data-name="C#">
              <img src="https://cdn.worldvectorlogo.com/logos/c-sharp-1.svg" alt="C#" />
            </div>
            <div class="tech-item" data-name="Python">
              <img src="https://cdn.worldvectorlogo.com/logos/python-5.svg" alt="Python" />
            </div>
            <div class="tech-item" data-name=".NET">
              <img src="https://cdn.worldvectorlogo.com/logos/dot-net.svg" alt=".NET" />
            </div>
          </div>
        </div>

        <div class="tech-category">
          <h3 class="category-title">🗄️ Databases & Storage</h3>
          <div class="tech-grid">
            <div class="tech-item" data-name="MySQL">
              <img src="https://cdn.worldvectorlogo.com/logos/mysql-6.svg" alt="MySQL" />
            </div>
            <div class="tech-item" data-name="PostgreSQL">
              <img src="https://cdn.worldvectorlogo.com/logos/postgresql.svg" alt="PostgreSQL" />
            </div>
            <div class="tech-item" data-name="SQL Server">
              <img src="https://cdn.worldvectorlogo.com/logos/microsoft-sql-server.svg" alt="SQL Server" />
            </div>
            <div class="tech-item" data-name="Oracle">
              <img src="https://cdn.worldvectorlogo.com/logos/oracle.svg" alt="Oracle" />
            </div>
          </div>
        </div>

        <div class="tech-category">
          <h3 class="category-title">☁️ Cloud & Infrastructure</h3>
          <div class="tech-grid">
            <div class="tech-item" data-name="AWS">
              <img src="https://cdn.worldvectorlogo.com/logos/aws-2.svg" alt="AWS" />
            </div>
            <div class="tech-item" data-name="Docker">
              <img src="https://cdn.worldvectorlogo.com/logos/docker.svg" alt="Docker" />
            </div>
            <div class="tech-item" data-name="Kubernetes">
              <img src="https://cdn.worldvectorlogo.com/logos/kubernetes.svg" alt="Kubernetes" />
            </div>
          </div>
        </div>

        <div class="tech-category">
          <h3 class="category-title">🔧 DevOps & Tools</h3>
          <div class="tech-grid">
            <div class="tech-item" data-name="Git">
              <img src="https://cdn.worldvectorlogo.com/logos/git-icon.svg" alt="Git" />
            </div>
            <div class="tech-item" data-name="Jenkins">
              <img src="https://cdn.worldvectorlogo.com/logos/jenkins.svg" alt="Jenkins" />
            </div>
            <div class="tech-item" data-name="GitHub">
              <img src="https://cdn.worldvectorlogo.com/logos/github-icon-1.svg" alt="GitHub" />
            </div>
            <div class="tech-item" data-name="Azure DevOps">
              <img src="https://cdn.worldvectorlogo.com/logos/azure-devops.svg" alt="Azure DevOps" />
            </div>
          </div>
        </div>

        <div class="tech-category">
          <h3 class="category-title">🤖 AI & Modern Tools</h3>
          <div class="tech-grid">
            <div class="tech-item" data-name="GitHub Copilot">
              <img src="https://cdn.worldvectorlogo.com/logos/copilot.svg" alt="GitHub Copilot" />
            </div>
            <div class="tech-item" data-name="Cursor AI">
              <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/60529d0a-b6fd-4a79-adda-0c4d6ea9779f.png" alt="Cursor AI" />
            </div>
            <div class="tech-item" data-name="Ollama">
              <img src="https://cdn.worldvectorlogo.com/logos/ollama.svg" alt="Ollama" />
            </div>
          </div>
        </div>

        <div class="tech-category">
          <h3 class="category-title">📋 Project Management</h3>
          <div class="tech-grid">
            <div class="tech-item" data-name="Jira">
              <img src="https://cdn.worldvectorlogo.com/logos/jira.svg" alt="Jira" />
            </div>
            <div class="tech-item" data-name="Confluence">
              <img src="https://cdn.worldvectorlogo.com/logos/confluence.svg" alt="Confluence" />
            </div>
            <div class="tech-item" data-name="Trello">
              <img src="https://cdn.worldvectorlogo.com/logos/trello.svg" alt="Trello" />
            </div>
            <div class="tech-item" data-name="Slack">
              <img src="https://cdn.worldvectorlogo.com/logos/slack-icon.svg" alt="Slack" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- GitHub Stats -->
    <section class="github-stats">
      <h2 class="section-title">📊 GitHub Analytics</h2>
      <div class="stats-container">
        <img src="https://github-readme-stats.vercel.app/api?username=indking&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=4facfe&icon_color=00f2fe&text_color=ffffff" alt="GitHub Stats" />
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=indking&theme=tokyonight&hide_border=true&background=0D1117&stroke=4facfe&ring=00f2fe&fire=00ff88&currStreakLabel=ffffff" alt="GitHub Streak" />
      </div>
      <div class="stats-container">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=indking&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=4facfe&text_color=ffffff" alt="Top Languages" />
        <img src="https://github-readme-activity-graph.vercel.app/graph?username=indking&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=4facfe&line=00f2fe&point=00ff88" alt="Activity Graph" />
      </div>
    </section>

    <!-- Activity Section -->
    <section class="activity-section">
      <h2 class="section-title">🎯 Current Focus</h2>
      <div class="activity-graph">
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 2rem; text-align: left;">
          <div>
            <h3 style="color: var(--accent-color); margin-bottom: 1rem;">🔭 Currently Working On</h3>
            <ul style="list-style: none; padding: 0;">
              <li style="margin-bottom: 0.5rem;">🚀 Next-gen microservices architecture</li>
              <li style="margin-bottom: 0.5rem;">🤖 AI-powered development tools</li>
              <li style="margin-bottom: 0.5rem;">☁️ Cloud-native applications</li>
            </ul>
          </div>
          <div>
            <h3 style="color: var(--accent-color); margin-bottom: 1rem;">🌱 Currently Learning</h3>
            <ul style="list-style: none; padding: 0;">
              <li style="margin-bottom: 0.5rem;">🧠 Machine Learning & AI</li>
              <li style="margin-bottom: 0.5rem;">🔗 Blockchain Technology</li>
              <li style="margin-bottom: 0.5rem;">🌐 Web3 Development</li>
            </ul>
          </div>
          <div>
            <h3 style="color: var(--accent-color); margin-bottom: 1rem;">🤝 Looking to Collaborate</h3>
            <ul style="list-style: none; padding: 0;">
              <li style="margin-bottom: 0.5rem;">🔧 Open source projects</li>
              <li style="margin-bottom: 0.5rem;">💡 Innovative startups</li>
              <li style="margin-bottom: 0.5rem;">🎯 Technical leadership roles</li>
            </ul>
          </div>
          <div>
            <h3 style="color: var(--accent-color); margin-bottom: 1rem;">💬 Ask Me About</h3>
            <ul style="list-style: none; padding: 0;">
              <li style="margin-bottom: 0.5rem;">🏗️ System Architecture</li>
              <li style="margin-bottom: 0.5rem;">⚡ Performance Optimization</li>
              <li style="margin-bottom: 0.5rem;">👥 Team Leadership</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Quote Section -->
    <section style="text-align: center; margin: 4rem 0; padding: 3rem; background: var(--glass-bg); backdrop-filter: blur(20px); border: 1px solid var(--glass-border); border-radius: 16px;">
      <blockquote style="font-size: 1.5rem; font-style: italic; color: var(--accent-color); margin: 0; font-weight: 300;">
        "Innovation distinguishes between a leader and a follower."
      </blockquote>
      <cite style="display: block; margin-top: 1rem; color: var(--text-secondary);">- Steve Jobs</cite>
    </section>
  </div>

  <script>
    // Enhanced 3D Avatar Interaction
    const sphere = document.getElementById('avatarSphere');
    if (sphere) {
      const maxRotation = 25;
      
      function onPointerMove(e) {
        const rect = sphere.getBoundingClientRect();
        let clientX, clientY;
        
        if (e.touches) {
          if (e.touches.length === 0) return;
          clientX = e.touches[0].clientX;
          clientY = e.touches[0].clientY;
        } else {
          clientX = e.clientX;
          clientY = e.clientY;
        }
        
        const x = (clientX - rect.left) / rect.width;
        const y = (clientY - rect.top) / rect.height;
        const rotateY = (x - 0.5) * maxRotation * 2;
        const rotateX = -(y - 0.5) * maxRotation * 2;
        
        sphere.style.transform = `rotateX(${rotateX}deg) rotateY(${rotateY}deg) scale(1.05)`;
      }
      
      function resetRotation() {
        sphere.style.transform = 'rotateX(0deg) rotateY(0deg) scale(1)';
      }
      
      sphere.addEventListener('mousemove', onPointerMove);
      sphere.addEventListener('touchmove', onPointerMove, { passive: true });
      sphere.addEventListener('mouseleave', resetRotation);
      sphere.addEventListener('touchend', resetRotation);
      sphere.addEventListener('mouseenter', () => {
        sphere.style.transform = 'rotateX(5deg) rotateY(5deg) scale(1.05)';
      });
    }

    // Intersection Observer for animations
    const observerOptions = {
      threshold: 0.1,
      rootMargin: '0px 0px -50px 0px'
    };

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = '1';
          entry.target.style.transform = 'translateY(0)';
        }
      });
    }, observerOptions);

    // Observe all sections
    document.querySelectorAll('.tech-category, .stat-card, .contact-item').forEach(el => {
      el.style.opacity = '0';
      el.style.transform = 'translateY(30px)';
      el.style.transition = 'all 0.6s ease';
      observer.observe(el);
    });

    // Tech item hover effects
    document.querySelectorAll('.tech-item').forEach(item => {
      item.addEventListener('mouseenter', function() {
        this.style.transform = 'translateY(-10px) scale(1.1)';
      });
      
      item.addEventListener('mouseleave', function() {
        this.style.transform = 'translateY(0) scale(1)';
      });
    });

    // Dynamic typing effect for subtitle
    const subtitle = document.querySelector('.subtitle');
    if (subtitle) {
      const texts = [
        '🚀 Elite Software Architect & Innovation Leader',
        '💡 Full-Stack Developer & System Designer', 
        '🔧 DevOps Engineer & Cloud Specialist',
        '🤖 AI Enthusiast & Technology Evangelist'
      ];
      let currentIndex = 0;
      
      setInterval(() => {
        currentIndex = (currentIndex + 1) % texts.length;
        subtitle.style.opacity = '0';
        setTimeout(() => {
          subtitle.textContent = texts[currentIndex];
          subtitle.style.opacity = '1';
        }, 300);
      }, 4000);
    }

    // Smooth scrolling for internal links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({
            behavior: 'smooth',
            block: 'start'
          });
        }
      });
    });

    // Performance monitoring
    if ('performance' in window) {
      window.addEventListener('load', () => {
        const perfData = performance.getEntriesByType('navigation')[0];
        console.log(`Page load time: ${perfData.loadEventEnd - perfData.loadEventStart}ms`);
      });
    }
  </script>
</body>
</html>

---

## 🎯 Quick Navigation
- [🏠 Home](#) | [📊 Projects](https://github.com/indking?tab=repositories) | [📝 Blog](https://indking.in/blog) | [📧 Contact](mailto:contact@indking.in)

---

<div align="center">

### 🌟 "Code is poetry written in logic" 🌟

[![Profile Views](https://komarev.com/ghpvc/?username=indking&color=4facfe&style=for-the-badge)](https://github.com/indking)
[![GitHub Followers](https://img.shields.io/github/followers/indking?color=4facfe&style=for-the-badge)](https://github.com/indking)
[![GitHub Stars](https://img.shields.io/github/stars/indking?color=00f2fe&style=for-the-badge)](https://github.com/indking)

</div>

---

<div align="center">
  <img src="https://raw.githubusercontent.com/indking/indking/main/assets/footer-wave.svg" width="100%" alt="Footer Wave" />
</div>

**Last Updated:** `2025-01-27` | **Made with** ❤️ **and** ⚡ **by Nikhil Kawade**
