# Gráfico de Gantt do Projeto

<p class="subtitle">Construído a partir dos valores de ES, EF, LF e Folga Total já calculados pelo CPM (rede AON)</p>

<div class="duration-banner">
  Duração total do projeto: <b>16 meses</b> — as atividades em vermelho (B, D, H, K, O) formam o caminho crítico e não têm nenhuma barra tracejada de folga.
</div>

<h2>1. Gantt</h2>

![alt text](image-39.png)

<p class="note">Cada barra sólida vai de <b>ES</b> (início mais cedo) até <b>EF</b> (fim mais cedo) — é a duração real da atividade. A faixa tracejada, quando existe, mostra até onde a atividade poderia se estender sem atrasar o projeto, indo até o <b>LF</b> (fim mais tarde).</p>

<h2>2. Como ler o gráfico</h2>
<ul>
  <li><b>Linha do tempo (eixo horizontal):</b> os 16 meses do projeto, com uma linha tracejada vermelha marcando o mês 16 — o fim do projeto.</li>
  <li><b>Barras vermelhas sem faixa tracejada:</b> são as atividades do caminho crítico (B, D, H, K, O) — repare que, juntas, elas cobrem a linha do tempo inteira, do mês 0 ao mês 16, sem nenhuma lacuna.</li>
  <li><b>Barras azuis com faixa tracejada:</b> atividades com folga — a barra sólida mostra quando elas realmente ocorrem no cenário mais cedo, e a faixa tracejada mostra o quanto elas poderiam atrasar (a folga total) sem comprometer o prazo final.</li>
  <li><b>Atividades "empilhadas" na vertical</b> (como D, E, F, G, todas começando no mês 2): representam atividades que podem ocorrer em paralelo, já que todas dependem só de B ter terminado.</li>
</ul>

<h2>3. Por que o Gantt é útil aqui</h2>
<p>Diferente da rede AON/AOA (que mostra a <b>lógica de precedência</b> entre atividades), o Gantt mostra a <b>linha do tempo real</b> do projeto — é o formato que normalmente se usa para acompanhar o andamento físico do cronograma, mês a mês, e para visualizar rapidamente quais atividades estão acontecendo em paralelo em um determinado momento. A rede (AON/AOA) responde "o que precisa terminar antes de quê"; o Gantt responde "o que está acontecendo quando".</p>
