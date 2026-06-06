
<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;700;800&display=swap');

* { box-sizing: border-box; margin: 0; padding: 0; }

.gh-root {
  font-family: 'Syne', sans-serif;
  background: #0a0a0f;
  color: #e8e8f0;
  min-height: 100vh;
  padding: 0;
  overflow-x: hidden;
}

.hero {
  position: relative;
  text-align: center;
  padding: 3rem 2rem 2rem;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background: 
    radial-gradient(ellipse 60% 40% at 50% 0%, rgba(147,51,234,0.18) 0%, transparent 70%),
    radial-gradient(ellipse 30% 50% at 80% 50%, rgba(59,130,246,0.10) 0%, transparent 60%);
  pointer-events: none;
}

.scanline {
  position: absolute;
  inset: 0;
  background: repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(255,255,255,0.012) 2px, rgba(255,255,255,0.012) 4px);
  pointer-events: none;
}

.hero-title {
  font-size: clamp(1.4rem, 4vw, 2.2rem);
  font-weight: 800;
  letter-spacing: -0.02em;
  line-height: 1.3;
  position: relative;
  z-index: 1;
  margin-bottom: 0.5rem;
  color: #c084fc;
}

.hero-title .sub {
  display: block;
  font-size: 0.55em;
  font-weight: 400;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: #e8e8f0;
  opacity: 0.6;
  margin-top: 0.4rem;
}

.avatar-wrap {
  position: relative;
  width: 130px;
  height: 130px;
  margin: 1.5rem auto 1rem;
  z-index: 1;
}

