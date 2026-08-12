<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Rede PERT/CPM do Projeto</title>
<style>
  body {
    font-family: -apple-system, "Segoe UI", Arial, Helvetica, sans-serif;
    max-width: 1200px;
    margin: 0 auto;
    padding: 32px 24px 60px;
    color: #1f2937;
    background: #ffffff;
    line-height: 1.55;
  }
  h1 { font-size: 26px; margin-bottom: 4px; color: #1f3864; }
  h2 { font-size: 19px; margin-top: 40px; color: #1f3864; border-bottom: 2px solid #e3e8f0; padding-bottom: 6px; }
  .subtitle { color: #6b7280; margin-top: 0; margin-bottom: 28px; font-size: 15px; }
  .duration-banner {
    background: #fdecea;
    border: 1px solid #f0c4bf;
    border-radius: 10px;
    padding: 18px 22px;
    margin: 18px 0 30px;
    font-size: 16px;
  }
  .duration-banner b { color: #c0392b; font-size: 20px; }
  .legend {
    display: flex;
    gap: 28px;
    flex-wrap: wrap;
    margin: 14px 0 24px;
    font-size: 13.5px;
    color: #4b5563;
  }
  .legend span { display: inline-flex; align-items: center; gap: 8px; }
  .swatch { width: 22px; height: 3px; display: inline-block; border-radius: 2px; }
  .box-legend { display:inline-block; width:16px; height:16px; border-radius:3px; }
  table {
    border-collapse: collapse;
    width: 100%;
    margin: 16px 0 12px;
    font-size: 14px;
  }
  th, td {
    border: 1px solid #dfe3ea;
    padding: 8px 10px;
    text-align: center;
  }
  th {
    background: #2f5496;
    color: #ffffff;
    font-weight: 600;
  }
  tr:nth-child(even) td { background: #f7f9fc; }
  .svg-wrap {
    overflow-x: auto;
    padding: 10px 0 20px;
    border: 1px solid #e5e7eb;
    border-radius: 10px;
    background: #fcfcfd;
  }
  .note { font-size: 13.5px; color: #6b7280; margin-top: 8px;}
  ul { padding-left: 22px; }
  li { margin-bottom: 6px; }
</style>
</head>
<body>

<h1>Rede PERT/CPM do Projeto</h1>
<p class="subtitle">Diagrama de rede AON (Activity-on-Node) com cálculo de datas cedo/tarde, folgas e caminho crítico</p>

<div class="duration-banner">
  Duração total do projeto: <b>16 meses</b> — definida pelo caminho crítico <b>B → D → H → K → O</b>
  (2 + 4 + 4 + 1 + 5 = 16 meses)
</div>

<h2>1. Rede AON (Activity-on-Node)</h2>
<div class="legend">
  <span><span class="swatch" style="background:#c0392b;"></span> Caminho crítico (folga = 0)</span>
  <span><span class="swatch" style="background:#9a9a9a;"></span> Caminho não crítico</span>
  <span><span class="box-legend" style="background:#fdecea;border:2px solid #c0392b;"></span> Atividade crítica</span>
  <span><span class="box-legend" style="background:#eef2f8;border:2px solid #3a5a8c;"></span> Atividade com folga</span>
</div>
<div class="svg-wrap">
<svg width="100%" viewBox="0 0 1340 830" xmlns="http://www.w3.org/2000/svg" font-family="Arial, Helvetica, sans-serif" role="img">
<title>Rede PERT/CPM (AON) do projeto</title>
<desc>Diagrama de rede atividade-no-nó com datas ES, EF, LS, LF e caminho crítico destacado.</desc>
<defs>
  <marker id="arrow-n" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse">
    <path d="M1 1L9 5L1 9" fill="none" stroke="#8b8b8b" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/>
  </marker>
  <marker id="arrow-c" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse">
    <path d="M1 1L9 5L1 9" fill="none" stroke="#c0392b" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/>
  </marker>
</defs>
<path d="M240.0,190.0 C270.0,190.0 270.0,115.0 300.0,115.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M240.0,490.0 C270.0,490.0 270.0,265.0 300.0,265.0" fill="none" stroke="#c0392b" stroke-width="2.4" marker-end="url(#arrow-c)"/>
<path d="M240.0,490.0 C270.0,490.0 270.0,415.0 300.0,415.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M240.0,490.0 C270.0,490.0 270.0,565.0 300.0,565.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M240.0,490.0 C270.0,490.0 270.0,715.0 300.0,715.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M500.0,265.0 C530.0,265.0 530.0,265.0 560.0,265.0" fill="none" stroke="#c0392b" stroke-width="2.4" marker-end="url(#arrow-c)"/>
<path d="M500.0,265.0 C530.0,265.0 530.0,415.0 560.0,415.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M500.0,415.0 C530.0,415.0 530.0,415.0 560.0,415.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M500.0,565.0 C530.0,565.0 530.0,565.0 560.0,565.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M500.0,715.0 C530.0,715.0 530.0,715.0 560.0,715.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M760.0,265.0 C790.0,265.0 790.0,265.0 820.0,265.0" fill="none" stroke="#c0392b" stroke-width="2.4" marker-end="url(#arrow-c)"/>
<path d="M500.0,715.0 C660.0,715.0 660.0,565.0 820.0,565.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M760.0,565.0 C790.0,565.0 790.0,565.0 820.0,565.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M760.0,715.0 C790.0,715.0 790.0,715.0 820.0,715.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M500.0,115.0 C790.0,115.0 790.0,190.0 1080.0,190.0" fill="none" stroke="#9a9a9a" stroke-width="1.4" marker-end="url(#arrow-n)"/>
<path d="M1020.0,265.0 C1050.0,265.0 1050.0,190.0 1080.0,190.0" fill="none" stroke="#c0392b" stroke-width="2.4" marker-end="url(#arrow-c)"/>
<g><rect x="40" y="135.0" width="200" height="110" rx="6" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.4"/><rect x="40" y="169.0" width="200" height="42" fill="#3a5a8c" opacity="0.08"/><line x1="40" y1="169.0" x2="240" y2="169.0" stroke="#3a5a8c" stroke-width="1"/><line x1="40" y1="211.0" x2="240" y2="211.0" stroke="#3a5a8c" stroke-width="1"/><line x1="140.0" y1="135.0" x2="140.0" y2="169.0" stroke="#3a5a8c" stroke-width="0.8"/><line x1="140.0" y1="211.0" x2="140.0" y2="245.0" stroke="#3a5a8c" stroke-width="0.8"/><text x="90.0" y="157.0" text-anchor="middle" font-size="13" fill="#2c4267">ES 0</text><text x="190.0" y="157.0" text-anchor="middle" font-size="13" fill="#2c4267">EF 1</text><text x="140.0" y="186.0" text-anchor="middle" font-size="20" font-weight="700" fill="#2c4267">A</text><text x="140.0" y="206.0" text-anchor="middle" font-size="12" fill="#2c4267">dur = 1 meses</text><text x="90.0" y="233.0" text-anchor="middle" font-size="13" fill="#2c4267">LS 7</text><text x="190.0" y="233.0" text-anchor="middle" font-size="13" fill="#2c4267">LF 8</text><text x="140.0" y="263.0" text-anchor="middle" font-size="12" fill="#6b6b6b">Folga = 7</text></g>
<g><rect x="40" y="435.0" width="200" height="110" rx="6" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/><rect x="40" y="469.0" width="200" height="42" fill="#c0392b" opacity="0.08"/><line x1="40" y1="469.0" x2="240" y2="469.0" stroke="#c0392b" stroke-width="1"/><line x1="40" y1="511.0" x2="240" y2="511.0" stroke="#c0392b" stroke-width="1"/><line x1="140.0" y1="435.0" x2="140.0" y2="469.0" stroke="#c0392b" stroke-width="0.8"/><line x1="140.0" y1="511.0" x2="140.0" y2="545.0" stroke="#c0392b" stroke-width="0.8"/><text x="90.0" y="457.0" text-anchor="middle" font-size="13" fill="#c0392b">ES 0</text><text x="190.0" y="457.0" text-anchor="middle" font-size="13" fill="#c0392b">EF 2</text><text x="140.0" y="486.0" text-anchor="middle" font-size="20" font-weight="700" fill="#c0392b">B</text><text x="140.0" y="506.0" text-anchor="middle" font-size="12" fill="#c0392b">dur = 2 meses</text><text x="90.0" y="533.0" text-anchor="middle" font-size="13" fill="#c0392b">LS 0</text><text x="190.0" y="533.0" text-anchor="middle" font-size="13" fill="#c0392b">LF 2</text><text x="140.0" y="563.0" text-anchor="middle" font-size="12" fill="#c0392b">Folga = 0 (crítica)</text></g>
<g><rect x="300" y="60" width="200" height="110" rx="6" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.4"/><rect x="300" y="94" width="200" height="42" fill="#3a5a8c" opacity="0.08"/><line x1="300" y1="94" x2="500" y2="94" stroke="#3a5a8c" stroke-width="1"/><line x1="300" y1="136" x2="500" y2="136" stroke="#3a5a8c" stroke-width="1"/><line x1="400.0" y1="60" x2="400.0" y2="94" stroke="#3a5a8c" stroke-width="0.8"/><line x1="400.0" y1="136" x2="400.0" y2="170" stroke="#3a5a8c" stroke-width="0.8"/><text x="350.0" y="82.0" text-anchor="middle" font-size="13" fill="#2c4267">ES 1</text><text x="450.0" y="82.0" text-anchor="middle" font-size="13" fill="#2c4267">EF 4</text><text x="400.0" y="111.0" text-anchor="middle" font-size="20" font-weight="700" fill="#2c4267">C</text><text x="400.0" y="131.0" text-anchor="middle" font-size="12" fill="#2c4267">dur = 3 meses</text><text x="350.0" y="158.0" text-anchor="middle" font-size="13" fill="#2c4267">LS 8</text><text x="450.0" y="158.0" text-anchor="middle" font-size="13" fill="#2c4267">LF 11</text><text x="400.0" y="188" text-anchor="middle" font-size="12" fill="#6b6b6b">Folga = 7</text></g>
<g><rect x="300" y="210" width="200" height="110" rx="6" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/><rect x="300" y="244" width="200" height="42" fill="#c0392b" opacity="0.08"/><line x1="300" y1="244" x2="500" y2="244" stroke="#c0392b" stroke-width="1"/><line x1="300" y1="286" x2="500" y2="286" stroke="#c0392b" stroke-width="1"/><line x1="400.0" y1="210" x2="400.0" y2="244" stroke="#c0392b" stroke-width="0.8"/><line x1="400.0" y1="286" x2="400.0" y2="320" stroke="#c0392b" stroke-width="0.8"/><text x="350.0" y="232.0" text-anchor="middle" font-size="13" fill="#c0392b">ES 2</text><text x="450.0" y="232.0" text-anchor="middle" font-size="13" fill="#c0392b">EF 6</text><text x="400.0" y="261.0" text-anchor="middle" font-size="20" font-weight="700" fill="#c0392b">D</text><text x="400.0" y="281.0" text-anchor="middle" font-size="12" fill="#c0392b">dur = 4 meses</text><text x="350.0" y="308.0" text-anchor="middle" font-size="13" fill="#c0392b">LS 2</text><text x="450.0" y="308.0" text-anchor="middle" font-size="13" fill="#c0392b">LF 6</text><text x="400.0" y="338" text-anchor="middle" font-size="12" fill="#c0392b">Folga = 0 (crítica)</text></g>
<g><rect x="300" y="360" width="200" height="110" rx="6" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.4"/><rect x="300" y="394" width="200" height="42" fill="#3a5a8c" opacity="0.08"/><line x1="300" y1="394" x2="500" y2="394" stroke="#3a5a8c" stroke-width="1"/><line x1="300" y1="436" x2="500" y2="436" stroke="#3a5a8c" stroke-width="1"/><line x1="400.0" y1="360" x2="400.0" y2="394" stroke="#3a5a8c" stroke-width="0.8"/><line x1="400.0" y1="436" x2="400.0" y2="470" stroke="#3a5a8c" stroke-width="0.8"/><text x="350.0" y="382.0" text-anchor="middle" font-size="13" fill="#2c4267">ES 2</text><text x="450.0" y="382.0" text-anchor="middle" font-size="13" fill="#2c4267">EF 7</text><text x="400.0" y="411.0" text-anchor="middle" font-size="20" font-weight="700" fill="#2c4267">E</text><text x="400.0" y="431.0" text-anchor="middle" font-size="12" fill="#2c4267">dur = 5 meses</text><text x="350.0" y="458.0" text-anchor="middle" font-size="13" fill="#2c4267">LS 9</text><text x="450.0" y="458.0" text-anchor="middle" font-size="13" fill="#2c4267">LF 14</text><text x="400.0" y="488" text-anchor="middle" font-size="12" fill="#6b6b6b">Folga = 7</text></g>
<g><rect x="300" y="510" width="200" height="110" rx="6" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.4"/><rect x="300" y="544" width="200" height="42" fill="#3a5a8c" opacity="0.08"/><line x1="300" y1="544" x2="500" y2="544" stroke="#3a5a8c" stroke-width="1"/><line x1="300" y1="586" x2="500" y2="586" stroke="#3a5a8c" stroke-width="1"/><line x1="400.0" y1="510" x2="400.0" y2="544" stroke="#3a5a8c" stroke-width="0.8"/><line x1="400.0" y1="586" x2="400.0" y2="620" stroke="#3a5a8c" stroke-width="0.8"/><text x="350.0" y="532.0" text-anchor="middle" font-size="13" fill="#2c4267">ES 2</text><text x="450.0" y="532.0" text-anchor="middle" font-size="13" fill="#2c4267">EF 8</text><text x="400.0" y="561.0" text-anchor="middle" font-size="20" font-weight="700" fill="#2c4267">F</text><text x="400.0" y="581.0" text-anchor="middle" font-size="12" fill="#2c4267">dur = 6 meses</text><text x="350.0" y="608.0" text-anchor="middle" font-size="13" fill="#2c4267">LS 4</text><text x="450.0" y="608.0" text-anchor="middle" font-size="13" fill="#2c4267">LF 10</text><text x="400.0" y="638" text-anchor="middle" font-size="12" fill="#6b6b6b">Folga = 2</text></g>
<g><rect x="300" y="660" width="200" height="110" rx="6" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.4"/><rect x="300" y="694" width="200" height="42" fill="#3a5a8c" opacity="0.08"/><line x1="300" y1="694" x2="500" y2="694" stroke="#3a5a8c" stroke-width="1"/><line x1="300" y1="736" x2="500" y2="736" stroke="#3a5a8c" stroke-width="1"/><line x1="400.0" y1="660" x2="400.0" y2="694" stroke="#3a5a8c" stroke-width="0.8"/><line x1="400.0" y1="736" x2="400.0" y2="770" stroke="#3a5a8c" stroke-width="0.8"/><text x="350.0" y="682.0" text-anchor="middle" font-size="13" fill="#2c4267">ES 2</text><text x="450.0" y="682.0" text-anchor="middle" font-size="13" fill="#2c4267">EF 7</text><text x="400.0" y="711.0" text-anchor="middle" font-size="20" font-weight="700" fill="#2c4267">G</text><text x="400.0" y="731.0" text-anchor="middle" font-size="12" fill="#2c4267">dur = 5 meses</text><text x="350.0" y="758.0" text-anchor="middle" font-size="13" fill="#2c4267">LS 5</text><text x="450.0" y="758.0" text-anchor="middle" font-size="13" fill="#2c4267">LF 10</text><text x="400.0" y="788" text-anchor="middle" font-size="12" fill="#6b6b6b">Folga = 3</text></g>
<g><rect x="560" y="210" width="200" height="110" rx="6" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/><rect x="560" y="244" width="200" height="42" fill="#c0392b" opacity="0.08"/><line x1="560" y1="244" x2="760" y2="244" stroke="#c0392b" stroke-width="1"/><line x1="560" y1="286" x2="760" y2="286" stroke="#c0392b" stroke-width="1"/><line x1="660.0" y1="210" x2="660.0" y2="244" stroke="#c0392b" stroke-width="0.8"/><line x1="660.0" y1="286" x2="660.0" y2="320" stroke="#c0392b" stroke-width="0.8"/><text x="610.0" y="232.0" text-anchor="middle" font-size="13" fill="#c0392b">ES 6</text><text x="710.0" y="232.0" text-anchor="middle" font-size="13" fill="#c0392b">EF 10</text><text x="660.0" y="261.0" text-anchor="middle" font-size="20" font-weight="700" fill="#c0392b">H</text><text x="660.0" y="281.0" text-anchor="middle" font-size="12" fill="#c0392b">dur = 4 meses</text><text x="610.0" y="308.0" text-anchor="middle" font-size="13" fill="#c0392b">LS 6</text><text x="710.0" y="308.0" text-anchor="middle" font-size="13" fill="#c0392b">LF 10</text><text x="660.0" y="338" text-anchor="middle" font-size="12" fill="#c0392b">Folga = 0 (crítica)</text></g>
<g><rect x="560" y="360" width="200" height="110" rx="6" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.4"/><rect x="560" y="394" width="200" height="42" fill="#3a5a8c" opacity="0.08"/><line x1="560" y1="394" x2="760" y2="394" stroke="#3a5a8c" stroke-width="1"/><line x1="560" y1="436" x2="760" y2="436" stroke="#3a5a8c" stroke-width="1"/><line x1="660.0" y1="360" x2="660.0" y2="394" stroke="#3a5a8c" stroke-width="0.8"/><line x1="660.0" y1="436" x2="660.0" y2="470" stroke="#3a5a8c" stroke-width="0.8"/><text x="610.0" y="382.0" text-anchor="middle" font-size="13" fill="#2c4267">ES 7</text><text x="710.0" y="382.0" text-anchor="middle" font-size="13" fill="#2c4267">EF 9</text><text x="660.0" y="411.0" text-anchor="middle" font-size="20" font-weight="700" fill="#2c4267">L</text><text x="660.0" y="431.0" text-anchor="middle" font-size="12" fill="#2c4267">dur = 2 meses</text><text x="610.0" y="458.0" text-anchor="middle" font-size="13" fill="#2c4267">LS 14</text><text x="710.0" y="458.0" text-anchor="middle" font-size="13" fill="#2c4267">LF 16</text><text x="660.0" y="488" text-anchor="middle" font-size="12" fill="#6b6b6b">Folga = 7</text></g>
<g><rect x="560" y="510" width="200" height="110" rx="6" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.4"/><rect x="560" y="544" width="200" height="42" fill="#3a5a8c" opacity="0.08"/><line x1="560" y1="544" x2="760" y2="544" stroke="#3a5a8c" stroke-width="1"/><line x1="560" y1="586" x2="760" y2="586" stroke="#3a5a8c" stroke-width="1"/><line x1="660.0" y1="510" x2="660.0" y2="544" stroke="#3a5a8c" stroke-width="0.8"/><line x1="660.0" y1="586" x2="660.0" y2="620" stroke="#3a5a8c" stroke-width="0.8"/><text x="610.0" y="532.0" text-anchor="middle" font-size="13" fill="#2c4267">ES 8</text><text x="710.0" y="532.0" text-anchor="middle" font-size="13" fill="#2c4267">EF 11</text><text x="660.0" y="561.0" text-anchor="middle" font-size="20" font-weight="700" fill="#2c4267">I</text><text x="660.0" y="581.0" text-anchor="middle" font-size="12" fill="#2c4267">dur = 3 meses</text><text x="610.0" y="608.0" text-anchor="middle" font-size="13" fill="#2c4267">LS 10</text><text x="710.0" y="608.0" text-anchor="middle" font-size="13" fill="#2c4267">LF 13</text><text x="660.0" y="638" text-anchor="middle" font-size="12" fill="#6b6b6b">Folga = 2</text></g>
<g><rect x="560" y="660" width="200" height="110" rx="6" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.4"/><rect x="560" y="694" width="200" height="42" fill="#3a5a8c" opacity="0.08"/><line x1="560" y1="694" x2="760" y2="694" stroke="#3a5a8c" stroke-width="1"/><line x1="560" y1="736" x2="760" y2="736" stroke="#3a5a8c" stroke-width="1"/><line x1="660.0" y1="660" x2="660.0" y2="694" stroke="#3a5a8c" stroke-width="0.8"/><line x1="660.0" y1="736" x2="660.0" y2="770" stroke="#3a5a8c" stroke-width="0.8"/><text x="610.0" y="682.0" text-anchor="middle" font-size="13" fill="#2c4267">ES 7</text><text x="710.0" y="682.0" text-anchor="middle" font-size="13" fill="#2c4267">EF 9</text><text x="660.0" y="711.0" text-anchor="middle" font-size="20" font-weight="700" fill="#2c4267">J</text><text x="660.0" y="731.0" text-anchor="middle" font-size="12" fill="#2c4267">dur = 2 meses</text><text x="610.0" y="758.0" text-anchor="middle" font-size="13" fill="#2c4267">LS 10</text><text x="710.0" y="758.0" text-anchor="middle" font-size="13" fill="#2c4267">LF 12</text><text x="660.0" y="788" text-anchor="middle" font-size="12" fill="#6b6b6b">Folga = 3</text></g>
<g><rect x="820" y="210" width="200" height="110" rx="6" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/><rect x="820" y="244" width="200" height="42" fill="#c0392b" opacity="0.08"/><line x1="820" y1="244" x2="1020" y2="244" stroke="#c0392b" stroke-width="1"/><line x1="820" y1="286" x2="1020" y2="286" stroke="#c0392b" stroke-width="1"/><line x1="920.0" y1="210" x2="920.0" y2="244" stroke="#c0392b" stroke-width="0.8"/><line x1="920.0" y1="286" x2="920.0" y2="320" stroke="#c0392b" stroke-width="0.8"/><text x="870.0" y="232.0" text-anchor="middle" font-size="13" fill="#c0392b">ES 10</text><text x="970.0" y="232.0" text-anchor="middle" font-size="13" fill="#c0392b">EF 11</text><text x="920.0" y="261.0" text-anchor="middle" font-size="20" font-weight="700" fill="#c0392b">K</text><text x="920.0" y="281.0" text-anchor="middle" font-size="12" fill="#c0392b">dur = 1 meses</text><text x="870.0" y="308.0" text-anchor="middle" font-size="13" fill="#c0392b">LS 10</text><text x="970.0" y="308.0" text-anchor="middle" font-size="13" fill="#c0392b">LF 11</text><text x="920.0" y="338" text-anchor="middle" font-size="12" fill="#c0392b">Folga = 0 (crítica)</text></g>
<g><rect x="820" y="510" width="200" height="110" rx="6" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.4"/><rect x="820" y="544" width="200" height="42" fill="#3a5a8c" opacity="0.08"/><line x1="820" y1="544" x2="1020" y2="544" stroke="#3a5a8c" stroke-width="1"/><line x1="820" y1="586" x2="1020" y2="586" stroke="#3a5a8c" stroke-width="1"/><line x1="920.0" y1="510" x2="920.0" y2="544" stroke="#3a5a8c" stroke-width="0.8"/><line x1="920.0" y1="586" x2="920.0" y2="620" stroke="#3a5a8c" stroke-width="0.8"/><text x="870.0" y="532.0" text-anchor="middle" font-size="13" fill="#2c4267">ES 11</text><text x="970.0" y="532.0" text-anchor="middle" font-size="13" fill="#2c4267">EF 14</text><text x="920.0" y="561.0" text-anchor="middle" font-size="20" font-weight="700" fill="#2c4267">M</text><text x="920.0" y="581.0" text-anchor="middle" font-size="12" fill="#2c4267">dur = 3 meses</text><text x="870.0" y="608.0" text-anchor="middle" font-size="13" fill="#2c4267">LS 13</text><text x="970.0" y="608.0" text-anchor="middle" font-size="13" fill="#2c4267">LF 16</text><text x="920.0" y="638" text-anchor="middle" font-size="12" fill="#6b6b6b">Folga = 2</text></g>
<g><rect x="820" y="660" width="200" height="110" rx="6" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.4"/><rect x="820" y="694" width="200" height="42" fill="#3a5a8c" opacity="0.08"/><line x1="820" y1="694" x2="1020" y2="694" stroke="#3a5a8c" stroke-width="1"/><line x1="820" y1="736" x2="1020" y2="736" stroke="#3a5a8c" stroke-width="1"/><line x1="920.0" y1="660" x2="920.0" y2="694" stroke="#3a5a8c" stroke-width="0.8"/><line x1="920.0" y1="736" x2="920.0" y2="770" stroke="#3a5a8c" stroke-width="0.8"/><text x="870.0" y="682.0" text-anchor="middle" font-size="13" fill="#2c4267">ES 9</text><text x="970.0" y="682.0" text-anchor="middle" font-size="13" fill="#2c4267">EF 13</text><text x="920.0" y="711.0" text-anchor="middle" font-size="20" font-weight="700" fill="#2c4267">N</text><text x="920.0" y="731.0" text-anchor="middle" font-size="12" fill="#2c4267">dur = 4 meses</text><text x="870.0" y="758.0" text-anchor="middle" font-size="13" fill="#2c4267">LS 12</text><text x="970.0" y="758.0" text-anchor="middle" font-size="13" fill="#2c4267">LF 16</text><text x="920.0" y="788" text-anchor="middle" font-size="12" fill="#6b6b6b">Folga = 3</text></g>
<g><rect x="1080" y="135.0" width="200" height="110" rx="6" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/><rect x="1080" y="169.0" width="200" height="42" fill="#c0392b" opacity="0.08"/><line x1="1080" y1="169.0" x2="1280" y2="169.0" stroke="#c0392b" stroke-width="1"/><line x1="1080" y1="211.0" x2="1280" y2="211.0" stroke="#c0392b" stroke-width="1"/><line x1="1180.0" y1="135.0" x2="1180.0" y2="169.0" stroke="#c0392b" stroke-width="0.8"/><line x1="1180.0" y1="211.0" x2="1180.0" y2="245.0" stroke="#c0392b" stroke-width="0.8"/><text x="1130.0" y="157.0" text-anchor="middle" font-size="13" fill="#c0392b">ES 11</text><text x="1230.0" y="157.0" text-anchor="middle" font-size="13" fill="#c0392b">EF 16</text><text x="1180.0" y="186.0" text-anchor="middle" font-size="20" font-weight="700" fill="#c0392b">O</text><text x="1180.0" y="206.0" text-anchor="middle" font-size="12" fill="#c0392b">dur = 5 meses</text><text x="1130.0" y="233.0" text-anchor="middle" font-size="13" fill="#c0392b">LS 11</text><text x="1230.0" y="233.0" text-anchor="middle" font-size="13" fill="#c0392b">LF 16</text><text x="1180.0" y="263.0" text-anchor="middle" font-size="12" fill="#c0392b">Folga = 0 (crítica)</text></g>
</svg>
</div>
<p class="note">Cada nó traz: <b>ES</b> (início mais cedo), <b>EF</b> (fim mais cedo), <b>LS</b> (início mais tarde), <b>LF</b> (fim mais tarde) e a folga (LS − ES). Atividades com folga = 0 formam o caminho crítico.</p>

<h2>2. Tabela de Cálculo (CPM)</h2>
<table>
  <tr>
    <th>Atividade</th><th>Duração (meses)</th><th>Precedências</th>
    <th>ES</th><th>EF</th><th>LS</th><th>LF</th><th>Folga</th><th>Crítica?</th>
  </tr>
  <tr><td>A</td><td>1</td><td>-----</td><td>0</td><td>1</td><td>7</td><td>8</td><td>7</td><td>Não</td></tr>
<tr style="background:#fdecea;font-weight:600;"><td>B</td><td>2</td><td>-----</td><td>0</td><td>2</td><td>0</td><td>2</td><td>0</td><td>Sim</td></tr>
<tr><td>C</td><td>3</td><td>A</td><td>1</td><td>4</td><td>8</td><td>11</td><td>7</td><td>Não</td></tr>
<tr style="background:#fdecea;font-weight:600;"><td>D</td><td>4</td><td>B</td><td>2</td><td>6</td><td>2</td><td>6</td><td>0</td><td>Sim</td></tr>
<tr><td>E</td><td>5</td><td>B</td><td>2</td><td>7</td><td>9</td><td>14</td><td>7</td><td>Não</td></tr>
<tr><td>F</td><td>6</td><td>B</td><td>2</td><td>8</td><td>4</td><td>10</td><td>2</td><td>Não</td></tr>
<tr><td>G</td><td>5</td><td>B</td><td>2</td><td>7</td><td>5</td><td>10</td><td>3</td><td>Não</td></tr>
<tr style="background:#fdecea;font-weight:600;"><td>H</td><td>4</td><td>D</td><td>6</td><td>10</td><td>6</td><td>10</td><td>0</td><td>Sim</td></tr>
<tr><td>I</td><td>3</td><td>F</td><td>8</td><td>11</td><td>10</td><td>13</td><td>2</td><td>Não</td></tr>
<tr><td>J</td><td>2</td><td>G</td><td>7</td><td>9</td><td>10</td><td>12</td><td>3</td><td>Não</td></tr>
<tr style="background:#fdecea;font-weight:600;"><td>K</td><td>1</td><td>H</td><td>10</td><td>11</td><td>10</td><td>11</td><td>0</td><td>Sim</td></tr>
<tr><td>L</td><td>2</td><td>D, E</td><td>7</td><td>9</td><td>14</td><td>16</td><td>7</td><td>Não</td></tr>
<tr><td>M</td><td>3</td><td>G, I</td><td>11</td><td>14</td><td>13</td><td>16</td><td>2</td><td>Não</td></tr>
<tr><td>N</td><td>4</td><td>J</td><td>9</td><td>13</td><td>12</td><td>16</td><td>3</td><td>Não</td></tr>
<tr style="background:#fdecea;font-weight:600;"><td>O</td><td>5</td><td>C, K</td><td>11</td><td>16</td><td>11</td><td>16</td><td>0</td><td>Sim</td></tr>
</table>

<h2>3. Como o cálculo foi feito</h2>
<p><b>Passagem de avanço (forward pass)</b> — calcula ES e EF de cada atividade:</p>
<ul>
  <li>ES de uma atividade = maior EF entre todas as suas predecessoras (0 se não tiver predecessora);</li>
  <li>EF = ES + duração da atividade.</li>
</ul>
<p><b>Passagem de retorno (backward pass)</b> — calcula LS e LF, partindo da duração total do projeto (16 meses):</p>
<ul>
  <li>LF de uma atividade = menor LS entre todas as suas sucessoras (igual à duração do projeto se não tiver sucessora);</li>
  <li>LS = LF − duração da atividade.</li>
</ul>
<p><b>Folga (slack)</b> = LS − ES (ou LF − EF). Atividades com folga igual a zero não podem atrasar sem atrasar o projeto inteiro — são as atividades <b>críticas</b>, e a sequência delas forma o <b>caminho crítico</b>.</p>

<h2>4. Caminho Crítico</h2>
<p>O caminho crítico do projeto é:</p>
<p style="font-size:18px; font-weight:700; color:#c0392b; text-align:center; margin: 18px 0;">
  B (2) → D (4) → H (4) → K (1) → O (5) = 16 meses
</p>
<p>Todas as demais atividades (A, C, E, F, G, I, J, L, M, N) possuem folga e podem, dentro do limite indicado na tabela, atrasar sem comprometer o prazo final de 16 meses — desde que essa folga não seja excedida.</p>







<h1>Rede PERT/CPM — Método Americano (AOA)</h1>
<p class="subtitle">Diagrama Activity-on-Arrow (atividade-na-seta), com eventos numerados, atividades fictícias (dummies) e comparação com o método francês (AON)</p>

<div class="duration-banner">
  Duração total do projeto: <b>16 meses</b> — mesmo resultado do método AON, pelo caminho crítico <b>1 → 3 → 4 → 9 → 11 → 15</b>
  (atividades B → D → H → K → O)
</div>

<h2>1. Rede AOA (Activity-on-Arrow)</h2>
<div class="legend">
  <span><span class="swatch" style="background:#c0392b;"></span> Caminho crítico</span>
  <span><span class="swatch" style="background:#9a9a9a;"></span> Caminho não crítico</span>
  <span><span class="swatch dash"></span> Atividade fictícia (dummy)</span>
  <span><span class="circle-legend" style="background:#fdecea;border:2px solid #c0392b;"></span> Evento crítico</span>
  <span><span class="circle-legend" style="background:#eef2f8;border:2px solid #3a5a8c;"></span> Evento com folga</span>
</div>
<div class="svg-wrap">
<svg width="100%" viewBox="0 0 1310 660" xmlns="http://www.w3.org/2000/svg" font-family="Arial, Helvetica, sans-serif" role="img">
<title>Rede PERT/CPM metodo americano AOA</title>
<desc>Diagrama de rede atividade-na-seta (AOA) com eventos, tempos TE/TL, atividades ficticias (dummies) e caminho critico destacado.</desc>
<defs>
  <marker id="arr-n" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse">
    <path d="M1 1L9 5L1 9" fill="none" stroke="#8b8b8b" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/>
  </marker>
  <marker id="arr-c" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse">
    <path d="M1 1L9 5L1 9" fill="none" stroke="#c0392b" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/>
  </marker>
</defs>
<path d="M106.3,278.4 C153.3,106.6 200.3,106.6 248.7,161.6" fill="none" stroke="#8b8b8b" stroke-width="1.3" marker-end="url(#arr-n)"/>
<text x="177.5" y="99.6" text-anchor="middle" font-size="13.5" font-weight="700" fill="#374151">A (1)</text>
<path d="M114.0,300.0 L241.0,300.0" fill="none" stroke="#c0392b" stroke-width="2.2" marker-end="url(#arr-c)"/>
<text x="177.5" y="288.0" text-anchor="middle" font-size="13.5" font-weight="700" fill="#c0392b">B (2)</text>
<path d="M307.8,149.0 C479.2,94.0 650.6,94.0 827.2,291.0" fill="none" stroke="#8b8b8b" stroke-width="1.3" marker-end="url(#arr-n)"/>
<text x="567.5" y="87.0" text-anchor="middle" font-size="13.5" font-weight="700" fill="#374151">C (3)</text>
<path d="M309.0,300.0 L436.0,300.0" fill="none" stroke="#c0392b" stroke-width="2.2" marker-end="url(#arr-c)"/>
<text x="372.5" y="288.0" text-anchor="middle" font-size="13.5" font-weight="700" fill="#c0392b">D (4)</text>
<path d="M300.6,322.3 C348.1,502.7 395.5,502.7 444.4,447.7" fill="none" stroke="#8b8b8b" stroke-width="1.3" marker-end="url(#arr-n)"/>
<text x="372.5" y="515.7" text-anchor="middle" font-size="13.5" font-weight="700" fill="#374151">G (5)</text>
<path d="M293.5,328.5 C345.7,626.5 397.8,626.5 451.5,571.5" fill="none" stroke="#8b8b8b" stroke-width="1.3" marker-end="url(#arr-n)"/>
<text x="372.5" y="639.5" text-anchor="middle" font-size="13.5" font-weight="700" fill="#374151">F (6)</text>
<path d="M306.5,287.1 C414.4,97.9 522.3,97.9 633.5,152.9" fill="none" stroke="#8b8b8b" stroke-width="1.3" marker-end="url(#arr-n)"/>
<text x="470.0" y="90.9" text-anchor="middle" font-size="13.5" font-weight="700" fill="#374151">E (5)</text>
<path d="M504.0,300.0 L631.0,300.0" fill="none" stroke="#c0392b" stroke-width="2.2" marker-end="url(#arr-c)"/>
<text x="567.5" y="288.0" text-anchor="middle" font-size="13.5" font-weight="700" fill="#c0392b">H (4)</text>
<path d="M496.3,278.4 C543.3,106.6 590.3,106.6 638.7,161.6" fill="none" stroke="#8b8b8b" stroke-width="1.3" stroke-dasharray="7 5" marker-end="url(#arr-n)"/>
<text x="567.5" y="99.6" text-anchor="middle" font-size="11.5" font-style="italic" fill="#9ca3af">dummy</text>
<path d="M504.0,470.0 L631.0,470.0" fill="none" stroke="#8b8b8b" stroke-width="1.3" marker-end="url(#arr-n)"/>
<text x="567.5" y="458.0" text-anchor="middle" font-size="13.5" font-weight="700" fill="#374151">J (2)</text>
<path d="M498.3,488.9 C544.0,636.1 589.6,636.1 636.7,581.1" fill="none" stroke="#8b8b8b" stroke-width="1.3" stroke-dasharray="7 5" marker-end="url(#arr-n)"/>
<text x="567.5" y="649.1" text-anchor="middle" font-size="11.5" font-style="italic" fill="#9ca3af">dummy</text>
<path d="M504.0,600.0 L631.0,600.0" fill="none" stroke="#8b8b8b" stroke-width="1.3" marker-end="url(#arr-n)"/>
<text x="567.5" y="588.0" text-anchor="middle" font-size="13.5" font-weight="700" fill="#374151">I (3)</text>
<path d="M699.0,140.0 L826.0,140.0" fill="none" stroke="#8b8b8b" stroke-width="1.3" marker-end="url(#arr-n)"/>
<text x="762.5" y="128.0" text-anchor="middle" font-size="13.5" font-weight="700" fill="#374151">L (2)</text>
<path d="M699.0,600.0 L826.0,600.0" fill="none" stroke="#8b8b8b" stroke-width="1.3" marker-end="url(#arr-n)"/>
<text x="762.5" y="588.0" text-anchor="middle" font-size="13.5" font-weight="700" fill="#374151">M (3)</text>
<path d="M699.0,300.0 L826.0,300.0" fill="none" stroke="#c0392b" stroke-width="2.2" marker-end="url(#arr-c)"/>
<text x="762.5" y="288.0" text-anchor="middle" font-size="13.5" font-weight="700" fill="#c0392b">K (1)</text>
<path d="M699.0,470.0 L826.0,470.0" fill="none" stroke="#8b8b8b" stroke-width="1.3" marker-end="url(#arr-n)"/>
<text x="762.5" y="458.0" text-anchor="middle" font-size="13.5" font-weight="700" fill="#374151">N (4)</text>
<path d="M894.0,300.0 L1021.0,300.0" fill="none" stroke="#c0392b" stroke-width="2.2" marker-end="url(#arr-c)"/>
<text x="957.5" y="288.0" text-anchor="middle" font-size="13.5" font-weight="700" fill="#c0392b">O (5)</text>
<path d="M891.5,152.9 C999.4,97.9 1107.3,97.9 1218.5,287.1" fill="none" stroke="#8b8b8b" stroke-width="1.3" stroke-dasharray="7 5" marker-end="url(#arr-n)"/>
<text x="1055.0" y="90.9" text-anchor="middle" font-size="11.5" font-style="italic" fill="#9ca3af">dummy</text>
<path d="M886.9,579.3 C997.9,634.3 1108.8,634.3 1223.1,320.7" fill="none" stroke="#8b8b8b" stroke-width="1.3" stroke-dasharray="7 5" marker-end="url(#arr-n)"/>
<text x="1055.0" y="647.3" text-anchor="middle" font-size="11.5" font-style="italic" fill="#9ca3af">dummy</text>
<path d="M891.2,456.4 C999.3,511.4 1107.4,511.4 1218.8,313.6" fill="none" stroke="#8b8b8b" stroke-width="1.3" stroke-dasharray="7 5" marker-end="url(#arr-n)"/>
<text x="1055.0" y="524.4" text-anchor="middle" font-size="11.5" font-style="italic" fill="#9ca3af">dummy</text>
<path d="M1089.0,300.0 L1216.0,300.0" fill="none" stroke="#c0392b" stroke-width="2.2" stroke-dasharray="7 5" marker-end="url(#arr-c)"/>
<text x="1152.5" y="288.0" text-anchor="middle" font-size="11.5" font-style="italic" fill="#c0392b">dummy</text>
<circle cx="80" cy="300" r="34" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/>
<line x1="80" y1="266" x2="80" y2="334" stroke="#c0392b" stroke-width="1"/>
<line x1="80" y1="300" x2="114" y2="300" stroke="#c0392b" stroke-width="1"/>
<text x="63.0" y="305.0" text-anchor="middle" font-size="15" font-weight="700" fill="#c0392b">1</text>
<text x="97.0" y="291.0" text-anchor="middle" font-size="12" fill="#c0392b">0</text>
<text x="97.0" y="318.0" text-anchor="middle" font-size="12" fill="#c0392b">0</text>
<circle cx="275" cy="140" r="34" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.6"/>
<line x1="275" y1="106" x2="275" y2="174" stroke="#3a5a8c" stroke-width="1"/>
<line x1="275" y1="140" x2="309" y2="140" stroke="#3a5a8c" stroke-width="1"/>
<text x="258.0" y="145.0" text-anchor="middle" font-size="15" font-weight="700" fill="#2c4267">2</text>
<text x="292.0" y="131.0" text-anchor="middle" font-size="12" fill="#2c4267">1</text>
<text x="292.0" y="158.0" text-anchor="middle" font-size="12" fill="#2c4267">8</text>
<circle cx="275" cy="300" r="34" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/>
<line x1="275" y1="266" x2="275" y2="334" stroke="#c0392b" stroke-width="1"/>
<line x1="275" y1="300" x2="309" y2="300" stroke="#c0392b" stroke-width="1"/>
<text x="258.0" y="305.0" text-anchor="middle" font-size="15" font-weight="700" fill="#c0392b">3</text>
<text x="292.0" y="291.0" text-anchor="middle" font-size="12" fill="#c0392b">2</text>
<text x="292.0" y="318.0" text-anchor="middle" font-size="12" fill="#c0392b">2</text>
<circle cx="470" cy="300" r="34" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/>
<line x1="470" y1="266" x2="470" y2="334" stroke="#c0392b" stroke-width="1"/>
<line x1="470" y1="300" x2="504" y2="300" stroke="#c0392b" stroke-width="1"/>
<text x="453.0" y="305.0" text-anchor="middle" font-size="15" font-weight="700" fill="#c0392b">4</text>
<text x="487.0" y="291.0" text-anchor="middle" font-size="12" fill="#c0392b">6</text>
<text x="487.0" y="318.0" text-anchor="middle" font-size="12" fill="#c0392b">6</text>
<circle cx="470" cy="470" r="34" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.6"/>
<line x1="470" y1="436" x2="470" y2="504" stroke="#3a5a8c" stroke-width="1"/>
<line x1="470" y1="470" x2="504" y2="470" stroke="#3a5a8c" stroke-width="1"/>
<text x="453.0" y="475.0" text-anchor="middle" font-size="15" font-weight="700" fill="#2c4267">5</text>
<text x="487.0" y="461.0" text-anchor="middle" font-size="12" fill="#2c4267">7</text>
<text x="487.0" y="488.0" text-anchor="middle" font-size="12" fill="#2c4267">10</text>
<circle cx="470" cy="600" r="34" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.6"/>
<line x1="470" y1="566" x2="470" y2="634" stroke="#3a5a8c" stroke-width="1"/>
<line x1="470" y1="600" x2="504" y2="600" stroke="#3a5a8c" stroke-width="1"/>
<text x="453.0" y="605.0" text-anchor="middle" font-size="15" font-weight="700" fill="#2c4267">6</text>
<text x="487.0" y="591.0" text-anchor="middle" font-size="12" fill="#2c4267">8</text>
<text x="487.0" y="618.0" text-anchor="middle" font-size="12" fill="#2c4267">10</text>
<circle cx="665" cy="140" r="34" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.6"/>
<line x1="665" y1="106" x2="665" y2="174" stroke="#3a5a8c" stroke-width="1"/>
<line x1="665" y1="140" x2="699" y2="140" stroke="#3a5a8c" stroke-width="1"/>
<text x="648.0" y="145.0" text-anchor="middle" font-size="15" font-weight="700" fill="#2c4267">7</text>
<text x="682.0" y="131.0" text-anchor="middle" font-size="12" fill="#2c4267">7</text>
<text x="682.0" y="158.0" text-anchor="middle" font-size="12" fill="#2c4267">14</text>
<circle cx="665" cy="600" r="34" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.6"/>
<line x1="665" y1="566" x2="665" y2="634" stroke="#3a5a8c" stroke-width="1"/>
<line x1="665" y1="600" x2="699" y2="600" stroke="#3a5a8c" stroke-width="1"/>
<text x="648.0" y="605.0" text-anchor="middle" font-size="15" font-weight="700" fill="#2c4267">8</text>
<text x="682.0" y="591.0" text-anchor="middle" font-size="12" fill="#2c4267">11</text>
<text x="682.0" y="618.0" text-anchor="middle" font-size="12" fill="#2c4267">13</text>
<circle cx="665" cy="300" r="34" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/>
<line x1="665" y1="266" x2="665" y2="334" stroke="#c0392b" stroke-width="1"/>
<line x1="665" y1="300" x2="699" y2="300" stroke="#c0392b" stroke-width="1"/>
<text x="648.0" y="305.0" text-anchor="middle" font-size="15" font-weight="700" fill="#c0392b">9</text>
<text x="682.0" y="291.0" text-anchor="middle" font-size="12" fill="#c0392b">10</text>
<text x="682.0" y="318.0" text-anchor="middle" font-size="12" fill="#c0392b">10</text>
<circle cx="665" cy="470" r="34" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.6"/>
<line x1="665" y1="436" x2="665" y2="504" stroke="#3a5a8c" stroke-width="1"/>
<line x1="665" y1="470" x2="699" y2="470" stroke="#3a5a8c" stroke-width="1"/>
<text x="648.0" y="475.0" text-anchor="middle" font-size="15" font-weight="700" fill="#2c4267">10</text>
<text x="682.0" y="461.0" text-anchor="middle" font-size="12" fill="#2c4267">9</text>
<text x="682.0" y="488.0" text-anchor="middle" font-size="12" fill="#2c4267">12</text>
<circle cx="860" cy="300" r="34" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/>
<line x1="860" y1="266" x2="860" y2="334" stroke="#c0392b" stroke-width="1"/>
<line x1="860" y1="300" x2="894" y2="300" stroke="#c0392b" stroke-width="1"/>
<text x="843.0" y="305.0" text-anchor="middle" font-size="15" font-weight="700" fill="#c0392b">11</text>
<text x="877.0" y="291.0" text-anchor="middle" font-size="12" fill="#c0392b">11</text>
<text x="877.0" y="318.0" text-anchor="middle" font-size="12" fill="#c0392b">11</text>
<circle cx="860" cy="140" r="34" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.6"/>
<line x1="860" y1="106" x2="860" y2="174" stroke="#3a5a8c" stroke-width="1"/>
<line x1="860" y1="140" x2="894" y2="140" stroke="#3a5a8c" stroke-width="1"/>
<text x="843.0" y="145.0" text-anchor="middle" font-size="15" font-weight="700" fill="#2c4267">12</text>
<text x="877.0" y="131.0" text-anchor="middle" font-size="12" fill="#2c4267">9</text>
<text x="877.0" y="158.0" text-anchor="middle" font-size="12" fill="#2c4267">16</text>
<circle cx="860" cy="600" r="34" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.6"/>
<line x1="860" y1="566" x2="860" y2="634" stroke="#3a5a8c" stroke-width="1"/>
<line x1="860" y1="600" x2="894" y2="600" stroke="#3a5a8c" stroke-width="1"/>
<text x="843.0" y="605.0" text-anchor="middle" font-size="15" font-weight="700" fill="#2c4267">13</text>
<text x="877.0" y="591.0" text-anchor="middle" font-size="12" fill="#2c4267">14</text>
<text x="877.0" y="618.0" text-anchor="middle" font-size="12" fill="#2c4267">16</text>
<circle cx="860" cy="470" r="34" fill="#eef2f8" stroke="#3a5a8c" stroke-width="1.6"/>
<line x1="860" y1="436" x2="860" y2="504" stroke="#3a5a8c" stroke-width="1"/>
<line x1="860" y1="470" x2="894" y2="470" stroke="#3a5a8c" stroke-width="1"/>
<text x="843.0" y="475.0" text-anchor="middle" font-size="15" font-weight="700" fill="#2c4267">14</text>
<text x="877.0" y="461.0" text-anchor="middle" font-size="12" fill="#2c4267">13</text>
<text x="877.0" y="488.0" text-anchor="middle" font-size="12" fill="#2c4267">16</text>
<circle cx="1055" cy="300" r="34" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/>
<line x1="1055" y1="266" x2="1055" y2="334" stroke="#c0392b" stroke-width="1"/>
<line x1="1055" y1="300" x2="1089" y2="300" stroke="#c0392b" stroke-width="1"/>
<text x="1038.0" y="305.0" text-anchor="middle" font-size="15" font-weight="700" fill="#c0392b">15</text>
<text x="1072.0" y="291.0" text-anchor="middle" font-size="12" fill="#c0392b">16</text>
<text x="1072.0" y="318.0" text-anchor="middle" font-size="12" fill="#c0392b">16</text>
<circle cx="1250" cy="300" r="34" fill="#fdecea" stroke="#c0392b" stroke-width="2.4"/>
<line x1="1250" y1="266" x2="1250" y2="334" stroke="#c0392b" stroke-width="1"/>
<line x1="1250" y1="300" x2="1284" y2="300" stroke="#c0392b" stroke-width="1"/>
<text x="1233.0" y="305.0" text-anchor="middle" font-size="15" font-weight="700" fill="#c0392b">16</text>
<text x="1267.0" y="291.0" text-anchor="middle" font-size="12" fill="#c0392b">16</text>
<text x="1267.0" y="318.0" text-anchor="middle" font-size="12" fill="#c0392b">16</text>
</svg>
</div>
<p class="note">Cada evento (círculo) é dividido em três campos: <b>número do evento</b> (esquerda), <b>TE</b> — tempo mais cedo (canto superior direito) e <b>TL</b> — tempo mais tarde (canto inferior direito). As setas tracejadas são atividades fictícias (dummies), com duração zero, usadas apenas para preservar a lógica de precedência.</p>

<h2>2. Por que precisamos de dummies aqui</h2>
<ul>
  <li><b>Evento 7 (tail de L):</b> a atividade L depende de D <i>e</i> E. Como H depende só de D, o evento 4 (fim de D) não pode ser o mesmo evento que "libera" L — então a atividade E chega diretamente ao evento 7, e uma dummy parte do evento 4 (fim de D) até o evento 7, garantindo que L só comece quando D <i>e</i> E estiverem prontas.</li>
  <li><b>Evento 8 (tail de M):</b> mesma lógica — M depende de G <i>e</i> I. J depende só de G, então G não pode "liberar" M sozinho. A atividade I chega direto ao evento 8, e uma dummy parte do evento 5 (fim de G) até o evento 8.</li>
  <li><b>Evento 11 (tail de O):</b> como nem C nem K alimentam mais nenhuma outra atividade, elas convergem diretamente no mesmo evento — <b>não é necessária dummy aqui</b>.</li>
  <li><b>Dummies finais (12→16, 13→16, 14→16, 15→16):</b> usadas apenas para unificar as quatro atividades "fim de rede" (L, M, N, O) em um único evento de término do projeto, permitindo ler a duração total em um só lugar.</li>
</ul>

<h2>3. Tabela de Tempos dos Eventos</h2>
<table>
  <tr><th>Evento</th><th>Significado</th><th>TE</th><th>TL</th><th>Folga</th><th>Crítico?</th></tr>
  <tr style="background:#fdecea;font-weight:600;"><td>1</td><td style='text-align:left;'>Início do projeto</td><td>0</td><td>0</td><td>0</td><td>Sim</td></tr>
<tr><td>2</td><td style='text-align:left;'>Fim de A</td><td>1</td><td>8</td><td>7</td><td>Não</td></tr>
<tr style="background:#fdecea;font-weight:600;"><td>3</td><td style='text-align:left;'>Fim de B</td><td>2</td><td>2</td><td>0</td><td>Sim</td></tr>
<tr style="background:#fdecea;font-weight:600;"><td>4</td><td style='text-align:left;'>Fim de D</td><td>6</td><td>6</td><td>0</td><td>Sim</td></tr>
<tr><td>5</td><td style='text-align:left;'>Fim de G</td><td>7</td><td>10</td><td>3</td><td>Não</td></tr>
<tr><td>6</td><td style='text-align:left;'>Fim de F</td><td>8</td><td>10</td><td>2</td><td>Não</td></tr>
<tr><td>7</td><td style='text-align:left;'>Convergência D+E (início de L)</td><td>7</td><td>14</td><td>7</td><td>Não</td></tr>
<tr><td>8</td><td style='text-align:left;'>Convergência G+I (início de M)</td><td>11</td><td>13</td><td>2</td><td>Não</td></tr>
<tr style="background:#fdecea;font-weight:600;"><td>9</td><td style='text-align:left;'>Fim de H</td><td>10</td><td>10</td><td>0</td><td>Sim</td></tr>
<tr><td>10</td><td style='text-align:left;'>Fim de J</td><td>9</td><td>12</td><td>3</td><td>Não</td></tr>
<tr style="background:#fdecea;font-weight:600;"><td>11</td><td style='text-align:left;'>Convergência C+K (início de O)</td><td>11</td><td>11</td><td>0</td><td>Sim</td></tr>
<tr><td>12</td><td style='text-align:left;'>Fim de L</td><td>9</td><td>16</td><td>7</td><td>Não</td></tr>
<tr><td>13</td><td style='text-align:left;'>Fim de M</td><td>14</td><td>16</td><td>2</td><td>Não</td></tr>
<tr><td>14</td><td style='text-align:left;'>Fim de N</td><td>13</td><td>16</td><td>3</td><td>Não</td></tr>
<tr style="background:#fdecea;font-weight:600;"><td>15</td><td style='text-align:left;'>Fim de O</td><td>16</td><td>16</td><td>0</td><td>Sim</td></tr>
<tr style="background:#fdecea;font-weight:600;"><td>16</td><td style='text-align:left;'>Fim do projeto</td><td>16</td><td>16</td><td>0</td><td>Sim</td></tr>
</table>

<h2>4. Comparação entre os Métodos</h2>
<table>
  <tr><th>Aspecto</th><th>Método Francês (AON)</th><th>Método Americano (AOA)</th></tr>
  <tr><td style='text-align:left;font-weight:600;'>Duração total do projeto</td><td>16 meses</td><td>16 meses</td></tr>
<tr><td style='text-align:left;font-weight:600;'>Caminho crítico (atividades)</td><td>B → D → H → K → O</td><td>B → D → H → K → O</td></tr>
<tr><td style='text-align:left;font-weight:600;'>Nº de elementos no diagrama</td><td>15 nós (uma caixa por atividade)</td><td>16 eventos + 15 atividades + 6 dummies</td></tr>
<tr><td style='text-align:left;font-weight:600;'>Precisa de atividades fictícias?</td><td>Não</td><td>Sim (para representar corretamente L e M, mais 4 dummies de fechamento)</td></tr>
<tr><td style='text-align:left;font-weight:600;'>Onde ficam ES/EF/LS/LF</td><td>Dentro da própria caixa da atividade</td><td>Distribuídos entre os eventos (TE/TL) que a atividade conecta</td></tr>
</table>

<h2>5. Conclusão</h2>
<p>Como esperado, os dois métodos chegam exatamente ao <b>mesmo resultado numérico</b>: duração total de <b>16 meses</b> e o mesmo caminho crítico, formado pelas atividades <b>B, D, H, K e O</b>. Isso confirma que AON e AOA são apenas <b>duas convenções gráficas diferentes</b> para representar a mesma lógica de precedência e os mesmos cálculos de CPM — a escolha entre elas é basicamente uma questão de preferência de notação (ou de exigência da disciplina/norma), não uma diferença de resultado. A principal diferença prática está no <b>método americano exigir atividades fictícias (dummies)</b> sempre que duas atividades compartilham parcialmente as mesmas predecessoras, o que deixa o diagrama AOA mais denso e mais sujeito a erros de construção do que o AON.</p>



</body>
</html>