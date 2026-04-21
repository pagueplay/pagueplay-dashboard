[rec_pague_play (4)21042026.txt](https://github.com/user-attachments/files/26948483/rec_pague_play.4.21042026.txt)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>PaguePay · Repasse Empresa · 2026</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700;800;900&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{
  --bg:#F7F8FB;
  --surface:#FFFFFF;
  --surface2:#F0F2F7;
  --bdr:#E2E6EF;
  --bdr2:#C8D0E0;
  --tx:#1A1F2E;
  --tx2:#5A6478;
  --tx3:#9BA3B5;
  --lime:#65A30D;
  --lime-l:#ECFCCB;
  --lime-m:#A3E635;
  --lime-d:#3F6212;
  --blue:#2563EB;
  --blue-l:#DBEAFE;
  --blue-m:#60A5FA;
  --blue-d:#1E3A8A;
  --amber:#D97706;
  --amber-l:#FEF3C7;
  --purple:#7C3AED;
  --purple-l:#EDE9FE;
  --r:10px;--r2:14px;--r3:20px;--r4:26px;
  --sh:0 1px 3px rgba(0,0,0,.06),0 1px 2px rgba(0,0,0,.04);
  --sh2:0 4px 12px rgba(0,0,0,.08),0 2px 4px rgba(0,0,0,.04);
}
*{scrollbar-width:thin;scrollbar-color:var(--bdr) transparent}
::-webkit-scrollbar{width:4px;height:4px}
::-webkit-scrollbar-thumb{background:var(--bdr2);border-radius:99px}
html{scroll-behavior:smooth}
body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--tx);min-height:100vh;overflow-x:hidden}

/* NAV */
nav{position:sticky;top:0;z-index:100;height:60px;
  background:rgba(255,255,255,.95);backdrop-filter:blur(20px);
  border-bottom:1px solid var(--bdr);
  display:flex;align-items:center;justify-content:space-between;padding:0 28px;gap:16px;
  box-shadow:0 1px 0 var(--bdr),0 2px 8px rgba(0,0,0,.04)}
