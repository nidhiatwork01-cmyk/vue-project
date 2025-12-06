<template>
  <div class="page-container">
    <h1 class="text-big">🧑‍💻 About Me</h1>

    <div class="card" style="margin-top:20px;">
      <h3 style="margin-bottom: 10px;">Summary</h3>
      <p class="text-small">
        Enthusiastic Front-End Developer skilled in HTML, CSS, Tailwind, JavaScript, React, and Redux, with hands-on project experience building responsive and interactive UIs. Currently learning Node.js to transition into full-stack development.
      </p>
    </div>

    <h2 style="margin-top:30px;">🚀 Technical Skills</h2>

    <div class="skills-section">
      <div class="skill-category">
        <h4>Programming Languages</h4>
        <div class="skills-grid">
          <span class="skill">JavaScript</span>
          <span class="skill">TypeScript</span>
          <span class="skill">C</span>
          <span class="skill">Python</span>
          <span class="skill">C++</span>
          <span class="skill">SQL</span>
        </div>
      </div>

      <div class="skill-category">
        <h4>Frontend Development</h4>
        <div class="skills-grid">
          <span class="skill">HTML</span>
          <span class="skill">CSS</span>
          <span class="skill">JavaScript (ES6+)</span>
          <span class="skill">React.js</span>
          <span class="skill">Vue.js</span>
          <span class="skill">Redux</span>
          <span class="skill">Tailwind CSS</span>
          <span class="skill">Responsive UI Design</span>
        </div>
      </div>

      <div class="skill-category">
        <h4>Libraries & Tools</h4>
        <div class="skills-grid">
          <span class="skill">Git & GitHub</span>
          <span class="skill">Axios</span>
          <span class="skill">React Router</span>
          <span class="skill">Vue Router</span>
          <span class="skill">Pinia</span>
          <span class="skill">Postman</span>
          <span class="skill">Vite</span>
        </div>
      </div>
    </div>

    <!-- Education Section -->
    <h2 style="margin-top:30px;">🎓 Education</h2>
    <div class="card" style="margin-top:15px;">
      <h3 style="margin-bottom: 8px;">Kalinga Institute of Industrial Technology</h3>
      <p class="text-small" style="opacity: 0.7;">Bhubaneshwar, Odisha</p>
      <p class="text-small" style="margin-top: 8px;">
        <strong>B.Tech in Electronics and Computer Science</strong><br>
        CGPA: 9.2 | 2023 – 2027
      </p>
    </div>

    <!-- Experience Section -->
    <h2 style="margin-top:30px;">💼 Experience</h2>
    <div class="card" style="margin-top:15px;">
      <h3 style="margin-bottom: 8px;">Frontend Developer – Personal Projects</h3>
      <p class="text-small" style="margin-bottom: 10px;">
        Built React-based applications including an E-commerce platform and a To-Do manager using React, Redux, Tailwind, and REST APIs.
      </p>
      <p class="text-small">
        As an active member of my college's Anchoring Society, I have hosted and led multiple major events, engaging diverse audiences with confidence and clarity. I managed event flow, coordinated with organizing teams, and ensured smooth execution on stage. This experience strengthened my public speaking, leadership, and adaptability.
      </p>
    </div>

    <!-- Contact Section -->
    <h2 style="margin-top:30px;">📞 Contact</h2>
    <div class="card" style="margin-top:15px;">
      <p class="text-small">
        <strong>Email:</strong> <a href="mailto:nidhiatwork.01@gmail.com">nidhiatwork.01@gmail.com</a><br>
        <strong>Phone:</strong> +91 8101414224<br>
        <strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/nidhi-singh-b0834b288/" target="_blank">linkedin.com/in/nidhi-singh-b0834b288</a><br>
        <strong>GitHub:</strong> <a href="https://github.com/nidhiatwork01-cmyk" target="_blank">github.com/nidhiatwork01-cmyk</a>
      </p>
    </div>

    <!-- Resume Section -->
    <h2 style="margin-top:30px;">📄 Resume</h2>
    <a href="/NidhiSingh-Resume.pdf" download>
      <button class="btn">Download Resume (PDF)</button>
    </a>

  </div>
</template>

<style scoped>
.skills-section {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  gap: 25px;
}

.skill-category h4 {
  margin-bottom: 12px;
  font-size: 16px;
  opacity: 0.9;
}

.skills-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.skill {
  background: var(--card-bg);
  padding: 8px 14px;
  border-radius: var(--radius);
  box-shadow: 0 0 6px rgba(0,0,0,0.2);
  font-size: 14px;
}

.card a {
  color: var(--accent);
  text-decoration: none;
}

.card a:hover {
  text-decoration: underline;
}
</style>