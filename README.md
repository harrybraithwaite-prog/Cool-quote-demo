# Cool-quote-demo
Cool quote 
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Cool Quote – Instant Air Conditioning Quote</title>
<meta name="description" content="At Cool Quote we work with local fitters to give you an instant price for your air conditioning supply and installation.">
<link rel="manifest" href="manifest.json">
<link rel="stylesheet" href="styles.css">
<script defer src="script.js"></script>
</head>
<body>
<header>
  <div class="brand">
    <img src="assets/logo.svg" alt="Cool Quote logo">
    <strong>Cool Quote</strong>
  </div>
  <nav>
    <a href="index.html">Home</a>
    <a href="faq.html">FAQ</a>
    <a href="terms.html">Terms</a>
    <a href="privacy.html">Privacy</a>
  </nav>
</header>

<section class="hero container">
  <div>
    <h1>Air Conditioning Quotes in Minutes</h1>
    <p>At Cool Quote we work with local fitters to give you an instant price for your air conditioning supply and installation.</p>
    <a class="cta" href="#quote">Get an instant quote</a>
    <div class="brand-strip">
      <span class="small">Starting with:</span>
      <img class="logo-inline" src="assets/wb.svg" alt="Worcester Bosch">
      <span class="small">More brands later.</span>
    </div>
  </div>
  <div class="card">
    <h2>What you’ll get</h2>
    <ul>
      <li>Instant pricing incl. installation</li>
      <li>30-day quote validity</li>
      <li>Deposit now (£150 + VAT), balance after completion</li>
      <li>Local, vetted fitters only</li>
    </ul>
    <span class="badge">Install as App (PWA)</span>
  </div>
</section>

<section id="quote" class="container card">
  <h2>Quote wizard</h2>
  <div class="progress" id="steps"></div>
  <form id="quoteForm" onsubmit="return false;">
    <div id="stepContainer"></div>
    <div style="display:flex;gap:8px;margin-top:12px;">
      <button id="prevBtn" class="secondary" type="button">Back</button>
      <button id="nextBtn" type="button">Next</button>
    </div>
  </form>

  <div id="summary" class="hidden">
    <h3>Your estimate</h3>
    <div id="btuLine" class="small"></div>
    <p class="price" id="totalPrice">£0</p>
    <ul id="breakdown"></ul>
    <div class="notice">Deposit: £150 + VAT (Cool Quote consignment fee). Balance after completion is paid to your fitter.</div>
    <div class="card success">
      <strong>Reference:</strong> <span id="refNo"></span><br>
      We’ll be in touch shortly to book in a time to come and complete the job.
      <div class="small" id="validUntil"></div>
    </div>

    <h4>Booking details</h4>
    <div class="grid two">
      <div>
        <label>Full name</label>
        <input id="name" required>
      </div>
      <div>
        <label>Email</label>
        <input id="email" type="email" required>
      </div>
      <div>
        <label>Phone</label>
        <input id="phone" required>
      </div>
      <div>
        <label>Installation address</label>
        <input id="address" required>
      </div>
    </div>
    <button type="button" id="confirmBtn">Confirm (demo)</button>
    <div id="confirmNote" class="hidden success" style="margin-top:10px;padding:10px;border-radius:10px;">
      Thank you. A local fitter will be in touch shortly.
    </div>
  </div>
</section>

<section class="container">
  <div class="card">
    <h3>Track your job</h3>
    <div class="progress">
      <div class="step active">Quote Created</div>
      <div class="step">Consignment Fee Paid</div>
      <div class="step">Fitter Assigned</div>
      <div class="step">Site Info Confirmed</div>
      <div class="step">Installation Booked</div>
    </div>
    <p class="small">You’ll receive email updates as your job progresses.</p>
  </div>
</section>

<footer class="container">
  <div>© <span id="year"></span> Cool Quote. All rights reserved.</div>
  <div><a href="terms.html">Terms</a> · <a href="privacy.html">Privacy</a> · <a href="faq.html">FAQ</a></div>
</footer>

