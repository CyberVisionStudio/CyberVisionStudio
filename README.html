
<style>
@import url('https://fonts.googleapis.com/css2?family=Silkscreen:wght@400;700&family=Fira+Code:wght@300;400;500;700&display=swap');

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

body { background: #000; }

.root {
  background: #000;
  color: #fff;
  font-family: 'Fira Code', monospace;
  max-width: 720px;
  margin: 0 auto;
  padding: 16px 12px 48px;
  position: relative;
  overflow: hidden;
}

/* ── SCANLINE OVERLAY ── */
.root::before {
  content: '';
  position: fixed;
  inset: 0;
  background: repeating-linear-gradient(
    0deg,
    transparent 0px,
    transparent 2px,
    rgba(255,255,255,0.018) 2px,
    rgba(255,255,255,0.018) 4px
  );
  pointer-events: none;
  z-index: 999;
}

/* ── PHANTOM MORPH HEADER ── */
.header-shell {
  position: relative;
  border: 2px solid #fff;
  padding: 32px 20px 26px;
  text-align: center;
  overflow: hidden;
  background: #000;
  margin-bottom: 0;
}

/* corner pixel brackets */
.header-shell::before, .header-shell::after {
  content: '';
  position: absolute;
  width: 14px; height: 14px;
  background: #fff;
}
.header-shell::before { top: 0; left: 0; }
.header-shell::after  { bottom: 0; right: 0; }
.corner-tr { position: absolute; top: 0; right: 0; width: 14px; height: 14px; background: #fff; }
.corner-bl { position: absolute; bottom: 0; left: 0; width: 14px; height: 14px; background: #fff; }

/* moving scanline inside header */
.header-scan {
  position: absolute;
  left: 0; right: 0;
  height: 4px;
  background: rgba(255,255,255,0.06);
  animation: scanmove 2.8s linear infinite;
  pointer-events: none;
}
@keyframes scanmove {
  0%   { top: -4px; }
  100% { top: 100%; }
}

/* MORPH text stack */
.morph-stage {
  position: relative;
  height: 62px;
  margin-bottom: 8px;
}
.morph-a, .morph-b {
  position: absolute;
  inset: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Silkscreen', monospace;
  font-size: 28px;
  font-weight: 700;
  letter-spacing: 5px;
  color: #fff;
  text-transform: uppercase;
}
/* pixel-block dissolve: clip-path steps + staggered opacity blocks */
.morph-a {
  animation: dissolveOut 8s ease-in-out infinite;
}
.morph-b {
  animation: dissolveIn 8s ease-in-out infinite;
  color: #ddd;
}

/* pseudo-pixel noise masks via clip-path polygon steps */
@keyframes dissolveOut {
  0%, 30%   { opacity: 1; clip-path: inset(0 0% 0 0); letter-spacing: 5px; }
  45%       { opacity: 0.6; clip-path: inset(0 20% 0 0); letter-spacing: 3px; }
  55%       { opacity: 0.2; clip-path: inset(0 60% 0 0); letter-spacing: 1px; }
  65%, 80%  { opacity: 0; clip-path: inset(0 100% 0 0); letter-spacing: 0px; }
  90%, 100% { opacity: 1; clip-path: inset(0 0% 0 0); letter-spacing: 5px; }
}
@keyframes dissolveIn {
  0%, 30%   { opacity: 0; clip-path: inset(0 0 0 100%); letter-spacing: 0px; }
  45%       { opacity: 0.3; clip-path: inset(0 0 0 60%); letter-spacing: 2px; }
  55%       { opacity: 0.7; clip-path: inset(0 0 0 20%); letter-spacing: 4px; }
  65%, 80%  { opacity: 1; clip-path: inset(0 0 0 0%); letter-spacing: 5px; }
  90%, 100% { opacity: 0; clip-path: inset(0 0 0 100%); letter-spacing: 0px; }
}

/* glitch noise layer — random pixel flicker over header text */
.noise-overlay {
  position: absolute;
  inset: 0;
  pointer-events: none;
  z-index: 2;
  opacity: 0;
  animation: noiseFlash 8s ease-in-out infinite;
  background-image:
    radial-gradient(circle 1px at 20% 40%, rgba(255,255,255,0.8) 0%, transparent 100%),
    radial-gradient(circle 1px at 80% 30%, rgba(255,255,255,0.6) 0%, transparent 100%),
    radial-gradient(circle 1px at 50% 70%, rgba(255,255,255,0.7) 0%, transparent 100%),
    radial-gradient(circle 2px at 35% 55%, rgba(255,255,255,0.5) 0%, transparent 100%),
    radial-gradient(circle 1px at 65% 45%, rgba(255,255,255,0.8) 0%, transparent 100%),
    radial-gradient(circle 1px at 15% 60%, rgba(255,255,255,0.6) 0%, transparent 100%),
    radial-gradient(circle 2px at 88% 65%, rgba(255,255,255,0.5) 0%, transparent 100%);
}
@keyframes noiseFlash {
  0%, 28%, 68%, 100% { opacity: 0; }
  40%, 60% { opacity: 1; }
}

.header-subtitle {
  font-family: 'Fira Code', monospace;
  font-size: 9px;
  color: #777;
  letter-spacing: 3px;
  animation: subtitlePulse 3s ease-in-out infinite;
  position: relative; z-index: 1;
}
@keyframes subtitlePulse {
  0%, 100% { color: #555; }
  50% { color: #999; }
}

.header-blink-row {
  display: flex;
  justify-content: center;
  gap: 6px;
  margin-top: 14px;
  position: relative; z-index: 1;
}
.hbdot {
  width: 7px; height: 7px;
  background: #fff;
}
.hbdot:nth-child(1) { animation: bdot 1.2s 0s infinite; }
.hbdot:nth-child(2) { animation: bdot 1.2s 0.3s infinite; }
.hbdot:nth-child(3) { animation: bdot 1.2s 0.6s infinite; }
.hbdot:nth-child(4) { animation: bdot 1.2s 0.9s infinite; }
@keyframes bdot { 0%, 100% { opacity: 1; } 50% { opacity: 0.1; } }

/* ── BREATHING DIVIDER ── */
.breath-div {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 2px;
  margin: 10px 0;
  overflow: hidden;
}
.breath-seg {
  height: 2px;
  background: #fff;
  flex: 1;
  max-width: 10px;
  animation: breathe 2.4s ease-in-out infinite;
  transform-origin: center;
}
.breath-seg:nth-child(odd)  { animation-delay: 0s; }
.breath-seg:nth-child(even) { animation-delay: 0.4s; }
.breath-seg:nth-child(3n)   { animation-delay: 0.8s; }
@keyframes breathe {
  0%, 100% { transform: scaleY(1); opacity: 0.3; }
  50% { transform: scaleY(4); opacity: 1; }
}
.breath-center {
  font-family: 'Silkscreen', monospace;
  font-size: 9px;
  color: #fff;
  letter-spacing: 3px;
  white-space: nowrap;
  padding: 0 10px;
  flex-shrink: 0;
}

/* ── TERMINAL ── */
.terminal {
  border: 1.5px solid #fff;
  background: #000;
  padding: 14px 16px;
  margin: 12px 0;
  position: relative;
}
.term-top {
  display: flex;
  align-items: center;
  gap: 6px;
  padding-bottom: 9px;
  border-bottom: 1px solid #1e1e1e;
  margin-bottom: 11px;
}
.tdot { width: 7px; height: 7px; background: #fff; display: inline-block; }
.tdot.d2 { background: #555; }
.tdot.d3 { background: #2a2a2a; }
.term-title { font-size: 7px; color: #666; letter-spacing: 2px; margin-left: 4px; font-family: 'Fira Code', monospace; }

.tline {
  font-family: 'Fira Code', monospace;
  font-size: 9px;
  margin: 6px 0;
  white-space: nowrap;
  overflow: hidden;
  width: 0;
  animation: typeReveal 0.9s steps(50, end) forwards;
  color: #d0d0d0;
}
.tl1 { animation-delay: 0.5s; }
.tl2 { animation-delay: 2.1s; }
.tl3 { animation-delay: 3.7s; }
.tl4 { animation-delay: 5.3s; }
.tl5 { animation-delay: 6.9s; }
@keyframes typeReveal { to { width: 100%; } }

.tprompt { color: #666; }
.tcmd { color: #fff; }
.tresult { color: #999; }
.tok { color: #fff; font-weight: 700; }
.tcur {
  display: inline-block;
  width: 7px; height: 11px;
  background: #fff;
  vertical-align: bottom;
  animation: cur 0.85s step-end infinite;
}
@keyframes cur { 50% { opacity: 0; } }

/* ── SECTION HEAD ── */
.section-head {
  text-align: center;
  margin: 20px 0 10px;
}
.section-head h2 {
  font-family: 'Silkscreen', monospace;
  font-size: 11px;
  letter-spacing: 3px;
  color: #fff;
  display: inline-block;
  border: 2px solid #fff;
  padding: 6px 16px;
  background: #000;
  position: relative;
}
.section-head h2::before, .section-head h2::after {
  content: '';
  position: absolute;
  width: 6px; height: 6px;
  background: #000;
  border: 2px solid #fff;
}
.section-head h2::before { top: -5px; left: -5px; }
.section-head h2::after  { bottom: -5px; right: -5px; }
.section-head .stag {
  font-size: 7px;
  color: #555;
  letter-spacing: 2px;
  margin-top: 5px;
  font-family: 'Fira Code', monospace;
}

/* ── ARMORY GRID ── */
.armory-label {
  font-family: 'Fira Code', monospace;
  font-size: 7px;
  color: #888;
  letter-spacing: 2px;
  border-left: 3px solid #fff;
  padding-left: 8px;
  margin: 12px 0 8px;
}

.pixel-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
  margin-bottom: 14px;
}

.px-badge {
  font-family: 'Fira Code', monospace;
  font-size: 7px;
  letter-spacing: 1px;
  padding: 6px 10px;
  border: 1.5px solid #fff;
  color: #fff;
  background: #000;
  text-transform: uppercase;
  position: relative;
  cursor: default;
  animation: randomGlow 6s ease-in-out infinite;
  white-space: nowrap;
}
/* stagger glow start times per child */
.px-badge:nth-child(1)  { animation-delay: 0.0s; }
.px-badge:nth-child(2)  { animation-delay: 0.7s; }
.px-badge:nth-child(3)  { animation-delay: 1.4s; }
.px-badge:nth-child(4)  { animation-delay: 2.1s; }
.px-badge:nth-child(5)  { animation-delay: 2.8s; }
.px-badge:nth-child(6)  { animation-delay: 3.5s; }
.px-badge:nth-child(7)  { animation-delay: 0.4s; }
.px-badge:nth-child(8)  { animation-delay: 1.1s; }
.px-badge:nth-child(9)  { animation-delay: 1.8s; }
@keyframes randomGlow {
  0%, 70%, 100% {
    box-shadow: none;
    border-color: #fff;
    color: #fff;
  }
  80%, 90% {
    box-shadow: 0 0 0 1px #fff, inset 0 0 6px rgba(255,255,255,0.15);
    border-color: #fff;
    color: #fff;
    background: rgba(255,255,255,0.07);
  }
}
.px-badge:hover {
  background: #fff;
  color: #000;
  transition: all 0.05s;
}

/* ── STATS HUD ── */
.stats-hud {
  display: flex;
  gap: 6px;
  justify-content: center;
  flex-wrap: wrap;
  margin: 14px 0;
}
.hud-card {
  border: 1.5px solid #fff;
  background: #000;
  padding: 12px 14px;
  flex: 1;
  min-width: 130px;
  text-align: center;
  position: relative;
  overflow: hidden;
}
/* scanline flicker mask on HUD cards */
.hud-card::before {
  content: '';
  position: absolute;
  inset: 0;
  background: repeating-linear-gradient(
    0deg,
    transparent 0px,
    transparent 3px,
    rgba(255,255,255,0.04) 3px,
    rgba(255,255,255,0.04) 4px
  );
  animation: hudFlicker 4s linear infinite;
  pointer-events: none;
  z-index: 1;
}
@keyframes hudFlicker {
  0%, 96%, 100% { opacity: 1; }
  97% { opacity: 0.4; }
  98% { opacity: 0.9; }
  99% { opacity: 0.3; }
}
/* HUD card corner accents */
.hud-card::after {
  content: '';
  position: absolute;
  bottom: -4px; right: -4px;
  width: 100%; height: 100%;
  border: 1px solid #2a2a2a;
  z-index: -1;
}
.hud-num {
  font-family: 'Silkscreen', monospace;
  font-size: 22px;
  color: #fff;
  display: block;
  margin-bottom: 4px;
  position: relative; z-index: 2;
  animation: numPulse 3s ease-in-out infinite;
}
@keyframes numPulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.7; }
}
.hud-lbl {
  font-family: 'Fira Code', monospace;
  font-size: 6px;
  color: #888;
  letter-spacing: 2px;
  position: relative; z-index: 2;
}
.hud-bar {
  display: flex;
  gap: 2px;
  margin-top: 8px;
  position: relative; z-index: 2;
}
.hb { height: 4px; flex: 1; background: #fff; }
.hb.off { background: #1e1e1e; }

/* ── SKILL BARS ── */
.skill-row {
  display: flex;
  align-items: center;
  gap: 8px;
  margin: 5px 0;
}
.sk-name {
  font-family: 'Fira Code', monospace;
  font-size: 7px;
  color: #999;
  width: 90px;
  flex-shrink: 0;
  letter-spacing: 1px;
}
.sk-bar {
  display: flex;
  gap: 2px;
  flex: 1;
}
.sk { width: 12px; height: 10px; background: #fff; }
.sk.o { background: #1e1e1e; }

/* ── ACTIVITY GRID ── */
.act-grid {
  display: grid;
  grid-template-columns: repeat(52, 1fr);
  gap: 2px;
  margin: 10px 0;
}
.ac {
  aspect-ratio: 1;
  background: #111;
  animation: acPulse 5s ease-in-out infinite;
}
.ac.l1 { background: #2a2a2a; }
.ac.l2 { background: #555; animation-delay: 0.5s; }
.ac.l3 { background: #999; animation-delay: 1s; }
.ac.l4 { background: #fff; animation-delay: 1.5s; }
@keyframes acPulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.6; }
}

/* ── INDUSTRIAL MONITOR PLATE ── */
.mission-plate {
  border: 2px solid #fff;
  background: #000;
  padding: 16px 20px;
  text-align: center;
  position: relative;
  margin: 16px 0;
  animation: alertBorder 1.2s step-end infinite;
  overflow: hidden;
}
@keyframes alertBorder {
  0%, 49%  { border-color: #fff; }
  50%, 100% { border-color: #888; box-shadow: 0 0 0 1px #888; }
}
.mission-plate::before {
  content: '! ALERT !';
  position: absolute;
  top: 4px; left: 8px;
  font-family: 'Fira Code', monospace;
  font-size: 6px;
  color: #fff;
  letter-spacing: 2px;
  animation: alertBorder 1.2s step-end infinite;
}
.mission-plate::after {
  content: '[ ARMED ]';
  position: absolute;
  top: 4px; right: 8px;
  font-family: 'Fira Code', monospace;
  font-size: 6px;
  color: #fff;
  letter-spacing: 2px;
  animation: alertFlicker 0.8s step-end infinite;
}
@keyframes alertFlicker {
  0%, 60%, 100% { opacity: 1; }
  30% { opacity: 0; }
}
.mission-link {
  font-family: 'Fira Code', monospace;
  font-size: 9px;
  letter-spacing: 2px;
  color: #fff;
  text-decoration: none;
  display: inline-block;
  padding: 10px 20px;
  border: 1.5px solid #fff;
  margin-top: 6px;
  position: relative;
  background: #000;
  transition: all 0.08s;
}
.mission-link::before { content: '▶ '; color: #888; }
.mission-link:hover { background: #fff; color: #000; }
.mission-note {
  font-family: 'Fira Code', monospace;
  font-size: 6px;
  color: #555;
  letter-spacing: 2px;
  margin-top: 8px;
}
.plate-scanline {
  position: absolute;
  left: 0; right: 0;
  height: 2px;
  background: rgba(255,255,255,0.08);
  animation: scanmove 1.8s linear infinite;
  pointer-events: none;
}

/* ── FOOTER ── */
.footer {
  text-align: center;
  margin-top: 24px;
  padding-top: 14px;
  border-top: 1px solid #1e1e1e;
}
.footer-sig {
  font-family: 'Fira Code', monospace;
  font-size: 7px;
  color: #555;
  letter-spacing: 2px;
  line-height: 2.2;
}
.footer-sig span { color: #aaa; }
.footer-pix {
  font-family: 'Silkscreen', monospace;
  font-size: 10px;
  color: #222;
  letter-spacing: 4px;
  margin-top: 10px;
  animation: footerPulse 4s ease-in-out infinite;
}
@keyframes footerPulse {
  0%, 100% { color: #1a1a1a; }
  50% { color: #3a3a3a; }
}
</style>

<div class="root">

  <!-- ░░ PHANTOM MORPH HEADER ░░ -->
  <div class="header-shell">
    <div class="header-scan"></div>
    <div class="corner-tr"></div>
    <div class="corner-bl"></div>
    <div class="noise-overlay"></div>
    <div class="morph-stage">
      <div class="morph-a">CYBER KING</div>
      <div class="morph-b">THE PIXEL TAMER</div>
    </div>
    <div class="header-subtitle">■ VFX ARTIST · TECHNICAL DEVELOPER · SYSTEMS ARCHITECT ■</div>
    <div class="header-blink-row">
      <div class="hbdot"></div>
      <div class="hbdot"></div>
      <div class="hbdot"></div>
      <div class="hbdot"></div>
    </div>
  </div>

  <!-- ░░ BREATHING DIVIDER 1 ░░ -->
  <div class="breath-div">
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-center">// SYSTEM ACTIVE //</div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
  </div>

  <!-- ░░ TERMINAL READOUT ░░ -->
  <div class="terminal">
    <div class="term-top">
      <div class="tdot"></div>
      <div class="tdot d2"></div>
      <div class="tdot d3"></div>
      <span class="term-title">CYBER_KING_OS v9.0 · PIPELINE HIJACK SEQUENCE</span>
    </div>
    <div class="tline tl1"><span class="tprompt">&gt; </span><span class="tcmd">HIJACKING_BLENDER_PIPELINE...</span><span class="tresult">  [BREACH: OK]</span></div>
    <div class="tline tl2"><span class="tprompt">&gt; </span><span class="tcmd">TAMING_PIXELS_WITH_MATHEMATICS...</span><span class="tresult"> [SOLVED]</span></div>
    <div class="tline tl3"><span class="tprompt">&gt; </span><span class="tcmd">REWRITING_VFX_REALITY...</span><span class="tresult">         [OVERWRITE: DONE]</span></div>
    <div class="tline tl4"><span class="tprompt">&gt; </span><span class="tcmd">LOADING_PIXEL_TAMER_IDENTITY...</span><span class="tresult"> [CONFIRMED]</span></div>
    <div class="tline tl5"><span class="tprompt">&gt; </span><span class="tok">ALL SYSTEMS NOMINAL · STANDING BY</span><span class="tcur"></span></div>
  </div>

  <!-- ░░ BREATHING DIVIDER 2 ░░ -->
  <div class="breath-div">
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-center">// ARMORY LOADED //</div>
    <div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div>
  </div>

  <!-- ░░ STEALTH ARMORY ░░ -->
  <div class="section-head">
    <h2>THE STEALTH ARMORY</h2>
    <div class="stag">// ACTIVE TECH STACK · RANDOM GLOW ENABLED //</div>
  </div>

  <div class="armory-label">VFX / 3D MASTERY</div>
  <div class="pixel-grid">
    <div class="px-badge">BLENDER</div>
    <div class="px-badge">HOUDINI</div>
    <div class="px-badge">MAYA</div>
    <div class="px-badge">UNREAL ENGINE</div>
    <div class="px-badge">ZBRUSH</div>
    <div class="px-badge">NUKE 16</div>
    <div class="px-badge">SYNTHEYES</div>
    <div class="px-badge">3DEQUALIZER</div>
    <div class="px-badge">GAEA</div>
  </div>

  <div class="armory-label">SYSTEMS &amp; CODE</div>
  <div class="pixel-grid">
    <div class="px-badge">PYTHON</div>
    <div class="px-badge">C++</div>
    <div class="px-badge">C#</div>
    <div class="px-badge">LINUX</div>
    <div class="px-badge">GIT</div>
    <div class="px-badge">PYCHARM</div>
  </div>

  <div class="armory-label">CREATIVE SUITE</div>
  <div class="pixel-grid">
    <div class="px-badge">AFTER EFFECTS</div>
    <div class="px-badge">PREMIERE</div>
    <div class="px-badge">ABLETON LIVE</div>
    <div class="px-badge">PHOTOSHOP</div>
    <div class="px-badge">FIGMA</div>
  </div>

  <!-- ░░ BREATHING DIVIDER 3 ░░ -->
  <div class="breath-div">
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-center">// SKILL MATRIX //</div>
    <div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div>
  </div>

  <!-- ░░ SKILL BARS ░░ -->
  <div class="skill-row"><span class="sk-name">VFX / 3D</span><div class="sk-bar"><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div></div></div>
  <div class="skill-row"><span class="sk-name">BLENDER</span><div class="sk-bar"><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk o"></div></div></div>
  <div class="skill-row"><span class="sk-name">PYTHON</span><div class="sk-bar"><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div></div></div>
  <div class="skill-row"><span class="sk-name">HOUDINI</span><div class="sk-bar"><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div></div></div>
  <div class="skill-row"><span class="sk-name">C++ / C#</span><div class="sk-bar"><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div><div class="sk o"></div></div></div>

  <!-- ░░ HOLOGRAPHIC HUD STATS ░░ -->
  <div class="breath-div" style="margin-top:18px">
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-center">// HUD STATS //</div>
    <div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div>
  </div>

  <div class="stats-hud">
    <div class="hud-card">
      <span class="hud-num">9+</span>
      <span class="hud-lbl">TOOLS MASTERED</span>
      <div class="hud-bar"><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div></div>
    </div>
    <div class="hud-card">
      <span class="hud-num">3</span>
      <span class="hud-lbl">SKILL DOMAINS</span>
      <div class="hud-bar"><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div></div>
    </div>
    <div class="hud-card">
      <span class="hud-num">∞</span>
      <span class="hud-lbl">PIPELINE OPS</span>
      <div class="hud-bar"><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div></div>
    </div>
    <div class="hud-card">
      <span class="hud-num">01</span>
      <span class="hud-lbl">ACTIVE EXT</span>
      <div class="hud-bar"><div class="hb"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div></div>
    </div>
  </div>

  <!-- ░░ ACTIVITY GRID ░░ -->
  <div class="section-head" style="margin-top:18px">
    <h2>CONTRIBUTION GRID</h2>
    <div class="stag">// PIXEL ACTIVITY MAP //</div>
  </div>
  <div class="act-grid" id="agrid"></div>

  <!-- ░░ BREATHING DIVIDER 4 ░░ -->
  <div class="breath-div">
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-center">// MISSION CRITICAL //</div>
    <div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div><div class="breath-seg"></div>
    <div class="breath-seg"></div><div class="breath-seg"></div>
  </div>

  <!-- ░░ INDUSTRIAL MONITOR PLATE ░░ -->
  <div class="mission-plate">
    <div class="plate-scanline"></div>
    <a class="mission-link" href="https://extensions.blender.org/approval-queue/pixelsync-porter/" target="_blank">
      PIXELSYNC PORTER — BLENDER EXTENSION
    </a>
    <div class="mission-note">■ BLENDER EXTENSIONS APPROVAL QUEUE · OPERATION: ACTIVE · CLASSIFIED ■</div>
  </div>

  <!-- ░░ FOOTER ░░ -->
  <div class="footer">
    <div class="footer-sig">
      ENGINEERED BY <span>THE PIXEL TAMER</span> · A.K.A. <span>CYBER KING</span><br/>
      ALL PIXELS CERTIFIED · NO GRADIENTS · NO COLORS · NO NOISE
    </div>
    <div class="footer-pix">■ □ ■ □ ■ □ ■ □ ■ □ ■</div>
  </div>

</div>

<script>
  const g = document.getElementById('agrid');
  const lvls = ['', 'l1', 'l2', 'l3', 'l4'];
  const w = [0.40, 0.28, 0.17, 0.10, 0.05];
  for (let i = 0; i < 364; i++) {
    const d = document.createElement('div');
    d.className = 'ac';
    let r = Math.random(), acc = 0;
    for (let l = 0; l < w.length; l++) {
      acc += w[l];
      if (r < acc) { if (lvls[l]) d.classList.add(lvls[l]); break; }
    }
    g.appendChild(d);
  }
</script>
