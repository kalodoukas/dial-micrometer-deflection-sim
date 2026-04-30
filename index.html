<!doctype html>
<html lang="el">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Dial Micrometer – v12 smooth zero-start indications</title>

<style>
html,body{
  margin:0;
  width:100%;
  height:100%;
  background:#0f1115;
  color:#e9eef7;
  font-family:system-ui,Segoe UI,Arial,sans-serif;
  overflow:hidden;
}

/* ===== TOP CONTROLS ===== */
#controls{
  position:fixed;
  top:14px;
  left:14px;
  display:flex;
  gap:10px;
  flex-wrap:wrap;
  z-index:120;
}
.btn{
  height:42px;
  min-width:44px;
  padding:0 12px;
  border-radius:12px;
  border:1px solid rgba(255,255,255,.18);
  background:rgba(0,0,0,.62);
  color:#fff;
  font-size:17px;
  line-height:42px;
  cursor:pointer;
  user-select:none;
  touch-action:none;
}
.btnIcon{
  width:44px;
  padding:0;
  font-size:22px;
}
.btn:disabled{
  opacity:.35;
  cursor:not-allowed;
}

/* ===== OVERALL LAYOUT ===== */
#mainLayout{
  position:fixed;
  inset:0;
  display:grid;
  grid-template-columns: clamp(240px, 25vw, 350px) 1fr 70px;
  align-items:center;
  gap:clamp(12px, 2vw, 28px);
  padding:78px 12px 12px 12px;
  box-sizing:border-box;
}

/* ===== LEFT VERTICAL DEFLECTION / TURNING PANEL ===== */
#deflPanel{
  height:min(86vh, 760px);
  width:100%;
  background:rgba(0,0,0,.64);
  border:1px solid rgba(255,255,255,.16);
  border-radius:14px;
  backdrop-filter:blur(6px);
  box-sizing:border-box;
  padding:12px 14px;
  display:flex;
  flex-direction:column;
  justify-content:flex-start;
  align-items:stretch;
  overflow:hidden;
}
#deflTitle{
  font-size:15px;
  color:rgba(233,238,247,.95);
  margin-bottom:8px;
}
#deflAngle{
  font-size:25px;
  font-weight:700;
  font-variant-numeric:tabular-nums;
  margin-bottom:6px;
}
.deflLine{
  font-size:15px;
  font-variant-numeric:tabular-nums;
  color:rgba(233,238,247,.92);
  margin-bottom:5px;
}
#turnStatus{
  color:#ffd24a;
}
#deflSub{
  font-size:12px;
  color:rgba(233,238,247,.72);
  margin-top:8px;
}

/* vertical crank / rod svg on the left */
#mechWrap{
  flex:1 1 auto;
  min-height:280px;
  margin-top:8px;
}
#mechSvg{
  width:100%;
  height:100%;
  display:block;
  overflow:visible;
}

/* ===== CENTER DIAL AREA ===== */
#dialStage{
  position:relative;
  width:100%;
  height:100%;
  display:flex;
  align-items:center;
  justify-content:center;
  min-width:0;
}

#wrap{
  position:relative;
  width:min(78vh, calc(100vw - clamp(240px, 25vw, 350px) - 120px));
  height:min(78vh, calc(100vw - clamp(240px, 25vw, 350px) - 120px));
  max-width:100%;
  max-height:100%;
}

#dialSvg{
  position:absolute;
  inset:0;
  width:100%;
  height:100%;
  display:block;
  z-index:10;
  pointer-events:none;
}

/* Digital micrometer indication */
#digital{
  position:absolute;
  left:50%;
  top:50%;
  transform:translate(-50%,-50%) translateY(100px);
  padding:12px 18px;
  border-radius:14px;
  background:rgba(0,0,0,.75);
  border:1px solid rgba(255,255,255,.22);
  backdrop-filter:blur(6px);
  z-index:30;
  display:none;
  text-align:center;
  pointer-events:none;
  box-shadow:0 8px 30px rgba(0,0,0,.35);
}
#digital .val{
  font-size:30px;
  font-weight:700;
  font-variant-numeric:tabular-nums;
  letter-spacing:.4px;
  color:#fff;
}