<div id="cookie" class="cookie hidden">
  <div><strong>Cookies:</strong> We use cookies to improve your experience. <a href="privacy.html">Learn more</a>.</div>
  <div>
    <button id="cookieAccept">Accept</button>
  </div>
</div>

<script>
  if('serviceWorker' in navigator){navigator.serviceWorker.register('sw.js');}
</script>
</body>
</html>
/ (repo root)
├─ index.html
├─ styles.css
├─ script.js
├─ manifest.json
├─ sw.js
├─ terms.html
├─ privacy.html
├─ faq.html
├─ fitters.html
└─ assets/
   ├─ logo.svg
   └─ wb.svg
   :root{
  --blue-900:#0b2e5c;
  --blue-800:#123a73;
  --blue-700:#1e3a8a;
  --blue-500:#3b82f6;
  --blue-100:#e0f2fe;
  --gray-25:#fafafa;
  --gray-100:#f3f4f6;
  --gray-200:#e5e7eb;
  --gray-600:#4b5563;
  --green-600:#059669;
  --amber-600:#d97706;
  --red-600:#dc2626;
}
*{box-sizing:border-box}
html,body{margin:0;padding:0;font-family:system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;color:#0b2239;background:#fff}
a{color:var(--blue-700);text-decoration:none}
header{display:flex;align-items:center;justify-content:space-between;padding:14px 18px;border-bottom:1px solid #eee;position:sticky;top:0;background:#fff;z-index:10}
.brand{display:flex;align-items:center;gap:12px}
.brand img{height:38px}
nav a{margin:0 10px;font-weight:600}
.container{max-width:1080px;margin:0 auto;padding:18px}
.hero{display:grid;grid-template-columns:1fr;gap:18px;padding:28px 18px;background:linear-gradient(180deg,#f0f7ff,#ffffff)}
.hero h1{font-size:32px;margin:0;color:var(--blue-900)}
.hero p{margin:8px 0 16px;color:#223}
.cta{display:inline-block;background:var(--blue-700);color:#fff;padding:12px 16px;border-radius:10px;font-weight:700}
.card{background:#fff;border:1px solid #eee;border-radius:12px;padding:16px;margin:12px 0}
.grid{display:grid;gap:12px}
.grid.two{grid-template-columns:1fr 1fr}
.grid.three{grid-template-columns:repeat(3,1fr)}
label{display:block;margin:8px 0 4px;font-weight:600}
input[type="text"],input[type="number"],input[type="email"],select{width:100%;padding:10px;border:1px solid #ddd;border-radius:10px}
button{padding:12px 16px;border:0;border-radius:10px;background:var(--blue-700);color:#fff;font-weight:700;cursor:pointer}
button.secondary{background:#e5e7eb;color:#111}
.progress{display:flex;gap:8px;flex-wrap:wrap;margin:8px 0}
.step{padding:6px 10px;border-radius:999px;border:1px solid #ddd}
.step.active{background:var(--blue-100);border-color:var(--blue-500);color:var(--blue-700)}
.notice{background:#fff7ed;border:1px solid #fed7aa;padding:10px;border-radius:8px;color:#92400e;margin:10px 0}
.success{background:#ecfdf5;border:1px solid #a7f3d0;color:#065f46}
.error{background:#fef2f2;border:1px solid #fecaca;color:#991b1b}
.small{font-size:12px;color:#555}
.price{font-size:26px;font-weight:800;color:var(--blue-900)}
.brand-strip{display:flex;align-items:center;gap:12px;flex-wrap:wrap;margin-top:10px}
img.logo-inline{height:28px}
footer{margin-top:40px;padding:20px;border-top:1px solid #eee;font-size:14px;color:#445}
.badge{display:inline-block;background:var(--blue-100);color:var(--blue-700);padding:4px 8px;border-radius:999px;font-size:12px;font-weight:700}
.cookie{position:fixed;bottom:14px;left:14px;right:14px;background:#fff;border:1px solid #ddd;border-radius:12px;padding:12px;box-shadow:0 10px 30px rgba(0,0,0,.08);display:flex;align-items:center;justify-content:space-between;gap:12px}
.hidden{display:none}
@media(min-width:900px){
  .hero{grid-template-columns:1.1fr .9fr;align-items:center}
  .hero h1{font-size:38px}
}
const steps = [
  {key:'houseType', label:'House type', type:'select', options:[
    {v:'detached', t:'Detached'},{v:'semi', t:'Semi-detached'},{v:'terraced', t:'Terraced'},{v:'flat', t:'Flat'}
  ]},
  {key:'room', label:'Room it’s going in', type:'select', options:[
    {v:'bedroom', t:'Bedroom'},{v:'living', t:'Living room'},{v:'office', t:'Home office'},{v:'other', t:'Other'}
  ]},
  {key:'floor', label:'Floor the room is in', type:'select', options:[
    {v:'ground', t:'Ground'},{v:'first', t:'First'},{v:'second_plus', t:'Second or above'}
  ]},
  {key:'upperConfirm', label:'If above first floor, confirm you\'re happy to upload photos after booking for fitter approval', type:'confirm', depends:(data)=>data.floor==='second_plus'},
  {key:'roomSize', label:'Room size', type:'select', options:[
    {v:'small', t:'Small (0–150 sq ft)'},{v:'medium', t:'Medium (151–300 sq ft)'},{v:'large', t:'Large (301–500 sq ft)'},{v:'xl', t:'Extra Large (500+ sq ft)'}
  ]},
  {key:'sun', label:'How much sunlight does the room get?', type:'select', options:[
    {v:'low', t:'Low'},{v:'med', t:'Medium'},{v:'high', t:'High (faces sun most of day)'}
  ]},
  {key:'wallType', label:'Type of wall the unit will be on', type:'select', options:[
    {v:'external', t:'External wall (direct to outside)'},{v:'internal', t:'Internal wall (pipework required)'}
  ]},
  {key:'height', label:'Install height', type:'select', options:[
    {v:'floor', t:'Floor level'},{v:'mid', t:'Mid wall'},{v:'high', t:'High wall'}
  ]},
  {key:'distanceUnits', label:'Distance between indoor and outdoor unit (metres)', type:'select', options:[
    {v:'lt3', t:'Under 3m'},{v:'3to7', t:'3–7m'},{v:'gt7', t:'Over 7m'}
  ]},
  {key:'neighbour', label:'Do you have at least 2.5m clearance to your nearest neighbour?', type:'select', options:[
    {v:'yes', t:'Yes'},{v:'no', t:'No'}
  ]},
  {key:'fuse', label:'Approximate distance from fuse board to install location', type:'select', options:[
    {v:'lt5', t:'Less than 5m'},{v:'5to10', t:'5–10m'},{v:'gt10', t:'Over 10m'},{v:'unsure', t:'Not sure'}
  ]},
  {key:'fusePhoto', label:'Please upload a photo of the route from fuse board (demo only, not uploaded)', type:'file', depends:(data)=>data.fuse==='gt10' || data.fuse==='unsure'},
];

const data = {};
let current = 0;

const stepsEl = document.getElementById('steps');
const stepContainer = document.getElementById('stepContainer');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');
const summary = document.getElementById('summary');

function renderSteps(){
  stepsEl.innerHTML='';
  visibleSteps().forEach((s,i)=>{
    const el = document.createElement('div');
    el.className='step'+(i===current?' active':'');
    el.textContent = s.label;
    stepsEl.appendChild(el);
  });
}

function renderCurrent(){
  const s = visibleSteps()[current];
  stepContainer.innerHTML='';
  const wrap = document.createElement('div');
  wrap.className='grid';
  const label = document.createElement('label');
  label.textContent = s.label;
  wrap.appendChild(label);

  if(s.type==='select'){
    const sel = document.createElement('select');
    sel.id = s.key;
    s.options.forEach(o=>{
      const opt = document.createElement('option');
      opt.value = o.v; opt.textContent = o.t;
      sel.appendChild(opt);
    });
    if(data[s.key]) sel.value = data[s.key];
    sel.addEventListener('change',()=> data[s.key]=sel.value );
    wrap.appendChild(sel);
  } else if(s.type==='confirm'){
    const note = document.createElement('div');
    note.className='notice';
    note.innerHTML = "Because your room is above first floor, after booking you’ll need to upload photos for the fitter to confirm there’s no extra cost.";
    wrap.appendChild(note);
    const sel = document.createElement('select');
    sel.id = s.key;
    sel.innerHTML = '<option value="yes">I\'m happy to provide photos after booking</option><option value="no">I\'m not happy to provide photos now</option>';
    if(data[s.key]) sel.value = data[s.key];
    sel.addEventListener('change',()=> data[s.key]=sel.value );
    wrap.appendChild(sel);
  } else if(s.type==='file'){
    const inp = document.createElement('input');
    inp.type='file';
    inp.id=s.key;
    wrap.appendChild(inp);
  }

  stepContainer.appendChild(wrap);
}

function visibleSteps(){
  return steps.filter(s=>!s.depends || s.depends(data));
}

function showSummary(){
  document.getElementById('quoteForm').classList.add('hidden');
  summary.classList.remove('hidden');

  // BTU calculator (simple baseline by size + sunlight)
  let btu = 6000;
  if(data.roomSize==='medium') btu += 3000;
  if(data.roomSize==='large') btu += 6000;
  if(data.roomSize==='xl') btu += 9000;
  if(data.sun==='med') btu += 1000;
  if(data.sun==='high') btu += 2000;

  document.getElementById('btuLine').textContent = `Estimated requirement: ~${btu.toLocaleString()} BTU`;

  // Product price based on btu bands
  let product = 900;
  if(btu>8000) product = 1100;
  if(btu>12000) product = 1400;
  if(btu>18000) product = 1800;

  // Installation (single line)
  let install = 700;
  if(data.wallType==='internal') install += 150;     // pipework
  if(data.height==='mid') install += 75;
  if(data.height==='high') install += 150;
  if(data.distanceUnits==='3to7') install += 120;
  if(data.distanceUnits==='gt7') install += 250;
  if(data.houseType==='detached') install += 120;
  if(data.houseType==='semi') install += 60;
  // Fuse board distance (silent)
  if(data.fuse==='5to10') install += 120;
  if(data.fuse==='gt10' || data.fuse==='unsure') install += 240;

  const consignment = 150;
  const vatRate = 0.20;

  const subtotal = product + install + consignment;
  const vat = (product + install) * vatRate; // VAT on product+install (adjust later if needed)
  const total = subtotal + vat;

  document.getElementById('totalPrice').textContent = `£${total.toFixed(2)}`;

  const breakdown = document.getElementById('breakdown');
  breakdown.innerHTML = '';
  breakdown.appendChild(li(`Product: £${product.toFixed(2)}`));
  breakdown.appendChild(li(`Installation charges: £${install.toFixed(2)}`));
  breakdown.appendChild(li(`Cool Quote consignment fee: £${consignment.toFixed(2)} + VAT`));
  breakdown.appendChild(li(`VAT (on product + installation): £${vat.toFixed(2)}`));

  // Reference number CQ-0000001 style
  const n = Math.floor(Math.random()*9999999)+1;
  const ref = `CQ-${String(n).padStart(7,'0')}`;
  document.getElementById('refNo').textContent = ref;

  // Valid until (30 days)
  const now = new Date();
  const valid = new Date(now.getTime() + 30*24*60*60*1000);
  document.getElementById('validUntil').textContent = `Valid until: ${valid.toDateString()}`;

  document.getElementById('confirmBtn').onclick = () => {
    document.getElementById('confirmNote').classList.remove('hidden');
  };
}

function li(text){ const el=document.createElement('li'); el.textContent=text; return el; }

prevBtn.addEventListener('click', ()=>{
  if(current>0){ current--; renderSteps(); renderCurrent(); }
});

nextBtn.addEventListener('click', ()=>{
  const s = visibleSteps()[current];
  if(s.type==='select'){
    const v = document.getElementById(s.key).value;
    data[s.key]=v;
  } else if(s.type==='confirm'){
    const v = document.getElementById(s.key).value;
    data[s.key]=v;
    if(v==='no'){ window.location.href='fitters.html'; return; }
  } else if(s.type==='file'){
    data[s.key]='uploaded';
  }

  if(s.key==='neighbour' && data.neighbour==='no'){
    stepContainer.innerHTML = '<div class="error">A minimum 2.5m clearance to the nearest neighbour is required. Please contact a local fitter for alternatives.</div>';
    nextBtn.disabled=true;
    return;
  }

  const vs = visibleSteps();
  if(current < vs.length - 1){
    current++; renderSteps(); renderCurrent();
  } else {
    showSummary();
  }
});

function init(){
  document.getElementById('year').textContent = new Date().getFullYear();
  const cookie = document.getElementById('cookie');
  if(!localStorage.getItem('cq_cookie')) cookie.classList.remove('hidden');
  document.getElementById('cookieAccept').onclick = ()=>{ localStorage.setItem('cq_cookie','1'); cookie.classList.add('hidden'); };
  renderSteps(); renderCurrent();
}
document.addEventListener('DOMContentLoaded', init);
{
  "name": "Cool Quote",
  "short_name": "CoolQuote",
  "start_url": "index.html",
  "display": "standalone",
  "background_color": "#ffffff",
  "theme_color": "#1e3a8a",
  "icons": []
}
self.addEventListener('install', e=>{ self.skipWaiting(); });
self.addEventListener('activate', e=>{});
self.addEventListener('fetch', e=>{});
<!doctype html>
<html lang="en"><head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1">
<title>FAQ – Cool Quote</title>
<link rel="stylesheet" href="styles.css">
</head><body>
<header>
  <div class="brand"><img src="assets/logo.svg" alt="Cool Quote logo"><strong>Cool Quote</strong></div>
  <nav><a href="index.html">Home</a><a href="faq.html">FAQ</a><a href="terms.html">Terms</a><a href="privacy.html">Privacy</a></nav>
</header>
<section class="container">
  <h1>FAQ</h1>
  <h3>How fast is the quote?</h3><p>Instant, based on your answers.</p>
  <h3>Who does the installation?</h3><p>Independent, vetted local fitters. Cool Quote facilitates the connection.</p>
  <h3>Is payment secure?</h3><p>Yes. Payments are processed by Stripe (test mode in this demo).</p>
</section>
<footer class="container"><div>© <span id="year"></span> Cool Quote.</div></footer>
<script>document.getElementById('year').textContent = new Date().getFullYear();</script>
</body></html>
<!doctype html>
<html lang="en"><head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1">
<title>Terms & Conditions – Cool Quote</title>
<link rel="stylesheet" href="styles.css">
</head><body>
<header>
  <div class="brand"><img src="assets/logo.svg" alt="Cool Quote logo"><strong>Cool Quote</strong></div>
  <nav><a href="index.html">Home</a><a href="faq.html">FAQ</a><a href="terms.html">Terms</a><a href="privacy.html">Privacy</a></nav>
</header>
<section class="container">
  <h1>Terms & Conditions</h1>
  <p><strong>Cool Quote is a facilitator.</strong> We do not supply or install products. We connect you with independent, qualified local fitters who carry out the installation. Any installation contract is between you and the fitter.</p>
  <h3>Quotes</h3>
  <ul>
    <li>Quotes are indicative and based on information you provide.</li>
    <li>Quotes are valid for 30 days unless stated otherwise.</li>
    <li>Further site information or photos may be requested by the fitter.</li>
  </ul>
  <h3>Payments</h3>
  <ul>
    <li>The consignment fee/deposit (£150 + VAT) is payable to Cool Quote at acceptance.</li>
    <li>Remaining balance is paid through the platform to the fitter after job completion.</li>
  </ul>
  <h3>Liability</h3>
  <p>Cool Quote is not responsible for the works carried out by the fitter. Responsibility for workmanship, warranties and compliance sits with the fitter.</p>
</section>
<footer class="container"><div>© <span id="year"></span> Cool Quote.</div></footer>
<script>document.getElementById('year').textContent = new Date().getFullYear();</script>
</body></html>
<!doctype html>
<html lang="en"><head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1">
<title>Privacy Policy – Cool Quote</title>
<link rel="stylesheet" href="styles.css">
</head><body>
<header>
  <div class="brand"><img src="assets/logo.svg" alt="Cool Quote logo"><strong>Cool Quote</strong></div>
  <nav><a href="index.html">Home</a><a href="faq.html">FAQ</a><a href="terms.html">Terms</a><a href="privacy.html">Privacy</a></nav>
</header>
<section class="container">
  <h1>Privacy Policy</h1>
  <p>We use your information to provide quotes, manage bookings, and connect you with local fitters. We do not sell your data. We use cookies to improve your experience. Payments are processed securely by Stripe (test mode for demo).</p>
  <p>You can request access, correction, or deletion of your data at any time by contacting us.</p>
</section>
<footer class="container"><div>© <span id="year"></span> Cool Quote.</div></footer>
<script>document.getElementById('year').textContent = new Date().getFullYear();</script>
</body></html>
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1">
<title>Cool Quote – Local Fitters</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<header>
  <div class="brand">
    <img src="assets/logo.svg" alt="Cool Quote logo">
    <strong>Cool Quote</strong>
  </div>
  <nav>
    <a href="index.html">Home</a>
    <a href="faq.html">FAQ</a>
    <a href="terms.html">Terms</a>
    <a href="privacy.html">Privacy</a>
  </nav>
</header>
<section class="container">
  <h1>Contact a local fitter</h1>
  <p>If you can’t provide photos for upper-floor installations right now, please contact one of our trusted local fitters below to receive a full quote directly.</p>
  <div class="grid two">
    <div class="card">
      <h3>AC Specialists North</h3>
      <div class="small">Leeds & Yorkshire</div>
      <div class="small">Phone: 01234 567890</div>
      <div class="small">Email: north@example.com</div>
    </div>
    <div class="card">
      <h3>SouthCool Installations</h3>
      <div class="small">London & South East</div>
      <div class="small">Phone: 0207 123 4567</div>
      <div class="small">Email: south@example.com</div>
    </div>
  </div>
</section>
<footer class="container">
  <div>© <span id="year"></span> Cool Quote.</div>
</footer>
<script>
  document.getElementById('year').textContent = new Date().getFullYear();
</script>
</body>
</html>
<svg xmlns="http://www.w3.org/2000/svg" width="220" height="60" viewBox="0 0 220 60">
  <defs><linearGradient id="g" x1="0" y1="0" x2="1" y2="1">
    <stop offset="0" stop-color="#0b2e5c"/><stop offset="1" stop-color="#3b82f6"/></linearGradient></defs>
  <rect width="220" height="60" rx="8" fill="url(#g)"/>
  <g transform="translate(10,10)">
    <rect x="0" y="0" width="46" height="26" rx="4" fill="#e0f2fe" stroke="#0b2e5c"/>
    <circle cx="12" cy="13" r="6" fill="#93c5fd"/>
    <path d="M6,24 h34" stroke="#0b2e5c" stroke-width="2"/>
    <text x="58" y="19" font-family="Arial" font-weight="700" font-size="18" fill="#ffffff">Cool Quote</text>
  </g>
</svg>
<svg xmlns="http://www.w3.org/2000/svg" width="200" height="48" viewBox="0 0 200 48">
  <rect width="200" height="48" fill="#ffffff"/>
  <rect x="2" y="2" width="196" height="44" rx="6" fill="#dbeafe" stroke="#1e3a8a"/>
  <text x="100" y="30" text-anchor="middle" font-family="Arial" font-size="14" fill="#1e3a8a">Worcester Bosch (placeholder)</text>
</svg>