.nav-brand{display:flex;align-items:center;gap:12px;flex-shrink:0}
.nav-logo{width:36px;height:36px;background:linear-gradient(135deg,var(--lime),#84CC16);
  border-radius:10px;display:flex;align-items:center;justify-content:center;
  font-size:16px;box-shadow:0 2px 8px rgba(101,163,13,.35)}
.nav-title{font-size:15px;font-weight:800;color:var(--tx);letter-spacing:-.3px}
.nav-period{font-size:10px;color:var(--tx3);font-weight:500;letter-spacing:.5px;text-transform:uppercase;margin-top:1px}
.nav-btns{display:flex;gap:10px;align-items:center}
.nav-btn{display:flex;align-items:center;gap:6px;padding:7px 16px;
  border-radius:var(--r2);cursor:pointer;font-family:inherit;
  font-size:12px;font-weight:700;transition:all .2s;border:none;white-space:nowrap;text-decoration:none}
.btn-import{background:linear-gradient(135deg,var(--lime),#84CC16);color:#fff;box-shadow:0 2px 8px rgba(101,163,13,.3)}
.btn-import:hover{box-shadow:0 4px 14px rgba(101,163,13,.4);transform:translateY(-1px)}
.btn-geral{background:var(--surface);border:1.5px solid var(--bdr2)!important;color:var(--tx2)}
.btn-geral:hover{border-color:var(--blue)!important;color:var(--blue);background:var(--blue-l)}
.nav-sep{width:1px;height:26px;background:var(--bdr)}
#fi-pp{display:none}

main{max-width:1400px;margin:0 auto;padding:28px 24px 80px}

/* HERO BANNER */
.hero-banner{
  background:linear-gradient(135deg,#0F2557 0%,#1B3A8A 40%,#2563EB 80%,#3B82F6 100%);
  border-radius:var(--r4);padding:36px 40px;margin-bottom:28px;
  position:relative;overflow:hidden;box-shadow:0 8px 32px rgba(37,99,235,.25)}
.hero-banner::before{content:'';position:absolute;top:-60px;right:-60px;
  width:280px;height:280px;border-radius:50%;
  background:radial-gradient(circle,rgba(163,230,53,.15),transparent 70%);pointer-events:none}
.hero-banner::after{content:'';position:absolute;bottom:-40px;left:180px;
  width:200px;height:200px;border-radius:50%;
  background:radial-gradient(circle,rgba(96,165,250,.12),transparent 70%);pointer-events:none}
.hero-eyebrow{font-size:10px;font-weight:700;letter-spacing:2.5px;text-transform:uppercase;
  color:rgba(163,230,53,.8);margin-bottom:10px;display:flex;align-items:center;gap:8px}
.hero-eyebrow::before{content:'';width:24px;height:2px;background:rgba(163,230,53,.6);border-radius:99px}
.hero-amount{font-size:56px;font-weight:900;color:#fff;line-height:1;letter-spacing:-2.5px;margin-bottom:10px}
.hero-amount sup{font-size:22px;opacity:.65;vertical-align:top;margin-top:12px;font-weight:600}
.hero-meta{display:flex;gap:20px;flex-wrap:wrap;font-size:12px;color:rgba(255,255,255,.65);font-weight:500}
.hero-meta strong{color:rgba(163,230,53,.9)}
.hero-kpis{display:grid;grid-template-columns:repeat(4,1fr);gap:14px;margin-top:28px}
@media(max-width:880px){.hero-kpis{grid-template-columns:1fr 1fr}}
@media(max-width:480px){.hero-kpis{grid-template-columns:1fr}}

.hkpi{background:rgba(255,255,255,.08);border:1px solid rgba(255,255,255,.12);
  border-radius:var(--r2);padding:16px 18px;backdrop-filter:blur(4px);transition:all .2s}
.hkpi:hover{background:rgba(255,255,255,.13);border-color:rgba(163,230,53,.3)}
.hkpi-lbl{font-size:9px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;
  color:rgba(255,255,255,.45);margin-bottom:8px}
.hkpi-val{font-family:'DM Mono',monospace;font-size:20px;font-weight:500;color:#fff;line-height:1}
.hkpi-sub{font-size:10px;color:rgba(255,255,255,.45);margin-top:5px}
.hkpi-bar{height:2px;background:rgba(255,255,255,.1);border-radius:99px;margin-top:8px;overflow:hidden}
.hkpi-fill{height:100%;border-radius:99px;background:linear-gradient(90deg,var(--lime-m),#84CC16)}

/* MÊS CARDS */
.month-row{display:grid;grid-template-columns:repeat(4,1fr);gap:14px;margin-bottom:26px}
@media(max-width:900px){.month-row{grid-template-columns:1fr 1fr}}
@media(max-width:500px){.month-row{grid-template-columns:1fr}}

.mcard{background:var(--surface);border:1.5px solid var(--bdr);border-radius:var(--r3);
  padding:20px 22px;box-shadow:var(--sh);transition:all .22s;position:relative;overflow:hidden}
.mcard:hover{box-shadow:var(--sh2);border-color:var(--bdr2);transform:translateY(-2px)}
.mcard::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;border-radius:var(--r3) var(--r3) 0 0}
.mcard-jan::before{background:linear-gradient(90deg,#60A5FA,#3B82F6)}
.mcard-fev::before{background:linear-gradient(90deg,#A78BFA,#7C3AED)}
.mcard-mar::before{background:linear-gradient(90deg,#34D399,#059669)}
.mcard-abr::before{background:linear-gradient(90deg,var(--lime-m),var(--lime))}
.mcard-head{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:12px}
.mcard-title{font-size:12px;font-weight:700;color:var(--tx2);text-transform:uppercase;letter-spacing:.8px}
.mcard-badge{font-size:10px;font-weight:600;background:var(--surface2);color:var(--tx3);
  border-radius:99px;padding:3px 10px;border:1px solid var(--bdr)}
.mcard-pp{font-family:'DM Mono',monospace;font-size:26px;font-weight:500;line-height:1;margin-bottom:6px}
.mcard-rec{font-size:11px;color:var(--tx3);font-weight:500;margin-bottom:14px}
.mcard-stat{display:flex;gap:14px}
.mstat{display:flex;flex-direction:column;gap:2px}
.mstat-lbl{font-size:9px;font-weight:700;color:var(--tx3);text-transform:uppercase;letter-spacing:.8px}
.mstat-val{font-size:13px;font-weight:700;color:var(--tx2)}
.mcard-prog{height:4px;background:var(--surface2);border-radius:99px;overflow:hidden;margin-top:14px}
.mcard-prog-fill{height:100%;border-radius:99px;transition:width 1.2s cubic-bezier(.4,0,.2,1)}

/* SECTION HEADER */
.sec-hd{display:flex;align-items:center;justify-content:space-between;margin-bottom:16px;flex-wrap:wrap;gap:10px}
.sec-title{font-size:16px;font-weight:800;color:var(--tx);letter-spacing:-.3px}
.sec-sub{font-size:12px;color:var(--tx3);font-weight:500;margin-top:2px}

/* TABS */
.tabs{display:flex;gap:4px;background:var(--surface2);border:1px solid var(--bdr);
  border-radius:var(--r2);padding:4px;margin-bottom:22px;flex-wrap:wrap}
.tab{flex:1;padding:9px 8px;border-radius:var(--r);border:none;cursor:pointer;
  font-family:inherit;font-size:12px;font-weight:600;color:var(--tx3);
  background:transparent;transition:all .2s;white-space:nowrap;min-width:80px;text-align:center}
.tab.active{background:var(--surface);color:var(--blue);box-shadow:var(--sh);font-weight:700}
.tab:hover:not(.active){color:var(--tx2);background:rgba(255,255,255,.6)}

.panel{display:none;animation:slideUp .26s both}
.panel.active{display:block}
@keyframes slideUp{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:none}}

/* CARD */
.card{background:var(--surface);border:1.5px solid var(--bdr);border-radius:var(--r3);
  padding:22px 24px;margin-bottom:18px;box-shadow:var(--sh)}
.chart-box{position:relative;width:100%}

/* PILLS */
.pill-row{display:flex;gap:6px;flex-wrap:wrap;margin-bottom:16px;align-items:center}
.pill-lbl{font-size:10px;font-weight:700;letter-spacing:1px;text-transform:uppercase;color:var(--tx3);margin-right:4px}
.pill{padding:5px 14px;border-radius:99px;border:1.5px solid var(--bdr);
  background:var(--surface);color:var(--tx2);font-family:inherit;
  font-size:11px;font-weight:600;cursor:pointer;transition:all .18s}
.pill.active{background:var(--blue-l);border-color:var(--blue-m);color:var(--blue);font-weight:700}
.pill:hover:not(.active){border-color:var(--bdr2);color:var(--tx)}

/* LEGEND */
.legend{display:flex;gap:14px;flex-wrap:wrap;margin-bottom:14px}
.leg{display:flex;align-items:center;gap:6px;font-size:11px;font-weight:600;color:var(--tx2)}
.leg-dot{width:8px;height:8px;border-radius:50%;flex-shrink:0}
.leg-line{width:20px;height:3px;border-radius:99px;flex-shrink:0}

/* TABLE */
.tbl-wrap{overflow-x:auto}
table{width:100%;border-collapse:collapse;font-size:12px;min-width:500px}
thead th{padding:9px 14px;font-size:9px;font-weight:700;letter-spacing:1.5px;
  text-transform:uppercase;color:var(--tx3);border-bottom:2px solid var(--bdr);text-align:left;white-space:nowrap;background:var(--surface2)}
thead th.tr{text-align:right}
thead th.tc{text-align:center}
tbody tr{border-bottom:1px solid var(--bdr);transition:background .12s}
tbody tr:hover{background:var(--surface2)}
tbody td{padding:9px 14px;vertical-align:middle}
td.key{font-weight:700;color:var(--tx)}
td.cn{text-align:center;font-family:'DM Mono',monospace;font-size:11px;color:var(--tx3)}
td.mo{font-family:'DM Mono',monospace;font-size:11px;text-align:right;color:var(--tx2)}
.c-lime{color:var(--lime)!important;font-weight:700}
.c-blue{color:var(--blue)!important}
.c-amber{color:var(--amber)!important}
.c-purple{color:var(--purple)!important}
tfoot td{padding:10px 14px;font-weight:800;font-size:12px;
  border-top:2px solid var(--bdr2);background:linear-gradient(90deg,var(--lime-l),var(--blue-l));color:var(--tx)}
tfoot td.mo{font-family:'DM Mono',monospace}

/* COREN TABLE */
.coren-badge{display:inline-flex;align-items:center;justify-content:center;
  width:32px;height:20px;border-radius:6px;font-size:10px;font-weight:800;letter-spacing:.5px}
.c-PI{background:#DBEAFE;color:#1D4ED8}
.c-MA{background:#D1FAE5;color:#065F46}
.c-CE{background:#FEF9C3;color:#92400E}
.c-MT{background:#EDE9FE;color:#5B21B6}
.c-RO{background:#FFE4E6;color:#9F1239}

/* IMPORT DROP */
.drop-area{border:2px dashed var(--bdr2);border-radius:var(--r3);
  padding:40px 24px;text-align:center;cursor:pointer;transition:all .2s;background:var(--surface2)}
.drop-area:hover,.drop-area.drag{border-color:var(--lime);background:var(--lime-l)}
.drop-icon{font-size:40px;margin-bottom:12px}
.drop-title{font-size:15px;font-weight:700;color:var(--tx);margin-bottom:4px}
.drop-sub{font-size:12px;color:var(--tx3)}
.prog-bar{height:4px;background:var(--bdr);border-radius:99px;overflow:hidden;margin-top:8px}
.prog-fill{height:100%;background:linear-gradient(90deg,var(--lime),#84CC16);border-radius:99px;width:0%;transition:width .4s}
.status-txt{font-size:12px;min-height:18px;font-weight:600;margin-top:6px;text-align:center}
.hint-box{background:var(--surface2);border:1px solid var(--bdr);border-radius:var(--r2);padding:12px 16px;font-size:11px;color:var(--tx2);line-height:1.9;margin-top:14px}
.hint-box strong{color:var(--tx)}

/* MODAL */
.modal-bg{position:fixed;inset:0;background:rgba(15,22,40,.55);backdrop-filter:blur(10px);
  z-index:500;display:none;align-items:center;justify-content:center;padding:16px}
.modal-bg.open{display:flex}
.modal{background:var(--surface);border:1.5px solid var(--bdr);border-radius:var(--r4);
  padding:30px;width:100%;max-width:480px;position:relative;max-height:90vh;overflow-y:auto;box-shadow:0 20px 60px rgba(0,0,0,.15)}
.modal-x{position:absolute;top:16px;right:16px;background:var(--surface2);border:none;
  color:var(--tx3);font-size:16px;cursor:pointer;padding:5px 9px;border-radius:8px;font-weight:700}
.modal-x:hover{background:var(--bdr);color:var(--tx)}
.modal-title{font-size:17px;font-weight:800;color:var(--tx);margin-bottom:5px;letter-spacing:-.3px}
.modal-sub{font-size:12px;color:var(--tx2);margin-bottom:20px;line-height:1.6}

/* EMPTY STATE */
.empty{text-align:center;padding:60px 24px;color:var(--tx3)}
.empty-icon{font-size:48px;margin-bottom:16px;opacity:.5}
.empty-title{font-size:15px;font-weight:700;color:var(--tx2);margin-bottom:6px}
.empty-sub{font-size:13px;line-height:1.6}

/* TOAST */
.toast{position:fixed;bottom:24px;right:24px;z-index:600;
  background:var(--tx);color:#fff;border-radius:var(--r2);
  padding:11px 18px;font-size:12px;font-weight:600;
  box-shadow:0 8px 32px rgba(0,0,0,.2);
  transform:translateY(70px);opacity:0;transition:all .3s cubic-bezier(.4,0,.2,1)}
.toast.show{transform:none;opacity:1}

/* BEST DAY CHIP */
.best-chip{display:inline-flex;align-items:center;gap:5px;background:var(--lime-l);
  border:1px solid rgba(101,163,13,.3);border-radius:99px;padding:3px 10px;
  font-size:10px;font-weight:700;color:var(--lime-d)}

@media(max-width:500px){main{padding:14px 12px 60px}.hero-amount{font-size:38px}}
</style>

  <script type="module">
    import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.0/firebase-app.js";
    import { getAnalytics } from "https://www.gstatic.com/firebasejs/11.6.0/firebase-analytics.js";
    const firebaseConfig={apiKey:"AIzaSyCxwgEvm-XB1BQfpVXfALn2GmaSFYmFEyk",authDomain:"pagueplay-70a8c.firebaseapp.com",projectId:"pagueplay-70a8c",storageBucket:"pagueplay-70a8c.firebasestorage.app",messagingSenderId:"710050568740",appId:"1:710050568740:web:ffc29d70161463484cd6b1",measurementId:"G-0H24XL39GG"};
    const app=initializeApp(firebaseConfig);
    const analytics=getAnalytics(app);
  </script>
</head>
<body>
<nav>
  <div class="nav-brand">
    <div class="nav-logo">💚</div>
    <div>
      <div class="nav-title">PaguePay · Repasse Empresa</div>
      <div class="nav-period">COFEN · COREN · 2026</div>
    </div>
  </div>
  <div class="nav-btns">
    <button class="nav-btn btn-import" onclick="openModal()">⬆ Importar XLS</button>
    <div class="nav-sep"></div>
    <a class="nav-btn btn-geral" href="rec_geral.html">← Recebimento Geral</a>
  </div>
  <input type="file" id="fi-pp" accept=".xls,.xlsx,.csv,.tsv,.txt">
</nav>

<main>

<!-- HERO -->
<div class="hero-banner">
  <div class="hero-eyebrow">PaguePay 24,96% · Repasse Empresa</div>
  <div class="hero-amount"><sup>R$</sup> <span id="h-total">370.480,23</span></div>
  <div class="hero-meta">
    <span>📅 <strong id="h-dias">95</strong> dias com movimento</span>
    <span>📆 <strong id="h-meses">4</strong> meses</span>
    <span>🗓 até <strong id="h-last">20/04/2026</strong></span>
    <span>📋 <strong id="h-regs">3.776</strong> registros</span>
  </div>
  <div class="hero-kpis">
    <div class="hkpi">
      <div class="hkpi-lbl">Janeiro 2026</div>
      <div class="hkpi-val" id="hk-jan">R$ 21.769,93</div>
      <div class="hkpi-sub" id="hks-jan">19 dias · 320 reg</div>
      <div class="hkpi-bar"><div class="hkpi-fill" id="hkb-jan" style="width:12%"></div></div>
    </div>
    <div class="hkpi">
      <div class="hkpi-lbl">Fevereiro 2026</div>
      <div class="hkpi-val" id="hk-fev">R$ 30.424,29</div>
      <div class="hkpi-sub" id="hks-fev">20 dias · 494 reg</div>
      <div class="hkpi-bar"><div class="hkpi-fill" id="hkb-fev" style="width:17%"></div></div>
    </div>
    <div class="hkpi">
      <div class="hkpi-lbl">Março 2026</div>
      <div class="hkpi-val" id="hk-mar">R$ 144.215,85</div>
      <div class="hkpi-sub" id="hks-mar">31 dias · 1.499 reg</div>
      <div class="hkpi-bar"><div class="hkpi-fill" id="hkb-mar" style="width:78%"></div></div>
    </div>
    <div class="hkpi" style="border-color:rgba(163,230,53,.4);background:rgba(163,230,53,.1)">
      <div class="hkpi-lbl" style="color:rgba(163,230,53,.8)">Abril 2026 🔴 ao vivo</div>
      <div class="hkpi-val" id="hk-abr">R$ 174.070,16</div>
      <div class="hkpi-sub" id="hks-abr">17 dias · 1.463 reg</div>
      <div class="hkpi-bar"><div class="hkpi-fill" id="hkb-abr" style="width:94%"></div></div>
    </div>
  </div>
</div>

<!-- MÊS CARDS -->
<div class="month-row" id="month-cards"></div>

<!-- TABS -->
<div class="tabs">
  <button class="tab active" onclick="switchTab('dia',this)">🗓 Por Dia</button>
  <button class="tab" onclick="switchTab('semana',this)">📆 Por Semana</button>
  <button class="tab" onclick="switchTab('mes',this)">📅 Por Mês</button>
  <button class="tab" onclick="switchTab('coren',this)">🏛 Por COREN</button>
  <button class="tab" onclick="switchTab('importar',this)">⬆ Importar</button>
</div>

<!-- PANEL DIA -->
<div class="panel active" id="p-dia">
  <div class="pill-row" id="pills-dia">
    <span class="pill-lbl">Filtrar:</span>
    <button class="pill active" onclick="setDayFilter('all',this)">Todos</button>
    <button class="pill" onclick="setDayFilter('2026-01',this)" data-m="2026-01">Jan/26</button>
    <button class="pill" onclick="setDayFilter('2026-02',this)" data-m="2026-02">Fev/26</button>
    <button class="pill" onclick="setDayFilter('2026-03',this)" data-m="2026-03">Mar/26</button>
    <button class="pill" onclick="setDayFilter('2026-04',this)" data-m="2026-04">Abr/26</button>
  </div>
  <div class="card">
    <div class="sec-hd">
      <div>
        <div class="sec-title">Movimento Diário PaguePay</div>
        <div class="sec-sub" id="dia-sub">Jan → Abr 2026 · todos os dias</div>
      </div>
      <div style="display:flex;align-items:center;gap:8px">
        <span class="best-chip" id="best-day-chip">🏆 Melhor dia: —</span>
        <span id="dia-badge" style="font-size:11px;font-weight:600;color:var(--tx3)">95 dias</span>
      </div>
    </div>
    <div class="chart-box" style="height:260px"><canvas id="chart-dia"></canvas></div>
  </div>
  <div class="card">
    <div class="sec-hd"><div><div class="sec-title">Tabela Diária</div></div></div>
    <div class="tbl-wrap">
      <table>
        <thead><tr>
          <th>Data</th><th>Dia</th>
          <th class="tr" style="color:var(--lime)">PaguePay</th>
          <th class="tr" style="color:var(--blue)">Recebido</th>
          <th class="tr">Reg</th>
          <th class="tr">% Mês</th>
        </tr></thead>
        <tbody id="tb-dia"></tbody>
        <tfoot id="tf-dia"></tfoot>
      </table>
    </div>
  </div>
</div>

<!-- PANEL SEMANA -->
<div class="panel" id="p-semana">
  <div class="card">
    <div class="sec-hd">
      <div><div class="sec-title">PaguePay por Semana ISO</div><div class="sec-sub">Jan → Abr 2026</div></div>
      <span id="sem-badge" style="font-size:11px;font-weight:600;color:var(--tx3)">15 semanas</span>
    </div>
    <div class="chart-box" style="height:260px"><canvas id="chart-sem"></canvas></div>
  </div>
  <div class="card">
    <div class="sec-hd"><div><div class="sec-title">Tabela Semanal</div></div></div>
    <div class="tbl-wrap">
      <table>
        <thead><tr>
          <th>Semana ISO</th><th>Período</th>
          <th class="tr" style="color:var(--lime)">PaguePay</th>
          <th class="tr" style="color:var(--blue)">Recebido</th>
          <th class="tr">Dias</th><th class="tr">Reg</th>
          <th class="tr">% Total</th>
        </tr></thead>
        <tbody id="tb-sem"></tbody>
        <tfoot id="tf-sem"></tfoot>
      </table>
    </div>
  </div>
</div>

<!-- PANEL MÊS -->
<div class="panel" id="p-mes">
  <div style="display:grid;grid-template-columns:1fr 1fr;gap:18px;margin-bottom:18px">
    <div class="card" style="margin-bottom:0">
      <div class="sec-hd"><div class="sec-title">Comparativo Mensal</div></div>
      <div class="legend">
        <div class="leg"><div class="leg-dot" style="background:var(--lime)"></div>PaguePay</div>
        <div class="leg"><div class="leg-dot" style="background:var(--blue-m)"></div>Recebido</div>
      </div>
      <div class="chart-box" style="height:220px"><canvas id="chart-mes-bar"></canvas></div>
    </div>
    <div class="card" style="margin-bottom:0">
      <div class="sec-hd"><div class="sec-title">% Crescimento</div></div>
      <div class="chart-box" style="height:260px"><canvas id="chart-mes-line"></canvas></div>
    </div>
  </div>
  <div class="card">
    <div class="sec-hd"><div><div class="sec-title">Tabela Mensal</div></div></div>
    <div class="tbl-wrap">
      <table>
        <thead><tr>
          <th>Mês</th>
          <th class="tr" style="color:var(--lime)">PaguePay</th>
          <th class="tr" style="color:var(--blue)">Recebido</th>
          <th class="tr">Coren</th><th class="tr">Cofen</th>
          <th class="tr">Dias</th><th class="tr">Reg</th>
          <th class="tr">Média/Dia</th><th class="tr">% Ano</th>
        </tr></thead>
        <tbody id="tb-mes"></tbody>
        <tfoot id="tf-mes"></tfoot>
      </table>
    </div>
  </div>
</div>

<!-- PANEL COREN -->
<div class="panel" id="p-coren">
  <div style="display:grid;grid-template-columns:1fr 1fr;gap:18px;margin-bottom:18px">
    <div class="card" style="margin-bottom:0">
      <div class="sec-hd"><div class="sec-title">PaguePay por COREN</div><div class="sec-sub">Total acumulado Jan–Abr 2026</div></div>
      <div class="chart-box" style="height:240px"><canvas id="chart-coren-donut"></canvas></div>
    </div>
    <div class="card" style="margin-bottom:0">
      <div class="sec-hd"><div class="sec-title">Evolução por COREN</div><div class="sec-sub">Mês a mês</div></div>
      <div class="chart-box" style="height:240px"><canvas id="chart-coren-lines"></canvas></div>
    </div>
  </div>
  <div class="card">
    <div class="sec-hd"><div><div class="sec-title">Recebimento por COREN × Mês</div></div></div>
    <div class="tbl-wrap">
      <table>
        <thead><tr>
          <th>COREN</th>
          <th class="tr">Jan/26</th><th class="tr">Fev/26</th>
          <th class="tr">Mar/26</th><th class="tr">Abr/26</th>
          <th class="tr" style="color:var(--lime)">Total</th>
          <th class="tr">% Total</th>
        </tr></thead>
        <tbody id="tb-coren"></tbody>
        <tfoot id="tf-coren"></tfoot>
      </table>
    </div>
  </div>
</div>

<!-- PANEL IMPORTAR -->
<div class="panel" id="p-importar">
  <div id="import-empty-state" style="display:block">
    <div class="card">
      <div class="sec-hd">
        <div><div class="sec-title">⬆ Importar Relatório PaguePay</div><div class="sec-sub">Arquivo XLS exportado do sistema · rec_empresa_DD-MM-AAAA.xls</div></div>
      </div>
      <div class="drop-area" id="dz-pp" onclick="document.getElementById('fi-pp').click()">
        <div class="drop-icon">💚</div>
        <div class="drop-title">Clique ou arraste o arquivo aqui</div>
        <div class="drop-sub">XLS · XLSX · CSV · TSV · TXT</div>
      </div>
      <div class="prog-bar"><div class="prog-fill" id="prog-pp"></div></div>
      <div class="status-txt" id="status-pp"></div>
      <div class="hint-box">
        <strong>Colunas detectadas automaticamente:</strong><br>
        📅 Data: <code>Dt.Pagamento</code> (col 21, ou pelo cabeçalho)<br>
        💚 Valor: <code>Pague Play (24,96%)</code> (col 16, ou pelo cabeçalho)<br>
        💙 Recebido: <code>Valor Recebido</code> (col 14)<br>
        Funciona com <em>rec_empresa</em> e <em>geral_rec</em> do sistema.
      </div>
    </div>
  </div>

  <!-- Resultados da importação dinâmica -->
  <div id="import-results" style="display:none">
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-bottom:20px">
      <div style="background:linear-gradient(135deg,var(--lime-l),#f0ffe0);border:1.5px solid rgba(101,163,13,.25);border-radius:var(--r3);padding:24px;position:relative;overflow:hidden">
        <div style="position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--lime),#84CC16)"></div>
        <div style="font-size:10px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--lime-d);margin-bottom:10px" id="imp-mes-lbl">MÊS MAIS RECENTE</div>
        <div style="font-size:34px;font-weight:800;color:var(--lime-d);line-height:1;letter-spacing:-1px"><span style="font-size:16px;opacity:.6">R$</span><span id="imp-mes-val">0,00</span></div>
        <div style="font-size:11px;color:var(--tx3);margin-top:6px" id="imp-mes-meta">—</div>
        <div style="display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:12px">
          <div><div style="font-size:9px;color:var(--tx3);text-transform:uppercase;letter-spacing:.8px;font-weight:700">Dias</div><div style="font-size:14px;font-weight:700;color:var(--tx)" id="imp-mes-dias">—</div></div>
          <div><div style="font-size:9px;color:var(--tx3);text-transform:uppercase;letter-spacing:.8px;font-weight:700">Média/Dia</div><div style="font-size:14px;font-weight:700;color:var(--lime)" id="imp-mes-avg">—</div></div>
        </div>
      </div>
      <div style="background:linear-gradient(135deg,var(--blue-l),#eff6ff);border:1.5px solid rgba(37,99,235,.2);border-radius:var(--r3);padding:24px;position:relative;overflow:hidden">
        <div style="position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--blue),var(--blue-m))"></div>
        <div style="font-size:10px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--blue-d);margin-bottom:10px" id="imp-ano-lbl">TOTAL 2026</div>
        <div style="font-size:34px;font-weight:800;color:var(--blue-d);line-height:1;letter-spacing:-1px"><span style="font-size:16px;opacity:.6">R$</span><span id="imp-ano-val">0,00</span></div>
        <div style="font-size:11px;color:var(--tx3);margin-top:6px" id="imp-ano-meta">—</div>
        <div style="display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:12px">
          <div><div style="font-size:9px;color:var(--tx3);text-transform:uppercase;letter-spacing:.8px;font-weight:700">Meses</div><div style="font-size:14px;font-weight:700;color:var(--tx)" id="imp-ano-meses">—</div></div>
          <div><div style="font-size:9px;color:var(--tx3);text-transform:uppercase;letter-spacing:.8px;font-weight:700">Média/Mês</div><div style="font-size:14px;font-weight:700;color:var(--blue)" id="imp-ano-avg">—</div></div>
        </div>
      </div>
    </div>

    <div class="pill-row" id="imp-pills">
      <span class="pill-lbl">Período:</span>
      <button class="pill active" onclick="setImpFilter('all',this)">Todos</button>
    </div>

    <div style="display:grid;grid-template-columns:1fr 1fr;gap:18px;margin-bottom:18px">
      <div class="card" style="margin-bottom:0">
        <div style="font-size:11px;font-weight:700;color:var(--tx3);text-transform:uppercase;letter-spacing:.8px;margin-bottom:12px">Por Mês</div>
        <div class="chart-box" style="height:200px"><canvas id="chart-imp-mes"></canvas></div>
      </div>
      <div class="card" style="margin-bottom:0">
        <div style="font-size:11px;font-weight:700;color:var(--tx3);text-transform:uppercase;letter-spacing:.8px;margin-bottom:12px">Por Semana</div>
        <div class="chart-box" style="height:200px"><canvas id="chart-imp-sem"></canvas></div>
      </div>
    </div>
    <div class="card">
      <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:12px">
        <div style="font-size:11px;font-weight:700;color:var(--tx3);text-transform:uppercase;letter-spacing:.8px">Por Dia</div>
        <span id="imp-dia-badge" style="font-size:11px;color:var(--tx3);font-weight:600"></span>
      </div>
      <div class="chart-box" style="height:200px;margin-bottom:18px"><canvas id="chart-imp-dia"></canvas></div>
    </div>

    <!-- Tabelas importadas -->
    <div class="card">
      <div style="font-size:11px;font-weight:700;color:var(--tx3);text-transform:uppercase;letter-spacing:.8px;margin-bottom:12px">Total por Mês (importado)</div>
      <div class="tbl-wrap" style="margin-bottom:20px">
        <table>
          <thead><tr><th>Mês</th><th class="tr" style="color:var(--lime)">PaguePay</th><th class="tr">Dias</th><th class="tr">Reg</th><th class="tr">Média/Dia</th><th class="tr">% Ano</th></tr></thead>
          <tbody id="tb-imp-mes"></tbody><tfoot id="tf-imp-mes"></tfoot>
        </table>
      </div>
      <div style="font-size:11px;font-weight:700;color:var(--tx3);text-transform:uppercase;letter-spacing:.8px;margin-bottom:12px">Total por Semana (importado)</div>
      <div class="tbl-wrap" style="margin-bottom:20px">
        <table>
          <thead><tr><th>Semana</th><th>Período</th><th class="tr" style="color:var(--lime)">PaguePay</th><th class="tr">Dias</th><th class="tr">Reg</th></tr></thead>
          <tbody id="tb-imp-sem"></tbody><tfoot id="tf-imp-sem"></tfoot>
        </table>
      </div>
      <div style="font-size:11px;font-weight:700;color:var(--tx3);text-transform:uppercase;letter-spacing:.8px;margin-bottom:12px">Por Dia (importado)</div>
      <div class="tbl-wrap">
        <table>
          <thead><tr><th>Data</th><th>Dia</th><th class="tr" style="color:var(--lime)">PaguePay</th><th class="tr">Reg</th><th class="tr">% Mês</th></tr></thead>
          <tbody id="tb-imp-dia"></tbody><tfoot id="tf-imp-dia"></tfoot>
        </table>
      </div>
    </div>
    <div style="margin-top:16px">
      <button onclick="resetImport()" style="padding:8px 18px;border-radius:var(--r2);border:1.5px solid var(--bdr2);background:var(--surface);color:var(--tx2);font-family:inherit;font-size:12px;font-weight:600;cursor:pointer">↩ Limpar importação</button>
    </div>
  </div>
</div>

</main>

<!-- MODAL -->
<div class="modal-bg" id="modal-pp">
  <div class="modal">
    <button class="modal-x" onclick="closeModal()">✕</button>
    <div class="modal-title">💚 Importar PaguePay</div>
    <div class="modal-sub">Arquivo XLS do sistema. Extrai automaticamente <strong>Dt.Pagamento</strong> e <strong>Pague Play (24,96%)</strong>.</div>
    <div class="drop-area" id="dz-modal" onclick="document.getElementById('fi-pp').click()" style="padding:28px 16px">
      <div class="drop-icon" style="font-size:28px">📂</div>
      <div class="drop-title" style="font-size:14px">Clique ou arraste aqui</div>
      <div class="drop-sub">XLS · XLSX · CSV · TSV · TXT</div>
    </div>
    <div class="prog-bar"><div class="prog-fill" id="prog-modal"></div></div>
    <div class="status-txt" id="status-modal"></div>
    <div class="hint-box">
      <strong>Detectado automaticamente:</strong> col 21 = Dt.Pagamento · col 16 = Pague Play (24,96%)<br>
      Compatível com <em>rec_empresa</em> e <em>geral_rec</em>.
    </div>
  </div>
</div>

<div class="toast" id="toast"></div>

<script>
// ── DADOS BASE (rec_empresa + geral_rec extraídos) ──
const PP_DATA = {"by_day":{"2026-01-09":{"rec":136.38,"pp":34.05,"cor":76.75,"cof":25.58,"n":1},"2026-01-12":{"rec":1642.59,"pp":410.0,"cor":924.44,"cof":308.15,"n":3},"2026-01-13":{"rec":420.81,"pp":105.03,"cor":236.84,"cof":78.94,"n":3},"2026-01-14":{"rec":1701.64,"pp":424.73,"cor":957.68,"cof":319.23,"n":6},"2026-01-15":{"rec":610.43,"pp":152.36,"cor":343.55,"cof":114.52,"n":2},"2026-01-16":{"rec":2269.14,"pp":566.38,"cor":1277.07,"cof":425.69,"n":9},"2026-01-19":{"rec":2095.18,"pp":522.92,"cor":1179.18,"cof":393.08,"n":10},"2026-01-20":{"rec":6491.69,"pp":1620.27,"cor":3653.54,"cof":1217.88,"n":26},"2026-01-21":{"rec":6516.03,"pp":1626.42,"cor":3667.2,"cof":1222.41,"n":21},"2026-01-22":{"rec":6485.32,"pp":1618.73,"cor":3649.93,"cof":1216.66,"n":15},"2026-01-23":{"rec":8280.32,"pp":2066.74,"cor":4660.16,"cof":1553.42,"n":25},"2026-01-24":{"rec":2741.56,"pp":684.28,"cor":1542.96,"cof":514.32,"n":7},"2026-01-25":{"rec":237.93,"pp":59.38,"cor":133.91,"cof":44.64,"n":1},"2026-01-26":{"rec":3412.21,"pp":851.67,"cor":1920.41,"cof":640.13,"n":15},"2026-01-27":{"rec":6505.52,"pp":1623.76,"cor":3661.3,"cof":1220.46,"n":18},"2026-01-28":{"rec":6665.9,"pp":1663.83,"cor":3751.55,"cof":1250.52,"n":28},"2026-01-29":{"rec":7055.26,"pp":1760.95,"cor":3970.71,"cof":1323.6,"n":30},"2026-01-30":{"rec":18272.18,"pp":4560.63,"cor":10283.62,"cof":3427.93,"n":74},"2026-01-31":{"rec":5680.37,"pp":1417.8,"cor":3196.92,"cof":1065.65,"n":26},"2026-02-01":{"rec":486.55,"pp":121.44,"cor":273.83,"cof":91.28,"n":2},"2026-02-02":{"rec":6587.43,"pp":1644.19,"cor":3707.41,"cof":1235.83,"n":27},"2026-02-03":{"rec":3950.79,"pp":986.1,"cor":2223.51,"cof":741.18,"n":12},"2026-02-04":{"rec":6411.91,"pp":1600.37,"cor":3608.63,"cof":1202.91,"n":22},"2026-02-05":{"rec":4313.29,"pp":1076.62,"cor":2427.49,"cof":809.18,"n":18},"2026-02-06":{"rec":7690.84,"pp":1919.62,"cor":4328.41,"cof":1442.81,"n":23},"2026-02-07":{"rec":2074.3,"pp":517.73,"cor":1167.42,"cof":389.15,"n":4},"2026-02-08":{"rec":180.52,"pp":45.06,"cor":101.59,"cof":33.87,"n":3},"2026-02-09":{"rec":6740.54,"pp":1682.41,"cor":3793.58,"cof":1264.55,"n":29},"2026-02-10":{"rec":4177.51,"pp":1042.7,"cor":2351.1,"cof":783.71,"n":16},"2026-02-11":{"rec":9560.73,"pp":2386.36,"cor":5380.78,"cof":1793.59,"n":30},"2026-02-12":{"rec":6551.68,"pp":1635.28,"cor":3687.29,"cof":1229.11,"n":20},"2026-02-13":{"rec":5959.18,"pp":1487.39,"cor":3353.85,"cof":1117.94,"n":27},"2026-02-14":{"rec":562.18,"pp":140.32,"cor":316.39,"cof":105.47,"n":2},"2026-02-15":{"rec":908.66,"pp":226.81,"cor":511.39,"cof":170.46,"n":3},"2026-02-16":{"rec":486.66,"pp":121.46,"cor":273.9,"cof":91.3,"n":3},"2026-02-17":{"rec":564.57,"pp":140.91,"cor":317.74,"cof":105.92,"n":2},"2026-02-18":{"rec":1928.72,"pp":481.4,"cor":1085.49,"cof":361.83,"n":8},"2026-02-19":{"rec":4707.31,"pp":1174.96,"cor":2649.28,"cof":883.07,"n":23},"2026-02-20":{"rec":6765.85,"pp":1688.78,"cor":3807.82,"cof":1269.25,"n":29},"2026-02-21":{"rec":911.27,"pp":227.46,"cor":512.86,"cof":170.95,"n":5},"2026-02-22":{"rec":141.43,"pp":35.3,"cor":79.6,"cof":26.53,"n":1},"2026-02-23":{"rec":6689.79,"pp":1669.8,"cor":3764.99,"cof":1255.0,"n":26},"2026-02-24":{"rec":4694.76,"pp":1171.8,"cor":2642.22,"cof":880.74,"n":21},"2026-02-25":{"rec":5731.11,"pp":1430.5,"cor":3225.47,"cof":1075.14,"n":28},"2026-02-26":{"rec":3042.67,"pp":759.48,"cor":1712.41,"cof":570.78,"n":18},"2026-02-27":{"rec":15559.83,"pp":3883.76,"cor":8757.07,"cof":2919.0,"n":66},"2026-02-28":{"rec":4923.47,"pp":1228.85,"cor":2770.95,"cof":923.67,"n":26},"2026-03-01":{"rec":1068.15,"pp":266.6,"cor":601.16,"cof":200.39,"n":6},"2026-03-02":{"rec":12548.91,"pp":3132.23,"cor":7062.51,"cof":2354.17,"n":50},"2026-03-03":{"rec":22354.56,"pp":5579.67,"cor":12581.17,"cof":4193.72,"n":54},"2026-03-04":{"rec":11461.35,"pp":2860.73,"cor":6450.45,"cof":2150.17,"n":30},"2026-03-05":{"rec":15070.02,"pp":3761.47,"cor":8481.4,"cof":2827.15,"n":41},"2026-03-06":{"rec":21321.3,"pp":5321.82,"cor":11999.61,"cof":3999.87,"n":76},"2026-03-07":{"rec":3398.25,"pp":848.2,"cor":1912.55,"cof":637.5,"n":9},"2026-03-08":{"rec":2013.32,"pp":502.52,"cor":1133.1,"cof":377.7,"n":6},"2026-03-09":{"rec":21445.82,"pp":5352.89,"cor":12069.71,"cof":4023.22,"n":57},"2026-03-10":{"rec":32003.56,"pp":7988.08,"cor":18011.61,"cof":6003.87,"n":71},"2026-03-11":{"rec":17012.21,"pp":4246.24,"cor":9574.48,"cof":3191.49,"n":58},"2026-03-12":{"rec":21406.97,"pp":5343.18,"cor":12047.86,"cof":4015.93,"n":54},"2026-03-13":{"rec":16332.08,"pp":4076.47,"cor":9191.7,"cof":3063.91,"n":45},"2026-03-14":{"rec":306.01,"pp":76.38,"cor":172.22,"cof":57.41,"n":2},"2026-03-15":{"rec":278.54,"pp":69.53,"cor":156.76,"cof":52.25,"n":1},"2026-03-16":{"rec":18975.47,"pp":4736.24,"cor":10679.41,"cof":3559.82,"n":43},"2026-03-17":{"rec":10694.56,"pp":2669.36,"cor":6018.88,"cof":2006.32,"n":33},"2026-03-18":{"rec":11970.05,"pp":2987.71,"cor":6736.75,"cof":2245.59,"n":31},"2026-03-19":{"rec":12848.55,"pp":3206.99,"cor":7231.17,"cof":2410.39,"n":23},"2026-03-20":{"rec":21449.03,"pp":5353.68,"cor":12071.52,"cof":4023.83,"n":43},"2026-03-21":{"rec":1253.45,"pp":312.86,"cor":705.44,"cof":235.15,"n":5},"2026-03-22":{"rec":758.53,"pp":189.32,"cor":426.91,"cof":142.3,"n":3},"2026-03-23":{"rec":20785.2,"pp":5188.05,"cor":11697.88,"cof":3899.27,"n":42},"2026-03-24":{"rec":11771.96,"pp":2938.3,"cor":6625.26,"cof":2208.4,"n":42},"2026-03-25":{"rec":23386.82,"pp":5837.27,"cor":13162.16,"cof":4387.39,"n":68},"2026-03-26":{"rec":36697.65,"pp":9159.81,"cor":20653.36,"cof":6884.48,"n":98},"2026-03-27":{"rec":44009.56,"pp":10984.79,"cor":24768.56,"cof":8256.21,"n":100},"2026-03-28":{"rec":5609.43,"pp":1400.08,"cor":3157.01,"cof":1052.34,"n":23},"2026-03-29":{"rec":3178.6,"pp":793.35,"cor":1788.94,"cof":596.31,"n":11},"2026-03-30":{"rec":72850.95,"pp":18183.61,"cor":41000.49,"cof":13666.85,"n":161},"2026-03-31":{"rec":83800.47,"pp":20916.66,"cor":47162.83,"cof":15720.98,"n":213},"2026-04-01":{"rec":41697.48,"pp":10407.67,"cor":23467.35,"cof":7822.46,"n":90},"2026-04-02":{"rec":22878.61,"pp":5710.48,"cor":12876.08,"cof":4292.05,"n":56},"2026-04-03":{"rec":1037.53,"pp":258.98,"cor":583.91,"cof":194.64,"n":6},"2026-04-04":{"rec":1125.74,"pp":281.0,"cor":633.56,"cof":211.18,"n":2},"2026-04-05":{"rec":79.22,"pp":19.77,"cor":44.59,"cof":14.86,"n":1},"2026-04-06":{"rec":50648.69,"pp":12641.85,"cor":28505.1,"cof":9501.74,"n":110},"2026-04-07":{"rec":53608.81,"pp":13380.73,"cor":30171.05,"cof":10057.03,"n":113},"2026-04-08":{"rec":53952.13,"pp":13466.31,"cor":30364.31,"cof":10121.51,"n":116},"2026-04-09":{"rec":74376.07,"pp":18564.28,"cor":41858.84,"cof":13952.95,"n":124},"2026-04-10":{"rec":57107.81,"pp":14254.07,"cor":32140.3,"cof":10713.44,"n":121},"2026-04-11":{"rec":11583.99,"pp":2891.4,"cor":6519.44,"cof":2173.15,"n":28},"2026-04-12":{"rec":1260.0,"pp":314.49,"cor":709.13,"cof":236.38,"n":4},"2026-04-13":{"rec":47139.49,"pp":11766.0,"cor":26530.09,"cof":8843.4,"n":105},"2026-04-14":{"rec":72496.73,"pp":18095.18,"cor":40801.18,"cof":13600.37,"n":144},"2026-04-15":{"rec":63643.32,"pp":15885.29,"cor":35818.51,"cof":11939.52,"n":152},"2026-04-16":{"rec":72524.99,"pp":18102.32,"cor":40817.05,"cof":13605.62,"n":145},"2026-04-17":{"rec":72237.56,"pp":18030.34,"cor":40655.37,"cof":13551.85,"n":146}},"by_month":{"2026-01":{"rec":87220.46,"pp":21769.93,"cor":49087.72,"cof":16362.81,"n":320},"2026-02":{"rec":122303.55,"pp":30526.86,"cor":68832.47,"cof":22944.22,"n":494},"2026-03":{"rec":578061.33,"pp":144284.09,"cor":325332.86,"cof":108444.38,"n":1499},"2026-04":{"rec":697398.17,"pp":174070.16,"cor":392495.86,"cof":130832.15,"n":1463}},"by_coren_mes":{"2026-01":{"PI":{"rec":87220.46,"pp":21769.93,"n":320}},"2026-02":{"PI":{"rec":121624.14,"pp":30357.29,"n":487},"RO":{"rec":679.41,"pp":169.57,"n":7}},"2026-03":{"MA":{"rec":169833.88,"pp":42390.52,"n":340},"PI":{"rec":408227.45,"pp":101893.57,"n":1159}},"2026-04":{"CE":{"rec":79959.07,"pp":19957.67,"n":183},"MA":{"rec":315057.03,"pp":78638.17,"n":683},"MT":{"rec":190890.2,"pp":47645.9,"n":296},"PI":{"rec":111491.87,"pp":27828.42,"n":301}}}};

// ── STATE ──
let dayFilter = 'all';
let impFilter = 'all';
let PPI = (()=>{
  try{
    const raw=localStorage.getItem('ppi_v2');
    if(!raw) return null;
    const d=JSON.parse(raw);
    if(d&&d.byDayKeys&&!d.byDay){
      d.byDay=Object.fromEntries(Object.entries(d.byDayKeys).map(([k,v])=>[k,{val:v,n:0}]));
      delete d.byDayKeys;
    }
    return d;
  }catch(e){return null;}
})();
let chartDia, chartSem, chartMesBar, chartMesLine, chartCorenDonut, chartCorenLines;
let chartImpMes, chartImpSem, chartImpDia;

// ── FORMATTERS ──
const fBR = v => 'R$ '+(v||0).toLocaleString('pt-BR',{minimumFractionDigits:2,maximumFractionDigits:2});
const fBRk = v => { if(v>=1e6) return 'R$ '+(v/1e6).toLocaleString('pt-BR',{minimumFractionDigits:2})+'M'; if(v>=1e3) return 'R$ '+(v/1e3).toLocaleString('pt-BR',{minimumFractionDigits:1})+'k'; return fBR(v); };
const fDate = s => { const [y,m,d]=s.split('-'); return `${d}/${m}/${y}`; };
const fPct = (v,t) => t>0?((v/t)*100).toFixed(1)+'%':'—';
const MNAMES = {'01':'Janeiro','02':'Fevereiro','03':'Março','04':'Abril','05':'Maio','06':'Junho','07':'Julho','08':'Agosto','09':'Setembro','10':'Outubro','11':'Novembro','12':'Dezembro'};
const MSNAMES = {'01':'Jan','02':'Fev','03':'Mar','04':'Abr','05':'Mai','06':'Jun','07':'Jul','08':'Ago','09':'Set','10':'Out','11':'Nov','12':'Dez'};
const WDAYS = ['Dom','Seg','Ter','Qua','Qui','Sex','Sáb'];
const wdayOf = s => WDAYS[new Date(s+'T12:00:00').getDay()];

function weekRange(wk){
  const [yr,wn]=wk.split('-W'); const w=parseInt(wn);
  const jan4=new Date(parseInt(yr),0,4); const mon=new Date(jan4);
  mon.setDate(jan4.getDate()-((jan4.getDay()+6)%7)+(w-1)*7);
  const sun=new Date(mon); sun.setDate(mon.getDate()+6);
  const f=d=>`${String(d.getDate()).padStart(2,'0')}/${String(d.getMonth()+1).padStart(2,'0')}`;
  return `${f(mon)} – ${f(sun)}`;
}
function getISOWeek(d){
  const j4=new Date(d.getFullYear(),0,4); const sw=new Date(j4); sw.setDate(j4.getDate()-((j4.getDay()+6)%7));
  const w=Math.floor((d-sw)/604800000)+1;
  if(w<1){const py=d.getFullYear()-1;const[,pw]=getISOWeek(new Date(py,11,31));return[py,pw];}
  if(w>52){const j4n=new Date(d.getFullYear()+1,0,4);const sn=new Date(j4n);sn.setDate(j4n.getDate()-((j4n.getDay()+6)%7));if(d>=sn)return[d.getFullYear()+1,1];}
  return [d.getFullYear(),w];
}

// ── CHART CONFIG ──
const CG = {
  responsive:true,maintainAspectRatio:false,
  interaction:{mode:'index',intersect:false},
  plugins:{legend:{display:false},tooltip:{backgroundColor:'rgba(15,22,40,.96)',borderColor:'#E2E6EF',borderWidth:1,titleColor:'#1A1F2E',bodyColor:'#5A6478',padding:10,callbacks:{label:ctx=>' '+ctx.dataset.label+': '+fBR(ctx.parsed.y)}}},
  scales:{x:{grid:{color:'rgba(0,0,0,.04)'},ticks:{color:'#9BA3B5',font:{size:10}}},y:{grid:{color:'rgba(0,0,0,.04)'},ticks:{color:'#9BA3B5',font:{size:10},callback:v=>fBRk(v)}}}
};

// ── INIT HERO ──
function initHero(){
  const months = Object.keys(PP_DATA.by_month).sort();
  const maxPP = Math.max(...months.map(mk=>PP_DATA.by_month[mk].pp));
  let total=0,totalRec=0,totalN=0,totalDays=0;
  months.forEach(mk=>{const m=PP_DATA.by_month[mk];total+=m.pp;totalRec+=m.rec;totalN+=m.n;totalDays+=Object.keys(PP_DATA.by_day).filter(d=>d.startsWith(mk)).length;});
  document.getElementById('h-total').textContent=total.toLocaleString('pt-BR',{minimumFractionDigits:2,maximumFractionDigits:2});
  document.getElementById('h-dias').textContent=totalDays;
  document.getElementById('h-meses').textContent=months.length;
  document.getElementById('h-regs').textContent=totalN.toLocaleString('pt-BR');
  const lastDay=Object.keys(PP_DATA.by_day).sort().pop();
  if(lastDay) document.getElementById('h-last').textContent=fDate(lastDay);
  const mk2labels={'2026-01':'jan','2026-02':'fev','2026-03':'mar','2026-04':'abr'};
  months.forEach(mk=>{
    const id=mk2labels[mk];if(!id)return;
    const m=PP_DATA.by_month[mk]; const days=Object.keys(PP_DATA.by_day).filter(d=>d.startsWith(mk)).length;
    document.getElementById('hk-'+id).textContent=fBR(m.pp);
    document.getElementById('hks-'+id).textContent=days+' dias · '+m.n.toLocaleString('pt-BR')+' reg';
    document.getElementById('hkb-'+id).style.width=Math.round(m.pp/maxPP*100)+'%';
  });
}

// ── MÊS CARDS ──
function renderMonthCards(){
  const months=Object.keys(PP_DATA.by_month).sort();
  const maxPP=Math.max(...months.map(mk=>PP_DATA.by_month[mk].pp));
  const mColors={'2026-01':'mcard-jan','2026-02':'mcard-fev','2026-03':'mcard-mar','2026-04':'mcard-abr'};
  const ppColors={'2026-01':'#3B82F6','2026-02':'#7C3AED','2026-03':'#059669','2026-04':'var(--lime)'};
  document.getElementById('month-cards').innerHTML=months.map(mk=>{
    const m=PP_DATA.by_month[mk]; const[y,mo]=mk.split('-');
    const days=Object.keys(PP_DATA.by_day).filter(d=>d.startsWith(mk)).length;
    const avgDay=days>0?m.rec/days:0; const pct=Math.round(m.pp/maxPP*100);
    const pctPp=((m.pp/m.rec)*100).toFixed(1);
    return `<div class="mcard ${mColors[mk]||''}">
      <div class="mcard-head">
        <div class="mcard-title">${MNAMES[mo]} ${y}</div>
        <div class="mcard-badge">${m.n.toLocaleString('pt-BR')} reg</div>
      </div>
      <div class="mcard-pp" style="color:${ppColors[mk]||'var(--lime)'}">${fBR(m.pp)}</div>
      <div class="mcard-rec">Recebido: ${fBR(m.rec)} · PP ${pctPp}%</div>
      <div class="mcard-stat">
        <div class="mstat"><div class="mstat-lbl">Dias</div><div class="mstat-val">${days}</div></div>
        <div class="mstat"><div class="mstat-lbl">Média/Dia</div><div class="mstat-val" style="color:${ppColors[mk]||'var(--lime)'}">${fBRk(avgDay)}</div></div>
        <div class="mstat"><div class="mstat-lbl">PP/Dia</div><div class="mstat-val">${fBRk(m.pp/days)}</div></div>
      </div>
      <div class="mcard-prog"><div class="mcard-prog-fill" style="background:${ppColors[mk]||'var(--lime)'};width:${pct}%"></div></div>
    </div>`;
  }).join('');
}

// ── DIA ──
function renderDia(){
  let days=Object.keys(PP_DATA.by_day).sort();
  if(dayFilter!=='all') days=days.filter(d=>d.startsWith(dayFilter));
  const cnt=days.length;
  document.getElementById('dia-badge').textContent=cnt+' dias';
  const monthName=dayFilter==='all'?'Jan → Abr 2026':MNAMES[dayFilter.split('-')[1]]+' 2026';
  document.getElementById('dia-sub').textContent=monthName+' · '+cnt+' dias com movimento';
  const maxPP=days.length?Math.max(...days.map(d=>PP_DATA.by_day[d].pp)):1;
  const bestDayKey=days.reduce((a,b)=>PP_DATA.by_day[a].pp>PP_DATA.by_day[b].pp?a:b,'');
  if(bestDayKey) document.getElementById('best-day-chip').textContent='🏆 Melhor: '+fDate(bestDayKey)+' · '+fBRk(PP_DATA.by_day[bestDayKey].pp);
  if(chartDia) chartDia.destroy();
  chartDia=new Chart(document.getElementById('chart-dia'),{type:'bar',data:{
    labels:days.map(d=>{const[,m,dd]=d.split('-');return dd+'/'+m;}),
    datasets:[
      {label:'PaguePay',data:days.map(d=>PP_DATA.by_day[d].pp),backgroundColor:days.map(d=>PP_DATA.by_day[d].pp===maxPP?'rgba(101,163,13,.9)':'rgba(163,230,53,.5)'),borderColor:days.map(d=>PP_DATA.by_day[d].pp===maxPP?'#65A30D':'rgba(101,163,13,.4)'),borderWidth:1.5,borderRadius:4},
      {label:'Recebido',data:days.map(d=>PP_DATA.by_day[d].rec),type:'line',borderColor:'rgba(37,99,235,.5)',backgroundColor:'transparent',borderWidth:1.5,pointRadius:0,tension:.4},
    ]},options:{...CG,plugins:{...CG.plugins,legend:{display:true,labels:{color:'#5A6478',font:{size:10},boxWidth:10}}},
    scales:{...CG.scales,x:{...CG.scales.x,ticks:{...CG.scales.x.ticks,maxRotation:45,callback:(_,i,tks)=>cnt>30&&i%Math.max(1,Math.floor(cnt/24))!==0?'':tks[i].label}}}}});
  const mTotals={};
  days.forEach(d=>{const mk=d.slice(0,7);if(!mTotals[mk])mTotals[mk]=0;mTotals[mk]+=PP_DATA.by_day[d].pp;});
  let sumPP=0,sumRec=0,sumN=0;
  document.getElementById('tb-dia').innerHTML=days.map(dk=>{
    const d=PP_DATA.by_day[dk]; const isMax=d.pp===maxPP;
    const mTotal=mTotals[dk.slice(0,7)]||1; const pct=((d.pp/mTotal)*100).toFixed(1);
    sumPP+=d.pp;sumRec+=d.rec;sumN+=d.n;
    return `<tr${isMax?' style="background:rgba(101,163,13,.06)"':''}>
      <td class="key"${isMax?' style="color:var(--lime)"':''}>${fDate(dk)}${isMax?' <span class="best-chip">🏆</span>':''}</td>
      <td style="font-size:11px;color:var(--tx3)">${wdayOf(dk)}</td>
      <td class="mo c-lime">${fBR(d.pp)}</td>
      <td class="mo c-blue">${fBR(d.rec)}</td>
      <td class="cn">${d.n}</td>
      <td class="cn">${pct}%</td>
    </tr>`;
  }).join('');
  document.getElementById('tf-dia').innerHTML=`<tr><td class="key">TOTAL</td><td></td><td class="mo c-lime">${fBR(Math.round(sumPP*100)/100)}</td><td class="mo c-blue">${fBR(Math.round(sumRec*100)/100)}</td><td class="cn">${sumN.toLocaleString('pt-BR')}</td><td class="cn">100%</td></tr>`;
}

// ── SEMANA ──
function buildWeekData(){
  const wData={};
  Object.entries(PP_DATA.by_day).forEach(([dk,v])=>{
    const dt=new Date(dk+'T12:00:00');const[wy,wn]=getISOWeek(dt);
    const wk=`${wy}-W${String(wn).padStart(2,'0')}`;
    if(!wData[wk])wData[wk]={pp:0,rec:0,n:0,days:0};
    wData[wk].pp=Math.round((wData[wk].pp+v.pp)*100)/100;
    wData[wk].rec=Math.round((wData[wk].rec+v.rec)*100)/100;
    wData[wk].n+=v.n;wData[wk].days++;
  });
  return wData;
}
function renderSem(){
  const wData=buildWeekData(); const weeks=Object.keys(wData).sort();
  document.getElementById('sem-badge').textContent=weeks.length+' semanas';
  const maxPP=Math.max(...weeks.map(w=>wData[w].pp));
  if(chartSem) chartSem.destroy();
  chartSem=new Chart(document.getElementById('chart-sem'),{type:'bar',data:{
    labels:weeks.map(w=>w.replace('2026-','')),
    datasets:[
      {label:'PaguePay',data:weeks.map(w=>wData[w].pp),backgroundColor:weeks.map(w=>wData[w].pp===maxPP?'rgba(101,163,13,.85)':'rgba(163,230,53,.45)'),borderColor:'rgba(101,163,13,.5)',borderWidth:1.5,borderRadius:5},
      {label:'Recebido',data:weeks.map(w=>wData[w].rec),type:'line',borderColor:'rgba(37,99,235,.55)',backgroundColor:'rgba(37,99,235,.05)',borderWidth:2,pointRadius:3,pointBackgroundColor:'#2563EB',tension:.4,fill:true},
    ]},options:{...CG,plugins:{...CG.plugins,legend:{display:true,labels:{color:'#5A6478',font:{size:10},boxWidth:10}}}}});
  const totalPP=weeks.reduce((s,w)=>s+wData[w].pp,0);
  let sumPP=0,sumRec=0,sumN=0,sumD=0;
  document.getElementById('tb-sem').innerHTML=weeks.map(wk=>{
    const w=wData[wk]; const isMax=w.pp===maxPP; const pct=((w.pp/totalPP)*100).toFixed(1);
    sumPP+=w.pp;sumRec+=w.rec;sumN+=w.n;sumD+=w.days;
    return `<tr${isMax?' style="background:rgba(101,163,13,.05)"':''}>
      <td class="key"${isMax?' style="color:var(--lime)"':''}>${wk}${isMax?' 🏆':''}</td>
      <td style="font-size:11px;color:var(--tx3)">${weekRange(wk)}</td>
      <td class="mo c-lime">${fBR(w.pp)}</td>
      <td class="mo c-blue">${fBR(w.rec)}</td>
      <td class="cn">${w.days}</td><td class="cn">${w.n}</td>
      <td class="cn">${pct}%</td>
    </tr>`;
  }).join('');
  document.getElementById('tf-sem').innerHTML=`<tr><td class="key">TOTAL</td><td></td><td class="mo c-lime">${fBR(Math.round(sumPP*100)/100)}</td><td class="mo c-blue">${fBR(Math.round(sumRec*100)/100)}</td><td class="cn">${sumD}</td><td class="cn">${sumN}</td><td class="cn">100%</td></tr>`;
}

// ── MÊS ──
function renderMes(){
  const months=Object.keys(PP_DATA.by_month).sort();
  const labels=months.map(mk=>{const[y,mo]=mk.split('-');return MSNAMES[mo]+'/'+y.slice(2);});
  if(chartMesBar) chartMesBar.destroy();
  chartMesBar=new Chart(document.getElementById('chart-mes-bar'),{type:'bar',data:{labels,datasets:[
    {label:'PaguePay',data:months.map(mk=>PP_DATA.by_month[mk].pp),backgroundColor:'rgba(101,163,13,.8)',borderColor:'#65A30D',borderWidth:2,borderRadius:6},
    {label:'Recebido',data:months.map(mk=>PP_DATA.by_month[mk].rec),backgroundColor:'rgba(37,99,235,.2)',borderColor:'rgba(37,99,235,.7)',borderWidth:2,borderRadius:6},
  ]},options:{...CG,plugins:{...CG.plugins,legend:{display:true,labels:{color:'#5A6478',font:{size:10},boxWidth:10}}}}});
  // Growth line
  const growthData=months.map((mk,i)=>{if(i===0)return null;const prev=PP_DATA.by_month[months[i-1]].pp;return ((PP_DATA.by_month[mk].pp-prev)/prev*100).toFixed(1);});
  if(chartMesLine) chartMesLine.destroy();
  chartMesLine=new Chart(document.getElementById('chart-mes-line'),{type:'line',data:{labels,datasets:[{label:'Crescimento %',data:growthData,borderColor:'#65A30D',backgroundColor:'rgba(101,163,13,.1)',borderWidth:2.5,pointRadius:6,pointBackgroundColor:'#65A30D',pointBorderColor:'#fff',pointBorderWidth:2,tension:.4,fill:true}]},options:{...CG,scales:{...CG.scales,y:{...CG.scales.y,ticks:{...CG.scales.y.ticks,callback:v=>v==null?'':v+'%'}}},plugins:{...CG.plugins,legend:{display:false},tooltip:{...CG.plugins.tooltip,callbacks:{label:ctx=>ctx.parsed.y==null?' Sem comparação':' Crescimento: '+ctx.parsed.y+'%'}}}}});
  const totalPP=Object.values(PP_DATA.by_month).reduce((s,m)=>s+m.pp,0);
  const totalRec=Object.values(PP_DATA.by_month).reduce((s,m)=>s+m.rec,0);
  const totalCor=Object.values(PP_DATA.by_month).reduce((s,m)=>s+m.cor,0);
  const totalCof=Object.values(PP_DATA.by_month).reduce((s,m)=>s+m.cof,0);
  const totalN=Object.values(PP_DATA.by_month).reduce((s,m)=>s+m.n,0);
  const maxPP=Math.max(...months.map(mk=>PP_DATA.by_month[mk].pp));
  document.getElementById('tb-mes').innerHTML=months.map(mk=>{
    const m=PP_DATA.by_month[mk];const[y,mo]=mk.split('-');
    const days=Object.keys(PP_DATA.by_day).filter(d=>d.startsWith(mk)).length;
    const avgDay=days>0?m.rec/days:0;const pct=((m.pp/totalPP)*100).toFixed(1);
    const bar=Math.round(m.pp/maxPP*50);
    return `<tr>
      <td class="key"><span style="display:inline-block;width:${bar}px;height:3px;background:var(--lime);border-radius:2px;margin-right:6px;vertical-align:middle"></span>${MNAMES[mo]} ${y}</td>
      <td class="mo c-lime">${fBR(m.pp)}</td><td class="mo c-blue">${fBR(m.rec)}</td>
      <td class="mo" style="color:var(--amber)">${fBR(m.cor)}</td><td class="mo" style="color:var(--purple)">${fBR(m.cof)}</td>
      <td class="cn">${days}</td><td class="cn">${m.n.toLocaleString('pt-BR')}</td>
      <td class="mo" style="color:var(--tx2)">${fBRk(avgDay)}</td><td class="cn">${pct}%</td>
    </tr>`;
  }).join('');
  document.getElementById('tf-mes').innerHTML=`<tr><td class="key">TOTAL</td><td class="mo c-lime">${fBR(Math.round(totalPP*100)/100)}</td><td class="mo c-blue">${fBR(Math.round(totalRec*100)/100)}</td><td class="mo" style="color:var(--amber)">${fBR(Math.round(totalCor*100)/100)}</td><td class="mo" style="color:var(--purple)">${fBR(Math.round(totalCof*100)/100)}</td><td class="cn">${Object.keys(PP_DATA.by_day).length}</td><td class="cn">${totalN.toLocaleString('pt-BR')}</td><td></td><td class="cn">100%</td></tr>`;
}

// ── COREN ──
function renderCoren(){
  const months=['2026-01','2026-02','2026-03','2026-04'];
  const allCorens=[...new Set(months.flatMap(mk=>Object.keys(PP_DATA.by_coren_mes[mk]||{})))].sort();
  const corenColors={PI:'#2563EB',MA:'#059669',CE:'#D97706',MT:'#7C3AED',RO:'#DB2777'};
  const totalByState={};
  allCorens.forEach(s=>{totalByState[s]=months.reduce((sum,mk)=>sum+(PP_DATA.by_coren_mes[mk]?.[s]?.pp||0),0);});
  const grandTotal=Object.values(totalByState).reduce((s,v)=>s+v,0);
  if(chartCorenDonut) chartCorenDonut.destroy();
  chartCorenDonut=new Chart(document.getElementById('chart-coren-donut'),{type:'doughnut',data:{labels:allCorens,datasets:[{data:allCorens.map(s=>totalByState[s]),backgroundColor:allCorens.map(s=>corenColors[s]||'#888'),borderColor:'#fff',borderWidth:3}]},options:{responsive:true,maintainAspectRatio:false,cutout:'65%',plugins:{legend:{display:true,position:'bottom',labels:{color:'#5A6478',font:{size:11},padding:14,boxWidth:10}},tooltip:{backgroundColor:'rgba(15,22,40,.96)',borderColor:'#E2E6EF',borderWidth:1,titleColor:'#1A1F2E',bodyColor:'#5A6478',padding:10,callbacks:{label:ctx=>` ${ctx.label}: ${fBR(ctx.parsed)} (${fPct(ctx.parsed,grandTotal)})`}}}}});
  if(chartCorenLines) chartCorenLines.destroy();
  const labels=months.map(mk=>{const[y,mo]=mk.split('-');return MSNAMES[mo]+'/'+y.slice(2);});
  chartCorenLines=new Chart(document.getElementById('chart-coren-lines'),{type:'line',data:{labels,datasets:allCorens.map(s=>({label:s,data:months.map(mk=>PP_DATA.by_coren_mes[mk]?.[s]?.rec||null),borderColor:corenColors[s]||'#888',backgroundColor:'transparent',borderWidth:2.5,pointRadius:5,pointBackgroundColor:corenColors[s]||'#888',pointBorderColor:'#fff',pointBorderWidth:2,tension:.4,spanGaps:false}))},options:{...CG,plugins:{...CG.plugins,legend:{display:true,position:'bottom',labels:{color:'#5A6478',font:{size:10},boxWidth:8,padding:10}},tooltip:{...CG.plugins.tooltip,callbacks:{label:ctx=>ctx.parsed.y==null?null:` ${ctx.dataset.label}: ${fBR(ctx.parsed.y)}`}}}}});
  document.getElementById('tb-coren').innerHTML=allCorens.map(s=>{
    const total=totalByState[s]; const pct=fPct(total,grandTotal);
    const cells=months.map(mk=>{const v=PP_DATA.by_coren_mes[mk]?.[s]?.pp||0;return v>0?`<td class="mo" style="color:${corenColors[s]||'var(--tx)'}">${fBR(v)}</td>`:`<td class="mo" style="color:var(--tx3)">—</td>`;}).join('');
    return `<tr><td><span class="coren-badge c-${s}">${s}</span></td>${cells}<td class="mo c-lime">${fBR(total)}</td><td class="cn">${pct}</td></tr>`;
  }).join('');
  const totals=months.map(mk=>Object.values(PP_DATA.by_coren_mes[mk]||{}).reduce((s,v)=>s+v.pp,0));
  document.getElementById('tf-coren').innerHTML=`<tr><td class="key">TOTAL</td>${totals.map(v=>`<td class="mo c-lime">${fBR(Math.round(v*100)/100)}</td>`).join('')}<td class="mo c-lime">${fBR(Math.round(grandTotal*100)/100)}</td><td class="cn">100%</td></tr>`;
}

// ── TABS / FILTERS ──
function switchTab(id,btn){
  document.querySelectorAll('.tab').forEach(b=>b.classList.remove('active'));
  document.querySelectorAll('.panel').forEach(p=>p.classList.remove('active'));
  btn.classList.add('active'); document.getElementById('p-'+id).classList.add('active');
}
function setDayFilter(f,btn){
  dayFilter=f;
  document.querySelectorAll('#pills-dia .pill').forEach(p=>p.classList.remove('active'));
  btn.classList.add('active'); renderDia();
}

// ── MODAL / FILE ──
function openModal(){ document.getElementById('modal-pp').classList.add('open'); }
function closeModal(){ document.getElementById('modal-pp').classList.remove('open'); }
document.getElementById('modal-pp').addEventListener('click',e=>{if(e.target===document.getElementById('modal-pp'))closeModal();});

['dz-pp','dz-modal'].forEach(id=>{
  const dz=document.getElementById(id);
  if(!dz) return;
  dz.addEventListener('dragover',e=>{e.preventDefault();dz.classList.add('drag');});
  dz.addEventListener('dragleave',()=>dz.classList.remove('drag'));
  dz.addEventListener('drop',e=>{e.preventDefault();dz.classList.remove('drag');const f=e.dataTransfer.files[0];if(f)processFile(f);});
});
document.getElementById('fi-pp').addEventListener('change',e=>{const f=e.target.files[0];if(f)processFile(f);e.target.value='';});

function setProg(v){['prog-pp','prog-modal'].forEach(id=>{const el=document.getElementById(id);if(el)el.style.width=v+'%';});}
function setStat(msg,ok){['status-pp','status-modal'].forEach(id=>{const el=document.getElementById(id);if(!el)return;el.textContent=msg;el.style.color=ok===true?'var(--lime-d)':ok===false?'#DC2626':'var(--tx3)';});}

function processFile(file){
  setStat('📂 Lendo arquivo…'); setProg(10);
  const ext=file.name.split('.').pop().toLowerCase();
  const reader=new FileReader();
  reader.onerror=()=>setStat('❌ Erro ao ler o arquivo.',false);
  reader.onload=e=>{
    setProg(45);
    try{
      let rows; if(['csv','tsv','txt'].includes(ext)) rows=parseCSV(e.target.result); else rows=parseXLS(new Uint8Array(e.target.result));
      if(!rows||rows.length<2){setStat('❌ Arquivo vazio.',false);return;}
      setProg(75);
      const result=mergePP(rows);
      setProg(100); setStat('✅ '+result.msg,true);
      closeModal(); renderImpAll(); updateHeroFromPPI(); showToast('✅ '+result.msg);
      document.getElementById('import-empty-state').style.display='none';
      document.getElementById('import-results').style.display='block';
      switchTab('importar',document.querySelector('.tab:nth-child(5)'));
    }catch(err){setStat('❌ '+err.message,false);console.error(err);}
  };
  if(['csv','tsv','txt'].includes(ext)) reader.readAsText(file,'UTF-8'); else reader.readAsArrayBuffer(file);
}

function parseCSV(raw){const lines=raw.replace(/\r\n/g,'\n').replace(/\r/g,'\n').trim().split('\n');const sep=lines[0].includes('\t')?'\t':lines[0].includes(';')?';':',';return lines.map(l=>l.split(sep).map(v=>v.trim().replace(/^"|"$/g,'')));}

function parseXLS(bytes){
  if(bytes[0]!==0xD0||bytes[1]!==0xCF||bytes[2]!==0x11||bytes[3]!==0xE0) throw new Error('Formato não reconhecido. Use XLS (Excel 97-2003) ou CSV.');
  const SS=Math.pow(2,(bytes[0x1F]<<8)|bytes[0x1E]);
  const getU16=o=>bytes[o]|(bytes[o+1]<<8);const getU32=o=>bytes[o]|(bytes[o+1]<<8)|(bytes[o+2]<<16)|(bytes[o+3]<<24);
  const fat=[];for(let i=0;i<109;i++){const sec=getU32(0x4C+i*4);if(sec>=0xFFFFFFFE)break;const off=(sec+1)*SS;for(let j=0;j<SS;j+=4)fat.push(getU32(off+j));}
  const firstDir=getU32(0x30);let wbSec=-1,wbSize=0;{let sec=firstDir;const vis=new Set();while(sec>=0&&sec<0xFFFFFFFE&&!vis.has(sec)&&sec<fat.length){vis.add(sec);const off=(sec+1)*SS;for(let j=0;j+128<=SS;j+=128){const base=off+j;if(base+128>bytes.length)break;const nlen=getU16(base+64);if(!nlen)continue;let nm='';for(let k=0;k<Math.min(nlen-2,62);k+=2)nm+=String.fromCharCode(getU16(base+k));if(nm==='Workbook'){wbSec=getU32(base+116);wbSize=getU32(base+120);}}sec=fat[sec]??0xFFFFFFFE;}}
  if(wbSec<0)throw new Error('Stream Workbook não encontrado.');
  const wb=new Uint8Array(wbSize);let pos=0,sec=wbSec;const vis2=new Set();while(sec>=0&&sec<0xFFFFFFFE&&!vis2.has(sec)&&sec<fat.length&&pos<wbSize){vis2.add(sec);const off=(sec+1)*SS;const chunk=Math.min(SS,wbSize-pos);wb.set(bytes.slice(off,off+chunk),pos);pos+=chunk;sec=fat[sec]??0xFFFFFFFE;}
  const rows={};const sst=[];let sstBuf=null;let p=0;
  const wbU16=o=>wb[o]|(wb[o+1]<<8);const wbU32=o=>wb[o]|(wb[o+1]<<8)|(wb[o+2]<<16)|(wb[o+3]<<24);
  const wbF64=o=>{const buf=new ArrayBuffer(8);new Uint8Array(buf).set(wb.slice(o,o+8));return new DataView(buf).getFloat64(0,true);};
  const dec=new TextDecoder('windows-1252');
  while(p+4<=wb.length){
    const rt=wbU16(p),rl=wbU16(p+2);if(p+4+rl>wb.length)break;
    if(rt===0x00FC){sstBuf=wb.slice(p+4,p+4+rl);}
    else if(rt===0x003C&&sstBuf!==null){const prev=sstBuf,cur=wb.slice(p+4,p+4+rl);const combined=new Uint8Array(prev.length+cur.length);combined.set(prev);combined.set(cur,prev.length);sstBuf=combined;}
    else if(sstBuf!==null&&rt!==0x003C){
      const sb=sstBuf;const sbU16=o=>sb[o]|(sb[o+1]<<8);const sbU32=o=>sb[o]|(sb[o+1]<<8)|(sb[o+2]<<16)|(sb[o+3]<<24);
      if(sb.length>=8){const unique=sbU32(4);let sp=8;for(let u=0;u<unique;u++){if(sp+3>sb.length)break;try{const nc=sbU16(sp);const fl=sb[sp+2];sp+=3;let cRuns=0,cbExt=0;if(fl&8){if(sp+2>sb.length)break;cRuns=sbU16(sp);sp+=2;}if(fl&4){if(sp+4>sb.length)break;cbExt=sbU32(sp);sp+=4;}if(fl&1){let s='';for(let k=0;k<nc&&sp+1<sb.length;k++){s+=String.fromCharCode(sbU16(sp));sp+=2;}sst.push(s);}else{sst.push(dec.decode(sb.slice(sp,sp+nc)));sp+=nc;}sp+=cRuns*4+cbExt;}catch(e){break;}}}
      sstBuf=null;
    }
    if(rt===0x0203&&rl>=14){const r=wbU16(p+4),c=wbU16(p+6),v=wbF64(p+10);if(!rows[r])rows[r]={};rows[r][c]=v;}
    else if(rt===0x027E&&rl>=10){const r=wbU16(p+4),c=wbU16(p+6),rk=wbU32(p+10);let v;if(rk&2)v=rk>>2;else{const buf=new ArrayBuffer(8);const dv2=new DataView(buf);dv2.setUint32(4,rk&0xFFFFFFFC,true);v=dv2.getFloat64(0,true);}if(rk&1)v/=100;if(!rows[r])rows[r]={};rows[r][c]=v;}
    else if(rt===0x00FD&&rl>=8){const r=wbU16(p+4),c=wbU16(p+6),idx=wbU32(p+10);if(!rows[r])rows[r]={};rows[r][c]=idx<sst.length?sst[idx]:'';}
    else if(rt===0x0204&&rl>=8){const r=wbU16(p+4),c=wbU16(p+6),n=wbU16(p+10);if(!rows[r])rows[r]={};rows[r][c]=dec.decode(wb.slice(p+12,p+12+n));}
    else if(rt===0x00BD&&rl>=6){const r=wbU16(p+4);let fc=wbU16(p+6),off2=p+8;while(off2+6<=p+4+rl){const rk=wbU32(off2+2);let v;if(rk&2)v=rk>>2;else{const buf=new ArrayBuffer(8);const dv2=new DataView(buf);dv2.setUint32(4,rk&0xFFFFFFFC,true);v=dv2.getFloat64(0,true);}if(rk&1)v/=100;if(!rows[r])rows[r]={};rows[r][fc]=v;fc++;off2+=6;}}
    p+=4+rl;
  }
  const maxRow=Math.max(0,...Object.keys(rows).map(Number));
  return Array.from({length:maxRow+1},(_,r)=>{const row=rows[r]||{};const maxCol=Object.keys(row).length?Math.max(...Object.keys(row).map(Number)):0;return Array.from({length:maxCol+1},(_,c)=>row[c]??'');});
}

function xlDate(n){if(!n||n<1)return null;const d=new Date(1899,11,30);d.setDate(d.getDate()+Math.floor(n));return d.toISOString().slice(0,10);}
function parseDate(raw){if(typeof raw==='number'&&raw>1)return xlDate(raw);if(typeof raw==='string'&&raw.length>=8){const m1=raw.match(/^(\d{2})\/(\d{2})\/(\d{4})/);const m2=raw.match(/^(\d{4})-(\d{2})-(\d{2})/);if(m1)return `${m1[3]}-${m1[2]}-${m1[1]}`;if(m2)return raw.slice(0,10);}return null;}
function parseVal(v){if(typeof v==='number')return v;return parseFloat(String(v||0).replace(/\./g,'').replace(',','.'))||0;}

function mergePP(rows){
  const hdr=(rows[0]||[]).map(h=>String(h||'').toLowerCase());
  const fi=(cands,exact=[])=>{for(const c of exact){const i=hdr.findIndex(h=>h===c);if(i>=0)return i;}for(const c of cands){const i=hdr.findIndex(h=>h.includes(c));if(i>=0)return i;}return -1;};
  let iDt=20,iPP=15;
  const d2=fi(['dt.pagamento','pagamento'],['dt.pagamento']);if(d2>=0)iDt=d2;
  const p2=fi(['pague play (','pague play'],['pague play (24,96%)']);if(p2>=0)iPP=p2;
  const byDay={};let records=0;
  for(let r=1;r<rows.length;r++){
    const row=rows[r];if(!row?.length)continue;
    const dt=parseDate(row[iDt]);if(!dt)continue;
    const val=parseVal(row[iPP]);if(val<=0)continue;
    if(!byDay[dt])byDay[dt]={val:0,n:0};
    byDay[dt].val+=val;byDay[dt].n++;records++;
  }
  if(records===0)throw new Error(`Nenhum dado PaguePay encontrado. Verifique o arquivo.`);
  const round2=x=>Math.round(x*100)/100;
  Object.keys(byDay).forEach(k=>byDay[k].val=round2(byDay[k].val));
  const byMonth={},byWeek={};
  Object.entries(byDay).forEach(([dk,v])=>{
    const mk=dk.slice(0,7);const dt=new Date(dk+'T12:00:00');const[wy,wn]=getISOWeek(dt);const wk=`${wy}-W${String(wn).padStart(2,'0')}`;
    if(!byMonth[mk])byMonth[mk]={val:0,n:0,days:0};byMonth[mk].val=round2(byMonth[mk].val+v.val);byMonth[mk].n+=v.n;byMonth[mk].days++;
    if(!byWeek[wk])byWeek[wk]={val:0,n:0,days:0};byWeek[wk].val=round2(byWeek[wk].val+v.val);byWeek[wk].n+=v.n;byWeek[wk].days++;
  });
  PPI={byDay,byMonth,byWeek};
  try{
    localStorage.removeItem('ppi_v2');
    const compact={byMonth:PPI.byMonth,byWeek:PPI.byWeek,byDayKeys:Object.fromEntries(Object.entries(PPI.byDay).map(([k,v])=>[k,v.val]))};
    localStorage.setItem('ppi_v2',JSON.stringify(compact));
  }catch(e){ console.warn('localStorage cheio — dados em memória'); }
  return {msg:`${records} registros · ${Object.keys(byDay).length} dias · ${Object.keys(byMonth).length} meses`};
}

// ── IMPORT RENDER ──
function setImpFilter(f,btn){impFilter=f;document.querySelectorAll('#imp-pills .pill').forEach(p=>p.classList.remove('active'));btn.classList.add('active');renderImpCharts();renderImpTables();}

function renderImpAll(){
  if(!PPI)return;
  renderImpHero();renderImpFilters();renderImpCharts();renderImpTables();
}

function renderImpHero(){
  if(!PPI)return;
  const months=Object.keys(PPI.byMonth).sort();const totalAno=Object.values(PPI.byMonth).reduce((s,m)=>s+m.val,0);
  const curMk=months[months.length-1]||'';const curM=PPI.byMonth[curMk]||{val:0,n:0,days:0};
  const[cy,cm]=curMk.split('-')||['2026','04'];
  document.getElementById('imp-mes-lbl').textContent=(MNAMES[cm]||cm).toUpperCase()+' '+cy;
  document.getElementById('imp-mes-val').textContent=curM.val.toLocaleString('pt-BR',{minimumFractionDigits:2,maximumFractionDigits:2});
  document.getElementById('imp-mes-meta').textContent=`${curM.n.toLocaleString('pt-BR')} registros`;
  document.getElementById('imp-mes-dias').textContent=curM.days+' dias';
  document.getElementById('imp-mes-avg').textContent=fBRk(curM.days>0?curM.val/curM.days:0);
  const avgMes=months.length>0?totalAno/months.length:0;
  document.getElementById('imp-ano-lbl').textContent='TOTAL '+cy;
  document.getElementById('imp-ano-val').textContent=totalAno.toLocaleString('pt-BR',{minimumFractionDigits:2,maximumFractionDigits:2});
  document.getElementById('imp-ano-meta').textContent=`${Object.values(PPI.byMonth).reduce((s,m)=>s+m.n,0).toLocaleString('pt-BR')} registros`;
  document.getElementById('imp-ano-meses').textContent=months.length+' meses';
  document.getElementById('imp-ano-avg').textContent=fBRk(avgMes);
}

function renderImpFilters(){
  if(!PPI)return;const months=Object.keys(PPI.byMonth).sort();const row=document.getElementById('imp-pills');
  [...row.querySelectorAll('.pill[data-m]')].forEach(p=>p.remove());
  months.forEach(mk=>{const[y,m]=mk.split('-');const btn=document.createElement('button');btn.className='pill';btn.dataset.m=mk;btn.textContent=MSNAMES[m]+'/'+y.slice(2);btn.onclick=function(){setImpFilter(mk,this);};row.appendChild(btn);});
}

function renderImpCharts(){
  if(!PPI)return;
  const months=Object.keys(PPI.byMonth).sort();const labels=months.map(mk=>{const[y,m]=mk.split('-');return MSNAMES[m]+'/'+y.slice(2);});
  const maxM=Math.max(...months.map(mk=>PPI.byMonth[mk].val));
  if(chartImpMes)chartImpMes.destroy();
  chartImpMes=new Chart(document.getElementById('chart-imp-mes'),{type:'bar',data:{labels,datasets:[{label:'PaguePay',data:months.map(mk=>PPI.byMonth[mk].val),backgroundColor:months.map(mk=>PPI.byMonth[mk].val===maxM?'rgba(101,163,13,.88)':'rgba(163,230,53,.45)'),borderColor:'rgba(101,163,13,.6)',borderWidth:2,borderRadius:6}]},options:{...CG,plugins:{...CG.plugins,legend:{display:false}}}});
  let weeks=Object.keys(PPI.byWeek).sort();
  if(impFilter!=='all')weeks=weeks.filter(wk=>Object.keys(PPI.byDay).some(dk=>dk.startsWith(impFilter)&&(()=>{const dt=new Date(dk+'T12:00:00');const[wy,wn]=getISOWeek(dt);return wk===`${wy}-W${String(wn).padStart(2,'0')}`;})()));
  const maxW=weeks.length?Math.max(...weeks.map(w=>PPI.byWeek[w]?.val||0)):1;
  if(chartImpSem)chartImpSem.destroy();
  chartImpSem=new Chart(document.getElementById('chart-imp-sem'),{type:'bar',data:{labels:weeks.map(w=>w.replace(/^\d+-/,'')),datasets:[{label:'PaguePay',data:weeks.map(w=>PPI.byWeek[w]?.val||0),backgroundColor:weeks.map(w=>(PPI.byWeek[w]?.val||0)===maxW?'rgba(101,163,13,.85)':'rgba(163,230,53,.4)'),borderColor:'rgba(101,163,13,.5)',borderWidth:1.5,borderRadius:4}]},options:{...CG,plugins:{...CG.plugins,legend:{display:false}}}});
  let days=Object.keys(PPI.byDay).sort();if(impFilter!=='all')days=days.filter(d=>d.startsWith(impFilter));
  const cnt=days.length;document.getElementById('imp-dia-badge').textContent=cnt+' dias';
  const maxD=days.length?Math.max(...days.map(d=>PPI.byDay[d].val)):1;
  if(chartImpDia)chartImpDia.destroy();
  chartImpDia=new Chart(document.getElementById('chart-imp-dia'),{type:'bar',data:{labels:days.map(d=>{const[,m,dd]=d.split('-');return dd+'/'+m;}),datasets:[{label:'PaguePay',data:days.map(d=>PPI.byDay[d].val),backgroundColor:days.map(d=>PPI.byDay[d].val===maxD?'rgba(101,163,13,.88)':'rgba(163,230,53,.38)'),borderColor:'rgba(101,163,13,.5)',borderWidth:1,borderRadius:3}]},options:{...CG,scales:{...CG.scales,x:{...CG.scales.x,ticks:{...CG.scales.x.ticks,maxRotation:45,callback:(_,i,tks)=>cnt>30&&i%Math.max(1,Math.floor(cnt/22))!==0?'':tks[i].label}}},plugins:{...CG.plugins,legend:{display:false}}}});
}

function renderImpTables(){
  if(!PPI)return;
  const totalAno=Object.values(PPI.byMonth).reduce((s,m)=>s+m.val,0);
  const months=Object.keys(PPI.byMonth).sort();const maxM=Math.max(...months.map(mk=>PPI.byMonth[mk].val));
  document.getElementById('tb-imp-mes').innerHTML=months.map(mk=>{const m=PPI.byMonth[mk];const[y,mo]=mk.split('-');const pct=((m.val/totalAno)*100).toFixed(1);const avg=m.days>0?m.val/m.days:0;const bar=Math.round(m.val/maxM*44);return `<tr><td class="key"><span style="display:inline-block;width:${bar}px;height:3px;background:var(--lime);border-radius:2px;margin-right:6px;vertical-align:middle"></span>${MNAMES[mo]} ${y}</td><td class="mo c-lime">${fBR(m.val)}</td><td class="cn">${m.days}</td><td class="cn">${m.n}</td><td class="mo" style="color:var(--tx2)">${fBR(Math.round(avg*100)/100)}</td><td class="cn">${pct}%</td></tr>`;}).join('');
  const tN=Object.values(PPI.byMonth).reduce((s,m)=>s+m.n,0);const tD=Object.values(PPI.byMonth).reduce((s,m)=>s+m.days,0);
  document.getElementById('tf-imp-mes').innerHTML=`<tr><td class="key">TOTAL</td><td class="mo c-lime">${fBR(Math.round(totalAno*100)/100)}</td><td class="cn">${tD}</td><td class="cn">${tN}</td><td class="mo" style="color:var(--tx2)">${fBR(Math.round(totalAno/Math.max(tD,1)*100)/100)}</td><td class="cn">100%</td></tr>`;
  let weeks=Object.keys(PPI.byWeek).sort();if(impFilter!=='all')weeks=weeks.filter(wk=>Object.keys(PPI.byDay).some(dk=>dk.startsWith(impFilter)&&(()=>{const dt=new Date(dk+'T12:00:00');const[wy,wn]=getISOWeek(dt);return wk===`${wy}-W${String(wn).padStart(2,'0')}`;})()));
  const totSemV=weeks.reduce((s,wk)=>s+(PPI.byWeek[wk]?.val||0),0);const totSemN=weeks.reduce((s,wk)=>s+(PPI.byWeek[wk]?.n||0),0);const totSemD=weeks.reduce((s,wk)=>s+(PPI.byWeek[wk]?.days||0),0);
  document.getElementById('tb-imp-sem').innerHTML=weeks.map(wk=>{const w=PPI.byWeek[wk];return `<tr><td class="key">${wk}</td><td style="font-size:11px;color:var(--tx3)">${weekRange(wk)}</td><td class="mo c-lime">${fBR(w.val)}</td><td class="cn">${w.days}</td><td class="cn">${w.n}</td></tr>`;}).join('');
  document.getElementById('tf-imp-sem').innerHTML=`<tr><td class="key">TOTAL</td><td></td><td class="mo c-lime">${fBR(Math.round(totSemV*100)/100)}</td><td class="cn">${totSemD}</td><td class="cn">${totSemN}</td></tr>`;
  let days=Object.keys(PPI.byDay).sort();if(impFilter!=='all')days=days.filter(d=>d.startsWith(impFilter));
  const mesTotal=impFilter==='all'?totalAno:(PPI.byMonth[impFilter]?.val||1);let sumV=0,sumN=0;const maxDv=days.length?Math.max(...days.map(d=>PPI.byDay[d].val)):1;
  document.getElementById('tb-imp-dia').innerHTML=days.map(dk=>{const d=PPI.byDay[dk];const isMax=d.val===maxDv;const pct=((d.val/mesTotal)*100).toFixed(2);sumV+=d.val;sumN+=d.n;return `<tr${isMax?' style="background:rgba(101,163,13,.06)"':''}><td class="key"${isMax?' style="color:var(--lime)"':''}>${fDate(dk)}${isMax?' 🏆':''}</td><td style="font-size:11px;color:var(--tx3)">${wdayOf(dk)}</td><td class="mo c-lime">${fBR(d.val)}</td><td class="cn">${d.n}</td><td class="cn">${pct}%</td></tr>`;}).join('');
  document.getElementById('tf-imp-dia').innerHTML=`<tr><td class="key">TOTAL</td><td></td><td class="mo c-lime">${fBR(Math.round(sumV*100)/100)}</td><td class="cn">${sumN}</td><td class="cn"></td></tr>`;
}

function resetImport(){if(!confirm('Limpar dados importados?'))return;PPI=null;localStorage.removeItem('ppi_v2');document.getElementById('import-results').style.display='none';document.getElementById('import-empty-state').style.display='block';setProg(0);setStat('');}

function showToast(msg){const t=document.getElementById('toast');t.textContent=msg;t.classList.add('show');setTimeout(()=>t.classList.remove('show'),3500);}


// ── ATUALIZA HERO COM DADOS IMPORTADOS ──
function updateHeroFromPPI(){
  if(!PPI||!PPI.byMonth) return;
  const months = Object.keys(PPI.byMonth).sort();
  const maxPP = Math.max(...months.map(mk=>PPI.byMonth[mk].val));
  let total=0, totalN=0, totalDays=0;
  months.forEach(mk=>{
    const m=PPI.byMonth[mk];
    total+=m.val; totalN+=m.n; totalDays+=m.days;
  });
  // Update hero banner totals
  document.getElementById('h-total').textContent=total.toLocaleString('pt-BR',{minimumFractionDigits:2,maximumFractionDigits:2});
  document.getElementById('h-dias').textContent=totalDays;
  document.getElementById('h-meses').textContent=months.length;
  document.getElementById('h-regs').textContent=totalN.toLocaleString('pt-BR');
  // Update last day
  const days=Object.keys(PPI.byDay||{});
  if(days.length){ const last=days.sort().pop(); document.getElementById('h-last').textContent=fDate(last); }
  // Update month KPI cards in hero
  const mk2id={'2026-01':'jan','2026-02':'fev','2026-03':'mar','2026-04':'abr'};
  months.forEach(mk=>{
    const id=mk2id[mk]; if(!id) return;
    const m=PPI.byMonth[mk];
    const el=document.getElementById('hk-'+id);
    if(el) el.textContent=fBR(m.val);
    const sub=document.getElementById('hks-'+id);
    if(sub) sub.textContent=m.days+' dias · '+m.n.toLocaleString('pt-BR')+' reg';
    const bar=document.getElementById('hkb-'+id);
    if(bar) bar.style.width=Math.round(m.val/maxPP*100)+'%';
  });
  // Update month cards section
  updateMonthCardsFromPPI();
}

function updateMonthCardsFromPPI(){
  if(!PPI||!PPI.byMonth) return;
  const months=Object.keys(PPI.byMonth).sort();
  const maxPP=Math.max(...months.map(mk=>PPI.byMonth[mk].val));
  const mColors={'2026-01':'mcard-jan','2026-02':'mcard-fev','2026-03':'mcard-mar','2026-04':'mcard-abr'};
  const ppColors={'2026-01':'#3B82F6','2026-02':'#7C3AED','2026-03':'#059669','2026-04':'var(--lime)'};
  document.getElementById('month-cards').innerHTML=months.map(mk=>{
    const m=PPI.byMonth[mk]; const[y,mo]=mk.split('-');
    const avgDay=m.days>0?m.val/m.days:0; const pct=Math.round(m.val/maxPP*100);
    return `<div class="mcard ${mColors[mk]||''}">
      <div class="mcard-head">
        <div class="mcard-title">${MNAMES[mo]} ${y}</div>
        <div class="mcard-badge">${m.n.toLocaleString('pt-BR')} reg</div>
      </div>
      <div class="mcard-pp" style="color:${ppColors[mk]||'var(--lime)'}">${fBR(m.val)}</div>
      <div class="mcard-rec">Importado · ${m.days} dias com movimento</div>
      <div class="mcard-stat">
        <div class="mstat"><div class="mstat-lbl">Dias</div><div class="mstat-val">${m.days}</div></div>
        <div class="mstat"><div class="mstat-lbl">Média/Dia</div><div class="mstat-val" style="color:${ppColors[mk]||'var(--lime)'}">${fBRk(avgDay)}</div></div>
        <div class="mstat"><div class="mstat-lbl">PP/Dia</div><div class="mstat-val">${fBRk(m.val/m.days)}</div></div>
      </div>
      <div class="mcard-prog"><div class="mcard-prog-fill" style="background:${ppColors[mk]||'var(--lime)'};width:${pct}%"></div></div>
    </div>`;
  }).join('');
}

// ── BOOT ──
initHero();
renderMonthCards();
renderDia();
renderSem();
renderMes();
renderCoren();
if(PPI){document.getElementById('import-empty-state').style.display='none';document.getElementById('import-results').style.display='block';renderImpAll();updateHeroFromPPI();}
</script>
</body>
</html>