/* ===== RIGHT SLIDER ===== */
#right{
  width:70px;
  height:100%;
  display:flex;
  align-items:center;
  justify-content:center;
  background:rgba(0,0,0,.35);
  border-left:1px solid rgba(255,255,255,.12);
  border-radius:10px;
}
#pos{
  height:calc(100% - 30px);
  width:26px;
  writing-mode:bt-lr;
  -webkit-appearance:slider-vertical;
  appearance:slider-vertical;
}

/* ===== Responsive fallback for narrower screens ===== */
@media (max-width: 1100px){
  #mainLayout{
    grid-template-columns: clamp(210px, 28vw, 280px) 1fr 60px;
    gap:12px;
  }
  #wrap{
    width:min(72vh, calc(100vw - clamp(210px, 28vw, 280px) - 100px));
    height:min(72vh, calc(100vw - clamp(210px, 28vw, 280px) - 100px));
  }
  #deflAngle{ font-size:22px; }
  .deflLine{ font-size:14px; }
}

/* ===== Signature ===== */
#signatureNK{
  position:fixed;
  right:12px;
  bottom:8px;
  z-index:140;
  color:rgba(233,238,247,.72);
  font-size:13px;
  font-weight:600;
  letter-spacing:.2px;
  background:rgba(0,0,0,.28);
  border:1px solid rgba(255,255,255,.10);
  border-radius:10px;
  padding:5px 9px;
  pointer-events:none;
  user-select:none;
}

</style>

<!-- PWA metadata -->
<meta name="theme-color" content="#0f1115">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Deflection Sim">
<link rel="manifest" href="./manifest.webmanifest">
<link rel="icon" href="./icons/icon-192.png" sizes="192x192">
<link rel="apple-touch-icon" href="./icons/icon-192.png">

</head>

<body>

<div id="signatureNK">By N.Kalodoukas</div>


<div id="controls">
  <button id="minus" class="btn btnIcon">−</button>
  <button id="plus" class="btn btnIcon">+</button>
  <button id="toggleDigital" class="btn">Digital</button>
  <button id="startTurning" class="btn" disabled>Start Turning</button>
  <button id="stopTurning" class="btn" disabled>Stop Turning</button>
</div>

