<style>
  .typewriter-container {
    font-family: monospace;
    padding: 3rem 2rem;
    text-align: center;
    background: transparent;
  }
  
  .typewriter-title {
    font-size: 28px;
    font-weight: 500;
    letter-spacing: 1px;
    min-height: 40px;
    margin-bottom: 0.5rem;
  }
  
  .typewriter-subtitle {
    font-size: 14px;
    letter-spacing: 0.5px;
    min-height: 24px;
    margin-bottom: 2rem;
    opacity: 0.8;
  }
  
  .cursor {
    display: inline-block;
    width: 2px;
    height: 1.2em;
    background-color: currentColor;
    margin-left: 4px;
    animation: blink 1s infinite;
    vertical-align: text-bottom;
  }
  
  .cursor.done {
    animation: none;
    opacity: 0;
  }
  
  @keyframes blink {
    0%, 49% { opacity: 1; }
    50%, 100% { opacity: 0; }
  }
  
  .divider {
    width: 60px;
    height: 1px;
    background: currentColor;
    margin: 1rem auto;
    opacity: 0.3;
  }
  
  .tech-stack {
    font-size: 12px;
    letter-spacing: 0.5px;
    margin-top: 1.5rem;
    opacity: 0.8;
  }
  
  .projects-section {
    margin-top: 3rem;
    text-align: left;
    display: inline-block;
    opacity: 0;
    animation: fadeInUp 0.8s ease forwards 3.5s;
  }
  
  .projects-section h2 {
    font-size: 18px;
    font-weight: 500;
    margin-bottom: 1rem;
    text-align: center;
  }
  
  .project-item {
    margin: 0.8rem 0;
    padding: 0.8rem 1rem;
    border-left: 2px solid currentColor;
    opacity: 0;
    animation: slideInLeft 0.6s ease forwards;
  }
  
  .project-item:nth-child(1) { animation-delay: 3.8s; }
  .project-item:nth-child(2) { animation-delay: 4.3s; }
  .project-item:nth-child(3) { animation-delay: 4.8s; }
  
  .project-item a {
    color: var(--text-accent, #0066cc);
    text-decoration: none;
    font-weight: 500;
  }
  
  .project-item a:hover {
    text-decoration: underline;
  }
  
  .contact-section {
    margin-top: 2rem;
    padding-top: 1.5rem;
    border-top: 1px solid currentColor;
    border-top-opacity: 0.2;
    opacity: 0;
    animation: fadeIn 0.8s ease forwards 5.3s;
  }
  
  .contact-links {
    font-size: 13px;
    letter-spacing: 0.5px;
    display: flex;
    gap: 1.5rem;
    justify-content: center;
    flex-wrap: wrap;
  }
  
  .contact-links a {
    color: var(--text-primary);
    text-decoration: none;
    padding: 0.5rem 1rem;
    border-radius: 4px;
    transition: all 0.3s ease;
    opacity: 0;
    animation: popIn 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55) forwards;
  }
  
  .contact-links a:nth-child(1) { animation-delay: 5.5s; }
  .contact-links a:nth-child(2) { animation-delay: 5.8s; }
  .contact-links a:nth-child(3) { animation-delay: 6.1s; }
  
  .contact-links a:hover {
    background: var(--bg-accent, rgba(0, 102, 204, 0.1));
    transform: translateY(-2px);
  }
  
  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  @keyframes slideInLeft {
    from {
      opacity: 0;
      transform: translateX(-20px);
    }
    to {
      opacity: 1;
      transform: translateX(0);
    }
  }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }
  
  @keyframes popIn {
    from {
      opacity: 0;
      transform: scale(0.8);
    }
    to {
      opacity: 1;
      transform: scale(1);
    }
  }
</style>

<div class="typewriter-container">
  <div class="typewriter-title" id="title">
    <span id="titleText"></span><span class="cursor" id="cursor1"></span>
  </div>
  
  <div class="typewriter-subtitle" id="subtitle">
    <span id="subtitleText"></span><span class="cursor" id="cursor2"></span>
  </div>
  
  <div class="divider"></div>
  
  <div class="tech-stack">
    Python • TypeScript • React • Node.js • PostgreSQL
  </div>
</div>

<script>
  const titleText = "Nicholas Guillet";
  const subtitleText = "Computer Engineer • Villanova • Backend Developer";
  
  let titleIndex = 0;
  let subtitleIndex = 0;
  
  const titleElement = document.getElementById('titleText');
  const subtitleElement = document.getElementById('subtitleText');
  const cursor1 = document.getElementById('cursor1');
  const cursor2 = document.getElementById('cursor2');
  
  function typeTitle() {
    if (titleIndex < titleText.length) {
      titleElement.textContent += titleText.charAt(titleIndex);
      titleIndex++;
      setTimeout(typeTitle, 60);
    } else {
      cursor1.classList.add('done');
      setTimeout(typeSubtitle, 300);
    }
  }
  
  function typeSubtitle() {
    if (subtitleIndex < subtitleText.length) {
      subtitleElement.textContent += subtitleText.charAt(subtitleIndex);
      subtitleIndex++;
      setTimeout(typeSubtitle, 40);
    } else {
      cursor2.classList.add('done');
    }
  }
  
  typeTitle();
</script>
<!----
<div class="projects-section">
  <h2>Projects</h2>
  <div class="project-item">
    <a href="#">[Project Name]</a> – Brief description of what it does
  </div>
  <div class="project-item">
    <a href="#">[Another Project]</a> – What makes it cool and highlights your skills
  </div>
  <div class="project-item">
    <a href="#">[Third Project]</a> – Additional project showcasing backend expertise
  </div>
</div>
---->
<div class="contact-section">
  <div class="contact-links">
    <a href="mailto:nguillet@villanova.edu">Email</a>
    <a href="https://www.linkedin.com/in/nicholas-guillet/">LinkedIn</a>
    <a href="https://nguillet23.github.io/GuilletPersonalWebsite/">Portfolio</a>
  </div>
</div>
