<div align="center">

<!-- ========================= -->
<!-- FONT IMPORTS -->
<!-- ========================= -->
<link href="https://fonts.googleapis.com/css2?family=Silkscreen&family=Fira+Code&display=swap" rel="stylesheet">

<!-- ========================= -->
<!-- GLOBAL STYLE -->
<!-- ========================= -->
<style>
* {
  background: #000000;
  color: #FFFFFF;
  font-family: 'Fira Code', monospace;
  text-align: center;
}

/* Header glitch morph */
@keyframes morph {
  0% { opacity: 1; filter: blur(0px); }
  40% { opacity: 0; filter: blur(6px); }
  60% { opacity: 0; filter: blur(6px); }
  100% { opacity: 1; filter: blur(0px); }
}

.morphA {
  animation: morph 6s infinite;
  position: absolute;
}

.morphB {
  animation: morph 6s infinite reverse;
  position: absolute;
}

/* Divider breathing */
@keyframes breathe {
  0% { transform: scaleX(0.6); opacity: 0.5; }
  50% { transform: scaleX(1); opacity: 1; }
  100% { transform: scaleX(0.6); opacity: 0.5; }
}

.divider {
  width: 60%;
  height: 2px;
  margin: 40px auto;
  background: #FFFFFF;
  animation: breathe 4s infinite ease-in-out;
}

/* HUD scanlines */
.hud {
  display: inline-block;
  margin: 10px;
  filter: contrast(120%);
  position: relative;
}

.hud::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background: repeating-linear-gradient(
    to bottom,
    rgba(255,255,255,0.08) 0px,
    rgba(255,255,255,0.08) 1px,
    transparent 2px,
    transparent 4px
  );
  pointer-events: none;
}

/* Tech glow */
@keyframes glow {
  0% { opacity: 0.5; }
  50% { opacity: 1; }
  100% { opacity: 0.5; }
}

.tech img {
  animation: glow 3s infinite;
}

/* Alert link */
@keyframes alert {
  0% { border-color: #FFFFFF; }
  50% { border-color: #FF0000; }
  100% { border-color: #FFFFFF; }
}

.alert-box {
  display: inline-block;
  padding: 15px 30px;
  border: 2px solid #FFFFFF;
  animation: alert 1s infinite;
  font-family: monospace;
  letter-spacing: 2px;
}

</style>

<!-- ========================= -->
<!-- HEADER -->
<!-- ========================= -->
<div style="position:relative; height:80px;">
  <h1 class="morphA" style="font-family:Silkscreen;">CYBER KING</h1>
  <h1 class="morphB" style="font-family:Silkscreen;">THE PIXEL TAMER</h1>
</div>

<div class="divider"></div>

<!-- ========================= -->
<!-- TERMINAL -->
<!-- ========================= -->
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=3000&pause=500&color=FFFFFF&center=true&vCenter=true&width=700&lines=HIJACKING_BLENDER_PIPELINE...;TAMING_PIXELS_WITH_MATHEMATICS...;REWRITING_VFX_REALITY..." />

<div class="divider"></div>

<!-- ========================= -->
<!-- HUD STATS -->
<!-- ========================= -->
<div>
  <span class="hud">
    <img src="https://github-readme-stats.vercel.app/api?username=MikeCyber&show_icons=true&theme=transparent&hide_border=true&title_color=FFFFFF&text_color=FFFFFF" height="150"/>
  </span>

  <span class="hud">
    <img src="https://github-readme-streak-stats.herokuapp.com?user=MikeCyber&theme=transparent&hide_border=true&ring=FFFFFF&fire=FFFFFF&currStreakLabel=FFFFFF" height="150"/>
  </span>

  <span class="hud">
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=MikeCyber&layout=compact&theme=transparent&hide_border=true&title_color=FFFFFF&text_color=FFFFFF" height="150"/>
  </span>
</div>

<div class="divider"></div>

<!-- ========================= -->
<!-- TECH GRID -->
<!-- ========================= -->
<div class="tech">
  <img src="https://skillicons.dev/icons?i=blender,js,ts,nodejs,react,threejs,python,cpp&theme=light" />
</div>

<div class="divider"></div>

<!-- ========================= -->
<!-- MISSION LINK -->
<!-- ========================= -->
<a href="https://extensions.blender.org/approval-queue/pixelsync-porter/">
  <div class="alert-box">
    ACCESS: PIXELSYNC PORTER
  </div>
</a>

<div class="divider"></div>

<!-- ========================= -->
<!-- FOOTER -->
<!-- ========================= -->
<p style="font-family:Silkscreen; opacity:0.6;">
SYSTEM STATUS: ACTIVE
</p>

</div>