<div id="mainLayout">

  <!-- LEFT: vertical crank/rod + readings -->
  <div id="deflPanel">
    <div id="deflTitle">Main Bearing Deflection / Turning Simulation</div>
    <div id="deflAngle">Crank angle: 190.0°</div>
    <div id="deflValue" class="deflLine">Deflection: +0.000 mm</div>
    <div id="bearingWear" class="deflLine">Main Bearing Wear Index: 0.00</div>
    <div id="turnStatus" class="deflLine">Status: Set offset with + / −</div>

    <div id="mechWrap">
      <svg id="mechSvg" viewBox="0 0 240 420" aria-label="Vertical crank and connecting rod simulation">
        <!-- guide / reference -->
        <line x1="120" y1="24" x2="120" y2="250" stroke="rgba(233,238,247,.22)" stroke-width="1.2"/>
        <line x1="105" y1="24" x2="105" y2="250" stroke="rgba(233,238,247,.13)" stroke-width="1"/>
        <line x1="135" y1="24" x2="135" y2="250" stroke="rgba(233,238,247,.13)" stroke-width="1"/>

        <!-- crank circle -->
        <circle cx="120" cy="325" r="56" fill="none" stroke="rgba(233,238,247,.20)" stroke-width="1.2"/>

        <!-- crank -->
        <line id="crankLine" x1="120" y1="325" x2="176" y2="325"
              stroke="#ffd24a" stroke-width="3" stroke-linecap="round"/>

        <!-- crank pin -->
        <circle id="crankPin" cx="176" cy="325" r="4.8" fill="#ffd24a"/>

        <!-- connecting rod -->
        <line id="rodLine" x1="176" y1="325" x2="120" y2="200"
              stroke="rgba(233,238,247,.90)" stroke-width="3" stroke-linecap="round"/>

        <!-- slider / crosshead -->
        <rect id="sliderBlock" x="108" y="188" width="24" height="26" rx="2"
              fill="rgba(233,238,247,.22)" stroke="rgba(233,238,247,.70)" stroke-width="1.1"/>

        <!-- center -->
        <circle cx="120" cy="325" r="4.5" fill="rgba(233,238,247,.85)"/>
      </svg>
    </div>

    <div id="deflSub">1 measurement cycle / 5 minutes • 0° = ΑΝΣ / TDC • indications start from zero and change gradually</div>
  </div>

  <!-- CENTER: dial -->
  <div id="dialStage">
    <div id="wrap">
      <svg id="dialSvg" viewBox="0 0 150 150" aria-label="Dial micrometer demo">
        <!-- MAIN DIAL / BEZEL: rotates only with + / − -->
        <g id="bezel" transform="rotate(0 75 75)">
          <circle cx="75" cy="75" r="74"
                  fill="rgba(0,0,0,.18)"
                  stroke="rgba(233,238,247,.35)"
                  stroke-width="0.8"/>
          <circle cx="75" cy="75" r="70.8"
                  fill="rgba(0,0,0,.10)"
                  stroke="rgba(233,238,247,.15)"
                  stroke-width="0.6"/>
          <g id="ticks"></g>
          <g id="nums"></g>
        </g>

        <!-- BIG NEEDLE -->
        <g id="big" transform="rotate(0 75 75)">
          <line x1="75" y1="75" x2="75" y2="10"
                stroke="#ffd24a"
                stroke-width="0.9"
                stroke-linecap="round"/>
          <circle cx="75" cy="75" r="2.0" fill="#ffd24a"/>
        </g>

        <!-- SMALL DIAL FACE -->
        <g id="subFace">
          <circle cx="100" cy="75" r="15"
                  fill="rgba(0,0,0,.20)"
                  stroke="rgba(233,238,247,.30)"
                  stroke-width="0.6"/>
          <circle cx="100" cy="75" r="13.6"
                  fill="rgba(0,0,0,.10)"
                  stroke="rgba(233,238,247,.12)"
                  stroke-width="0.5"/>
          <g id="subTicks"></g>
          <g id="subNums"></g>
        </g>

        <!-- SMALL NEEDLE -->
        <g id="small" transform="rotate(0 100 75)">
          <line x1="100" y1="75" x2="100" y2="63.5"
                stroke="#ffd24a"
                stroke-width="0.6"
                stroke-linecap="round"/>
          <circle cx="100" cy="75" r="1.2" fill="#ffd24a"/>
        </g>

        <!-- Centers -->
        <circle cx="75" cy="75" r="2.6"
                fill="rgba(233,238,247,.85)"
                stroke="rgba(0,0,0,.35)"
                stroke-width="0.4"/>
        <circle cx="100" cy="75" r="1.6"
                fill="rgba(233,238,247,.85)"
                stroke="rgba(0,0,0,.35)"
                stroke-width="0.3"/>
      </svg>

      <div id="digital">
        <div class="val"><span id="mm">0.00</span> mm</div>
      </div>
    </div>
  </div>

  <!-- RIGHT: slider -->
  <div id="right">
    <input id="pos" type="range" min="0" max="1000" step="1" value="0">
  </div>

</div>

<script>
/* ===== Helper ===== */
function polar(cx, cy, r, deg){
  const a = deg * Math.PI / 180;
  return {
    x: cx + r * Math.cos(a),
    y: cy + r * Math.sin(a)
  };
}
function clamp(v, min, max){
  return Math.max(min, Math.min(max, v));
}
function normalizeDeg(deg){
  return ((deg % 360) + 360) % 360;
}
function angularDifference(a, b){
  let d = Math.abs(normalizeDeg(a) - normalizeDeg(b));
  return Math.min(d, 360 - d);
}

function smoothstep01(x){
  const t = clamp(x, 0, 1);
  return t * t * (3 - 2 * t);
}

/* ===== MAIN DIAL GRAPHICS ===== */
const ticks = document.getElementById("ticks");
const nums  = document.getElementById("nums");

const CX = 75, CY = 75;
const OUTER_R = 74;
const TICK_W = 0.5;
const LEN_1 = 5.0;
const LEN_5 = 7.5;
const LEN_10 = 10.0;
const TEXT_R = OUTER_R - 15.0;

