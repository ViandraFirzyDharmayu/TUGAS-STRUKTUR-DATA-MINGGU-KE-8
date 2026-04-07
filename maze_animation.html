<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Animasi Labirin – Stack Backtracking | Bab 7</title>
  <style>
    :root {
      --bg: #0d1117;
      --surface: #161b22;
      --surface2: #21262d;
      --border: #30363d;
      --text: #e6edf3;
      --text-muted: #8b949e;
      --green: #1D9E75;
      --green-light: #9FE1CB;
      --green-dark: #0F6E56;
      --amber: #EF9F27;
      --amber-light: #FAC775;
      --red: #D4537E;
      --wall: #010409;
      --open: #1c2128;
      --path: #1D9E75;
      --dead: #5a3e00;
      --font-mono: 'Courier New', monospace;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: var(--font-mono);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 2rem 1rem;
    }

    header {
      text-align: center;
      margin-bottom: 1.5rem;
    }

    header h1 {
      font-size: 1.4rem;
      font-weight: 700;
      letter-spacing: 0.05em;
      color: var(--green-light);
      margin-bottom: 4px;
    }

    header p {
      font-size: 0.8rem;
      color: var(--text-muted);
    }

    .badge {
      display: inline-block;
      background: var(--green-dark);
      color: var(--green-light);
      font-size: 0.7rem;
      padding: 2px 8px;
      border-radius: 999px;
      margin-bottom: 8px;
      letter-spacing: 0.08em;
    }

    .main-layout {
      display: flex;
      gap: 1.5rem;
      align-items: flex-start;
      flex-wrap: wrap;
      justify-content: center;
      width: 100%;
      max-width: 1100px;
    }

    /* MAZE */
    #maze-wrap {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 1rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.75rem;
    }

    canvas {
      display: block;
      border-radius: 4px;
      border: 1px solid var(--border);
    }

    /* LEGEND */
    .legend {
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
      justify-content: center;
    }

    .leg {
      display: flex;
      align-items: center;
      gap: 5px;
      font-size: 0.7rem;
      color: var(--text-muted);
    }

    .leg-box {
      width: 13px;
      height: 13px;
      border-radius: 3px;
      flex-shrink: 0;
    }

    /* SIDE PANEL */
    .side-panel {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      min-width: 260px;
      max-width: 300px;
    }

    .panel-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 1rem;
    }

    .panel-card h3 {
      font-size: 0.75rem;
      font-weight: 700;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.1em;
      margin-bottom: 10px;
      border-bottom: 1px solid var(--border);
      padding-bottom: 6px;
    }

    /* CONTROLS */
    .controls {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
      margin-bottom: 10px;
    }

    button {
      font-family: var(--font-mono);
      font-size: 0.78rem;
      padding: 6px 14px;
      border-radius: 6px;
      border: 1px solid var(--border);
      background: var(--surface2);
      color: var(--text);
      cursor: pointer;
      transition: background 0.15s, transform 0.1s;
      letter-spacing: 0.03em;
    }

    button:hover { background: #2d333b; }
    button:active { transform: scale(0.97); }
    button:disabled { opacity: 0.35; cursor: not-allowed; }

    button.primary {
      background: var(--green-dark);
      color: var(--green-light);
      border-color: var(--green);
    }

    button.primary:hover { background: var(--green); color: white; }

    /* SPEED */
    .speed-row {
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 0.78rem;
      color: var(--text-muted);
    }

    input[type=range] {
      flex: 1;
      accent-color: var(--green);
      height: 4px;
    }

    /* STATUS */
    #status-box {
      font-size: 0.8rem;
      padding: 8px 10px;
      border-radius: 6px;
      background: var(--surface2);
      border: 1px solid var(--border);
      color: var(--text-muted);
      min-height: 36px;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    #status-dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--text-muted);
      flex-shrink: 0;
      transition: background 0.3s;
    }

    /* STATS */
    .stats-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
    }

    .stat {
      background: var(--surface2);
      border-radius: 6px;
      padding: 8px 10px;
      text-align: center;
    }

    .stat-label {
      font-size: 0.65rem;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    .stat-value {
      font-size: 1.3rem;
      font-weight: 700;
      color: var(--green-light);
      line-height: 1.2;
    }

    /* STACK VIS */
    #stack-vis-area {
      display: flex;
      flex-direction: column;
      gap: 4px;
      max-height: 180px;
      overflow-y: auto;
      scrollbar-width: thin;
      scrollbar-color: var(--border) transparent;
    }

    .stack-row {
      display: flex;
      align-items: center;
      gap: 6px;
      animation: slideIn 0.15s ease;
    }

    @keyframes slideIn {
      from { opacity: 0; transform: translateX(-8px); }
      to   { opacity: 1; transform: translateX(0); }
    }

    .stack-idx {
      font-size: 0.65rem;
      color: var(--text-muted);
      min-width: 22px;
      text-align: right;
    }

    .stack-cell {
      font-size: 0.72rem;
      padding: 3px 8px;
      border-radius: 4px;
      background: var(--surface2);
      border: 1px solid var(--border);
      color: var(--text-muted);
      font-family: var(--font-mono);
    }

    .stack-cell.top-item {
      background: #0f3b2a;
      color: var(--green-light);
      border-color: var(--green);
    }

    .stack-top-label {
      font-size: 0.65rem;
      color: var(--green);
      margin-left: 2px;
    }

    /* CODE PANEL */
    .code-block {
      background: var(--wall);
      border-radius: 6px;
      padding: 10px 12px;
      font-size: 0.7rem;
      line-height: 1.7;
      color: #8b949e;
      overflow-x: auto;
      border: 1px solid var(--border);
    }

    .code-block .kw { color: #ff7b72; }
    .code-block .fn { color: #d2a8ff; }
    .code-block .cm { color: #3d444d; }
    .code-block .str { color: #a5d6ff; }
    .code-block .hl { background: rgba(29,158,117,0.18); display: block; border-left: 2px solid var(--green); padding-left: 6px; margin-left: -12px; }

    #hl-push { transition: background 0.3s; }
    #hl-pop  { transition: background 0.3s; }

    .active-line {
      background: rgba(29,158,117,0.25) !important;
    }

    /* PROGRESS */
    #progress-bar-wrap {
      width: 100%;
      height: 4px;
      background: var(--surface2);
      border-radius: 2px;
      overflow: hidden;
    }
    #progress-bar {
      height: 100%;
      background: var(--green);
      width: 0%;
      transition: width 0.1s;
      border-radius: 2px;
    }
  </style>
</head>
<body>

<header>
  <div class="badge">BAB 7 — STRUKTUR DATA</div>
  <h1>Animasi Pemecahan Labirin</h1>
  <p>Algoritma Backtracking menggunakan Tumpukan (Stack) &nbsp;·&nbsp; LIFO</p>
</header>

<div class="main-layout">

  <!-- MAZE CANVAS -->
  <div id="maze-wrap">
    <canvas id="maze-canvas"></canvas>
    <div id="progress-bar-wrap"><div id="progress-bar"></div></div>
    <div class="legend">
      <div class="leg"><div class="leg-box" style="background:#1D9E75;"></div> Start (S)</div>
      <div class="leg"><div class="leg-box" style="background:#EF9F27;"></div> Exit (E)</div>
      <div class="leg"><div class="leg-box" style="background:#010409; border:1px solid #30363d;"></div> Dinding</div>
      <div class="leg"><div class="leg-box" style="background:#1D9E75; opacity:0.5;"></div> Jalur (x)</div>
      <div class="leg"><div class="leg-box" style="background:#5a3e00;"></div> Buntu (o)</div>
      <div class="leg"><div class="leg-box" style="background:#D4537E; border-radius:50%;"></div> Posisi kini</div>
    </div>
  </div>

  <!-- SIDE PANEL -->
  <div class="side-panel">

    <!-- Controls -->
    <div class="panel-card">
      <h3>Kontrol</h3>
      <div class="controls">
        <button class="primary" id="btn-play">▶ Mulai</button>
        <button id="btn-step" disabled>→ Langkah</button>
        <button id="btn-reset">↺ Reset</button>
      </div>
      <div class="speed-row">
        <span>Lambat</span>
        <input type="range" id="speed" min="1" max="6" value="3" step="1" />
        <span>Cepat</span>
      </div>
      <br>
      <div id="status-box">
        <div id="status-dot"></div>
        <span id="status-text">Siap — klik Mulai untuk animasi</span>
      </div>
    </div>

    <!-- Stats -->
    <div class="panel-card">
      <h3>Statistik</h3>
      <div class="stats-grid">
        <div class="stat">
          <div class="stat-label">Stack Size</div>
          <div class="stat-value" id="stat-stack">0</div>
        </div>
        <div class="stat">
          <div class="stat-label">Langkah</div>
          <div class="stat-value" id="stat-steps">0</div>
        </div>
        <div class="stat">
          <div class="stat-label">Jalur (x)</div>
          <div class="stat-value" id="stat-path">0</div>
        </div>
        <div class="stat">
          <div class="stat-label">Buntu (o)</div>
          <div class="stat-value" id="stat-dead">0</div>
        </div>
      </div>
    </div>

    <!-- Stack Visualizer -->
    <div class="panel-card">
      <h3>Isi Tumpukan (Stack)</h3>
      <div id="stack-vis-area">
        <span style="font-size:0.75rem; color:var(--text-muted);">Stack kosong</span>
      </div>
    </div>

    <!-- Code -->
    <div class="panel-card">
      <h3>Pseudocode findPath()</h3>
      <div class="code-block">
<span><span class="kw">def</span> <span class="fn">findPath</span>(self):</span>
<span>  stack = <span class="fn">Stack</span>()</span>
<span>  stack.<span class="fn">push</span>(selAwal)</span>
<span>  <span class="cm"># tandai awal</span></span>
<span>&nbsp;</span>
<span id="hl-while">  <span class="kw">while not</span> stack.<span class="fn">isEmpty</span>():</span>
<span>    r, c = stack.<span class="fn">peek</span>()</span>
<span>    <span class="kw">if</span> keluarDitemukan(r,c):</span>
<span>      <span class="kw">return True</span></span>
<span id="hl-push">    <span class="kw">if</span> gerakValid(tetangga):</span>
<span>      tandaiJalur(nr, nc)</span>
<span>      stack.<span class="fn">push</span>((nr, nc))  <span class="cm"># maju</span></span>
<span id="hl-pop">    <span class="kw">else</span>:  <span class="cm"># jalan buntu</span></span>
<span>      tandaiBuntu(r, c)</span>
<span>      stack.<span class="fn">pop</span>()  <span class="cm"># backtrack</span></span>
<span>  <span class="kw">return False</span></span>
      </div>
    </div>

  </div>
</div>

<script>
const MAZE_STR = [
  "#####################",
  "#S  #     #         #",
  "# # # ### # ####### #",
  "# # #   # #       # #",
  "# ##### # ####### # #",
  "#       #     #   # #",
  "####### ##### # ### #",
  "#     #     # #   # #",
  "# ### ##### # ### # #",
  "#   #       #     # #",
  "### ######### ##### #",
  "#   #         #     #",
  "# ### ######### ### #",
  "#     #         # # #",
  "##### # ######### # #",
  "#     #       #   # #",
  "# ########### # ### #",
  "#           # #     #",
  "########### # ##### #",
  "#           #      E#",
  "#####################"
];

const ROWS = MAZE_STR.length;
const COLS = MAZE_STR[0].length;
const CELL = 22;

const canvas = document.getElementById('maze-canvas');
const ctx = canvas.getContext('2d');
canvas.width = COLS * CELL;
canvas.height = ROWS * CELL;

let startR, startC, exitR, exitC;
let steps = [], stepIdx = 0;
let animTimer = null, running = false;
let deadEndGrid, pathSet, stackState;
let totalSteps = 0;

const DIRS = [[-1,0],[0,1],[1,0],[0,-1]];

function initMaze() {
  deadEndGrid = Array.from({length: ROWS}, () => new Array(COLS).fill(false));
  pathSet = new Set();
  stackState = [];
  totalSteps = 0;
  for (let r = 0; r < ROWS; r++) {
    for (let c = 0; c < COLS; c++) {
      const ch = MAZE_STR[r][c];
      if (ch === 'S') { startR = r; startC = c; }
      if (ch === 'E') { exitR = r; exitC = c; }
    }
  }
}

function buildSteps() {
  steps = [];
  const vs = Array.from({length: ROWS}, () => new Array(COLS).fill(false));
  const de = Array.from({length: ROWS}, () => new Array(COLS).fill(false));
  const stk = [[startR, startC]];
  const ps = new Set([startR + ',' + startC]);
  vs[startR][startC] = true;

  const snap = (cur, action) => ({
    stk: stk.map(x => [...x]),
    ps: new Set(ps),
    de: de.map(r => [...r]),
    cur: cur ? [...cur] : null,
    action,
    done: false, found: false
  });

  steps.push(snap([startR, startC], 'push'));

  let iter = 0;
  while (stk.length > 0 && iter < 100000) {
    iter++;
    const [r, c] = stk[stk.length - 1];
    if (r === exitR && c === exitC) {
      steps.push({ ...snap([r, c], 'found'), done: true, found: true });
      break;
    }
    let moved = false;
    for (const [dr, dc] of DIRS) {
      const nr = r + dr, nc = c + dc;
      if (nr >= 0 && nr < ROWS && nc >= 0 && nc < COLS &&
          MAZE_STR[nr][nc] !== '#' && !vs[nr][nc] && !de[nr][nc]) {
        vs[nr][nc] = true;
        ps.add(nr + ',' + nc);
        stk.push([nr, nc]);
        steps.push(snap([nr, nc], 'push'));
        moved = true;
        break;
      }
    }
    if (!moved) {
      de[r][c] = true;
      ps.delete(r + ',' + c);
      stk.pop();
      steps.push(snap(stk.length ? stk[stk.length-1] : null, 'pop'));
    }
  }
  if (!steps.length || !steps[steps.length-1].found) {
    steps.push({ stk: [], ps: new Set(), de: de.map(r=>[...r]), cur: null, done: true, found: false, action: 'end' });
  }
}

function hexAlpha(hex, alpha) {
  const r = parseInt(hex.slice(1,3),16);
  const g = parseInt(hex.slice(3,5),16);
  const b = parseInt(hex.slice(5,7),16);
  return `rgba(${r},${g},${b},${alpha})`;
}

function drawMaze(s) {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  const cur = s ? s.cur : null;
  const ps = s ? s.ps : new Set();
  const de = s ? s.de : deadEndGrid;

  for (let r = 0; r < ROWS; r++) {
    for (let c = 0; c < COLS; c++) {
      const x = c * CELL, y = r * CELL;
      const ch = MAZE_STR[r][c];
      const key = r + ',' + c;
      const isPath = ps.has(key);
      const isDead = de[r][c];

      if (ch === '#') {
        ctx.fillStyle = '#010409';
        ctx.fillRect(x, y, CELL, CELL);
        ctx.strokeStyle = 'rgba(48,54,61,0.4)';
        ctx.lineWidth = 0.5;
        ctx.strokeRect(x+0.5, y+0.5, CELL-1, CELL-1);
      } else if (ch === 'S') {
        ctx.fillStyle = '#1D9E75';
        ctx.fillRect(x, y, CELL, CELL);
      } else if (ch === 'E') {
        ctx.fillStyle = '#EF9F27';
        ctx.fillRect(x, y, CELL, CELL);
      } else if (isDead) {
        ctx.fillStyle = '#5a3e00';
        ctx.fillRect(x, y, CELL, CELL);
        ctx.fillStyle = '#EF9F27';
        ctx.font = `${Math.round(CELL*0.5)}px monospace`;
        ctx.textAlign = 'center';
        ctx.textBaseline = 'middle';
        ctx.fillText('o', x+CELL/2, y+CELL/2+1);
      } else if (isPath) {
        ctx.fillStyle = hexAlpha('#1D9E75', 0.5);
        ctx.fillRect(x, y, CELL, CELL);
        ctx.fillStyle = '#9FE1CB';
        ctx.font = `${Math.round(CELL*0.45)}px monospace`;
        ctx.textAlign = 'center';
        ctx.textBaseline = 'middle';
        ctx.fillText('x', x+CELL/2, y+CELL/2+1);
      } else {
        ctx.fillStyle = '#1c2128';
        ctx.fillRect(x, y, CELL, CELL);
        ctx.strokeStyle = 'rgba(48,54,61,0.3)';
        ctx.lineWidth = 0.5;
        ctx.strokeRect(x+0.5, y+0.5, CELL-1, CELL-1);
      }

      if (ch === 'S') {
        ctx.fillStyle = 'white';
        ctx.font = `bold ${Math.round(CELL*0.5)}px monospace`;
        ctx.textAlign = 'center';
        ctx.textBaseline = 'middle';
        ctx.fillText('S', x+CELL/2, y+CELL/2+1);
      }
      if (ch === 'E') {
        ctx.fillStyle = 'white';
        ctx.font = `bold ${Math.round(CELL*0.5)}px monospace`;
        ctx.textAlign = 'center';
        ctx.textBaseline = 'middle';
        ctx.fillText('E', x+CELL/2, y+CELL/2+1);
      }
    }
  }

  if (cur) {
    const [cr, cc] = cur;
    const x = cc*CELL + CELL/2, y = cr*CELL + CELL/2;
    ctx.beginPath();
    ctx.arc(x, y, CELL*0.28, 0, Math.PI*2);
    ctx.fillStyle = '#D4537E';
    ctx.fill();
    ctx.strokeStyle = 'rgba(212,83,126,0.4)';
    ctx.lineWidth = 2;
    ctx.stroke();
  }
}

function updateUI(s) {
  if (!s) return;
  const stackSize = s.stk.length;
  const pathSize = s.ps.size;
  let deadCount = 0;
  s.de.forEach(row => row.forEach(v => { if(v) deadCount++; }));

  document.getElementById('stat-stack').textContent = stackSize;
  document.getElementById('stat-steps').textContent = totalSteps;
  document.getElementById('stat-path').textContent = pathSize;
  document.getElementById('stat-dead').textContent = deadCount;

  const prog = steps.length > 1 ? Math.round((stepIdx / (steps.length-1)) * 100) : 0;
  document.getElementById('progress-bar').style.width = prog + '%';

  // Stack vis
  const area = document.getElementById('stack-vis-area');
  area.innerHTML = '';
  if (s.stk.length === 0) {
    area.innerHTML = '<span style="font-size:0.75rem;color:var(--text-muted)">Stack kosong</span>';
  } else {
    [...s.stk].reverse().forEach((pos, i) => {
      const isTop = i === 0;
      const row = document.createElement('div');
      row.className = 'stack-row';
      row.innerHTML = `
        <span class="stack-idx">${s.stk.length - i}</span>
        <span class="stack-cell ${isTop ? 'top-item' : ''}">(${pos[0]}, ${pos[1]})</span>
        ${isTop ? '<span class="stack-top-label">← TOP</span>' : ''}
      `;
      area.appendChild(row);
    });
  }

  // Status
  const dot = document.getElementById('status-dot');
  const txt = document.getElementById('status-text');
  if (s.done && s.found) {
    dot.style.background = '#1D9E75';
    txt.textContent = '✓ Jalur ditemukan! Exit tercapai.';
    txt.style.color = '#9FE1CB';
  } else if (s.done && !s.found) {
    dot.style.background = '#D4537E';
    txt.textContent = '✗ Tidak ada jalur ke exit.';
    txt.style.color = '#D4537E';
  } else if (s.action === 'pop') {
    dot.style.background = '#EF9F27';
    txt.textContent = 'Backtrack ← Pop dari stack';
    txt.style.color = '#EF9F27';
  } else if (s.action === 'push') {
    const p = s.stk[s.stk.length-1];
    dot.style.background = '#1D9E75';
    txt.textContent = `Push (${p[0]},${p[1]}) → maju`;
    txt.style.color = 'var(--text-muted)';
  }

  // Code highlight
  document.getElementById('hl-push').style.background = s.action === 'push' ? 'rgba(29,158,117,0.25)' : '';
  document.getElementById('hl-pop').style.background  = s.action === 'pop'  ? 'rgba(239,159,39,0.2)'  : '';
}

function applyStep(idx) {
  const s = steps[idx];
  drawMaze(s);
  updateUI(s);
}

function speedMs() {
  const v = parseInt(document.getElementById('speed').value);
  return [500, 200, 80, 30, 10, 2][v-1];
}

function runAnim() {
  if (stepIdx >= steps.length) { stopAnim(); return; }
  totalSteps++;
  applyStep(stepIdx);
  if (steps[stepIdx].done) { stepIdx++; stopAnim(); return; }
  stepIdx++;
  animTimer = setTimeout(runAnim, speedMs());
}

function stopAnim() {
  clearTimeout(animTimer);
  animTimer = null;
  running = false;
  document.getElementById('btn-play').textContent = stepIdx >= steps.length ? '▶ Selesai' : '▶ Lanjut';
  document.getElementById('btn-play').disabled = stepIdx >= steps.length && steps[steps.length-1]?.done;
  document.getElementById('btn-step').disabled = stepIdx >= steps.length;
}

function ensureSteps() {
  if (!steps.length) {
    initMaze();
    buildSteps();
    stepIdx = 0;
    totalSteps = 0;
    applyStep(0);
    document.getElementById('btn-step').disabled = false;
  }
}

document.getElementById('btn-play').addEventListener('click', () => {
  ensureSteps();
  if (running) {
    clearTimeout(animTimer);
    animTimer = null;
    running = false;
    document.getElementById('btn-play').textContent = '▶ Lanjut';
    document.getElementById('btn-step').disabled = false;
  } else {
    running = true;
    document.getElementById('btn-play').textContent = '⏸ Pause';
    document.getElementById('btn-step').disabled = true;
    runAnim();
  }
});

document.getElementById('btn-step').addEventListener('click', () => {
  ensureSteps();
  if (stepIdx < steps.length) {
    totalSteps++;
    applyStep(stepIdx);
    stepIdx++;
    if (stepIdx >= steps.length || steps[stepIdx-1].done) {
      document.getElementById('btn-step').disabled = true;
      document.getElementById('btn-play').disabled = true;
    }
  }
});

document.getElementById('btn-reset').addEventListener('click', () => {
  clearTimeout(animTimer);
  animTimer = null;
  running = false;
  steps = [];
  stepIdx = 0;
  totalSteps = 0;
  initMaze();
  drawMaze(null);
  document.getElementById('stack-vis-area').innerHTML =
    '<span style="font-size:0.75rem;color:var(--text-muted)">Stack kosong</span>';
  document.getElementById('stat-stack').textContent = '0';
  document.getElementById('stat-steps').textContent = '0';
  document.getElementById('stat-path').textContent = '0';
  document.getElementById('stat-dead').textContent = '0';
  document.getElementById('progress-bar').style.width = '0%';
  document.getElementById('btn-play').textContent = '▶ Mulai';
  document.getElementById('btn-play').disabled = false;
  document.getElementById('btn-step').disabled = true;
  document.getElementById('status-dot').style.background = 'var(--text-muted)';
  document.getElementById('status-text').textContent = 'Siap — klik Mulai untuk animasi';
  document.getElementById('status-text').style.color = '';
  document.getElementById('hl-push').style.background = '';
  document.getElementById('hl-pop').style.background = '';
});

initMaze();
drawMaze(null);
</script>
</body>
</html>
