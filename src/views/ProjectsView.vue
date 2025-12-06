<template>
  <div class="page-container">
    <h1 class="text-big">📚 My Projects</h1>
    <p class="text-small" style="margin-top: 10px; max-width: 700px;">
      A collection of my frontend development work showcasing responsive design, state management, and modern UI/UX practices.
    </p>

    <div class="projects-grid">

      <!-- VUE PORTFOLIO PROJECT -->
      <div class="project-card">
        <h3>Personal Portfolio Dashboard (Vue.js)</h3>
        <p class="project-date">Jan 2026 – Present</p>
        <p>Created a responsive and professional personal dashboard using Vue.js and Pinia for state management. Implemented theme toggling, routing pages, resume download feature, and interactive UI components.</p>
        <div class="tags">
          <span class="tag">Vue.js</span>
          <span class="tag">Pinia</span>
          <span class="tag">Vite</span>
          <span class="tag">Vue Router</span>
        </div>

        <div class="btn-group">
          <a href="https://nid-portfolio.netlify.app/" class="btn" target="_blank">Live Demo</a>
          <a href="https://github.com/nidhiatwork01-cmyk/vue-project" class="btn" target="_blank">GitHub</a>
        </div>
      </div>

      <!-- ECOMMERCE PROJECT -->
      <div class="project-card">
        <h3>E-Commerce Web Application</h3>
        <p class="project-date">Dec 2025 – Present</p>
        <p>Developed a fully responsive platform with product listing, filtering, and dynamic UI components. Implemented cart, wishlist, authentication, and state management using Redux with a clean, modern UI.</p>
        <div class="tags">
          <span class="tag">React</span>
          <span class="tag">Redux</span>
          <span class="tag">Tailwind CSS</span>
          <span class="tag">REST APIs</span>
        </div>

        <div class="btn-group">
          <a href="https://messishopss.netlify.app/" class="btn" target="_blank">Live Demo</a>
          <a href="https://github.com/nidhiatwork01-cmyk/ecoapp" class="btn" target="_blank">GitHub</a>
        </div>
      </div>

      <!-- TODO PROJECT -->
      <div class="project-card">
        <h3>To-Do List Application</h3>
        <p class="project-date">Oct 2025 – Nov 2025</p>
        <p>Built an interactive task management app using React functional components. Implemented editing, completion, deletion, and reusable hooks with a minimal and responsive interface ensuring great UX.</p>
        <div class="tags">
          <span class="tag">React</span>
          <span class="tag">Hooks</span>
          <span class="tag">State Management</span>
          <span class="tag">UI/UX</span>
        </div>

        <div class="btn-group">
          <a href="https://smartytodo.netlify.app/" class="btn" target="_blank">Live Demo</a>
          <a href="https://github.com/nidhiatwork01-cmyk/smarter-todo" class="btn" target="_blank">GitHub</a>
        </div>
      </div>

    </div>
  </div>
</template>

<style scoped>
.projects-grid {
  display: grid;
  gap: 20px;
  margin-top: 30px;
  grid-template-columns: 1fr;
}

@media (min-width: 768px) {
  .projects-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1024px) {
  .projects-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

.project-card {
  background: var(--card-bg);
  padding: 20px;
  border-radius: var(--radius);
  box-shadow: 0 0 8px rgba(0,0,0,0.3);
  transition: transform 0.2s;
}

.project-card:hover {
  transform: translateY(-4px);
}

.project-card h3 {
  margin-bottom: 5px;
  font-size: 18px;
}

.project-date {
  font-size: 12px;
  opacity: 0.6;
  margin-bottom: 10px;
  font-style: italic;
}

.project-card p {
  margin-bottom: 12px;
  line-height: 1.5;
  font-size: 14px;
}

.tags {
  margin: 10px 0;
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.tag {
  background: #48e1ff;
  color: black;
  border-radius: 8px;
  padding: 3px 8px;
  font-size: 12px;
}

.btn-group {
  display: flex;
  gap: 10px;
  margin-top: 12px;
  flex-wrap: wrap;
}

.btn {
  background: #00eaff;
  color: black;
  padding: 7px 12px;
  border-radius: 10px;
  border: none;
  cursor: pointer;
  font-weight: 600;
  text-decoration: none;
  display: inline-block;
}
</style>