for(let i=0; i<100; i++){
  const ang = -90 + i * 3.6;

  let L = LEN_1;
  if(i % 10 === 0) L = LEN_10;
  else if(i % 5 === 0) L = LEN_5;

  const p1 = polar(CX, CY, OUTER_R, ang);
  const p2 = polar(CX, CY, OUTER_R - L, ang);

  const line = document.createElementNS("http://www.w3.org/2000/svg","line");
  line.setAttribute("x1", p1.x.toFixed(3));
  line.setAttribute("y1", p1.y.toFixed(3));
  line.setAttribute("x2", p2.x.toFixed(3));
  line.setAttribute("y2", p2.y.toFixed(3));
  line.setAttribute("stroke", "rgba(233,238,247,.85)");
  line.setAttribute("stroke-width", TICK_W);
  line.setAttribute("stroke-linecap", "round");
  ticks.appendChild(line);

  if(i % 10 === 0){
    const tp = polar(CX, CY, TEXT_R, ang);
    const text = document.createElementNS("http://www.w3.org/2000/svg","text");
    text.textContent = i;
    text.setAttribute("x", tp.x.toFixed(3));
    text.setAttribute("y", tp.y.toFixed(3));
    text.setAttribute("text-anchor", "middle");
    text.setAttribute("dominant-baseline", "middle");
    text.setAttribute("font-size", "6.2");
    text.setAttribute("font-weight", "600");
    text.setAttribute("fill", "rgba(233,238,247,.92)");
    nums.appendChild(text);
  }
}

/* ===== SMALL DIAL GRAPHICS ===== */
const subTicks = document.getElementById("subTicks");
const subNums  = document.getElementById("subNums");

const SCX = 100, SCY = 75;
const S_OUTER_R = 15;
const S_TICK_W = 0.45;
const S_LEN = 3.8;
const S_LEN_MAJOR = 5.2;
const S_TEXT_R = S_OUTER_R - 7;

for(let i=0; i<10; i++){
  const ang = -90 + i * 36;
  const L = (i === 0 || i === 5) ? S_LEN_MAJOR : S_LEN;

  const p1 = polar(SCX, SCY, S_OUTER_R, ang);
  const p2 = polar(SCX, SCY, S_OUTER_R - L, ang);

  const line = document.createElementNS("http://www.w3.org/2000/svg","line");
  line.setAttribute("x1", p1.x.toFixed(3));
  line.setAttribute("y1", p1.y.toFixed(3));
  line.setAttribute("x2", p2.x.toFixed(3));
  line.setAttribute("y2", p2.y.toFixed(3));
  line.setAttribute("stroke", "rgba(233,238,247,.85)");
  line.setAttribute("stroke-width", S_TICK_W);
  line.setAttribute("stroke-linecap", "round");
  subTicks.appendChild(line);

  const tp = polar(SCX, SCY, S_TEXT_R, ang);
  const text = document.createElementNS("http://www.w3.org/2000/svg","text");
  text.textContent = i;
  text.setAttribute("x", tp.x.toFixed(3));
  text.setAttribute("y", tp.y.toFixed(3));
  text.setAttribute("text-anchor", "middle");
  text.setAttribute("dominant-baseline", "middle");
  text.setAttribute("font-size", "4.2");
  text.setAttribute("font-weight", "600");
  text.setAttribute("fill", "rgba(233,238,247,.92)");
  subNums.appendChild(text);
}

/* ===== DIAL / OFFSET CALIBRATION LOGIC ===== */
const big = document.getElementById("big");
const small = document.getElementById("small");
const pos = document.getElementById("pos");
const mmText = document.getElementById("mm");

const toggleDigitalBtn = document.getElementById("toggleDigital");
const startTurningBtn = document.getElementById("startTurning");
const stopTurningBtn = document.getElementById("stopTurning");
const plusBtn = document.getElementById("plus");
const minusBtn = document.getElementById("minus");
const digital = document.getElementById("digital");

let baseHundredths = 401 + Math.floor(Math.random() * 99); // 4.01..4.99 mm
let currentHundredths = baseHundredths;

function setDisplay(hundredths){
  currentHundredths = hundredths;
  const mmValue = currentHundredths / 100.0;

  // Big needle: 1 revolution per 1.00 mm
  // Small needle: 1 revolution per 10.00 mm
  const bigRevs = mmValue;
  const smallRevs = mmValue / 10.0;

  big.setAttribute("transform", `rotate(${bigRevs * 360.0} 75 75)`);
  small.setAttribute("transform", `rotate(${smallRevs * 360.0} 100 75)`);

  mmText.textContent = mmValue.toFixed(2);
}

