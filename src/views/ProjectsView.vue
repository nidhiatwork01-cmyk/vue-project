<template>
  <div style="padding:40px;">
    <h1 class="text-big">📚 My Projects</h1>

    <div class="projects-grid">

      <!-- VUE PORTFOLIO PROJECT -->
      <div class="project-card">
        <h3>Personal Portfolio (Vue.js)</h3>
        <p>A responsive portfolio built with Vue.js, routing, Pinia store, and dark/light themes.</p>
        <div class="tags">
          <span class="tag">Vue.js</span>
          <span class="tag">Pinia</span>
          <span class="tag">Vite</span>
        </div>

        <div class="btn-group">
          <a class="btn" target="_blank">Live Demo</a>
          <a class="btn" target="_blank">GitHub</a>
        </div>
      </div>

      <!-- ECOMMERCE PROJECT -->
      <div class="project-card">
        <h3>E-Commerce Web App</h3>
        <p>A feature-rich shopping UI with cart, wishlist, filtering and responsive UI.</p>
        <div class="tags">
          <span class="tag">React</span>
          <span class="tag">Redux</span>
          <span class="tag">Tailwind</span>
        </div>

        <div class="btn-group">
          <a href="https://messishopss.netlify.app/" class="btn" target="_blank">Live Demo</a>
          <a href="https://github.com/nidhiatwork01-cmyk/ecoapp" class="btn" target="_blank">GitHub</a>
        </div>
      </div>

      <!-- TODO PROJECT -->
      <div class="project-card">
        <h3>To-Do Manager App</h3>
        <p>A smooth task manager with add/delete/edit and responsive design.</p>
        <div class="tags">
          <span class="tag">React</span>
          <span class="tag">Hooks</span>
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

<style>
.projects-grid {
  display: grid;
  gap: 20px;
  margin-top: 30px;
}

.project-card {
  background: var(--card-bg);
  padding: 20px;
  border-radius: var(--radius);
  box-shadow: 0 0 8px rgba(0,0,0,0.3);
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
}
</style>
