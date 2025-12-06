<template>
  <div style="padding:40px;">
    <h1 class="text-big">🧑‍💻 About Me</h1>

    <div class="card" style="margin-top:20px;">
      <p class="text-small">
        I am a passionate Frontend Developer focused on building responsive,
        high-performance web applications using Vue.js, React, and modern web
        technologies.
      </p>
    </div>

    <h2 style="margin-top:30px;">🚀 Technical Skills</h2>

    <div class="skills-grid">
      <span class="skill">Vue.js</span>
      <span class="skill">JavaScript</span>
      <span class="skill">React.js</span>
      <span class="skill">Redux</span>
      <span class="skill">Pinia</span>
      <span class="skill">HTML</span>
      <span class="skill">CSS</span>
      <span class="skill">Tailwind CSS</span>
      <span class="skill">Git & GitHub</span>
      <span class="skill">REST APIs</span>
    </div>

    <!-- Resume Section -->
    <h2 style="margin-top:30px;">📄 Resume</h2>
    <a href="/NidhiSingh-Resume.pdf" download>
      <button class="btn">Download Resume</button>
    </a>

  </div>
</template>

<style>
.skills-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 15px;
}

.skill {
  background: var(--card-bg);
  padding: 8px 14px;
  border-radius: var(--radius);
  box-shadow: 0 0 6px rgba(0,0,0,0.2);
  font-size: 14px;
}
</style>