// Initial random position shown immediately
pos.value = String(baseHundredths);
setDisplay(baseHundredths);

/* ===== Bezel rotation only ===== */
const bezel = document.getElementById("bezel");
let bezelAngle = 0;
let hold = null;
const STEP_DEG = 0.36; // 0.1 division of large dial

function applyBezel(){
  bezel.setAttribute("transform", `rotate(${bezelAngle} 75 75)`);
}
function targetBezelAngle(){
  // align dial "0" to current big needle at the initial/base value
  return normalizeDeg((baseHundredths % 100) * 3.6);
}
function isOffsetAligned(){
  return angularDifference(bezelAngle, targetBezelAngle()) <= 0.20;
}
function nudge(dir){
  if(mechRunning) return; // keep offset fixed during turning
  bezelAngle = (bezelAngle + dir * STEP_DEG + 360.0) % 360.0;
  applyBezel();
  updateCalibrationState();
}
function startHold(dir){
  nudge(dir);
  stopHold();
  hold = setInterval(() => nudge(dir), 60);
}
function stopHold(){
  if(hold){
    clearInterval(hold);
    hold = null;
  }
}

plusBtn.addEventListener("pointerdown", e => { e.preventDefault(); startHold(+1); });
minusBtn.addEventListener("pointerdown", e => { e.preventDefault(); startHold(-1); });
["pointerup","pointerleave","pointercancel"].forEach(ev => {
  plusBtn.addEventListener(ev, stopHold);
  minusBtn.addEventListener(ev, stopHold);
});
window.addEventListener("pointerup", stopHold);

/* ===== Digital toggle ===== */
toggleDigitalBtn.addEventListener("click", () => {
  const hidden = digital.style.display === "" || digital.style.display === "none";
  digital.style.display = hidden ? "block" : "none";
});

/* Slider manual input allowed before turning only */
pos.addEventListener("input", () => {
  if(mechRunning) return;
  baseHundredths = Number(pos.value);
  setDisplay(baseHundredths);
  updateCalibrationState();
});

/* ===== Crank / rod / wear simulation ===== */
const deflAngleEl = document.getElementById("deflAngle");
const deflValueEl = document.getElementById("deflValue");
const bearingWearEl = document.getElementById("bearingWear");
const turnStatusEl = document.getElementById("turnStatus");

const crankLine = document.getElementById("crankLine");
const crankPin = document.getElementById("crankPin");
const rodLine = document.getElementById("rodLine");
const sliderBlock = document.getElementById("sliderBlock");

const MECH_CX = 120;
const MECH_CY = 325;
const CRANK_R = 56;
const ROD_L = 145;
const GUIDE_X = 120;
const SLIDER_W = 24;
const SLIDER_H = 26;

const REV_MS = 300000; // 5 minutes
const DISPLAY_START_DEG = 190;
const DISPLAY_END_DEG = 170;
// Angle convention: 0° at piston TDC / ΑΝΣ.

let mechRunning = false;
let mechProgress = 0;
let lastFrameTime = performance.now();
let turningElapsedMs = 0;

