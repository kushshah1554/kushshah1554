[kush_header_section.html](https://github.com/user-attachments/files/26568856/kush_header_section.html)
[Uploadi
<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=DM+Mono:wght@400;500&display=swap');

  .hdr-root {
    font-family: 'DM Mono', monospace;
    padding: 2.5rem 1rem 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 0;
    position: relative;
    overflow: hidden;
  }

  .hdr-bg-grid {
    position: absolute;
    inset: 0;
    background-image:
      linear-gradient(var(--color-border-tertiary) 1px, transparent 1px),
      linear-gradient(90deg, var(--color-border-tertiary) 1px, transparent 1px);
    background-size: 40px 40px;
    opacity: 0.5;
    pointer-events: none;
  }

  .hdr-bg-glow {
    position: absolute;
    top: -60px;
    left: 50%;
    transform: translateX(-50%);
    width: 400px;
    height: 200px;
    background: radial-gradient(ellipse, rgba(79,142,247,0.1) 0%, transparent 70%);
    pointer-events: none;
  }

  .hdr-badge-row {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 1.25rem;
    position: relative;
    animation: fadeDown 0.5s ease both;
  }

  .hdr-badge {
    font-size: 10px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    padding: 3px 10px;
    border-radius: 20px;
    border: 1px solid rgba(79,142,247,0.35);
    background: rgba(79,142,247,0.08);
    color: #4f8ef7;
    font-family: 'DM Mono', monospace;
  }

  .hdr-dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: #4ade80;
    box-shadow: 0 0 0 3px rgba(74,222,128,0.2);
    animation: pulse 2s infinite;
  }

  .hdr-available {
    font-size: 10px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: #4ade80;
    font-family: 'DM Mono', monospace;
  }

  .hdr-name-wrap {
    position: relative;
    margin-bottom: 0.4rem;
    animation: fadeDown 0.55s 0.05s ease both;
  }

  .hdr-greeting {
    font-family: 'DM Mono', monospace;
    font-size: 13px;
    color: var(--color-text-secondary);
    margin: 0 0 4px;
  }

  .hdr-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(42px, 8vw, 72px);
    font-weight: 800;
    color: var(--color-text-primary);
    line-height: 1;
    letter-spacing: -2px;
    margin: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.15em;
  }

  .hdr-name-k {
    color: #4f8ef7;
    display: inline-block;
    animation: tiltIn 0.6s 0.1s ease both;
  }

  .hdr-name-rest {
    display: inline-block;
    animation: tiltIn 0.6s 0.15s ease both;
  }

  .hdr-wave {
    font-size: 0.7em;
    display: inline-block;
    animation: wave 2.5s ease-in-out infinite;
    transform-origin: 70% 70%;
    margin-left: 8px;
  }

  .hdr-tagline {
    position: relative;
    margin: 1rem 0 0;
    animation: fadeDown 0.6s 0.2s ease both;
  }

  .hdr-tagline-inner {
    font-family: 'DM Mono', monospace;
    font-size: 13px;
    color: var(--color-text-secondary);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    flex-wrap: wrap;
  }

  .hdr-pill {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 5px 12px;
    border-radius: 20px;
    font-size: 12px;
    font-family: 'DM Mono', monospace;
    border: 1px solid var(--color-border-secondary);
    background: var(--color-background-secondary);
    color: var(--color-text-secondary);
    transition: transform 0.15s, border-color 0.15s;
    cursor: default;
  }

  .hdr-pill:hover {
    transform: translateY(-2px);
    border-color: var(--pill-accent);
    color: var(--pill-accent);
  }

  .hdr-sep {
    color: var(--color-border-secondary);
    font-size: 18px;
    font-weight: 300;
    line-height: 1;
  }

  .hdr-gif-wrap {
    position: relative;
    margin-top: 1.75rem;
    animation: fadeUp 0.65s 0.3s ease both;
  }

  .hdr-gif-frame {
    border-radius: 16px;
    overflow: hidden;
    border: 1px solid var(--color-border-tertiary);
    position: relative;
    display: inline-block;
    line-height: 0;
  }

  .hdr-gif-frame::before {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: 16px;
    box-shadow: inset 0 0 0 1px rgba(79,142,247,0.15);
    z-index: 1;
    pointer-events: none;
  }

  .hdr-gif-frame img {
    width: 320px;
    max-width: 100%;
    display: block;
    border-radius: 16px;
  }

  .hdr-corner {
    position: absolute;
    width: 12px;
    height: 12px;
    border-color: #4f8ef7;
    border-style: solid;
    opacity: 0.6;
  }
  .hdr-corner.tl { top: -5px; left: -5px; border-width: 2px 0 0 2px; border-radius: 3px 0 0 0; }
  .hdr-corner.tr { top: -5px; right: -5px; border-width: 2px 2px 0 0; border-radius: 0 3px 0 0; }
  .hdr-corner.bl { bottom: -5px; left: -5px; border-width: 0 0 2px 2px; border-radius: 0 0 0 3px; }
  .hdr-corner.br { bottom: -5px; right: -5px; border-width: 0 2px 2px 0; border-radius: 0 0 3px 0; }

  .hdr-stat-row {
    display: flex;
    gap: 12px;
    margin-top: 1.5rem;
    flex-wrap: wrap;
    justify-content: center;
    animation: fadeUp 0.65s 0.35s ease both;
  }

  .hdr-stat {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 10px 20px;
    border-radius: 10px;
    border: 1px solid var(--color-border-tertiary);
    background: var(--color-background-secondary);
    min-width: 90px;
    transition: transform 0.15s, border-color 0.15s;
    cursor: default;
  }

  .hdr-stat:hover {
    transform: translateY(-2px);
    border-color: rgba(79,142,247,0.3);
  }

  .hdr-stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 20px;
    font-weight: 800;
    color: #4f8ef7;
    line-height: 1.1;
  }

  .hdr-stat-lbl {
    font-size: 10px;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--color-text-tertiary);
    margin-top: 2px;
  }

  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-12px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(12px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes tiltIn {
    from { opacity: 0; transform: skewX(-6deg) translateX(-8px); }
    to   { opacity: 1; transform: skewX(0) translateX(0); }
  }

  @keyframes wave {
    0%, 100% { transform: rotate(0deg); }
    20%       { transform: rotate(18deg); }
    40%       { transform: rotate(-8deg); }
    60%       { transform: rotate(14deg); }
    80%       { transform: rotate(-4deg); }
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50%       { opacity: 0.3; }
  }
</style>

<div class="hdr-root">
  <div class="hdr-bg-grid"></div>
  <div class="hdr-bg-glow"></div>

  <div class="hdr-badge-row">
    <span class="hdr-badge">Full-stack dev</span>
    <span class="hdr-dot"></span>
    <span class="hdr-available">available for work</span>
  </div>

  <div class="hdr-name-wrap">
    <p class="hdr-greeting">// hello, world —</p>
    <h1 class="hdr-name">
      <span>Hi, I'm&nbsp;</span>
      <span class="hdr-name-k">K</span><span class="hdr-name-rest">ush</span>
      <span class="hdr-wave">👋</span>
    </h1>
  </div>

  <div class="hdr-tagline">
    <div class="hdr-tagline-inner">
      <span class="hdr-pill" style="--pill-accent:#4f8ef7;">💻 Building</span>
      <span class="hdr-sep">·</span>
      <span class="hdr-pill" style="--pill-accent:#a78bfa;">📚 Learning</span>
      <span class="hdr-sep">·</span>
      <span class="hdr-pill" style="--pill-accent:#34d399;">🚀 Evolving</span>
    </div>
  </div>

  <div class="hdr-gif-wrap">
    <div class="hdr-corner tl"></div>
    <div class="hdr-corner tr"></div>
    <div class="hdr-corner bl"></div>
    <div class="hdr-corner br"></div>
    <div class="hdr-gif-frame">
      <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" alt="coding gif" />
    </div>
  </div>

  <div class="hdr-stat-row">
    <div class="hdr-stat">
      <span class="hdr-stat-num">3+</span>
      <span class="hdr-stat-lbl">Yrs exp</span>
    </div>
    <div class="hdr-stat">
      <span class="hdr-stat-num">20+</span>
      <span class="hdr-stat-lbl">Projects</span>
    </div>
    <div class="hdr-stat">
      <span class="hdr-stat-num">∞</span>
      <span class="hdr-stat-lbl">Curiosity</span>
    </div>
  </div>
</div>
ng kush_header_section.html…]()

---

## 🌸 About Me
- 🌱 Currently learning *Web Development + DSA*
- 💡 Building projects that actually make sense (slowly but surely)
- 🎯 Goal: Financial independence + strong dev skills 💸
- ⚡ Fun fact: I fix bugs by accident more than intention 🙂

---


<img width="1440" height="1340" alt="image" src="https://github.com/user-attachments/assets/8b32bc82-a767-44d5-9ae3-304bbfce4fe2" />



---



## 🚀 Current Focus
```text
✨ Writing cleaner code every day
🚀 Building real-world projects
🧠 Learning without rushing the process
🔥 Staying consistent (even on low-energy days)
