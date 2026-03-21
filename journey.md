---
layout: default
title: My Journey
---

<link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=VT323&display=swap" rel="stylesheet">

<style>
.ce-wrap {
  width: 800px;
  height: 450px;
  max-width: 100%;
  aspect-ratio: 16/9;
  position: relative;
  overflow: hidden;
  background: #000;
  font-family: 'Share Tech Mono', monospace;
  transform-origin: top left;
}

.ce-outer {
  width: 100%;
  max-width: 800px;
  aspect-ratio: 16/9;
  position: relative;
  overflow: hidden;
}

.ce-outer .ce-wrap {
  position: absolute;
  top: 0; left: 0;
  width: 800px; height: 450px;
  transform-origin: top left;
}

.ce-crt {
  position: absolute; inset: 0;
  background: radial-gradient(ellipse at center, rgba(0,255,80,0.03) 0%, rgba(0,0,0,0.4) 100%);
  z-index: 1; pointer-events: none;
}

.ce-scanlines {
  position: absolute; inset: 0; z-index: 2; pointer-events: none;
  background: repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(0,0,0,0.18) 2px, rgba(0,0,0,0.18) 4px);
}

.ce-screen {
  position: relative; z-index: 10;
  height: 100%; padding: 14px 28px;
  display: flex; flex-direction: column;
  gap: 0;
  color-scheme: dark;
}

.ce-bios-header {
  border-bottom: 1px solid rgba(0,255,80,0.2);
  padding-bottom: 4px; margin-bottom: 7px;
  animation: ce-fadeIn 0.3s ease-out both;
}

.ce-bios-right {
  float: right; text-align: right;
  font-size: 10px; color: rgba(0,255,80,0.4);
  line-height: 1.7;
}

.ce-bios-title {
  font-family: 'VT323', monospace;
  font-size: 24px; color: #00ff50;
  letter-spacing: 2px;
  text-shadow: 0 0 10px rgba(0,255,80,0.5);
  line-height: 1;
}

.ce-bios-sub {
  font-size: 11px; color: rgba(0,255,80,0.5);
  margin-top: 3px; letter-spacing: 1px;
}

.ce-boot-lines { flex: 1; display: flex; flex-direction: column; gap: 0; }

.ce-line {
  display: flex; align-items: center;
  opacity: 0;
  font-size: 10.5px;
  color: rgba(0,255,80,0.85);
  line-height: 1.6;
  animation: ce-lineIn 0.1s ease-out forwards;
}

.ce-line.l1 { animation-delay: 0.4s; }
.ce-line.l2 { animation-delay: 1.2s; }
.ce-line.l3 { animation-delay: 2.0s; }
.ce-line.l4 { animation-delay: 2.8s; }
.ce-line.l5 { animation-delay: 3.6s; }
.ce-line.l6 { animation-delay: 4.4s; }
.ce-line.l7 { animation-delay: 5.2s; }
.ce-line.l8 { animation-delay: 6.0s; }

@keyframes ce-lineIn { to { opacity: 1; } }

.ce-label { color: rgba(0,255,80,0.5); min-width: 260px; }
.ce-dots  { color: rgba(0,255,80,0.3); flex: 1; overflow: hidden; white-space: nowrap; }

