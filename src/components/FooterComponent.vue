<template>
  <footer class="footer">
    <div class="footer-container">
      <p>© 2025 Nidhi Singh | Frontend Developer</p>
      <p style="font-size: 12px; margin-top: 5px; opacity: 0.6;">
        B.Tech in Electronics and Computer Science | KIIT Bhubaneswar
      </p>

      <div class="socials">
        <a href="https://github.com/nidhiatwork01-cmyk" target="_blank">🐙 GitHub</a>
        <a href="https://www.linkedin.com/in/nidhi-singh-b0834b288/" target="_blank">🔗 LinkedIn</a>
        <a href="mailto:nidhiatwork.01@gmail.com">📧 Email</a>
        <a href="/NidhiSingh-Resume.pdf" download>📄 Resume</a>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  width: 100%;
  text-align: center;
  padding: 30px 20px;
  margin-top: auto;
  font-size: 14px;
  opacity: 0.8;
  background: rgba(0, 0, 0, 0.2);
}

.footer-container {
  max-width: 1200px;
  margin: 0 auto;
}

.socials {
  display: flex;
  justify-content: center;
  gap: 15px;
  margin-top: 12px;
  flex-wrap: wrap;
}

.socials a {
  text-decoration: none;
  font-weight: 500;
  transition: opacity 0.2s;
}

.socials a:hover {
  opacity: 0.7;
}

@media (min-width: 1400px) {
  .footer-container {
    max-width: 1400px;
  }
}
</style>