function updateMechanism(progress){
  // 0° is at piston TDC / ΑΝΣ.
  // In SVG coordinates, TDC is the crank pin at the top, so the drawing angle is crankAngle - 90°.
  // The measurement cycle starts at 190° and ends at 170° through 360°/0°.
  const crankDegTDC = normalizeDeg(DISPLAY_START_DEG + progress * 340.0);
  const theta = (crankDegTDC - 90.0) * Math.PI / 180.0;

  const pinX = MECH_CX + CRANK_R * Math.cos(theta);
  const pinY = MECH_CY + CRANK_R * Math.sin(theta);

  // vertical slider-crank kinematics (slider moves along x = GUIDE_X)
  const dx = pinX - GUIDE_X;
  const dy = Math.sqrt(Math.max(ROD_L * ROD_L - dx * dx, 0));
  const sliderY = pinY - dy;

  crankLine.setAttribute("x1", MECH_CX.toFixed(2));
  crankLine.setAttribute("y1", MECH_CY.toFixed(2));
  crankLine.setAttribute("x2", pinX.toFixed(2));
  crankLine.setAttribute("y2", pinY.toFixed(2));

  crankPin.setAttribute("cx", pinX.toFixed(2));
  crankPin.setAttribute("cy", pinY.toFixed(2));

  rodLine.setAttribute("x1", pinX.toFixed(2));
  rodLine.setAttribute("y1", pinY.toFixed(2));
  rodLine.setAttribute("x2", GUIDE_X.toFixed(2));
  rodLine.setAttribute("y2", sliderY.toFixed(2));

  sliderBlock.setAttribute("x", (GUIDE_X - SLIDER_W / 2).toFixed(2));
  sliderBlock.setAttribute("y", (sliderY - SLIDER_H / 2).toFixed(2));

  // Displayed crank angle uses the same convention: 0° = ΑΝΣ/TDC.
  deflAngleEl.textContent = "Crank angle: " + crankDegTDC.toFixed(1) + "°";

  // Smooth ramp so there is NO abrupt jump at the beginning.
  // The indications start from zero and gradually build up.
  const ramp = smoothstep01(turningElapsedMs / 20000); // ~20 s smooth build-up

  // Base waveform shifted so that it is exactly zero at progress = 0.
  const wave1 = 0.090 * (Math.sin(2 * Math.PI * progress - 0.9) - Math.sin(-0.9));
  const wave2 = 0.040 * (Math.sin(4 * Math.PI * progress + 0.45) - Math.sin(0.45));
  const drift = 0.018 * progress;

  const deflection = ramp * (wave1 + wave2 + drift);

  // Wear index also starts from zero and changes gradually.
  const wearRaw =
    0.55
    + 0.26 * Math.sin(2 * Math.PI * progress - 0.4)
    + 0.09 * Math.sin(6 * Math.PI * progress + 0.2)
    - (0.55 + 0.26 * Math.sin(-0.4) + 0.09 * Math.sin(0.2));

  const wearIndex = clamp(ramp * Math.abs(wearRaw) * 1.6, 0, 1.00);

  deflValueEl.textContent =
    "Deflection: " + (deflection >= 0 ? "+" : "") + deflection.toFixed(3) + " mm";

  bearingWearEl.textContent =
    "Main Bearing Wear Index: " + wearIndex.toFixed(2);

  // During turning, show the changing indications on the micrometer.
  // Because the dial has been offset-aligned, these start from zero indication
  // and then vary smoothly around that zero.
  if(mechRunning){
    const simHundredths = clamp(baseHundredths + deflection * 100.0, 0, 1000);
    setDisplay(simHundredths);
    pos.value = String(Math.round(simHundredths));
  }
}

function updateCalibrationState(){
  if(mechRunning){
    startTurningBtn.disabled = true;
    stopTurningBtn.disabled = false;
    pos.disabled = true;
    plusBtn.disabled = true;
    minusBtn.disabled = true;
    turnStatusEl.textContent = "Status: Turning";
    return;
  }

  stopTurningBtn.disabled = true;
  pos.disabled = false;
  plusBtn.disabled = false;
  minusBtn.disabled = false;

  if(isOffsetAligned()){
    startTurningBtn.disabled = false;
    turnStatusEl.textContent = "Status: Ready - offset aligned";
  }else{
    startTurningBtn.disabled = true;
    turnStatusEl.textContent = "Status: Set offset with + / −";
  }
}

function animateMechanism(now){
  const dt = now - lastFrameTime;
  lastFrameTime = now;

  if(mechRunning){
    // One measurement cycle in 5 minutes.
    turningElapsedMs += dt;
    mechProgress = (turningElapsedMs / REV_MS) % 1.0;
  }

  updateMechanism(mechProgress);
  requestAnimationFrame(animateMechanism);
}

startTurningBtn.addEventListener("click", () => {
  if(!isOffsetAligned()) return;
  mechProgress = 0;
  turningElapsedMs = 0;
  mechRunning = true;
  updateMechanism(0);
  updateCalibrationState();
});

stopTurningBtn.addEventListener("click", () => {
  mechRunning = false;
  updateCalibrationState();
});

// initialize
applyBezel();
turningElapsedMs = 0;
updateMechanism(0);
updateCalibrationState();
requestAnimationFrame(animateMechanism);
</script>


<!-- PWA service worker registration -->
<script>
if ("serviceWorker" in navigator) {
  window.addEventListener("load", () => {
    navigator.serviceWorker.register("./sw.js").catch(err => {
      console.warn("Service worker registration failed:", err);
    });
  });
}
</script>

</body>
</html>
