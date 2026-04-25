<svg xmlns="http://www.w3.org/2000/svg" width="720" height="1780" viewBox="0 0 720 1780">
<defs>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Silkscreen:wght@400;700&amp;family=Fira+Code:wght@300;400;500;700&amp;display=swap');
  </style>
</defs>
<foreignObject x="0" y="0" width="720" height="1780">
<div xmlns="http://www.w3.org/1999/xhtml">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}

.root{
  background:#000;color:#fff;
  font-family:'Fira Code',monospace;
  width:720px;padding:16px 12px 48px;
  position:relative;overflow:hidden;
}

/* ── SCANLINE OVERLAY ── */
.root::before{
  content:'';position:absolute;inset:0;
  background:repeating-linear-gradient(0deg,transparent 0px,transparent 2px,rgba(255,255,255,0.018) 2px,rgba(255,255,255,0.018) 4px);
  pointer-events:none;z-index:999;
}

/* ── HEADER ── */
.header-shell{
  position:relative;border:2px solid #fff;
  padding:32px 20px 26px;text-align:center;
  overflow:hidden;background:#000;margin-bottom:0;
}
.header-shell::before,.header-shell::after{
  content:'';position:absolute;width:14px;height:14px;background:#fff;
}
.header-shell::before{top:0;left:0}
.header-shell::after{bottom:0;right:0}
.corner-tr{position:absolute;top:0;right:0;width:14px;height:14px;background:#fff}
.corner-bl{position:absolute;bottom:0;left:0;width:14px;height:14px;background:#fff}

.header-scan{
  position:absolute;left:0;right:0;height:4px;
  background:rgba(255,255,255,0.06);
  animation:scanmove 2.8s linear infinite;pointer-events:none;
}
@keyframes scanmove{0%{top:-4px}100%{top:100%}}

.morph-stage{position:relative;height:62px;margin-bottom:8px}
.morph-a,.morph-b{
  position:absolute;inset:0;display:flex;align-items:center;justify-content:center;
  font-family:'Silkscreen',monospace;font-size:28px;font-weight:700;
  letter-spacing:5px;color:#fff;text-transform:uppercase;
}
.morph-a{animation:dissolveOut 8s ease-in-out infinite}
.morph-b{animation:dissolveIn 8s ease-in-out infinite;color:#ddd}

@keyframes dissolveOut{
  0%,30%{opacity:1;clip-path:inset(0 0% 0 0);letter-spacing:5px}
  45%{opacity:0.6;clip-path:inset(0 20% 0 0);letter-spacing:3px}
  55%{opacity:0.2;clip-path:inset(0 60% 0 0);letter-spacing:1px}
  65%,80%{opacity:0;clip-path:inset(0 100% 0 0);letter-spacing:0px}
  90%,100%{opacity:1;clip-path:inset(0 0% 0 0);letter-spacing:5px}
}
@keyframes dissolveIn{
  0%,30%{opacity:0;clip-path:inset(0 0 0 100%);letter-spacing:0px}
  45%{opacity:0.3;clip-path:inset(0 0 0 60%);letter-spacing:2px}
  55%{opacity:0.7;clip-path:inset(0 0 0 20%);letter-spacing:4px}
  65%,80%{opacity:1;clip-path:inset(0 0 0 0%);letter-spacing:5px}
  90%,100%{opacity:0;clip-path:inset(0 0 0 100%);letter-spacing:0px}
}

.noise-overlay{
  position:absolute;inset:0;pointer-events:none;z-index:2;opacity:0;
  animation:noiseFlash 8s ease-in-out infinite;
  background-image:
    radial-gradient(circle 1px at 20% 40%,rgba(255,255,255,0.8) 0%,transparent 100%),
    radial-gradient(circle 1px at 80% 30%,rgba(255,255,255,0.6) 0%,transparent 100%),
    radial-gradient(circle 1px at 50% 70%,rgba(255,255,255,0.7) 0%,transparent 100%),
    radial-gradient(circle 2px at 35% 55%,rgba(255,255,255,0.5) 0%,transparent 100%),
    radial-gradient(circle 1px at 65% 45%,rgba(255,255,255,0.8) 0%,transparent 100%),
    radial-gradient(circle 1px at 15% 60%,rgba(255,255,255,0.6) 0%,transparent 100%),
    radial-gradient(circle 2px at 88% 65%,rgba(255,255,255,0.5) 0%,transparent 100%);
}
@keyframes noiseFlash{0%,28%,68%,100%{opacity:0}40%,60%{opacity:1}}

.header-subtitle{
  font-family:'Fira Code',monospace;font-size:9px;color:#777;
  letter-spacing:3px;animation:subtitlePulse 3s ease-in-out infinite;
  position:relative;z-index:1;
}
@keyframes subtitlePulse{0%,100%{color:#555}50%{color:#999}}

.header-blink-row{display:flex;justify-content:center;gap:6px;margin-top:14px;position:relative;z-index:1}
.hbdot{width:7px;height:7px;background:#fff}
.hbdot:nth-child(1){animation:bdot 1.2s 0s infinite}
.hbdot:nth-child(2){animation:bdot 1.2s 0.3s infinite}
.hbdot:nth-child(3){animation:bdot 1.2s 0.6s infinite}
.hbdot:nth-child(4){animation:bdot 1.2s 0.9s infinite}
@keyframes bdot{0%,100%{opacity:1}50%{opacity:0.1}}

/* ── BREATHING DIVIDER ── */
.breath-div{
  display:flex;align-items:center;justify-content:center;
  gap:2px;margin:10px 0;overflow:hidden;
}
.breath-seg{
  height:2px;background:#fff;flex:1;max-width:10px;
  animation:breathe 2.4s ease-in-out infinite;transform-origin:center;
}
.breath-seg:nth-child(odd){animation-delay:0s}
.breath-seg:nth-child(even){animation-delay:0.4s}
.breath-seg:nth-child(3n){animation-delay:0.8s}
@keyframes breathe{0%,100%{transform:scaleY(1);opacity:0.3}50%{transform:scaleY(4);opacity:1}}
.breath-center{
  font-family:'Silkscreen',monospace;font-size:9px;color:#fff;
  letter-spacing:3px;white-space:nowrap;padding:0 10px;flex-shrink:0;
}

/* ── TERMINAL ── */
.terminal{border:1.5px solid #fff;background:#000;padding:14px 16px;margin:12px 0;position:relative}
.term-top{
  display:flex;align-items:center;gap:6px;
  padding-bottom:9px;border-bottom:1px solid #1e1e1e;margin-bottom:11px;
}
.tdot{width:7px;height:7px;background:#fff;display:inline-block}
.tdot.d2{background:#555}.tdot.d3{background:#2a2a2a}
.term-title{font-size:7px;color:#666;letter-spacing:2px;margin-left:4px;font-family:'Fira Code',monospace}

.tline{
  font-family:'Fira Code',monospace;font-size:9px;margin:6px 0;
  white-space:nowrap;overflow:hidden;width:0;
  animation:typeReveal 0.9s steps(50,end) forwards;color:#d0d0d0;
}
.tl1{animation-delay:0.5s}.tl2{animation-delay:2.1s}.tl3{animation-delay:3.7s}
.tl4{animation-delay:5.3s}.tl5{animation-delay:6.9s}
@keyframes typeReveal{to{width:100%}}

.tprompt{color:#666}.tcmd{color:#fff}.tresult{color:#999}
.tok{color:#fff;font-weight:700}
.tcur{
  display:inline-block;width:7px;height:11px;background:#fff;
  vertical-align:bottom;animation:cur 0.85s step-end infinite;
}
@keyframes cur{50%{opacity:0}}

/* ── SECTION HEAD ── */
.section-head{text-align:center;margin:20px 0 10px}
.section-head h2{
  font-family:'Silkscreen',monospace;font-size:11px;letter-spacing:3px;color:#fff;
  display:inline-block;border:2px solid #fff;padding:6px 16px;background:#000;position:relative;
}
.section-head h2::before,.section-head h2::after{
  content:'';position:absolute;width:6px;height:6px;background:#000;border:2px solid #fff;
}
.section-head h2::before{top:-5px;left:-5px}
.section-head h2::after{bottom:-5px;right:-5px}
.section-head .stag{font-size:7px;color:#555;letter-spacing:2px;margin-top:5px;font-family:'Fira Code',monospace}

/* ── ARMORY ── */
.armory-label{
  font-family:'Fira Code',monospace;font-size:7px;color:#888;
  letter-spacing:2px;border-left:3px solid #fff;padding-left:8px;margin:12px 0 8px;
}
.pixel-grid{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:14px}
.px-badge{
  font-family:'Fira Code',monospace;font-size:7px;letter-spacing:1px;
  padding:6px 10px;border:1.5px solid #fff;color:#fff;background:#000;
  text-transform:uppercase;white-space:nowrap;
  animation:randomGlow 6s ease-in-out infinite;
}
.px-badge:nth-child(1){animation-delay:0.0s}.px-badge:nth-child(2){animation-delay:0.7s}
.px-badge:nth-child(3){animation-delay:1.4s}.px-badge:nth-child(4){animation-delay:2.1s}
.px-badge:nth-child(5){animation-delay:2.8s}.px-badge:nth-child(6){animation-delay:3.5s}
.px-badge:nth-child(7){animation-delay:0.4s}.px-badge:nth-child(8){animation-delay:1.1s}
.px-badge:nth-child(9){animation-delay:1.8s}
@keyframes randomGlow{
  0%,70%,100%{box-shadow:none;border-color:#fff;color:#fff}
  80%,90%{box-shadow:0 0 0 1px #fff,inset 0 0 6px rgba(255,255,255,0.15);background:rgba(255,255,255,0.07)}
}

/* ── SKILL BARS ── */
.skill-row{display:flex;align-items:center;gap:8px;margin:5px 0}
.sk-name{font-family:'Fira Code',monospace;font-size:7px;color:#999;width:90px;flex-shrink:0;letter-spacing:1px}
.sk-bar{display:flex;gap:2px;flex:1}
.sk{width:12px;height:10px;background:#fff}
.sk.o{background:#1e1e1e}

/* ── HUD STATS ── */
.stats-hud{display:flex;gap:6px;justify-content:center;flex-wrap:wrap;margin:14px 0}
.hud-card{
  border:1.5px solid #fff;background:#000;padding:12px 14px;
  flex:1;min-width:130px;text-align:center;position:relative;overflow:hidden;
}
.hud-card::before{
  content:'';position:absolute;inset:0;
  background:repeating-linear-gradient(0deg,transparent 0px,transparent 3px,rgba(255,255,255,0.04) 3px,rgba(255,255,255,0.04) 4px);
  animation:hudFlicker 4s linear infinite;pointer-events:none;z-index:1;
}
@keyframes hudFlicker{0%,96%,100%{opacity:1}97%{opacity:0.4}98%{opacity:0.9}99%{opacity:0.3}}
.hud-num{
  font-family:'Silkscreen',monospace;font-size:22px;color:#fff;
  display:block;margin-bottom:4px;position:relative;z-index:2;
  animation:numPulse 3s ease-in-out infinite;
}
@keyframes numPulse{0%,100%{opacity:1}50%{opacity:0.7}}
.hud-lbl{font-family:'Fira Code',monospace;font-size:6px;color:#888;letter-spacing:2px;position:relative;z-index:2}
.hud-bar{display:flex;gap:2px;margin-top:8px;position:relative;z-index:2}
.hb{height:4px;flex:1;background:#fff}
.hb.off{background:#1e1e1e}

/* ── CONTRIBUTION GRID — PURE CSS ── */
.act-grid{
  display:grid;
  grid-template-columns:repeat(52,1fr);
  gap:2px;margin:10px 0;
}
.ac{
  aspect-ratio:1;background:#111;
  animation:acPulse 5s ease-in-out infinite;
}
.ac.l1{background:#2a2a2a}
.ac.l2{background:#444}
.ac.l3{background:#888}
.ac.l4{background:#fff}

/* Staggered delays — golden-ratio offsets baked per child */
.ac:nth-child(1) { animation-delay: -1.62s; }
.ac:nth-child(2) { animation-delay: -3.24s; }
.ac:nth-child(3) { animation-delay: -4.85s; }
.ac:nth-child(4) { animation-delay: -6.47s; }
.ac:nth-child(5) { animation-delay: -0.09s; }
.ac:nth-child(6) { animation-delay: -1.71s; }
.ac:nth-child(7) { animation-delay: -3.33s; }
.ac:nth-child(8) { animation-delay: -4.94s; }
.ac:nth-child(9) { animation-delay: -6.56s; }
.ac:nth-child(10) { animation-delay: -0.18s; }
.ac:nth-child(11) { animation-delay: -1.8s; }
.ac:nth-child(12) { animation-delay: -3.42s; }
.ac:nth-child(13) { animation-delay: -5.03s; }
.ac:nth-child(14) { animation-delay: -6.65s; }
.ac:nth-child(15) { animation-delay: -0.27s; }
.ac:nth-child(16) { animation-delay: -1.89s; }
.ac:nth-child(17) { animation-delay: -3.51s; }
.ac:nth-child(18) { animation-delay: -5.12s; }
.ac:nth-child(19) { animation-delay: -6.74s; }
.ac:nth-child(20) { animation-delay: -0.36s; }
.ac:nth-child(21) { animation-delay: -1.98s; }
.ac:nth-child(22) { animation-delay: -3.6s; }
.ac:nth-child(23) { animation-delay: -5.21s; }
.ac:nth-child(24) { animation-delay: -6.83s; }
.ac:nth-child(25) { animation-delay: -0.45s; }
.ac:nth-child(26) { animation-delay: -2.07s; }
.ac:nth-child(27) { animation-delay: -3.69s; }
.ac:nth-child(28) { animation-delay: -5.3s; }
.ac:nth-child(29) { animation-delay: -6.92s; }
.ac:nth-child(30) { animation-delay: -0.54s; }
.ac:nth-child(31) { animation-delay: -2.16s; }
.ac:nth-child(32) { animation-delay: -3.78s; }
.ac:nth-child(33) { animation-delay: -5.4s; }
.ac:nth-child(34) { animation-delay: -7.01s; }
.ac:nth-child(35) { animation-delay: -0.63s; }
.ac:nth-child(36) { animation-delay: -2.25s; }
.ac:nth-child(37) { animation-delay: -3.87s; }
.ac:nth-child(38) { animation-delay: -5.49s; }
.ac:nth-child(39) { animation-delay: -7.1s; }
.ac:nth-child(40) { animation-delay: -0.72s; }
.ac:nth-child(41) { animation-delay: -2.34s; }
.ac:nth-child(42) { animation-delay: -3.96s; }
.ac:nth-child(43) { animation-delay: -5.58s; }
.ac:nth-child(44) { animation-delay: -7.19s; }
.ac:nth-child(45) { animation-delay: -0.81s; }
.ac:nth-child(46) { animation-delay: -2.43s; }
.ac:nth-child(47) { animation-delay: -4.05s; }
.ac:nth-child(48) { animation-delay: -5.67s; }
.ac:nth-child(49) { animation-delay: -7.28s; }
.ac:nth-child(50) { animation-delay: -0.9s; }
.ac:nth-child(51) { animation-delay: -2.52s; }
.ac:nth-child(52) { animation-delay: -4.14s; }
.ac:nth-child(53) { animation-delay: -5.76s; }
.ac:nth-child(54) { animation-delay: -7.37s; }
.ac:nth-child(55) { animation-delay: -0.99s; }
.ac:nth-child(56) { animation-delay: -2.61s; }
.ac:nth-child(57) { animation-delay: -4.23s; }
.ac:nth-child(58) { animation-delay: -5.85s; }
.ac:nth-child(59) { animation-delay: -7.46s; }
.ac:nth-child(60) { animation-delay: -1.08s; }
.ac:nth-child(61) { animation-delay: -2.7s; }
.ac:nth-child(62) { animation-delay: -4.32s; }
.ac:nth-child(63) { animation-delay: -5.94s; }
.ac:nth-child(64) { animation-delay: -7.55s; }
.ac:nth-child(65) { animation-delay: -1.17s; }
.ac:nth-child(66) { animation-delay: -2.79s; }
.ac:nth-child(67) { animation-delay: -4.41s; }
.ac:nth-child(68) { animation-delay: -6.03s; }
.ac:nth-child(69) { animation-delay: -7.64s; }
.ac:nth-child(70) { animation-delay: -1.26s; }
.ac:nth-child(71) { animation-delay: -2.88s; }
.ac:nth-child(72) { animation-delay: -4.5s; }
.ac:nth-child(73) { animation-delay: -6.12s; }
.ac:nth-child(74) { animation-delay: -7.73s; }
.ac:nth-child(75) { animation-delay: -1.35s; }
.ac:nth-child(76) { animation-delay: -2.97s; }
.ac:nth-child(77) { animation-delay: -4.59s; }
.ac:nth-child(78) { animation-delay: -6.21s; }
.ac:nth-child(79) { animation-delay: -7.82s; }
.ac:nth-child(80) { animation-delay: -1.44s; }
.ac:nth-child(81) { animation-delay: -3.06s; }
.ac:nth-child(82) { animation-delay: -4.68s; }
.ac:nth-child(83) { animation-delay: -6.3s; }
.ac:nth-child(84) { animation-delay: -7.91s; }
.ac:nth-child(85) { animation-delay: -1.53s; }
.ac:nth-child(86) { animation-delay: -3.15s; }
.ac:nth-child(87) { animation-delay: -4.77s; }
.ac:nth-child(88) { animation-delay: -6.39s; }
.ac:nth-child(89) { animation-delay: -0.0s; }
.ac:nth-child(90) { animation-delay: -1.62s; }
.ac:nth-child(91) { animation-delay: -3.24s; }
.ac:nth-child(92) { animation-delay: -4.86s; }
.ac:nth-child(93) { animation-delay: -6.48s; }
.ac:nth-child(94) { animation-delay: -0.1s; }
.ac:nth-child(95) { animation-delay: -1.71s; }
.ac:nth-child(96) { animation-delay: -3.33s; }
.ac:nth-child(97) { animation-delay: -4.95s; }
.ac:nth-child(98) { animation-delay: -6.57s; }
.ac:nth-child(99) { animation-delay: -0.19s; }
.ac:nth-child(100) { animation-delay: -1.8s; }
.ac:nth-child(101) { animation-delay: -3.42s; }
.ac:nth-child(102) { animation-delay: -5.04s; }
.ac:nth-child(103) { animation-delay: -6.66s; }
.ac:nth-child(104) { animation-delay: -0.28s; }
.ac:nth-child(105) { animation-delay: -1.89s; }
.ac:nth-child(106) { animation-delay: -3.51s; }
.ac:nth-child(107) { animation-delay: -5.13s; }
.ac:nth-child(108) { animation-delay: -6.75s; }
.ac:nth-child(109) { animation-delay: -0.37s; }
.ac:nth-child(110) { animation-delay: -1.98s; }
.ac:nth-child(111) { animation-delay: -3.6s; }
.ac:nth-child(112) { animation-delay: -5.22s; }
.ac:nth-child(113) { animation-delay: -6.84s; }
.ac:nth-child(114) { animation-delay: -0.46s; }
.ac:nth-child(115) { animation-delay: -2.07s; }
.ac:nth-child(116) { animation-delay: -3.69s; }
.ac:nth-child(117) { animation-delay: -5.31s; }
.ac:nth-child(118) { animation-delay: -6.93s; }
.ac:nth-child(119) { animation-delay: -0.55s; }
.ac:nth-child(120) { animation-delay: -2.16s; }
.ac:nth-child(121) { animation-delay: -3.78s; }
.ac:nth-child(122) { animation-delay: -5.4s; }
.ac:nth-child(123) { animation-delay: -7.02s; }
.ac:nth-child(124) { animation-delay: -0.64s; }
.ac:nth-child(125) { animation-delay: -2.25s; }
.ac:nth-child(126) { animation-delay: -3.87s; }
.ac:nth-child(127) { animation-delay: -5.49s; }
.ac:nth-child(128) { animation-delay: -7.11s; }
.ac:nth-child(129) { animation-delay: -0.73s; }
.ac:nth-child(130) { animation-delay: -2.34s; }
.ac:nth-child(131) { animation-delay: -3.96s; }
.ac:nth-child(132) { animation-delay: -5.58s; }
.ac:nth-child(133) { animation-delay: -7.2s; }
.ac:nth-child(134) { animation-delay: -0.82s; }
.ac:nth-child(135) { animation-delay: -2.43s; }
.ac:nth-child(136) { animation-delay: -4.05s; }
.ac:nth-child(137) { animation-delay: -5.67s; }
.ac:nth-child(138) { animation-delay: -7.29s; }
.ac:nth-child(139) { animation-delay: -0.91s; }
.ac:nth-child(140) { animation-delay: -2.52s; }
.ac:nth-child(141) { animation-delay: -4.14s; }
.ac:nth-child(142) { animation-delay: -5.76s; }
.ac:nth-child(143) { animation-delay: -7.38s; }
.ac:nth-child(144) { animation-delay: -1.0s; }
.ac:nth-child(145) { animation-delay: -2.61s; }
.ac:nth-child(146) { animation-delay: -4.23s; }
.ac:nth-child(147) { animation-delay: -5.85s; }
.ac:nth-child(148) { animation-delay: -7.47s; }
.ac:nth-child(149) { animation-delay: -1.09s; }
.ac:nth-child(150) { animation-delay: -2.7s; }
.ac:nth-child(151) { animation-delay: -4.32s; }
.ac:nth-child(152) { animation-delay: -5.94s; }
.ac:nth-child(153) { animation-delay: -7.56s; }
.ac:nth-child(154) { animation-delay: -1.18s; }
.ac:nth-child(155) { animation-delay: -2.8s; }
.ac:nth-child(156) { animation-delay: -4.41s; }
.ac:nth-child(157) { animation-delay: -6.03s; }
.ac:nth-child(158) { animation-delay: -7.65s; }
.ac:nth-child(159) { animation-delay: -1.27s; }
.ac:nth-child(160) { animation-delay: -2.89s; }
.ac:nth-child(161) { animation-delay: -4.5s; }
.ac:nth-child(162) { animation-delay: -6.12s; }
.ac:nth-child(163) { animation-delay: -7.74s; }
.ac:nth-child(164) { animation-delay: -1.36s; }
.ac:nth-child(165) { animation-delay: -2.98s; }
.ac:nth-child(166) { animation-delay: -4.59s; }
.ac:nth-child(167) { animation-delay: -6.21s; }
.ac:nth-child(168) { animation-delay: -7.83s; }
.ac:nth-child(169) { animation-delay: -1.45s; }
.ac:nth-child(170) { animation-delay: -3.07s; }
.ac:nth-child(171) { animation-delay: -4.68s; }
.ac:nth-child(172) { animation-delay: -6.3s; }
.ac:nth-child(173) { animation-delay: -7.92s; }
.ac:nth-child(174) { animation-delay: -1.54s; }
.ac:nth-child(175) { animation-delay: -3.16s; }
.ac:nth-child(176) { animation-delay: -4.77s; }
.ac:nth-child(177) { animation-delay: -6.39s; }
.ac:nth-child(178) { animation-delay: -0.01s; }
.ac:nth-child(179) { animation-delay: -1.63s; }
.ac:nth-child(180) { animation-delay: -3.25s; }
.ac:nth-child(181) { animation-delay: -4.86s; }
.ac:nth-child(182) { animation-delay: -6.48s; }
.ac:nth-child(183) { animation-delay: -0.1s; }
.ac:nth-child(184) { animation-delay: -1.72s; }
.ac:nth-child(185) { animation-delay: -3.34s; }
.ac:nth-child(186) { animation-delay: -4.95s; }
.ac:nth-child(187) { animation-delay: -6.57s; }
.ac:nth-child(188) { animation-delay: -0.19s; }
.ac:nth-child(189) { animation-delay: -1.81s; }
.ac:nth-child(190) { animation-delay: -3.43s; }
.ac:nth-child(191) { animation-delay: -5.04s; }
.ac:nth-child(192) { animation-delay: -6.66s; }
.ac:nth-child(193) { animation-delay: -0.28s; }
.ac:nth-child(194) { animation-delay: -1.9s; }
.ac:nth-child(195) { animation-delay: -3.52s; }
.ac:nth-child(196) { animation-delay: -5.13s; }
.ac:nth-child(197) { animation-delay: -6.75s; }
.ac:nth-child(198) { animation-delay: -0.37s; }
.ac:nth-child(199) { animation-delay: -1.99s; }
.ac:nth-child(200) { animation-delay: -3.61s; }
.ac:nth-child(201) { animation-delay: -5.22s; }
.ac:nth-child(202) { animation-delay: -6.84s; }
.ac:nth-child(203) { animation-delay: -0.46s; }
.ac:nth-child(204) { animation-delay: -2.08s; }
.ac:nth-child(205) { animation-delay: -3.7s; }
.ac:nth-child(206) { animation-delay: -5.31s; }
.ac:nth-child(207) { animation-delay: -6.93s; }
.ac:nth-child(208) { animation-delay: -0.55s; }
.ac:nth-child(209) { animation-delay: -2.17s; }
.ac:nth-child(210) { animation-delay: -3.79s; }
.ac:nth-child(211) { animation-delay: -5.4s; }
.ac:nth-child(212) { animation-delay: -7.02s; }
.ac:nth-child(213) { animation-delay: -0.64s; }
.ac:nth-child(214) { animation-delay: -2.26s; }
.ac:nth-child(215) { animation-delay: -3.88s; }
.ac:nth-child(216) { animation-delay: -5.5s; }
.ac:nth-child(217) { animation-delay: -7.11s; }
.ac:nth-child(218) { animation-delay: -0.73s; }
.ac:nth-child(219) { animation-delay: -2.35s; }
.ac:nth-child(220) { animation-delay: -3.97s; }
.ac:nth-child(221) { animation-delay: -5.59s; }
.ac:nth-child(222) { animation-delay: -7.2s; }
.ac:nth-child(223) { animation-delay: -0.82s; }
.ac:nth-child(224) { animation-delay: -2.44s; }
.ac:nth-child(225) { animation-delay: -4.06s; }
.ac:nth-child(226) { animation-delay: -5.68s; }
.ac:nth-child(227) { animation-delay: -7.29s; }
.ac:nth-child(228) { animation-delay: -0.91s; }
.ac:nth-child(229) { animation-delay: -2.53s; }
.ac:nth-child(230) { animation-delay: -4.15s; }
.ac:nth-child(231) { animation-delay: -5.77s; }
.ac:nth-child(232) { animation-delay: -7.38s; }
.ac:nth-child(233) { animation-delay: -1.0s; }
.ac:nth-child(234) { animation-delay: -2.62s; }
.ac:nth-child(235) { animation-delay: -4.24s; }
.ac:nth-child(236) { animation-delay: -5.86s; }
.ac:nth-child(237) { animation-delay: -7.47s; }
.ac:nth-child(238) { animation-delay: -1.09s; }
.ac:nth-child(239) { animation-delay: -2.71s; }
.ac:nth-child(240) { animation-delay: -4.33s; }
.ac:nth-child(241) { animation-delay: -5.95s; }
.ac:nth-child(242) { animation-delay: -7.56s; }
.ac:nth-child(243) { animation-delay: -1.18s; }
.ac:nth-child(244) { animation-delay: -2.8s; }
.ac:nth-child(245) { animation-delay: -4.42s; }
.ac:nth-child(246) { animation-delay: -6.04s; }
.ac:nth-child(247) { animation-delay: -7.65s; }
.ac:nth-child(248) { animation-delay: -1.27s; }
.ac:nth-child(249) { animation-delay: -2.89s; }
.ac:nth-child(250) { animation-delay: -4.51s; }
.ac:nth-child(251) { animation-delay: -6.13s; }
.ac:nth-child(252) { animation-delay: -7.74s; }
.ac:nth-child(253) { animation-delay: -1.36s; }
.ac:nth-child(254) { animation-delay: -2.98s; }
.ac:nth-child(255) { animation-delay: -4.6s; }
.ac:nth-child(256) { animation-delay: -6.22s; }
.ac:nth-child(257) { animation-delay: -7.83s; }
.ac:nth-child(258) { animation-delay: -1.45s; }
.ac:nth-child(259) { animation-delay: -3.07s; }
.ac:nth-child(260) { animation-delay: -4.69s; }
.ac:nth-child(261) { animation-delay: -6.31s; }
.ac:nth-child(262) { animation-delay: -7.92s; }
.ac:nth-child(263) { animation-delay: -1.54s; }
.ac:nth-child(264) { animation-delay: -3.16s; }
.ac:nth-child(265) { animation-delay: -4.78s; }
.ac:nth-child(266) { animation-delay: -6.4s; }
.ac:nth-child(267) { animation-delay: -0.01s; }
.ac:nth-child(268) { animation-delay: -1.63s; }
.ac:nth-child(269) { animation-delay: -3.25s; }
.ac:nth-child(270) { animation-delay: -4.87s; }
.ac:nth-child(271) { animation-delay: -6.49s; }
.ac:nth-child(272) { animation-delay: -0.1s; }
.ac:nth-child(273) { animation-delay: -1.72s; }
.ac:nth-child(274) { animation-delay: -3.34s; }
.ac:nth-child(275) { animation-delay: -4.96s; }
.ac:nth-child(276) { animation-delay: -6.58s; }
.ac:nth-child(277) { animation-delay: -0.2s; }
.ac:nth-child(278) { animation-delay: -1.81s; }
.ac:nth-child(279) { animation-delay: -3.43s; }
.ac:nth-child(280) { animation-delay: -5.05s; }
.ac:nth-child(281) { animation-delay: -6.67s; }
.ac:nth-child(282) { animation-delay: -0.29s; }
.ac:nth-child(283) { animation-delay: -1.9s; }
.ac:nth-child(284) { animation-delay: -3.52s; }
.ac:nth-child(285) { animation-delay: -5.14s; }
.ac:nth-child(286) { animation-delay: -6.76s; }
.ac:nth-child(287) { animation-delay: -0.38s; }
.ac:nth-child(288) { animation-delay: -1.99s; }
.ac:nth-child(289) { animation-delay: -3.61s; }
.ac:nth-child(290) { animation-delay: -5.23s; }
.ac:nth-child(291) { animation-delay: -6.85s; }
.ac:nth-child(292) { animation-delay: -0.47s; }
.ac:nth-child(293) { animation-delay: -2.08s; }
.ac:nth-child(294) { animation-delay: -3.7s; }
.ac:nth-child(295) { animation-delay: -5.32s; }
.ac:nth-child(296) { animation-delay: -6.94s; }
.ac:nth-child(297) { animation-delay: -0.56s; }
.ac:nth-child(298) { animation-delay: -2.17s; }
.ac:nth-child(299) { animation-delay: -3.79s; }
.ac:nth-child(300) { animation-delay: -5.41s; }
.ac:nth-child(301) { animation-delay: -7.03s; }
.ac:nth-child(302) { animation-delay: -0.65s; }
.ac:nth-child(303) { animation-delay: -2.26s; }
.ac:nth-child(304) { animation-delay: -3.88s; }
.ac:nth-child(305) { animation-delay: -5.5s; }
.ac:nth-child(306) { animation-delay: -7.12s; }
.ac:nth-child(307) { animation-delay: -0.74s; }
.ac:nth-child(308) { animation-delay: -2.35s; }
.ac:nth-child(309) { animation-delay: -3.97s; }
.ac:nth-child(310) { animation-delay: -5.59s; }
.ac:nth-child(311) { animation-delay: -7.21s; }
.ac:nth-child(312) { animation-delay: -0.83s; }
.ac:nth-child(313) { animation-delay: -2.44s; }
.ac:nth-child(314) { animation-delay: -4.06s; }
.ac:nth-child(315) { animation-delay: -5.68s; }
.ac:nth-child(316) { animation-delay: -7.3s; }
.ac:nth-child(317) { animation-delay: -0.92s; }
.ac:nth-child(318) { animation-delay: -2.53s; }
.ac:nth-child(319) { animation-delay: -4.15s; }
.ac:nth-child(320) { animation-delay: -5.77s; }
.ac:nth-child(321) { animation-delay: -7.39s; }
.ac:nth-child(322) { animation-delay: -1.01s; }
.ac:nth-child(323) { animation-delay: -2.62s; }
.ac:nth-child(324) { animation-delay: -4.24s; }
.ac:nth-child(325) { animation-delay: -5.86s; }
.ac:nth-child(326) { animation-delay: -7.48s; }
.ac:nth-child(327) { animation-delay: -1.1s; }
.ac:nth-child(328) { animation-delay: -2.71s; }
.ac:nth-child(329) { animation-delay: -4.33s; }
.ac:nth-child(330) { animation-delay: -5.95s; }
.ac:nth-child(331) { animation-delay: -7.57s; }
.ac:nth-child(332) { animation-delay: -1.19s; }
.ac:nth-child(333) { animation-delay: -2.8s; }
.ac:nth-child(334) { animation-delay: -4.42s; }
.ac:nth-child(335) { animation-delay: -6.04s; }
.ac:nth-child(336) { animation-delay: -7.66s; }
.ac:nth-child(337) { animation-delay: -1.28s; }
.ac:nth-child(338) { animation-delay: -2.9s; }
.ac:nth-child(339) { animation-delay: -4.51s; }
.ac:nth-child(340) { animation-delay: -6.13s; }
.ac:nth-child(341) { animation-delay: -7.75s; }
.ac:nth-child(342) { animation-delay: -1.37s; }
.ac:nth-child(343) { animation-delay: -2.99s; }
.ac:nth-child(344) { animation-delay: -4.6s; }
.ac:nth-child(345) { animation-delay: -6.22s; }
.ac:nth-child(346) { animation-delay: -7.84s; }
.ac:nth-child(347) { animation-delay: -1.46s; }
.ac:nth-child(348) { animation-delay: -3.08s; }
.ac:nth-child(349) { animation-delay: -4.69s; }
.ac:nth-child(350) { animation-delay: -6.31s; }
.ac:nth-child(351) { animation-delay: -7.93s; }
.ac:nth-child(352) { animation-delay: -1.55s; }
.ac:nth-child(353) { animation-delay: -3.17s; }
.ac:nth-child(354) { animation-delay: -4.78s; }
.ac:nth-child(355) { animation-delay: -6.4s; }
.ac:nth-child(356) { animation-delay: -0.02s; }
.ac:nth-child(357) { animation-delay: -1.64s; }
.ac:nth-child(358) { animation-delay: -3.26s; }
.ac:nth-child(359) { animation-delay: -4.87s; }
.ac:nth-child(360) { animation-delay: -6.49s; }
.ac:nth-child(361) { animation-delay: -0.11s; }
.ac:nth-child(362) { animation-delay: -1.73s; }
.ac:nth-child(363) { animation-delay: -3.35s; }
.ac:nth-child(364) { animation-delay: -4.96s; }

@keyframes acPulse{
  0%,100%{opacity:1}
  50%{opacity:0.45}
}

/* l4 (bright) cells get extra pop */
.ac.l4{animation:acPulse4 3.5s ease-in-out infinite}
@keyframes acPulse4{
  0%,100%{opacity:1;box-shadow:0 0 2px #fff}
  50%{opacity:0.6;box-shadow:none}
}

/* l3 cells — medium shimmer */
.ac.l3{animation:acPulse3 4.2s ease-in-out infinite}
@keyframes acPulse3{0%,100%{opacity:1}50%{opacity:0.5}}

/* ── MISSION PLATE ── */
.mission-plate{
  border:2px solid #fff;background:#000;padding:16px 20px;
  text-align:center;position:relative;margin:16px 0;
  animation:alertBorder 1.2s step-end infinite;overflow:hidden;
}
@keyframes alertBorder{
  0%,49%{border-color:#fff}
  50%,100%{border-color:#888;box-shadow:0 0 0 1px #888}
}
.mission-plate::before{
  content:'! ALERT !';position:absolute;top:4px;left:8px;
  font-family:'Fira Code',monospace;font-size:6px;color:#fff;letter-spacing:2px;
}
.mission-plate::after{
  content:'[ ARMED ]';position:absolute;top:4px;right:8px;
  font-family:'Fira Code',monospace;font-size:6px;color:#fff;letter-spacing:2px;
  animation:alertFlicker 0.8s step-end infinite;
}
@keyframes alertFlicker{0%,60%,100%{opacity:1}30%{opacity:0}}
.mission-link{
  font-family:'Fira Code',monospace;font-size:9px;letter-spacing:2px;
  color:#fff;text-decoration:none;display:inline-block;
  padding:10px 20px;border:1.5px solid #fff;margin-top:6px;background:#000;
}
.mission-link::before{content:'▶ ';color:#888}
.mission-note{font-family:'Fira Code',monospace;font-size:6px;color:#555;letter-spacing:2px;margin-top:8px}
.plate-scanline{
  position:absolute;left:0;right:0;height:2px;
  background:rgba(255,255,255,0.08);
  animation:scanmove 1.8s linear infinite;pointer-events:none;
}

/* ── FOOTER ── */
.footer{text-align:center;margin-top:24px;padding-top:14px;border-top:1px solid #1e1e1e}
.footer-sig{font-family:'Fira Code',monospace;font-size:7px;color:#555;letter-spacing:2px;line-height:2.2}
.footer-sig span{color:#aaa}
.footer-pix{
  font-family:'Silkscreen',monospace;font-size:10px;color:#222;
  letter-spacing:4px;margin-top:10px;
  animation:footerPulse 4s ease-in-out infinite;
}
@keyframes footerPulse{0%,100%{color:#1a1a1a}50%{color:#3a3a3a}}
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
    <div class="header-subtitle">&#x25A0; VFX ARTIST &#xB7; TECHNICAL DEVELOPER &#xB7; SYSTEMS ARCHITECT &#x25A0;</div>
    <div class="header-blink-row">
      <div class="hbdot"></div><div class="hbdot"></div>
      <div class="hbdot"></div><div class="hbdot"></div>
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
      <div class="tdot"></div><div class="tdot d2"></div><div class="tdot d3"></div>
      <span class="term-title">CYBER_KING_OS v9.0 &#xB7; PIPELINE HIJACK SEQUENCE</span>
    </div>
    <div class="tline tl1"><span class="tprompt">&gt; </span><span class="tcmd">HIJACKING_BLENDER_PIPELINE...</span><span class="tresult">  [BREACH: OK]</span></div>
    <div class="tline tl2"><span class="tprompt">&gt; </span><span class="tcmd">TAMING_PIXELS_WITH_MATHEMATICS...</span><span class="tresult"> [SOLVED]</span></div>
    <div class="tline tl3"><span class="tprompt">&gt; </span><span class="tcmd">REWRITING_VFX_REALITY...</span><span class="tresult">         [OVERWRITE: DONE]</span></div>
    <div class="tline tl4"><span class="tprompt">&gt; </span><span class="tcmd">LOADING_PIXEL_TAMER_IDENTITY...</span><span class="tresult"> [CONFIRMED]</span></div>
    <div class="tline tl5"><span class="tprompt">&gt; </span><span class="tok">ALL SYSTEMS NOMINAL &#xB7; STANDING BY</span><span class="tcur"></span></div>
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
    <div class="stag">// ACTIVE TECH STACK &#xB7; RANDOM GLOW ENABLED //</div>
  </div>

  <div class="armory-label">VFX / 3D MASTERY</div>
  <div class="pixel-grid">
    <div class="px-badge">BLENDER</div><div class="px-badge">HOUDINI</div>
    <div class="px-badge">MAYA</div><div class="px-badge">UNREAL ENGINE</div>
    <div class="px-badge">ZBRUSH</div><div class="px-badge">NUKE 16</div>
    <div class="px-badge">SYNTHEYES</div><div class="px-badge">3DEQUALIZER</div>
    <div class="px-badge">GAEA</div>
  </div>

  <div class="armory-label">SYSTEMS &amp; CODE</div>
  <div class="pixel-grid">
    <div class="px-badge">PYTHON</div><div class="px-badge">C++</div>
    <div class="px-badge">C#</div><div class="px-badge">LINUX</div>
    <div class="px-badge">GIT</div><div class="px-badge">PYCHARM</div>
  </div>

  <div class="armory-label">CREATIVE SUITE</div>
  <div class="pixel-grid">
    <div class="px-badge">AFTER EFFECTS</div><div class="px-badge">PREMIERE</div>
    <div class="px-badge">ABLETON LIVE</div><div class="px-badge">PHOTOSHOP</div>
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

  <!-- ░░ HUD STATS ░░ -->
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
      <span class="hud-num">9+</span><span class="hud-lbl">TOOLS MASTERED</span>
      <div class="hud-bar"><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div></div>
    </div>
    <div class="hud-card">
      <span class="hud-num">3</span><span class="hud-lbl">SKILL DOMAINS</span>
      <div class="hud-bar"><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div></div>
    </div>
    <div class="hud-card">
      <span class="hud-num">&#x221E;</span><span class="hud-lbl">PIPELINE OPS</span>
      <div class="hud-bar"><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div><div class="hb"></div></div>
    </div>
    <div class="hud-card">
      <span class="hud-num">01</span><span class="hud-lbl">ACTIVE EXT</span>
      <div class="hud-bar"><div class="hb"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div><div class="hb off"></div></div>
    </div>
  </div>

  <!-- ░░ CONTRIBUTION GRID — PURE CSS ░░ -->
  <div class="section-head" style="margin-top:18px">
    <h2>CONTRIBUTION GRID</h2>
    <div class="stag">// PIXEL ACTIVITY MAP &#xB7; CSS-ONLY &#xB7; NO SCRIPTS //</div>
  </div>
  <div class="act-grid"><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l2"></div><div class="ac"></div><div class="ac"></div><div class="ac l4"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac l4"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac l3"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l2"></div><div class="ac"></div><div class="ac"></div><div class="ac l4"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac l2"></div><div class="ac l2"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l3"></div><div class="ac"></div><div class="ac"></div><div class="ac l4"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac l4"></div><div class="ac l1"></div><div class="ac l4"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l4"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l3"></div><div class="ac l2"></div><div class="ac"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac"></div><div class="ac"></div><div class="ac l4"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l3"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac l2"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac l4"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l3"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l1"></div><div class="ac l3"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l4"></div><div class="ac l2"></div><div class="ac l4"></div><div class="ac l3"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac l4"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l4"></div><div class="ac l4"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac"></div><div class="ac"></div><div class="ac l4"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l4"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l2"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l4"></div><div class="ac l4"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l3"></div><div class="ac l3"></div><div class="ac"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac l4"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l3"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l3"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l3"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l2"></div><div class="ac l3"></div><div class="ac l3"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l3"></div><div class="ac l1"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l3"></div><div class="ac l4"></div><div class="ac l2"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l2"></div><div class="ac l3"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l2"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l2"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac"></div><div class="ac l3"></div><div class="ac l4"></div><div class="ac"></div><div class="ac l1"></div><div class="ac"></div><div class="ac l4"></div><div class="ac l1"></div><div class="ac l3"></div><div class="ac"></div><div class="ac l4"></div><div class="ac"></div><div class="ac l4"></div><div class="ac"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l2"></div><div class="ac"></div><div class="ac l1"></div><div class="ac l1"></div></div>

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

  <!-- ░░ MISSION PLATE ░░ -->
  <div class="mission-plate">
    <div class="plate-scanline"></div>
    <a class="mission-link" href="https://extensions.blender.org/approval-queue/pixelsync-porter/" target="_blank">
      PIXELSYNC PORTER &#x2014; BLENDER EXTENSION
    </a>
    <div class="mission-note">&#x25A0; BLENDER EXTENSIONS APPROVAL QUEUE &#xB7; OPERATION: ACTIVE &#xB7; CLASSIFIED &#x25A0;</div>
  </div>

  <!-- ░░ FOOTER ░░ -->
  <div class="footer">
    <div class="footer-sig">
      ENGINEERED BY <span>THE PIXEL TAMER</span> &#xB7; A.K.A. <span>CYBER KING</span><br/>
      ALL PIXELS CERTIFIED &#xB7; NO GRADIENTS &#xB7; NO COLORS &#xB7; NO NOISE
    </div>
    <div class="footer-pix">&#x25A0; &#x25A1; &#x25A0; &#x25A1; &#x25A0; &#x25A1; &#x25A0; &#x25A1; &#x25A0; &#x25A1; &#x25A0;</div>
  </div>

</div>
</foreignObject>
</svg>
