<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gogolook 走著瞧｜未來三年估值預測報告</title>
<style>
  :root {
    --primary: #0d2b55;
    --accent: #1e5fa8;
    --gold: #c8932a;
    --red: #c0392b;
    --green: #1a7a4a;
    --gray: #4a5568;
    --light: #f0f4fa;
    --border: #cfd8e8;
    --text: #1a2535;
    --white: #ffffff;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    font-family: 'Segoe UI','Microsoft JhengHei','PingFang TC',sans-serif;
    font-size: 10.5px;
    color: var(--text);
    background: #e8edf5;
    line-height: 1.3;
  }

  /* ── CONFIDENTIAL BANNER ── */
  .conf-banner {
    background: #8b0000;
    color: #fff;
    text-align: center;
    padding: 5px 0;
    font-size: 10.5px;
    font-weight: 700;
    letter-spacing: 2px;
    position: sticky;
    top: 0;
    z-index: 9999;
    border-bottom: 2px solid #ff4444;
  }

  /* ── SLIDES WRAPPER ── */
  .slide-container { max-width: 1100px; margin: 0 auto; padding: 8px 8px 20px; }

  /* ── EACH SLIDE ── */
  .slide {
    background: var(--white);
    border-radius: 6px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.12);
    margin-bottom: 10px;
    overflow: hidden;
    page-break-inside: avoid;
  }

  /* ── SLIDE HEADER ── */
  .slide-header {
    background: linear-gradient(135deg, var(--primary) 0%, var(--accent) 100%);
    color: white;
    padding: 10px 14px 8px;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
  }
  .slide-header h2 {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.5px;
  }
  .slide-header .slide-no {
    font-size: 9px;
    opacity: 0.7;
    font-weight: 400;
  }
  .slide-body { padding: 12px; }

  /* ── COVER SLIDE ── */
  .slide-cover {
    background: linear-gradient(160deg, #051c3f 0%, #0d2b55 40%, #1e5fa8 100%);
    color: white;
    padding: 24px 20px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .slide-cover::before {
    content: '';
    position: absolute;
    top: -40px; right: -40px;
    width: 220px; height: 220px;
    border-radius: 50%;
    background: rgba(255,255,255,0.04);
  }
  .slide-cover::after {
    content: '';
    position: absolute;
    bottom: -30px; left: -30px;
    width: 160px; height: 160px;
    border-radius: 50%;
    background: rgba(200,147,42,0.12);
  }
  .slide-cover .conf-tag {
    display: inline-block;
    background: #8b0000;
    color: #fff;
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 2px;
    padding: 3px 10px;
    border-radius: 2px;
    margin-bottom: 12px;
    border: 1px solid rgba(255,68,68,0.5);
  }
  .slide-cover .company-logo {
    font-size: 24px;
    font-weight: 900;
    letter-spacing: -1px;
    margin-bottom: 4px;
    color: #fff;
  }
  .slide-cover .company-logo span { color: var(--gold); }
  .slide-cover .subtitle {
    font-size: 12px;
    font-weight: 700;
    margin-bottom: 8px;
    color: rgba(255,255,255,0.9);
  }
  .slide-cover .meta {
    font-size: 9px;
    color: rgba(255,255,255,0.55);
    margin-bottom: 14px;
  }
  .cover-badges {
    display: flex;
    justify-content: center;
    gap: 1px;
    flex-wrap: wrap;
    margin-bottom: 10px;
  }
  .cover-badge {
    background: rgba(255,255,255,0.12);
    border: 1px solid rgba(255,255,255,0.2);
    color: rgba(255,255,255,0.85);
    font-size: 9px;
    padding: 3px 8px;
    border-radius: 20px;
  }
  .cover-kpis {
    display: grid;
    grid-template-columns: repeat(4,1fr);
    gap: 1px;
    margin-top: 10px;
  }
  .cover-kpi {
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.12);
    border-radius: 4px;
    padding: 8px 4px;
    text-align: center;
  }
  .cover-kpi .kpi-val {
    font-size: 14px;
    font-weight: 800;
    color: var(--gold);
    display: block;
  }
  .cover-kpi .kpi-lbl {
    font-size: 8.5px;
    color: rgba(255,255,255,0.6);
    margin-top: 1px;
    display: block;
  }

  /* ── SECTION TITLE ── */
  .sec-title {
    font-size: 11px;
    font-weight: 700;
    color: var(--primary);
    border-left: 3px solid var(--gold);
    padding-left: 7px;
    margin-bottom: 7px;
  }

  /* ── GRID LAYOUTS ── */
  .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 1px; }
  .grid-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 1px; }
  .grid-4 { display: grid; grid-template-columns: repeat(4,1fr); gap: 1px; }
  .grid-2-1 { display: grid; grid-template-columns: 2fr 1fr; gap: 1px; }

  /* ── CARDS ── */
  .card {
    background: var(--light);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 12px;
  }
  .card-title {
    font-size: 11px;
    font-weight: 700;
    color: var(--primary);
    margin-bottom: 5px;
  }
  .card-subtitle {
    font-size: 9px;
    color: var(--gray);
    margin-bottom: 5px;
  }

  /* ── INSIGHT LIST ── */
  .insight-list { list-style: none; }
  .insight-item {
    padding: 3px 0 3px 14px;
    position: relative;
    font-size: 10.5px;
    color: var(--text);
    border-bottom: 1px solid rgba(0,0,0,0.04);
    margin-bottom: 4px;
    line-height: 1.3;
  }
  .insight-item::before {
    content: '▸';
    position: absolute;
    left: 0;
    color: var(--accent);
    font-size: 9px;
  }
  .insight-item.warn::before { color: #e67e22; content: '⚠'; font-size: 8px; }
  .insight-item.ok::before { color: var(--green); content: '✓'; }
  .insight-item strong { color: var(--primary); font-weight: 700; }

  /* ── SCENARIO CARDS ── */
  .scenario-conservative { border-top: 3px solid #3498db; }
  .scenario-balanced     { border-top: 3px solid var(--green); }
  .scenario-aggressive   { border-top: 3px solid #e74c3c; }
  .scenario-label {
    display: inline-block;
    font-size: 9px;
    font-weight: 700;
    padding: 2px 7px;
    border-radius: 3px;
    margin-bottom: 5px;
    letter-spacing: 0.5px;
  }
  .label-c { background: #d6eaf8; color: #1a5276; }
  .label-b { background: #d5f5e3; color: #1a5e38; }
  .label-a { background: #fde8e7; color: #922b21; }

  /* ── FORECAST TABLE ── */
  .forecast-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 10.5px;
  }
  .forecast-table th {
    background: var(--primary);
    color: white;
    padding: 5px 6px;
    text-align: center;
    font-size: 10.5px;
    font-weight: 600;
    border-right: 1px solid rgba(255,255,255,0.15);
  }
  .forecast-table td {
    padding: 4px 6px;
    text-align: center;
    border-bottom: 1px solid var(--border);
    border-right: 1px solid var(--border);
    font-size: 10.5px;
    line-height: 1.3;
  }
  .forecast-table tr:nth-child(even) td { background: #f7f9fc; }
  .forecast-table tr:hover td { background: #eaf0fa; }
  .forecast-table .row-label {
    text-align: left;
    font-weight: 700;
    color: var(--primary);
    padding-left: 8px;
    background: #f0f4fa !important;
  }
  .forecast-table .c { color: #1a5276; font-weight: 600; }
  .forecast-table .b { color: #1a5e38; font-weight: 700; }
  .forecast-table .a { color: #922b21; font-weight: 700; }
  .forecast-table .section-divider th {
    background: #2c5282;
    font-size: 9.5px;
    text-align: left;
    padding-left: 10px;
    letter-spacing: 0.5px;
  }

  /* ── KPI BOX ── */
  .kpi-row { display: flex; gap: 1px; margin-bottom: 1px; }
  .kpi-box {
    flex: 1;
    background: var(--light);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 8px 10px;
    text-align: center;
  }
  .kpi-box .val {
    font-size: 15px;
    font-weight: 800;
    color: var(--primary);
    display: block;
    line-height: 1.2;
  }
  .kpi-box .val.positive { color: var(--green); }
  .kpi-box .val.negative { color: var(--red); }
  .kpi-box .val.highlight { color: var(--gold); }
  .kpi-box .lbl {
    font-size: 9px;
    color: var(--gray);
    margin-top: 1px;
  }

  /* ── COMPETITOR TABLE ── */
  .comp-table { width:100%; border-collapse:collapse; font-size:10.5px; }
  .comp-table th {
    background: var(--primary);
    color: white;
    padding: 4px 6px;
    text-align: center;
    font-size: 10.5px;
  }
  .comp-table td {
    padding: 4px 6px;
    border-bottom: 1px solid var(--border);
    text-align: center;
    line-height: 1.3;
  }
  .comp-table tr:nth-child(even) td { background: #f7f9fc; }
  .comp-table .highlight-row td { background: #fffbe6 !important; font-weight: 700; }
  .comp-table .name-col { text-align: left; font-weight: 600; color: var(--primary); }
  .tag { display:inline-block; font-size:8.5px; padding:1px 5px; border-radius:2px; margin:0 1px; }
  .tag-up { background:#d5f5e3; color:#1a5e38; }
  .tag-dn { background:#fde8e7; color:#922b21; }
  .tag-na { background:#f0f0f0; color:#666; }

  /* ── RISK TABLE ── */
  .risk-row {
    display: grid;
    grid-template-columns: 2fr 1fr 2fr 2fr;
    gap: 1px;
    margin-bottom: 3px;
    font-size: 10.5px;
  }
  .risk-cell {
    background: var(--light);
    border: 1px solid var(--border);
    border-radius: 3px;
    padding: 6px 8px;
    line-height: 1.3;
  }
  .risk-header .risk-cell {
    background: var(--primary);
    color: white;
    font-weight: 700;
    font-size: 10.5px;
  }
  .badge-h { background:#fde8e7; color:#922b21; border-radius:2px; padding:1px 5px; font-size:9px; font-weight:700; }
  .badge-m { background:#fef9e7; color:#7d6608; border-radius:2px; padding:1px 5px; font-size:9px; font-weight:700; }
  .badge-l { background:#d5f5e3; color:#1a5e38; border-radius:2px; padding:1px 5px; font-size:9px; font-weight:700; }

  /* ── TIMELINE ── */
  .timeline { display:flex; gap:1px; }
  .timeline-phase {
    flex:1;
    border-radius:4px;
    padding: 8px 10px;
    font-size: 10.5px;
  }
  .tp1 { background: #eaf4fd; border-top: 3px solid #3498db; }
  .tp2 { background: #eafaf1; border-top: 3px solid var(--green); }
  .tp3 { background: #fef9e7; border-top: 3px solid #e67e22; }
  .timeline-phase .ph-title {
    font-size: 11px;
    font-weight: 700;
    color: var(--primary);
    margin-bottom: 4px;
  }

  /* ── VALUATION BOX ── */
  .val-method {
    background: var(--light);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 10px 12px;
    margin-bottom: 3px;
  }
  .val-method .method-name {
    font-size: 11px;
    font-weight: 700;
    color: var(--primary);
    margin-bottom: 3px;
  }
  .val-range {
    display: flex;
    gap: 1px;
    margin-top: 4px;
  }
  .val-range-item {
    flex: 1;
    text-align: center;
    border-radius: 3px;
    padding: 5px 4px;
    font-size: 10.5px;
  }
  .vri-c { background: #d6eaf8; }
  .vri-b { background: #d5f5e3; }
  .vri-a { background: #fde8e7; }
  .val-range-item .price { font-size: 13px; font-weight: 800; display:block; line-height:1.2; }
  .val-range-item .price-label { font-size: 8.5px; color: var(--gray); }

  /* ── BUY PRICE HIGHLIGHT ── */
  .buy-box {
    background: linear-gradient(135deg, #0d2b55, #1e5fa8);
    color: white;
    border-radius: 5px;
    padding: 12px;
    text-align: center;
    margin-top: 5px;
  }
  .buy-box .buy-title { font-size: 10.5px; opacity: 0.8; margin-bottom: 4px; }
  .buy-box .buy-price { font-size: 22px; font-weight: 900; color: var(--gold); letter-spacing: -1px; }
  .buy-box .buy-sub { font-size: 9px; opacity: 0.7; margin-top: 2px; }

  /* ── PROGRESS BAR ── */
  .progress-bar-wrap { margin: 3px 0; }
  .progress-label { display:flex; justify-content:space-between; font-size:9.5px; margin-bottom:1px; }
  .progress-bar { height:8px; background:#dde3ee; border-radius:4px; overflow:hidden; }
  .progress-fill { height:100%; border-radius:4px; }

  /* ── REVENUE CHART (visual bar) ── */
  .bar-chart { display:flex; align-items:flex-end; gap:1px; height:70px; padding:0 4px; }
  .bar-group { display:flex; flex-direction:column; align-items:center; flex:1; }
  .bar-wrap { display:flex; gap:1px; align-items:flex-end; width:100%; justify-content:center; }
  .bar { border-radius:2px 2px 0 0; min-width:8px; }
  .bar-c { background: #3498db; }
  .bar-b { background: #27ae60; }
  .bar-a { background: #e74c3c; }
  .bar-actual { background: #0d2b55; }
  .bar-lbl { font-size:8px; color:var(--gray); margin-top:2px; text-align:center; }

  /* ── FOOTER DISCLAIMER ── */
  .disclaimer {
    background: #1a2535;
    color: rgba(255,255,255,0.65);
    font-size: 9px;
    padding: 10px 14px;
    border-radius: 0 0 5px 5px;
    line-height: 1.5;
    text-align: center;
  }

  /* ── DIVIDER ── */
  .divider { border: none; border-top: 1px solid var(--border); margin: 6px 0; }

  /* ── TWO-COL TEXT ── */
  .two-col { display:grid; grid-template-columns:1fr 1fr; gap:1px; }

  /* ── PAIN POINT ── */
  .pain-item {
    display: flex;
    gap: 8px;
    align-items: flex-start;
    background: var(--light);
    border: 1px solid var(--border);
    border-left: 3px solid var(--red);
    border-radius: 4px;
    padding: 8px 10px;
    margin-bottom: 3px;
  }
  .pain-item .pain-icon { font-size: 16px; flex-shrink: 0; line-height: 1; }
  .pain-item .pain-title { font-size: 11px; font-weight: 700; color: var(--red); margin-bottom: 2px; }

  /* ── OPPORTUNITY ITEM ── */
  .opp-item {
    display: flex;
    gap: 8px;
    align-items: flex-start;
    background: #eafaf1;
    border: 1px solid #a9dfbf;
    border-left: 3px solid var(--green);
    border-radius: 4px;
    padding: 8px 10px;
    margin-bottom: 3px;
  }
  .opp-item .opp-icon { font-size: 16px; flex-shrink: 0; line-height: 1; }
  .opp-item .opp-title { font-size: 11px; font-weight: 700; color: var(--green); margin-bottom: 2px; }
</style>
</head>
<body>

<!-- CONFIDENTIAL BANNER -->
<div class="conf-banner">⚠ 內部機密文件 STRICTLY CONFIDENTIAL ─ INTERNAL USE ONLY ─ NOT FOR DISTRIBUTION ⚠</div>

<div class="slide-container">

<!-- ========== SLIDE 1: COVER ========== -->
<div class="slide">
  <div class="slide-cover">
    <div class="conf-tag">🔒 STRICTLY CONFIDENTIAL · INTERNAL VALUATION REPORT</div>
    <div class="company-logo">Gogolook<span>｜走著瞧</span></div>
    <div class="subtitle">未來三年估值預測報告 · 三路線情境分析</div>
    <div class="meta">股票代號：6902.TW　｜　報告日期：2026年3月15日　｜　編製：資深估值分析團隊</div>
    <div class="cover-badges">
      <span class="cover-badge">📊 保守版 · 平衡版 · 激進版</span>
      <span class="cover-badge">🎯 客觀買進價格建議</span>
      <span class="cover-badge">⚖️ 同業估值比較</span>
      <span class="cover-badge">🌏 東南亞市場擴張分析</span>
    </div>
    <div class="cover-kpis">
      <div class="cover-kpi">
        <span class="kpi-val">NT$1.048B</span>
        <span class="kpi-lbl">2025全年營收</span>
      </div>
      <div class="cover-kpi">
        <span class="kpi-val">+20.9%</span>
        <span class="kpi-lbl">年增率</span>
      </div>
      <div class="cover-kpi">
        <span class="kpi-val">NT$1.58</span>
        <span class="kpi-lbl">EPS（歷史新高）</span>
      </div>
      <div class="cover-kpi">
        <span class="kpi-val">NT$77.9</span>
        <span class="kpi-lbl">現股價（2026/3/15）</span>
      </div>
    </div>
  </div>
</div>

<!-- ========== SLIDE 2: 前言 ========== -->
<div class="slide">
  <div class="slide-header">
    <h2>01 ｜ 前言與分析框架</h2>
    <span class="slide-no">02 / 12</span>
  </div>
  <div class="slide-body">
    <div class="grid-2" style="gap:8px;">
      <div>
        <div class="sec-title">公司概述</div>
        <div class="card" style="margin-bottom:6px;">
          <div class="card-title">🏢 Gogolook（走著瞧股份有限公司）</div>
          <div class="card-subtitle">全球信任科技（TrustTech）服務領導廠商</div>
          <ul class="insight-list">
            <li class="insight-item">成立：2012年；總部：台北市；上市代號：TWSE 6902</li>
            <li class="insight-item">核心產品：<strong>Whoscall</strong>（東亞/東南亞最大號碼資料庫）</li>
            <li class="insight-item">三大業務：消費者防詐、企業端信任雲、金融科技服務</li>
            <li class="insight-item">已獲 Google Play「2025年度最佳應用程式」殊榮</li>
            <li class="insight-item">泰國設立東南亞區域總部，積極擴展7億人口市場</li>
            <li class="insight-item">2025年完成「獲利元年」，四季度連續本業獲利</li>
          </ul>
        </div>
        <div class="card">
          <div class="card-title">📐 本報告分析框架</div>
          <ul class="insight-list">
            <li class="insight-item">基礎財務年份：FY2021–FY2025（5年歷史數據）</li>
            <li class="insight-item">預測期間：2026E–2028E（3年前瞻）</li>
            <li class="insight-item">估值方法：<strong>EV/Revenue + Forward P/E + P/B + 同業比較法</strong></li>
            <li class="insight-item">同業參照：TrueCaller（同類最直接競爭對手）</li>
            <li class="insight-item">三路線定義：<span class="tag tag-up">保守</span><span class="tag" style="background:#d5f5e3;color:#1a5e38">平衡</span><span class="tag tag-dn">激進</span></li>
          </ul>
        </div>
      </div>
      <div>
        <div class="sec-title">歷史財務摘要（NT$M）</div>
        <table class="forecast-table" style="margin-bottom:6px;">
          <tr>
            <th class="row-label">財務指標</th>
            <th>FY2022</th>
            <th>FY2023</th>
            <th>FY2024</th>
            <th style="background:#c8932a;">FY2025</th>
          </tr>
          <tr>
            <td class="row-label">合併營收</td>
            <td>420</td><td>774</td><td>867</td><td style="font-weight:800;color:#0d2b55;">1,048</td>
          </tr>
          <tr>
            <td class="row-label">YoY成長率</td>
            <td>+64%</td><td>+84%</td><td>+12%</td><td style="color:var(--green);font-weight:700;">+21%</td>
          </tr>
          <tr>
            <td class="row-label">毛利率</td>
            <td>85.5%</td><td>91.4%</td><td>90.6%</td><td style="font-weight:700;">88.3%</td>
          </tr>
          <tr>
            <td class="row-label">營業利益</td>
            <td style="color:var(--red);">-76</td><td>+12</td><td style="color:var(--red);">-53</td><td style="color:var(--green);font-weight:700;">+63</td>
          </tr>
          <tr>
            <td class="row-label">稅後淨利</td>
            <td style="color:var(--red);">-57</td><td>+5</td><td style="color:var(--red);">-40</td><td style="color:var(--green);font-weight:700;">+54</td>
          </tr>
          <tr>
            <td class="row-label">EPS（元）</td>
            <td style="color:var(--red);">-1.90</td><td>+0.16</td><td style="color:var(--red);">-1.24</td><td style="color:var(--green);font-weight:800;">+1.58</td>
          </tr>
        </table>
        <div class="card">
          <div class="card-title">📊 2025年Q4營業利益爆發</div>
          <div style="font-size:10px;color:var(--gray);margin-bottom:5px;">四季度季度營業利益（NT$M）</div>
          <div class="bar-chart" style="height:60px;">
            <div class="bar-group">
              <div class="bar-wrap">
                <div class="bar bar-actual" style="height:4px;"></div>
              </div>
              <div class="bar-lbl">Q4'24<br>-0.5</div>
            </div>
            <div class="bar-group">
              <div class="bar-wrap">
                <div class="bar bar-actual" style="height:8px;"></div>
              </div>
              <div class="bar-lbl">Q1'25<br>3.9</div>
            </div>
            <div class="bar-group">
              <div class="bar-wrap">
                <div class="bar bar-actual" style="height:20px;"></div>
              </div>
              <div class="bar-lbl">Q2'25<br>12.4</div>
            </div>
            <div class="bar-group">
              <div class="bar-wrap">
                <div class="bar bar-actual" style="height:16px;"></div>
              </div>
              <div class="bar-lbl">Q3'25<br>10.0</div>
            </div>
            <div class="bar-group">
              <div class="bar-wrap">
                <div class="bar" style="background:#c8932a;height:55px;"></div>
              </div>
              <div class="bar-lbl" style="font-weight:800;color:#c8932a;">Q4'25<br>37.0🔥</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ========== SLIDE 3: 痛點分析 ========== -->
<div class="slide">
  <div class="slide-header">
    <h2>02 ｜ 痛點分析 × 成長機遇</h2>
    <span class="slide-no">03 / 12</span>
  </div>
  <div class="slide-body">
    <div class="grid-2" style="gap:8px;">
      <div>
        <div class="sec-title" style="color:var(--red);">⚠ 核心痛點</div>
        <div class="pain-item">
          <div class="pain-icon">🔥</div>
          <div>
            <div class="pain-title">估值曾長期被壓制</div>
            <div style="font-size:10.5px;">連續虧損3年（2021-2024），市場缺乏獲利基準；EV/Revenue 2.57x低於同業（TrueCaller 3.4x），反映估值折價。</div>
          </div>
        </div>
        <div class="pain-item">
          <div class="pain-icon">⚡</div>
          <div>
            <div class="pain-title">自由現金流持續為負</div>
            <div style="font-size:10.5px;">FY2025自由現金流 -NT$159M，源於資本支出增加及研發持續投入；若不能轉正，將面臨融資壓力。</div>
          </div>
        </div>
        <div class="pain-item">
          <div class="pain-icon">🌐</div>
          <div>
            <div class="pain-title">海外擴張成本壓力</div>
            <div style="font-size:10.5px;">泰國、東南亞市場進入需大量行銷、本地化投入；2025年SG&amp;A佔營收70%，費用效率仍有改善空間。</div>
          </div>
        </div>
        <div class="pain-item">
          <div class="pain-icon">⚖️</div>
          <div>
            <div class="pain-title">監管與資料合規風險</div>
            <div style="font-size:10.5px;">各國個資法（PDPA/GDPR類似規範）對號碼資料庫使用限制趨嚴，澳洲、歐盟等地監管框架持續收緊。</div>
          </div>
        </div>
        <div class="pain-item">
          <div class="pain-icon">📊</div>
          <div>
            <div class="pain-title">股本稀釋風險</div>
            <div style="font-size:10.5px;">2021-2025年股本年均成長4.1%；未來若繼續以股票支付員工報酬或併購，恐持續稀釋每股價值。</div>
          </div>
        </div>
      </div>
      <div>
        <div class="sec-title" style="color:var(--green);">🚀 成長機遇</div>
        <div class="opp-item">
          <div class="opp-icon">🌏</div>
          <div>
            <div class="opp-title">東南亞7億人口市場</div>
            <div style="font-size:10.5px;">泰國72%民眾遭受詐騙；馬來西亞、越南、菲律賓等市場同樣高度需求；已與新加坡電信StarHub合作布局。</div>
          </div>
        </div>
        <div class="opp-item">
          <div class="opp-icon">🏦</div>
          <div>
            <div class="opp-title">金融科技飛速成長</div>
            <div style="font-size:10.5px;">袋鼠金融+JUJI招財麻吉 2025年營收年增<strong>54%</strong>；全球FinTech市場2025年$3,208億美元，年複合成長率16%+。</div>
          </div>
        </div>
        <div class="opp-item">
          <div class="opp-icon">🤖</div>
          <div>
            <div class="opp-title">AI防詐核心技術壁壘</div>
            <div style="font-size:10.5px;">全球詐騙損失已達$1兆美元（全球GDP 1%）；Gogolook擁有東亞最大號碼資料庫，AI模型持續強化，競爭護城河深。</div>
          </div>
        </div>
        <div class="opp-item">
          <div class="opp-icon">📈</div>
          <div>
            <div class="opp-title">訂閱收入高黏性成長</div>
            <div style="font-size:10.5px;">2025訂閱收入年增28%；遠傳合作Whoscall Premium自2025年12月試點後已翻倍；多元電信通路擴大觸及率。</div>
          </div>
        </div>
        <div class="opp-item">
          <div class="opp-icon">🏛️</div>
          <div>
            <div class="opp-title">轉掛一般板提升能見度</div>
            <div style="font-size:10.5px;">由創新板轉進TWSE一般板，擴大法人關注；2025年為連續獲利元年，符合一般板上市門檻要求。</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ========== SLIDE 4: 競爭對手分析 ========== -->
<div class="slide">
  <div class="slide-header">
    <h2>03 ｜ 市場競爭對手分析</h2>
    <span class="slide-no">04 / 12</span>
  </div>
  <div class="slide-body">
    <div class="sec-title">主要競爭者估值對照表</div>
    <table class="comp-table" style="margin-bottom:8px;">
      <thead>
        <tr>
          <th class="name-col" style="text-align:left;">公司名稱</th>
          <th>上市地</th>
          <th>業務重疊</th>
          <th>2025營收(M)</th>
          <th>YoY成長</th>
          <th>毛利率</th>
          <th>P/E(TTM)</th>
          <th>EV/Revenue</th>
          <th>P/B</th>
          <th>競爭威脅</th>
        </tr>
      </thead>
      <tbody>
        <tr class="highlight-row">
          <td class="name-col">⭐ Gogolook (6902)</td>
          <td>TWSE</td>
          <td>全部</td>
          <td>NT$1,048</td>
          <td><span class="tag tag-up">+20.9%</span></td>
          <td>88.3%</td>
          <td>49.3x</td>
          <td>2.57x</td>
          <td>3.94x</td>
          <td>—</td>
        </tr>
        <tr>
          <td class="name-col">TrueCaller (TRUE-B.ST)</td>
          <td>Stockholm</td>
          <td>來電辨識、防詐</td>
          <td>SEK ~3.3B</td>
          <td><span class="tag tag-dn">~-5%</span></td>
          <td>~72%</td>
          <td>10-17x</td>
          <td>2.0-3.4x</td>
          <td>3.0-3.3x</td>
          <td><span class="badge-h">高</span></td>
        </tr>
        <tr>
          <td class="name-col">Neustar (TransUnion)</td>
          <td>NYSE(TRU)</td>
          <td>數位身分驗證</td>
          <td>USD large</td>
          <td><span class="tag tag-na">—</span></td>
          <td>>60%</td>
          <td>~15x</td>
          <td>>5x</td>
          <td>—</td>
          <td><span class="badge-m">中</span></td>
        </tr>
        <tr>
          <td class="name-col">Telesign (private)</td>
          <td>私有</td>
          <td>號碼驗證API</td>
          <td>~USD 200M+</td>
          <td><span class="tag tag-na">—</span></td>
          <td>>60%</td>
          <td>—</td>
          <td>15-20x*</td>
          <td>—</td>
          <td><span class="badge-m">中</span></td>
        </tr>
        <tr>
          <td class="name-col">CallApp</td>
          <td>私有</td>
          <td>來電辨識App</td>
          <td>小型</td>
          <td><span class="tag tag-na">—</span></td>
          <td>—</td>
          <td>—</td>
          <td>—</td>
          <td>—</td>
          <td><span class="badge-l">低</span></td>
        </tr>
        <tr>
          <td class="name-col">Money101</td>
          <td>私有(TW)</td>
          <td>金融比較平台</td>
          <td>小型</td>
          <td><span class="tag tag-na">—</span></td>
          <td>—</td>
          <td>—</td>
          <td>—</td>
          <td>—</td>
          <td><span class="badge-l">低</span></td>
        </tr>
      </tbody>
    </table>
    <div class="grid-2" style="gap:8px;">
      <div>
        <div class="sec-title">🏆 Gogolook vs. TrueCaller 深度比較</div>
        <div class="card">
          <ul class="insight-list">
            <li class="insight-item ok">Gogolook毛利率88.3% > TrueCaller ~72%，SaaS訂閱佔比更高</li>
            <li class="insight-item ok">Gogolook 2025年EPS首度轉正，成長動能強於TrueCaller</li>
            <li class="insight-item ok">Gogolook金融科技業務(+54%)提供第二成長引擎，TrueCaller缺乏</li>
            <li class="insight-item warn">TrueCaller已在亞洲深耕，印度市場龐大，正面競爭明顯</li>
            <li class="insight-item warn">TrueCaller PE 10-17x vs Gogolook 49.3x，後者估值含高成長溢價</li>
            <li class="insight-item">TrueCaller EV/Sales 2-3.4x，Gogolook 2.57x → 估值實質相當</li>
            <li class="insight-item ok">Gogolook轉掛一般板後，機構投資人關注度將顯著提升</li>
          </ul>
        </div>
      </div>
      <div>
        <div class="sec-title">📐 同業估值指引（最適估值方式選擇）</div>
        <div class="card">
          <div class="card-title" style="color:var(--gold);">▶ 推薦估值方式：EV/Revenue + Forward P/E 雙軌並用</div>
          <ul class="insight-list">
            <li class="insight-item"><strong>EV/Revenue</strong>：適用因近期剛轉盈，歷史PE雜訊大；公開網路安全公司均值 7.8x，SaaS 5-7x</li>
            <li class="insight-item"><strong>Forward P/E</strong>：2026E獲利大幅提升，適用前瞻本益比；TrueCaller可比倍數 10-17x，Gogolook因更高成長享溢價 20-30x</li>
            <li class="insight-item"><strong>P/B</strong>：輔助指標；TrueCaller 3.0x，Gogolook 3.94x，溢價合理</li>
            <li class="insight-item warn">不建議使用TTM P/E（49.3x），因EPS仍處爬升初期，易誤導</li>
            <li class="insight-item ok">最終採用：<strong>EV/Revenue 5-8x × 2027E Revenue</strong> 作為核心估值區間</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ========== SLIDE 5: 三路線預測概覽 ========== -->
<div class="slide">
  <div class="slide-header">
    <h2>04 ｜ 三路線情境預測概覽（2026E–2028E）</h2>
    <span class="slide-no">05 / 12</span>
  </div>
  <div class="slide-body">
    <!-- Main Forecast Table -->
    <table class="forecast-table" style="margin-bottom:8px;">
      <thead>
        <tr>
          <th class="row-label" style="width:18%;">指標</th>
          <th colspan="3" style="background:#1a5276;">2026E</th>
          <th colspan="3" style="background:#1a5276;">2027E</th>
          <th colspan="3" style="background:#1a5276;">2028E</th>
        </tr>
        <tr>
          <th class="row-label"></th>
          <th style="background:#3498db;font-size:9.5px;">保守</th>
          <th style="background:#27ae60;font-size:9.5px;">平衡</th>
          <th style="background:#e74c3c;font-size:9.5px;">激進</th>
          <th style="background:#3498db;font-size:9.5px;">保守</th>
          <th style="background:#27ae60;font-size:9.5px;">平衡</th>
          <th style="background:#e74c3c;font-size:9.5px;">激進</th>
          <th style="background:#3498db;font-size:9.5px;">保守</th>
          <th style="background:#27ae60;font-size:9.5px;">平衡</th>
          <th style="background:#e74c3c;font-size:9.5px;">激進</th>
        </tr>
      </thead>
      <tbody>
        <tr class="section-divider"><th colspan="10">▌ 損益表（NT$M）</th></tr>
        <tr>
          <td class="row-label">合併營收</td>
          <td class="c">1,180</td><td class="b">1,350</td><td class="a">1,550</td>
          <td class="c">1,380</td><td class="b">1,720</td><td class="a">2,100</td>
          <td class="c">1,580</td><td class="b">2,120</td><td class="a">2,800</td>
        </tr>
        <tr>
          <td class="row-label">YoY成長率</td>
          <td class="c">+12.6%</td><td class="b">+28.8%</td><td class="a">+47.9%</td>
          <td class="c">+16.9%</td><td class="b">+27.4%</td><td class="a">+35.5%</td>
          <td class="c">+14.5%</td><td class="b">+23.3%</td><td class="a">+33.3%</td>
        </tr>
        <tr>
          <td class="row-label">毛利率</td>
          <td class="c">87%</td><td class="b">88%</td><td class="a">89%</td>
          <td class="c">87%</td><td class="b">89%</td><td class="a">90%</td>
          <td class="c">87%</td><td class="b">90%</td><td class="a">91%</td>
        </tr>
        <tr>
          <td class="row-label">營業利益率</td>
          <td class="c">8%</td><td class="b">13%</td><td class="a">16%</td>
          <td class="c">12%</td><td class="b">19%</td><td class="a">23%</td>
          <td class="c">15%</td><td class="b">23%</td><td class="a">29%</td>
        </tr>
        <tr>
          <td class="row-label">營業利益</td>
          <td class="c">94</td><td class="b">176</td><td class="a">248</td>
          <td class="c">166</td><td class="b">327</td><td class="a">483</td>
          <td class="c">237</td><td class="b">488</td><td class="a">812</td>
        </tr>
        <tr>
          <td class="row-label">稅後淨利</td>
          <td class="c">75</td><td class="b">149</td><td class="a">213</td>
          <td class="c">130</td><td class="b">221</td><td class="a">357</td>
          <td class="c">180</td><td class="b">358</td><td class="a">600</td>
        </tr>
        <tr class="section-divider"><th colspan="10">▌ 每股數據（NT$，股本預估34-36M股）</th></tr>
        <tr>
          <td class="row-label">EPS（元）</td>
          <td class="c"><strong>2.20</strong></td><td class="b"><strong>3.50</strong></td><td class="a"><strong>5.20</strong></td>
          <td class="c"><strong>3.80</strong></td><td class="b"><strong>6.50</strong></td><td class="a"><strong>10.50</strong></td>
          <td class="c"><strong>5.50</strong></td><td class="b"><strong>10.00</strong></td><td class="a"><strong>17.00</strong></td>
        </tr>
        <tr>
          <td class="row-label">EPS YoY成長</td>
          <td class="c">+39%</td><td class="b">+122%</td><td class="a">+229%</td>
          <td class="c">+73%</td><td class="b">+86%</td><td class="a">+102%</td>
          <td class="c">+45%</td><td class="b">+54%</td><td class="a">+62%</td>
        </tr>
        <tr class="section-divider"><th colspan="10">▌ 目標股價（NT$）</th></tr>
        <tr>
          <td class="row-label">P/E法目標價</td>
          <td class="c">55</td><td class="b">105</td><td class="a">156</td>
          <td class="c">76</td><td class="b">163</td><td class="a">315</td>
          <td class="c">110</td><td class="b">250</td><td class="a">510</td>
        </tr>
        <tr>
          <td class="row-label">EV/Rev法目標價</td>
          <td class="c">69</td><td class="b">198</td><td class="a">272</td>
          <td class="c">101</td><td class="b">253</td><td class="a">370</td>
          <td class="c">139</td><td class="b">373</td><td class="a">540</td>
        </tr>
        <tr style="background:#fffbe6;">
          <td class="row-label" style="font-weight:800;">綜合目標價區間</td>
          <td class="c"><strong>55-69</strong></td><td class="b"><strong>105-198</strong></td><td class="a"><strong>156-272</strong></td>
          <td class="c"><strong>76-101</strong></td><td class="b"><strong>163-253</strong></td><td class="a"><strong>315-370</strong></td>
          <td class="c"><strong>110-139</strong></td><td class="b"><strong>250-373</strong></td><td class="a"><strong>510-540</strong></td>
        </tr>
      </tbody>
    </table>
    <div class="card" style="background:#fffbe6;border-color:#f0c040;">
      <div class="card-title" style="color:var(--gold);">⭐ 分析師共識參考：2026年目標價 NT$105（Strong Buy；12個月）｜ 現股價 NT$77.9 → 隱含上漲空間 +34.8%</div>
    </div>
  </div>
</div>

<!-- ========== SLIDE 6: 保守版 ========== -->
<div class="slide">
  <div class="slide-header">
    <h2>05 ｜ 情境路線 A：保守版</h2>
    <span class="slide-no">06 / 12</span>
  </div>
  <div class="slide-body">
    <div class="grid-3" style="gap:8px;">
      <div>
        <span class="scenario-label label-c">🔵 保守路線假設</span>
        <div class="card scenario-conservative">
          <div class="card-title">核心假設</div>
          <ul class="insight-list">
            <li class="insight-item">2026-2028年營收年增12-17%（接近分析師共識下緣）</li>
            <li class="insight-item">東南亞市場進展緩慢，泰國成效需2年以上顯現</li>
            <li class="insight-item">金融科技成長降速至15-20%（監管趨嚴）</li>
            <li class="insight-item">SG&amp;A維持高位，費用率改善有限</li>
            <li class="insight-item">股本年均增長4%（股票薪酬持續）</li>
          </ul>
          <hr class="divider">
          <div class="card-title">預估效果</div>
          <ul class="insight-list">
            <li class="insight-item ok">2026E EPS: <strong>NT$2.20</strong>（YoY +39%）</li>
            <li class="insight-item ok">2027E EPS: <strong>NT$3.80</strong>（YoY +73%）</li>
            <li class="insight-item ok">2028E EPS: <strong>NT$5.50</strong>（YoY +45%）</li>
            <li class="insight-item">2028E 目標股價：<strong>NT$110-139</strong></li>
            <li class="insight-item">2026E 目標股價：<strong>NT$55-69</strong></li>
          </ul>
        </div>
      </div>
      <div>
        <span class="scenario-label label-c" style="opacity:0;">.</span>
        <div class="card scenario-conservative">
          <div class="card-title">⚠ 風險點</div>
          <ul class="insight-list">
            <li class="insight-item warn">東南亞市場監管障礙（個資法）阻礙資料庫擴張</li>
            <li class="insight-item warn">TrueCaller在泰國、印尼加大行銷攻勢</li>
            <li class="insight-item warn">AI詐騙升級，Whoscall識別率下降，用戶流失</li>
            <li class="insight-item warn">自由現金流無法轉正，被迫增資稀釋股本</li>
            <li class="insight-item warn">台灣廣告市場成長趨緩（年增5%以下）</li>
            <li class="insight-item warn">利率維持高位，DCF折現率偏高壓制估值</li>
          </ul>
          <hr class="divider">
          <div class="card-title">📦 資源需求</div>
          <ul class="insight-list">
            <li class="insight-item">研發投入維持NT$100-130M/年</li>
            <li class="insight-item">海外行銷預算NT$80-100M/年（泰國+馬來西亞為主）</li>
            <li class="insight-item">技術基礎設施年維護NT$40-50M</li>
            <li class="insight-item">合規/法務預算NT$20-30M（應對各國PDPA）</li>
            <li class="insight-item">預估3年資本支出總計：<strong>NT$600-700M</strong></li>
          </ul>
        </div>
      </div>
      <div>
        <span class="scenario-label label-c" style="opacity:0;">.</span>
        <div class="card" style="margin-bottom:6px;">
          <div class="card-title">📊 保守版財測摘要（NT$M）</div>
          <table class="forecast-table">
            <tr><th class="row-label">指標</th><th>2026E</th><th>2027E</th><th>2028E</th></tr>
            <tr><td class="row-label">營收</td><td class="c">1,180</td><td class="c">1,380</td><td class="c">1,580</td></tr>
            <tr><td class="row-label">YoY</td><td class="c">+12.6%</td><td class="c">+16.9%</td><td class="c">+14.5%</td></tr>
            <tr><td class="row-label">毛利</td><td class="c">1,027</td><td class="c">1,201</td><td class="c">1,375</td></tr>
            <tr><td class="row-label">營業利</td><td class="c">94</td><td class="c">166</td><td class="c">237</td></tr>
            <tr><td class="row-label">淨利</td><td class="c">75</td><td class="c">130</td><td class="c">180</td></tr>
            <tr><td class="row-label">EPS(元)</td><td class="c"><strong>2.20</strong></td><td class="c"><strong>3.80</strong></td><td class="c"><strong>5.50</strong></td></tr>
          </table>
        </div>
        <div class="card" style="background:#d6eaf8;">
          <div class="card-title" style="color:#1a5276;">🎯 保守版估值邏輯</div>
          <ul class="insight-list" style="font-size:10px;">
            <li class="insight-item">Forward P/E 20x（比TrueCaller打折，因成長疑慮）× 2027E EPS$3.80 = NT$76</li>
            <li class="insight-item">EV/Revenue 5x × 2027E Revenue $1.38B / 34M股 = NT$101</li>
            <li class="insight-item">保守情境2027年目標區間：<strong>NT$76-101</strong></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ========== SLIDE 7: 平衡版 ========== -->
<div class="slide">
  <div class="slide-header">
    <h2>06 ｜ 情境路線 B：平衡版（基準情境）</h2>
    <span class="slide-no">07 / 12</span>
  </div>
  <div class="slide-body">
    <div class="grid-3" style="gap:8px;">
      <div>
        <span class="scenario-label label-b">🟢 平衡路線假設</span>
        <div class="card scenario-balanced">
          <div class="card-title">核心假設</div>
          <ul class="insight-list">
            <li class="insight-item">2026-2028年營收年增23-29%（持續超越市場預期）</li>
            <li class="insight-item">金融科技服務持續高增長（30-40%/年）</li>
            <li class="insight-item">泰國市場於2026H2開始貢獻顯著營收</li>
            <li class="insight-item">SG&amp;A比率逐步降至60%以下（規模效益顯現）</li>
            <li class="insight-item">Whoscall MAU突破2,000萬（2027年）</li>
            <li class="insight-item">2025年Q4 NT$37M利潤爆發趨勢延續</li>
          </ul>
          <hr class="divider">
          <div class="card-title">預估效果</div>
          <ul class="insight-list">
            <li class="insight-item ok">2026E EPS: <strong>NT$3.50</strong>（YoY +122%）</li>
            <li class="insight-item ok">2027E EPS: <strong>NT$6.50</strong>（YoY +86%）</li>
            <li class="insight-item ok">2028E EPS: <strong>NT$10.00</strong>（YoY +54%）</li>
            <li class="insight-item ok">2028E 目標股價：<strong>NT$250-373</strong></li>
          </ul>
        </div>
      </div>
      <div>
        <span class="scenario-label label-b" style="opacity:0;">.</span>
        <div class="card scenario-balanced">
          <div class="card-title">⚠ 風險點</div>
          <ul class="insight-list">
            <li class="insight-item warn">競爭對手TrueCaller加速佈局東南亞，搶占市場</li>
            <li class="insight-item warn">金融科技業務受台灣央行監管政策影響</li>
            <li class="insight-item warn">AI技術替代風險（Google/Meta直接整合防詐功能）</li>
            <li class="insight-item warn">Q4利潤爆發是否具可持續性仍需觀察2026全年</li>
          </ul>
          <hr class="divider">
          <div class="card-title">📦 資源需求</div>
          <ul class="insight-list">
            <li class="insight-item">研發預算NT$130-180M/年（AI防詐模型深化）</li>
            <li class="insight-item">東南亞市場行銷投入NT$120-160M/年</li>
            <li class="insight-item">金融科技產品開發NT$80-100M/年</li>
            <li class="insight-item">企業端業務整合（ScamAdviser深化）NT$50M</li>
            <li class="insight-item">預估3年資本支出總計：<strong>NT$900-1,000M</strong></li>
          </ul>
        </div>
      </div>
      <div>
        <span class="scenario-label label-b" style="opacity:0;">.</span>
        <div class="card" style="margin-bottom:6px;">
          <div class="card-title">📊 平衡版財測摘要（NT$M）</div>
          <table class="forecast-table">
            <tr><th class="row-label">指標</th><th>2026E</th><th>2027E</th><th>2028E</th></tr>
            <tr><td class="row-label">營收</td><td class="b">1,350</td><td class="b">1,720</td><td class="b">2,120</td></tr>
            <tr><td class="row-label">YoY</td><td class="b">+28.8%</td><td class="b">+27.4%</td><td class="b">+23.3%</td></tr>
            <tr><td class="row-label">毛利</td><td class="b">1,188</td><td class="b">1,531</td><td class="b">1,908</td></tr>
            <tr><td class="row-label">營業利</td><td class="b">176</td><td class="b">327</td><td class="b">488</td></tr>
            <tr><td class="row-label">淨利</td><td class="b">149</td><td class="b">221</td><td class="b">358</td></tr>
            <tr><td class="row-label">EPS(元)</td><td class="b"><strong>3.50</strong></td><td class="b"><strong>6.50</strong></td><td class="b"><strong>10.00</strong></td></tr>
          </table>
        </div>
        <div class="card" style="background:#d5f5e3;">
          <div class="card-title" style="color:#1a5e38;">🎯 平衡版估值邏輯</div>
          <ul class="insight-list" style="font-size:10px;">
            <li class="insight-item">Forward P/E 25x（Gogolook成長溢價）× 2027E EPS$6.50 = NT$163</li>
            <li class="insight-item">EV/Revenue 7x × 2027E Revenue $1.72B / 34M股 = NT$253</li>
            <li class="insight-item">分析師1年目標價NT$105 → 與本模型2026E中點吻合</li>
            <li class="insight-item">2027年目標區間：<strong>NT$163-253</strong>（潛在2-3倍報酬）</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ========== SLIDE 8: 激進版 ========== -->
<div class="slide">
  <div class="slide-header">
    <h2>07 ｜ 情境路線 C：激進版</h2>
    <span class="slide-no">08 / 12</span>
  </div>
  <div class="slide-body">
    <div class="grid-3" style="gap:8px;">
      <div>
        <span class="scenario-label label-a">🔴 激進路線假設</span>
        <div class="card scenario-aggressive">
          <div class="card-title">核心假設</div>
          <ul class="insight-list">
            <li class="insight-item">2026-2028年營收年增33-48%（東南亞爆發+歐美布局）</li>
            <li class="insight-item">金融科技服務年增70%+（袋鼠金融+JUJI規模化）</li>
            <li class="insight-item">與電信商（遠傳、StarHub、AIS）大型合作全面擴張</li>
            <li class="insight-item">歐美ScamAdviser轉型為SaaS收入貢獻主力</li>
            <li class="insight-item">AI防詐服務定價能力提升，ARPU年增20%+</li>
            <li class="insight-item">2027年完成轉掛一般板，吸引外資法人買盤</li>
            <li class="insight-item">被大型集團（電信商或金融機構）策略入股/併購</li>
          </ul>
          <hr class="divider">
          <div class="card-title">預估效果</div>
          <ul class="insight-list">
            <li class="insight-item ok">2026E EPS: <strong>NT$5.20</strong>（YoY +229%）</li>
            <li class="insight-item ok">2027E EPS: <strong>NT$10.50</strong>（YoY +102%）</li>
            <li class="insight-item ok">2028E EPS: <strong>NT$17.00</strong>（YoY +62%）</li>
            <li class="insight-item ok">2028E 目標股價：<strong>NT$510-540</strong></li>
          </ul>
        </div>
      </div>
      <div>
        <span class="scenario-label label-a" style="opacity:0;">.</span>
        <div class="card scenario-aggressive">
          <div class="card-title">⚠ 風險點</div>
          <ul class="insight-list">
            <li class="insight-item warn"><strong>執行風險最高</strong>：多個市場同步擴張，管理能力面臨考驗</li>
            <li class="insight-item warn">電信商合作談判複雜，收入落地時間不可控</li>
            <li class="insight-item warn">科技泡沫或市場修正，高估值個股首當其衝</li>
            <li class="insight-item warn">歐美監管（GDPR）對號碼資料庫使用更嚴格</li>
            <li class="insight-item warn">大型競爭者（Google、Amazon）推出免費防詐功能</li>
            <li class="insight-item warn">若成長不及預期，高估值（40x+PE）修正幅度巨大</li>
          </ul>
          <hr class="divider">
          <div class="card-title">📦 資源需求</div>
          <ul class="insight-list">
            <li class="insight-item">研發投入NT$200-280M/年（大型AI防詐平台建設）</li>
            <li class="insight-item">全球行銷投入NT$200-250M/年</li>
            <li class="insight-item">可能需要辦理現增/發行公司債NT$500-800M</li>
            <li class="insight-item">海外公司設立/併購預算NT$300-500M</li>
            <li class="insight-item">預估3年資本支出總計：<strong>NT$1,500-2,000M</strong></li>
          </ul>
        </div>
      </div>
      <div>
        <span class="scenario-label label-a" style="opacity:0;">.</span>
        <div class="card" style="margin-bottom:6px;">
          <div class="card-title">📊 激進版財測摘要（NT$M）</div>
          <table class="forecast-table">
            <tr><th class="row-label">指標</th><th>2026E</th><th>2027E</th><th>2028E</th></tr>
            <tr><td class="row-label">營收</td><td class="a">1,550</td><td class="a">2,100</td><td class="a">2,800</td></tr>
            <tr><td class="row-label">YoY</td><td class="a">+47.9%</td><td class="a">+35.5%</td><td class="a">+33.3%</td></tr>
            <tr><td class="row-label">毛利</td><td class="a">1,380</td><td class="a">1,890</td><td class="a">2,548</td></tr>
            <tr><td class="row-label">營業利</td><td class="a">248</td><td class="a">483</td><td class="a">812</td></tr>
            <tr><td class="row-label">淨利</td><td class="a">213</td><td class="a">357</td><td class="a">600</td></tr>
            <tr><td class="row-label">EPS(元)</td><td class="a"><strong>5.20</strong></td><td class="a"><strong>10.50</strong></td><td class="a"><strong>17.00</strong></td></tr>
          </table>
        </div>
        <div class="card" style="background:#fde8e7;">
          <div class="card-title" style="color:#922b21;">🎯 激進版估值邏輯</div>
          <ul class="insight-list" style="font-size:10px;">
            <li class="insight-item">Forward P/E 30x（高成長+品牌護城河溢價）× 2027E EPS$10.50 = NT$315</li>
            <li class="insight-item">EV/Revenue 8-9x × 2027E Revenue $2.10B / 34M股 = NT$370-$494</li>
            <li class="insight-item">若成功被策略收購，控制權溢價可達30-50%</li>
            <li class="insight-item">2027年目標區間：<strong>NT$315-370</strong>（潛在4-5倍報酬）</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ========== SLIDE 9: 估值與買進價格 ========== -->
<div class="slide">
  <div class="slide-header">
    <h2>08 ｜ 客觀估值分析與買進價格建議</h2>
    <span class="slide-no">09 / 12</span>
  </div>
  <div class="slide-body">
    <div class="grid-2" style="gap:8px;">
      <div>
        <div class="sec-title">多元估值方法矩陣</div>
        <!-- Method 1 -->
        <div class="val-method">
          <div class="method-name">① EV/Revenue 法（主要方法）</div>
          <div style="font-size:10px;color:var(--gray);">邏輯：Gogolook SaaS+Cybersecurity混合業態；同業TrueCaller 2.0-3.4x，公開網安平均7.8x；採5-7x估值區間</div>
          <div class="val-range" style="margin-top:5px;">
            <div class="val-range-item vri-c">
              <span class="price" style="color:#1a5276;">NT$69-101</span>
              <div class="price-label">保守 (5x EV/Rev)</div>
            </div>
            <div class="val-range-item vri-b">
              <span class="price" style="color:#1a5e38;">NT$198-253</span>
              <div class="price-label">平衡 (7x EV/Rev)</div>
            </div>
            <div class="val-range-item vri-a">
              <span class="price" style="color:#922b21;">NT$272-370</span>
              <div class="price-label">激進 (8-9x EV/Rev)</div>
            </div>
          </div>
        </div>
        <!-- Method 2 -->
        <div class="val-method">
          <div class="method-name">② Forward P/E 法（次要方法）</div>
          <div style="font-size:10px;color:var(--gray);">邏輯：以2027E EPS為基準；TrueCaller同業10-17x；Gogolook因更高成長給予20-30x溢價倍數</div>
          <div class="val-range" style="margin-top:5px;">
            <div class="val-range-item vri-c">
              <span class="price" style="color:#1a5276;">NT$76</span>
              <div class="price-label">保守 (20x × $3.8)</div>
            </div>
            <div class="val-range-item vri-b">
              <span class="price" style="color:#1a5e38;">NT$163</span>
              <div class="price-label">平衡 (25x × $6.5)</div>
            </div>
            <div class="val-range-item vri-a">
              <span class="price" style="color:#922b21;">NT$315</span>
              <div class="price-label">激進 (30x × $10.5)</div>
            </div>
          </div>
        </div>
        <!-- Method 3 -->
        <div class="val-method">
          <div class="method-name">③ P/B 法（輔助參考）</div>
          <div style="font-size:10px;color:var(--gray);">邏輯：TrueCaller P/B ~3.0x；Gogolook因ROE仍低，P/B暫以3-5x為合理區間；輔助確認估值合理性</div>
          <div class="val-range" style="margin-top:5px;">
            <div class="val-range-item vri-c">
              <span class="price" style="color:#1a5276;">~NT$55-70</span>
              <div class="price-label">3.0-3.5x P/B</div>
            </div>
            <div class="val-range-item vri-b">
              <span class="price" style="color:#1a5e38;">~NT$70-95</span>
              <div class="price-label">3.5-4.5x P/B</div>
            </div>
            <div class="val-range-item vri-a">
              <span class="price" style="color:#922b21;">~NT$95-140</span>
              <div class="price-label">4.5-6x P/B</div>
            </div>
          </div>
        </div>
      </div>
      <div>
        <div class="sec-title">📊 目前估值指標（NT$77.9 / 2026.3.15）</div>
        <div class="kpi-row" style="margin-bottom:5px;">
          <div class="kpi-box">
            <span class="val">49.3x</span>
            <div class="lbl">TTM P/E</div>
          </div>
          <div class="kpi-box">
            <span class="val">22.3x</span>
            <div class="lbl">Forward P/E (2026E)</div>
          </div>
          <div class="kpi-box">
            <span class="val">3.94x</span>
            <div class="lbl">P/B</div>
          </div>
          <div class="kpi-box">
            <span class="val highlight">2.57x</span>
            <div class="lbl">EV/Revenue</div>
          </div>
        </div>
        <div class="card" style="margin-bottom:5px;">
          <div class="card-title">📌 客觀買進價格建議</div>
          <div class="val-range" style="margin-top:4px;">
            <div class="val-range-item vri-c" style="padding:8px 4px;">
              <span class="price" style="color:#1a5276;font-size:14px;">NT$65-70</span>
              <div class="price-label" style="font-weight:700;">保守建議入場</div>
              <div class="price-label">安全邊際15%+</div>
            </div>
            <div class="val-range-item vri-b" style="padding:8px 4px;">
              <span class="price" style="color:#1a5e38;font-size:14px;">NT$75-85</span>
              <div class="price-label" style="font-weight:700;color:#1a5e38;">✅ 現價合理區間</div>
              <div class="price-label">平衡入場建議</div>
            </div>
            <div class="val-range-item vri-a" style="padding:8px 4px;">
              <span class="price" style="color:#922b21;font-size:14px;">NT$90-105</span>
              <div class="price-label" style="font-weight:700;">激進者追價上限</div>
              <div class="price-label">分析師目標價</div>
            </div>
          </div>
        </div>
        <div class="buy-box">
          <div class="buy-title">⭐ 綜合估值師建議：客觀買進價格</div>
          <div class="buy-price">NT$75 ~ 85</div>
          <div class="buy-sub">現股價 NT$77.9 處於合理買入區間下緣</div>
          <div class="buy-sub" style="margin-top:3px;">強力加碼區：NT$65以下 ｜ 12個月目標：NT$105（+34.8%）</div>
        </div>
        <div class="card" style="margin-top:5px;">
          <div class="card-title">📐 估值邏輯說明</div>
          <ul class="insight-list" style="font-size:10px;">
            <li class="insight-item">現EV/Revenue 2.57x遠低於同業（SaaS均值5-7x），代表潛在估值修復空間</li>
            <li class="insight-item">2026E Forward P/E 22x（NT$77.9/NT$3.5）位於TrueCaller同業上緣，但Gogolook成長率高出3倍</li>
            <li class="insight-item">PEG Ratio（PE/成長率）：22x/122% = 0.18 → 遠低於1，高度低估</li>
            <li class="insight-item">強力加碼區NT$65：對應2027E EPS $3.8 × 17x = $64.6，同業最低倍數下限</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ========== SLIDE 10: 風險控管 ========== -->
<div class="slide">
  <div class="slide-header">
    <h2>09 ｜ 風險控管矩陣</h2>
    <span class="slide-no">10 / 12</span>
  </div>
  <div class="slide-body">
    <div class="risk-row risk-header">
      <div class="risk-cell">風險項目</div>
      <div class="risk-cell">風險等級</div>
      <div class="risk-cell">影響說明</div>
      <div class="risk-cell">緩解措施</div>
    </div>
    <div class="risk-row">
      <div class="risk-cell"><strong>競爭對手侵蝕</strong><br>TrueCaller東南亞加速</div>
      <div class="risk-cell" style="text-align:center;"><span class="badge-h">高</span></div>
      <div class="risk-cell">泰/馬市場份額流失，訂閱成長受限，MAU停滯</div>
      <div class="risk-cell">深化電信商獨家合作；加速AI功能差異化；提升轉換成本</div>
    </div>
    <div class="risk-row">
      <div class="risk-cell"><strong>監管合規風險</strong><br>個資法/PDPA趨嚴</div>
      <div class="risk-cell" style="text-align:center;"><span class="badge-h">高</span></div>
      <div class="risk-cell">號碼資料庫使用受限，企業端服務市場萎縮</div>
      <div class="risk-cell">設立隱私法遵部門；與政府機構合作取得授權；轉向KYC/AI模型輸出</div>
    </div>
    <div class="risk-row">
      <div class="risk-cell"><strong>AI平台替代風險</strong><br>Google/Meta內建防詐</div>
      <div class="risk-cell" style="text-align:center;"><span class="badge-h">高</span></div>
      <div class="risk-cell">Whoscall廣告+訂閱模式被系統級服務取代</div>
      <div class="risk-cell">轉型B2B（電信商、金融機構OEM授權）；深化企業端API服務</div>
    </div>
    <div class="risk-row">
      <div class="risk-cell"><strong>現金流壓力</strong><br>FCF持續為負</div>
      <div class="risk-cell" style="text-align:center;"><span class="badge-m">中</span></div>
      <div class="risk-cell">若FCF無法轉正，可能需增資，稀釋股東權益</div>
      <div class="risk-cell">優化資本配置；以訂閱預收款改善現金週期；審慎評估M&A時機</div>
    </div>
    <div class="risk-row">
      <div class="risk-cell"><strong>宏觀經濟衝擊</strong><br>全球衰退/利率環境</div>
      <div class="risk-cell" style="text-align:center;"><span class="badge-m">中</span></div>
      <div class="risk-cell">廣告預算縮減影響營收；高折現率壓縮成長股估值</div>
      <div class="risk-cell">提升訂閱收入佔比（抗景氣循環）；降低廣告依賴度</div>
    </div>
    <div class="risk-row">
      <div class="risk-cell"><strong>台幣匯率風險</strong><br>海外收入匯率波動</div>
      <div class="risk-cell" style="text-align:center;"><span class="badge-m">中</span></div>
      <div class="risk-cell">東南亞收入以泰銖/馬幣計價，台幣升值侵蝕獲利</div>
      <div class="risk-cell">自然對沖（在地成本與收入匹配）；考慮外匯避險工具</div>
    </div>
    <div class="risk-row">
      <div class="risk-cell"><strong>關鍵人才風險</strong><br>核心AI/技術人才流失</div>
      <div class="risk-cell" style="text-align:center;"><span class="badge-l">低</span></div>
      <div class="risk-cell">AI防詐核心競爭力依賴關鍵技術團隊維繫</div>
      <div class="risk-cell">RSU股票獎酬計畫；打造具吸引力的台灣科技品牌文化</div>
    </div>
    <div class="risk-row">
      <div class="risk-cell"><strong>股本稀釋風險</strong><br>股票薪酬/增資</div>
      <div class="risk-cell" style="text-align:center;"><span class="badge-l">低</span></div>
      <div class="risk-cell">歷史年均股本成長4%，若加速稀釋EPS成長效果</div>
      <div class="risk-cell">設定股本稀釋上限政策；增資前進行充分市場溝通</div>
    </div>
  </div>
</div>

<!-- ========== SLIDE 11: 預算與時程 ========== -->
<div class="slide">
  <div class="slide-header">
    <h2>10 ｜ 預算規劃與三年時程藍圖</h2>
    <span class="slide-no">11 / 12</span>
  </div>
  <div class="slide-body">
    <div class="sec-title" style="margin-bottom:6px;">📅 三年執行時程與里程碑</div>
    <div class="timeline" style="margin-bottom:8px;">
      <div class="timeline-phase tp1">
        <div class="ph-title">Phase 1：鞏固基礎（2026）</div>
        <ul class="insight-list">
          <li class="insight-item"><strong>Q1:</strong> 轉掛一般板完成，吸引外資法人</li>
          <li class="insight-item"><strong>Q1:</strong> 遠傳Whoscall Premium方案全面推出</li>
          <li class="insight-item"><strong>Q2:</strong> 泰國區域總部全面運營，新增電信合作夥伴</li>
          <li class="insight-item"><strong>Q2:</strong> 袋鼠金融+JUJI完成產品整合</li>
          <li class="insight-item"><strong>Q3:</strong> 星馬市場電信商合作落地</li>
          <li class="insight-item"><strong>Q4:</strong> ScamAdviser歐洲企業SaaS新合同</li>
          <li class="insight-item ok"><strong>目標：</strong>2026全年獲利NT$149M+（平衡）</li>
        </ul>
      </div>
      <div class="timeline-phase tp2">
        <div class="ph-title">Phase 2：規模擴張（2027）</div>
        <ul class="insight-list">
          <li class="insight-item"><strong>Q1:</strong> 東南亞MAU突破2,000萬，訂閱收入佔比40%+</li>
          <li class="insight-item"><strong>Q2:</strong> 越南、菲律賓、印尼市場正式進入</li>
          <li class="insight-item"><strong>Q2:</strong> 企業端信任雲收入由負轉正成長</li>
          <li class="insight-item"><strong>Q3:</strong> 金融科技AI風控服務推出企業版</li>
          <li class="insight-item"><strong>Q4:</strong> 自由現金流轉正（平衡情境達成目標）</li>
          <li class="insight-item ok"><strong>目標：</strong>2027全年獲利NT$221M+（平衡）</li>
        </ul>
      </div>
      <div class="timeline-phase tp3">
        <div class="ph-title">Phase 3：獲利高速期（2028）</div>
        <ul class="insight-list">
          <li class="insight-item"><strong>Q1:</strong> 東南亞收入占比超過50%（達成目標）</li>
          <li class="insight-item"><strong>Q2:</strong> 歐美ScamAdviser企業SaaS年收入破NT$200M</li>
          <li class="insight-item"><strong>Q3:</strong> AI防詐平台推出政府/公共事業版本</li>
          <li class="insight-item"><strong>Q4:</strong> 評估M&A目標或策略夥伴戰略入股</li>
          <li class="insight-item ok"><strong>目標：</strong>2028全年獲利NT$358M+（平衡）</li>
        </ul>
      </div>
    </div>
    <div class="sec-title" style="margin-bottom:5px;">💰 三年預算規劃（NT$M，平衡情境）</div>
    <table class="forecast-table">
      <tr>
        <th class="row-label">預算項目</th>
        <th>2026E</th><th>%營收</th>
        <th>2027E</th><th>%營收</th>
        <th>2028E</th><th>%營收</th>
        <th>3年合計</th>
      </tr>
      <tr>
        <td class="row-label">研發費用 (R&amp;D)</td>
        <td>148</td><td>11%</td>
        <td>172</td><td>10%</td>
        <td>212</td><td>10%</td>
        <td style="font-weight:700;">532</td>
      </tr>
      <tr>
        <td class="row-label">銷售行銷 (S&amp;M)</td>
        <td>405</td><td>30%</td>
        <td>430</td><td>25%</td>
        <td>466</td><td>22%</td>
        <td style="font-weight:700;">1,301</td>
      </tr>
      <tr>
        <td class="row-label">一般管理 (G&amp;A)</td>
        <td>162</td><td>12%</td>
        <td>172</td><td>10%</td>
        <td>190</td><td>9%</td>
        <td style="font-weight:700;">524</td>
      </tr>
      <tr>
        <td class="row-label">資本支出 (CAPEX)</td>
        <td>120</td><td>9%</td>
        <td>140</td><td>8%</td>
        <td>150</td><td>7%</td>
        <td style="font-weight:700;">410</td>
      </tr>
      <tr style="background:#fffbe6;">
        <td class="row-label" style="font-weight:800;">營業費用合計</td>
        <td style="font-weight:700;">715</td><td>53%</td>
        <td style="font-weight:700;">774</td><td>45%</td>
        <td style="font-weight:700;">868</td>
        <td>41%</td>
        <td style="font-weight:800;color:var(--primary);">2,357</td>
      </tr>
    </table>
    <div class="card" style="margin-top:5px;background:#fffbe6;border-color:#f0c040;">
      <div class="card-title" style="color:var(--gold);">⭐ 關鍵假設：隨收入增長，費用率持續下降（規模效益），是獲利能力大幅提升的核心驅動力</div>
      <ul class="insight-list" style="font-size:10px;margin-top:3px;">
        <li class="insight-item">S&amp;M費用率：2025年70% → 2028年目標22%，是「Critical Mass已達成」後槓桿效果最顯著指標</li>
        <li class="insight-item">毛利高達88%+，只需控制費用，獲利率將自然快速攀升</li>
      </ul>
    </div>
  </div>
</div>

<!-- ========== SLIDE 12: 方案比較摘要 ========== -->
<div class="slide">
  <div class="slide-header">
    <h2>11 ｜ 三路線方案比較摘要</h2>
    <span class="slide-no">12 / 12</span>
  </div>
  <div class="slide-body">
    <div class="grid-3" style="gap:8px;margin-bottom:6px;">
      <div class="card scenario-conservative">
        <div class="scenario-label label-c" style="display:block;margin-bottom:5px;">🔵 保守版</div>
        <div style="text-align:center;margin-bottom:5px;">
          <div style="font-size:11px;font-weight:700;color:#1a5276;">2028E EPS: NT$5.50</div>
          <div style="font-size:10px;color:var(--gray);">目標股價：NT$110-139</div>
          <div style="font-size:9px;color:var(--gray);">較現價潛在報酬：+41-79%</div>
        </div>
        <div class="progress-bar-wrap">
          <div class="progress-label"><span>成功機率</span><span>55%</span></div>
          <div class="progress-bar"><div class="progress-fill" style="width:55%;background:#3498db;"></div></div>
        </div>
        <div class="progress-bar-wrap">
          <div class="progress-label"><span>執行難度</span><span>低</span></div>
          <div class="progress-bar"><div class="progress-fill" style="width:30%;background:#3498db;"></div></div>
        </div>
        <div class="progress-bar-wrap">
          <div class="progress-label"><span>資本需求</span><span>NT$600-700M</span></div>
          <div class="progress-bar"><div class="progress-fill" style="width:35%;background:#3498db;"></div></div>
        </div>
        <hr class="divider">
        <ul class="insight-list" style="font-size:10px;">
          <li class="insight-item warn">東南亞進展緩慢</li>
          <li class="insight-item warn">金融科技成長降速</li>
          <li class="insight-item ok">現金消耗最低</li>
          <li class="insight-item ok">股本稀釋最少</li>
        </ul>
      </div>
      <div class="card scenario-balanced">
        <div class="scenario-label label-b" style="display:block;margin-bottom:5px;">🟢 平衡版（推薦）</div>
        <div style="text-align:center;margin-bottom:5px;">
          <div style="font-size:11px;font-weight:700;color:#1a5e38;">2028E EPS: NT$10.00</div>
          <div style="font-size:10px;color:var(--gray);">目標股價：NT$250-373</div>
          <div style="font-size:9px;color:var(--green);font-weight:700;">較現價潛在報酬：+221-379% ⭐</div>
        </div>
        <div class="progress-bar-wrap">
          <div class="progress-label"><span>成功機率</span><span>35%</span></div>
          <div class="progress-bar"><div class="progress-fill" style="width:35%;background:#27ae60;"></div></div>
        </div>
        <div class="progress-bar-wrap">
          <div class="progress-label"><span>執行難度</span><span>中</span></div>
          <div class="progress-bar"><div class="progress-fill" style="width:55%;background:#27ae60;"></div></div>
        </div>
        <div class="progress-bar-wrap">
          <div class="progress-label"><span>資本需求</span><span>NT$900-1,000M</span></div>
          <div class="progress-bar"><div class="progress-fill" style="width:55%;background:#27ae60;"></div></div>
        </div>
        <hr class="divider">
        <ul class="insight-list" style="font-size:10px;">
          <li class="insight-item ok">與分析師共識最接近</li>
          <li class="insight-item ok">Q4爆發趨勢的自然延伸</li>
          <li class="insight-item ok">金融科技30-40%持續成長</li>
          <li class="insight-item warn">東南亞競爭需積極應對</li>
        </ul>
      </div>
      <div class="card scenario-aggressive">
        <div class="scenario-label label-a" style="display:block;margin-bottom:5px;">🔴 激進版</div>
        <div style="text-align:center;margin-bottom:5px;">
          <div style="font-size:11px;font-weight:700;color:#922b21;">2028E EPS: NT$17.00</div>
          <div style="font-size:10px;color:var(--gray);">目標股價：NT$510-540</div>
          <div style="font-size:9px;color:var(--red);">較現價潛在報酬：+555-594%</div>
        </div>
        <div class="progress-bar-wrap">
          <div class="progress-label"><span>成功機率</span><span>10%</span></div>
          <div class="progress-bar"><div class="progress-fill" style="width:10%;background:#e74c3c;"></div></div>
        </div>
        <div class="progress-bar-wrap">
          <div class="progress-label"><span>執行難度</span><span>極高</span></div>
          <div class="progress-bar"><div class="progress-fill" style="width:90%;background:#e74c3c;"></div></div>
        </div>
        <div class="progress-bar-wrap">
          <div class="progress-label"><span>資本需求</span><span>NT$1,500-2,000M</span></div>
          <div class="progress-bar"><div class="progress-fill" style="width:85%;background:#e74c3c;"></div></div>
        </div>
        <hr class="divider">
        <ul class="insight-list" style="font-size:10px;">
          <li class="insight-item warn">需現增/發債融資</li>
          <li class="insight-item warn">多市場同步執行</li>
          <li class="insight-item ok">策略收購可能觸發</li>
          <li class="insight-item ok">一旦成功報酬率最高</li>
        </ul>
      </div>
    </div>
    <!-- Buy Price Summary -->
    <div class="grid-2" style="gap:8px;">
      <div class="buy-box" style="border-radius:5px;">
        <div class="buy-title">📊 加權期望值目標價（概率加權）</div>
        <div style="font-size:10px;opacity:0.8;margin-bottom:5px;">保守55% × NT$76 + 平衡35% × NT$163 + 激進10% × NT$315</div>
        <div class="buy-price">NT$132</div>
        <div class="buy-sub">2027年概率加權目標價 ≈ NT$132（較現價+69.4%）</div>
      </div>
      <div class="card">
        <div class="card-title">🎯 最終投資建議摘要</div>
        <ul class="insight-list">
          <li class="insight-item ok"><strong>強力買入區（支撐強）：NT$65以下</strong>——2027E EPS × 17x（同業最低倍數）</li>
          <li class="insight-item ok"><strong>合理買入區（現價位）：NT$75-85</strong>——2026E EPS × 22-24x，成長性合理</li>
          <li class="insight-item"><strong>分析師目標追蹤：NT$105</strong>——12個月目標，潛在+34.8%</li>
          <li class="insight-item warn"><strong>高估警戒區：NT$130+</strong>——需平衡情境EPS超預期才能支撐</li>
          <li class="insight-item">現股價 NT$77.9 = <strong>Forward P/E 22x（2026E）</strong>，相較成長率顯著低估（PEG 0.18）</li>
          <li class="insight-item ok">EV/Revenue 2.57x遠低於同業SaaS均值，具顯著估值修復潛力</li>
        </ul>
      </div>
    </div>
  </div>
</div>

<!-- DISCLAIMER -->
<div class="slide">
  <div class="disclaimer">
    <div style="font-size:10px;font-weight:700;color:rgba(255,255,255,0.9);margin-bottom:5px;letter-spacing:1px;">⚖ 法律聲明與免責條款 LEGAL DISCLAIMER</div>
    本報告為內部評估使用，由資深估值分析師依公開資訊及合理假設編製，僅供機構內部參考及決策輔助用途。本報告所有數據、預測及估值均基於特定假設，實際結果可能與預測存在重大差異。本報告不構成對外公開收購邀約（Public Tender Offer）或任何形式之公開招募，亦不構成任何證券之買賣建議或投資勸誘。投資人應審慎評估個人財務狀況、風險承受能力及投資目標，並自行判斷投資決策之適當性。本報告所載資訊之準確性、完整性及及時性不作任何明示或暗示保證。任何依賴本報告所作之投資決策，其風險由投資人自行承擔。本文件受版權法保護，未經授權不得複製、轉載或對外散佈。
    <div style="margin-top:5px;font-size:9px;">本報告僅供內部參考，不構成對外公開收購邀約，投資人應審慎評估風險。 ｜ Gogolook (6902.TW) ｜ 報告日期：2026年3月15日 ｜ 下次更新：2026年Q2財報公告後</div>
  </div>
</div>

</div><!-- /slide-container -->
</body>
</html>