.avatar-ring {
  width: 130px; height: 130px;
  border-radius: 50%;
  border: 2px solid rgba(192,132,252,0.5);
  background: linear-gradient(135deg, #1e1e2e, #2a1a3e);
  display: flex; align-items: center; justify-content: center;
  box-shadow: 0 0 0 6px rgba(147,51,234,0.08);
  animation: pulse-ring 3s ease-in-out infinite;
  overflow: hidden;
}

@keyframes pulse-ring {
  0%, 100% { box-shadow: 0 0 0 6px rgba(147,51,234,0.08); }
  50% { box-shadow: 0 0 0 14px rgba(147,51,234,0.04); }
}

.kemz-text {
  font-family: 'Syne', sans-serif;
  font-size: 1.35rem;
  font-weight: 800;
  letter-spacing: 0.14em;
  color: #c084fc;
  text-shadow: 0 0 18px rgba(192,132,252,0.4);
  padding: 0 8px;
}

.username {
  font-family: 'Space Mono', monospace;
  font-size: 0.85rem;
  color: #7c7c9a;
  margin-bottom: 0.25rem;
  position: relative; z-index: 1;
}
.username span { color: #c084fc; }

.tagline {
  font-size: 0.78rem;
  color: #4a4a6a;
  letter-spacing: 0.08em;
  position: relative; z-index: 1;
}

.section { padding: 1.5rem 1.5rem; border-top: 0.5px solid rgba(255,255,255,0.06); }

.section-label {
  font-family: 'Space Mono', monospace;
  font-size: 0.65rem;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: #c084fc;
  margin-bottom: 1rem;
  display: flex; align-items: center; gap: 8px;
}
.section-label::after { content: ''; flex: 1; height: 0.5px; background: rgba(192,132,252,0.2); }

.tech-grid { display: flex; flex-wrap: wrap; gap: 8px; }

.tech-badge {
  display: flex; align-items: center; gap: 5px;
  padding: 5px 10px;
  background: rgba(255,255,255,0.04);
  border: 0.5px solid rgba(255,255,255,0.08);
  border-radius: 6px;
  font-size: 0.72rem; color: #a8a8c8;
  transition: all 0.2s; cursor: default;
  font-family: 'Space Mono', monospace;
}
.tech-badge:hover { background: rgba(192,132,252,0.1); border-color: rgba(192,132,252,0.3); color: #e2c8ff; transform: translateY(-1px); }
.tech-badge img { width: 14px; height: 14px; object-fit: contain; }

.stats-row { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
.stat-card { background: rgba(255,255,255,0.03); border: 0.5px solid rgba(255,255,255,0.07); border-radius: 10px; overflow: hidden; }
.stat-card img { width: 100%; display: block; }

.connect-row { display: flex; gap: 12px; flex-wrap: wrap; align-items: center; }
.connect-btn {
  display: flex; align-items: center; gap: 6px;
  padding: 8px 14px; border-radius: 8px;
  font-size: 0.72rem; font-family: 'Space Mono', monospace;
  text-decoration: none; border: 0.5px solid transparent;
  transition: all 0.2s; font-weight: 700; cursor: pointer; color: inherit; background: none;
}
.connect-btn.linkedin { background: rgba(10,102,194,0.12); border-color: rgba(10,102,194,0.3); color: #60a5fa; }
.connect-btn.linkedin:hover { background: rgba(10,102,194,0.22); }
.connect-btn.email { background: rgba(234,67,53,0.1); border-color: rgba(234,67,53,0.25); color: #f87171; }
.connect-btn.email:hover { background: rgba(234,67,53,0.18); }
.connect-btn.instagram { background: rgba(193,53,132,0.1); border-color: rgba(193,53,132,0.25); color: #f0abfc; }
.connect-btn.instagram:hover { background: rgba(193,53,132,0.18); }
.connect-btn.facebook { background: rgba(24,119,242,0.1); border-color: rgba(24,119,242,0.25); color: #93c5fd; }
.connect-btn.facebook:hover { background: rgba(24,119,242,0.18); }
.connect-btn img { width: 14px; height: 14px; object-fit: contain; }

.hero-img-wrap {
  position: relative; margin: 0 1.5rem 0;
  border-radius: 12px; overflow: hidden;
  border: 0.5px solid rgba(192,132,252,0.15); height: 160px;
}
.hero-img-wrap img { width: 100%; height: 100%; object-fit: cover; object-position: center 30%; filter: brightness(0.7) saturate(1.2); display: block; }
.hero-img-overlay { position: absolute; inset: 0; background: linear-gradient(to top, rgba(10,10,15,0.85) 0%, transparent 60%); }

.footer-line { text-align: center; padding: 1rem; font-family: 'Space Mono', monospace; font-size: 0.6rem; color: #2e2e4a; letter-spacing: 0.15em; }
.blink { animation: blink 1.2s step-end infinite; }
@keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }
</style>

<div class="gh-root">
  <div class="scanline"></div>

  <div class="hero">
    <div class="avatar-wrap">
      <div class="avatar-ring">
        <span class="kemz-text">KEMZ</span>
      </div>
    </div>

    <div class="hero-title">
      Deadlier than the Night,<br>More Elegant than the Dawn
      <span class="sub">Kareem Yasser · Software Engineer</span>
    </div>
    <div class="username" style="margin-top:1rem"><span>@</span>Kareem1099</div>
    <div class="tagline">Full Stack · ML Enthusiast · Cairo, EG</div>
  </div>

  <div class="hero-img-wrap">
    <img src="https://wallpapercave.com/wp/wp12756497.jpg" alt="Cover" onerror="this.style.display='none'">
    <div class="hero-img-overlay"></div>
  </div>

  <div class="section">
    <div class="section-label">Technologies & Tools</div>
    <div class="tech-grid">
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg">Python</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg">JavaScript</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg">Docker</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/fastapi/fastapi-original.svg">FastAPI</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg">MySQL</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flutter/flutter-original.svg">Flutter</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dart/dart-original.svg">Dart</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg">HTML5</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg">CSS3</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg">Java</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg">C++</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/r/r-original.svg">R</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/anaconda/anaconda-original.svg">Anaconda</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg">PHP</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg">VS Code</div>
      <div class="tech-badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pycharm/pycharm-original.svg">PyCharm</div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">GitHub Stats</div>
    <div class="stats-row">
      <div class="stat-card">
        <img src="https://github-readme-stats.vercel.app/api?username=Kareem1099&show_icons=true&theme=dark&bg_color=0a0a0f&title_color=c084fc&icon_color=7c3aed&text_color=a8a8c8&border_color=1e1e2e" alt="GitHub Stats">
      </div>
      <div class="stat-card">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Kareem1099&layout=compact&theme=dark&bg_color=0a0a0f&title_color=c084fc&text_color=a8a8c8&border_color=1e1e2e" alt="Top Languages">
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">Connect</div>
    <div class="connect-row">
      <a class="connect-btn linkedin" href="https://www.linkedin.com/in/kareem-yasser-464ab222a" target="_blank">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg">LinkedIn
      </a>
      <a class="connect-btn email" href="mailto:Kareemyasser1054@gmail.com">✉ Email</a>
      <a class="connect-btn instagram" href="https://www.instagram.com/karemyassser/" target="_blank">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png">Instagram
      </a>
      <a class="connect-btn facebook" href="https://www.facebook.com/kareem.yasser.9862273/" target="_blank">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/facebook/facebook-original.svg">Facebook
      </a>
    </div>
  </div>

  <div class="footer-line">KAREEM1099 · CAIRO, EG · <span class="blink">█</span></div>
</div>