.ce-ok   { color: #00ff50; font-weight: bold; text-shadow: 0 0 8px rgba(0,255,80,0.7); white-space: nowrap; }
.ce-warn { color: #ffcc00; text-shadow: 0 0 6px rgba(255,200,0,0.5); white-space: nowrap; }
.ce-info { color: #00bfff; text-shadow: 0 0 6px rgba(0,191,255,0.4); white-space: nowrap; }

.ce-bar-wrap {
  display: flex; align-items: center; gap: 6px;
  opacity: 0;
  animation: ce-lineIn 0.1s ease-out forwards;
}

.ce-bar-wrap.b1 { animation-delay: 0.5s; }
.ce-bar-wrap.b2 { animation-delay: 1.3s; }
.ce-bar-wrap.b3 { animation-delay: 2.1s; }
.ce-bar-wrap.b4 { animation-delay: 2.9s; }
.ce-bar-wrap.b5 { animation-delay: 3.7s; }
.ce-bar-wrap.b6 { animation-delay: 4.5s; }
.ce-bar-wrap.b7 { animation-delay: 5.3s; }
.ce-bar-wrap.b8 { animation-delay: 6.1s; }

.ce-bar-label { font-size: 9px; color: rgba(0,255,80,0.45); min-width: 150px; }

.ce-bar-track {
  height: 5px; flex: 1; max-width: 220px;
  background: rgba(0,255,80,0.1);
  border: 1px solid rgba(0,255,80,0.2);
  position: relative; overflow: hidden;
}

.ce-bar-fill {
  position: absolute; top: 0; left: 0; bottom: 0;
  width: 0;
  background: linear-gradient(90deg, rgba(0,255,80,0.4), rgba(0,255,80,0.8));
  box-shadow: 0 0 6px rgba(0,255,80,0.5);
  animation: ce-fillBar 0.8s ease-out forwards;
}

.ce-bar-wrap.b1 .ce-bar-fill { animation-delay: 0.5s; }
.ce-bar-wrap.b2 .ce-bar-fill { animation-delay: 1.3s; }
.ce-bar-wrap.b3 .ce-bar-fill { animation-delay: 2.1s; }
.ce-bar-wrap.b4 .ce-bar-fill { animation-delay: 2.9s; }
.ce-bar-wrap.b5 .ce-bar-fill { animation-delay: 3.7s; }
.ce-bar-wrap.b6 .ce-bar-fill { animation-delay: 4.5s; }
.ce-bar-wrap.b7 .ce-bar-fill { animation-delay: 5.3s; }
.ce-bar-wrap.b8 .ce-bar-fill { animation-delay: 6.1s; }

@keyframes ce-fillBar { to { width: 100%; } }

.ce-bar-pct { font-size: 10px; color: rgba(0,255,80,0.5); }

.ce-final-banner {
  margin-top: 6px;
  border: 1px solid rgba(0,255,80,0.3);
  padding: 8px 16px;
  display: flex; justify-content: space-between; align-items: center;
  opacity: 0;
  animation: ce-lineIn 0.3s ease-out 7.2s forwards;
  background: rgba(0,255,80,0.05);
  box-shadow: 0 0 20px rgba(0,255,80,0.1);
}

.ce-final-name {
  font-family: 'VT323', monospace;
  font-size: 26px; color: #00ff50;
  text-shadow: 0 0 14px rgba(0,255,80,0.7);
  letter-spacing: 2px;
}

.ce-final-status {
  font-size: 11px; color: #00ff50;
  text-shadow: 0 0 8px rgba(0,255,80,0.5);
}

.ce-cursor {
  display: inline-block; width: 8px; height: 14px;
  background: #00ff50; margin-left: 2px;
  vertical-align: middle;
}

@keyframes ce-fadeIn { from { opacity: 0; } to { opacity: 1; } }
</style>

<div class="ce-outer">
  <div class="ce-wrap">
    <div class="ce-crt"></div>
    <div class="ce-scanlines"></div>

    <div class="ce-screen">

      <div class="ce-bios-header">
        <span class="ce-bios-right">BIOS v2026.03<br>MEM: 32GB OK</span>
        <div class="ce-bios-title">ESPEJO SYSTEMS BIOS</div>
        <div class="ce-bios-sub">CARLOS ESPEJO — PERSONAL RUNTIME INITIALIZATION</div>
      </div>

      <div class="ce-boot-lines">

        <div class="ce-line l1">
          <span class="ce-label">[ORIGIN]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Santiago, D.R.</span>
          <span class="ce-dots">&nbsp;...........</span>
          <span class="ce-ok">&nbsp;LOADED ✓</span>
        </div>
        <div class="ce-bar-wrap b1">
          <span class="ce-bar-label">&nbsp;&nbsp;&nbsp;&nbsp;island_roots.exe</span>
          <div class="ce-bar-track"><div class="ce-bar-fill"></div></div>
          <span class="ce-bar-pct">100%</span>
        </div>

        <div class="ce-line l2">
          <span class="ce-label">[RELOCATE]&nbsp;&nbsp;&nbsp;Sunset Park, Brooklyn</span>
          <span class="ce-dots">&nbsp;...........</span>
          <span class="ce-ok">&nbsp;LOADED ✓</span>
        </div>
        <div class="ce-bar-wrap b2">
          <span class="ce-bar-label">&nbsp;&nbsp;&nbsp;&nbsp;hustle_mode.dll</span>
          <div class="ce-bar-track"><div class="ce-bar-fill"></div></div>
          <span class="ce-bar-pct">100%</span>
        </div>

        <div class="ce-line l3">
          <span class="ce-label">[EDUCATION]&nbsp;&nbsp;John Jay College 2005</span>
          <span class="ce-dots">&nbsp;...........</span>
          <span class="ce-info">&nbsp;CIS + CRIM.JUSTICE</span>
        </div>
        <div class="ce-bar-wrap b3">
          <span class="ce-bar-label">&nbsp;&nbsp;&nbsp;&nbsp;dotnet_basics.dll</span>
          <div class="ce-bar-track"><div class="ce-bar-fill"></div></div>
          <span class="ce-bar-pct">100%</span>
        </div>

        <div class="ce-line l4">
          <span class="ce-label">[INTERNSHIP]&nbsp;CUNY Graduate Center</span>
          <span class="ce-dots">&nbsp;...........</span>
          <span class="ce-warn">&nbsp;⚡ SPARK DETECTED</span>
        </div>
        <div class="ce-bar-wrap b4">
          <span class="ce-bar-label">&nbsp;&nbsp;&nbsp;&nbsp;career_pivot.exe</span>
          <div class="ce-bar-track"><div class="ce-bar-fill"></div></div>
          <span class="ce-bar-pct">100%</span>
        </div>

        <div class="ce-line l5">
          <span class="ce-label">[JOB]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Software Engineer</span>
          <span class="ce-dots">&nbsp;...........</span>
          <span class="ce-ok">&nbsp;LOADED ✓</span>
        </div>
        <div class="ce-bar-wrap b5">
          <span class="ce-bar-label">&nbsp;&nbsp;&nbsp;&nbsp;software_eng.exe</span>
          <div class="ce-bar-track"><div class="ce-bar-fill"></div></div>
          <span class="ce-bar-pct">100%</span>
        </div>

        <div class="ce-line l6">
          <span class="ce-label">[PIVOT]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Cloud Engineer</span>
          <span class="ce-dots">&nbsp;...........</span>
          <span class="ce-warn">&nbsp;⚡ PIVOT ENGAGED</span>
        </div>
        <div class="ce-bar-wrap b6">
          <span class="ce-bar-label">&nbsp;&nbsp;&nbsp;&nbsp;cloud_migration.pkg</span>
          <div class="ce-bar-track"><div class="ce-bar-fill"></div></div>
          <span class="ce-bar-pct">100%</span>
        </div>

        <div class="ce-line l7">
          <span class="ce-label">[PROMOTED]&nbsp;&nbsp;&nbsp;Lead Cloud Engineer</span>
          <span class="ce-dots">&nbsp;...........</span>
          <span class="ce-info">&nbsp;RANK UP ▲</span>
        </div>
        <div class="ce-bar-wrap b7">
          <span class="ce-bar-label">&nbsp;&nbsp;&nbsp;&nbsp;leadership.dll</span>
          <div class="ce-bar-track"><div class="ce-bar-fill"></div></div>
          <span class="ce-bar-pct">100%</span>
        </div>

        <div class="ce-line l8">
          <span class="ce-label">[SKILL]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;AI / ML Engineering</span>
          <span class="ce-dots">&nbsp;...........</span>
          <span class="ce-ok">&nbsp;UNLOCKED ✓</span>
        </div>
        <div class="ce-bar-wrap b8">
          <span class="ce-bar-label">&nbsp;&nbsp;&nbsp;&nbsp;agentic_workflows.ai</span>
          <div class="ce-bar-track"><div class="ce-bar-fill"></div></div>
          <span class="ce-bar-pct">100%</span>
        </div>

      </div>

      <div class="ce-final-banner">
        <div class="ce-final-name">CARLOS ESPEJO v2026 — READY<span class="ce-cursor"></span></div>
        <div class="ce-final-status">▶ SYSTEM OPERATIONAL · NYC</div>
      </div>

    </div>
  </div>
</div>

<script>
(function() {
  function scaleWrap() {
    var outer = document.querySelector('.ce-outer');
    var wrap  = document.querySelector('.ce-wrap');
    if (!outer || !wrap) return;
    var scale = outer.offsetWidth / 800;
    wrap.style.transform = 'scale(' + scale + ')';
    outer.style.height = (450 * scale) + 'px';
  }
  scaleWrap();
  window.addEventListener('resize', scaleWrap);
})();
</script>
