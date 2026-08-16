<h1>Gráfico de Gantt do Projeto</h1>
<p class="subtitle">Construído a partir dos valores de ES, EF, LF e Folga Total já calculados pelo CPM (rede AON)</p>

<div class="duration-banner">
  Duração total do projeto: <b>16 meses</b> — as atividades em vermelho (B, D, H, K, O) formam o caminho crítico e não têm nenhuma barra tracejada de folga.
</div>

<h2>1. Gantt</h2>

![alt text](image-39.png)

![alt text](image-40.png)


<p class="note">Cada barra sólida vai de <b>ES</b> até <b>EF</b> — a duração real da atividade. Logo depois, a faixa <b>azul-clara preenchida</b> mostra a folga livre — o quanto essa atividade pode atrasar sem empurrar nada além dela mesma. Quando ainda sobra folga além disso, aparece uma faixa <b>só com contorno tracejado</b> até o LF — essa parte é "emprestada": só existe porque a atividade sucessora também tem margem para atrasar.</p>

<h2>2. Como ler o gráfico</h2>
<ul>
  <li><b>Linha do tempo (eixo horizontal):</b> os 16 meses do projeto, com uma linha tracejada vermelha marcando o mês 16 — o fim do projeto.</li>
  <li><b>Barras vermelhas sem faixa tracejada:</b> são as atividades do caminho crítico (B, D, H, K, O) — repare que, juntas, elas cobrem a linha do tempo inteira, do mês 0 ao mês 16, sem nenhuma lacuna.</li>
  <li><b>Barras azuis com faixa tracejada:</b> atividades com folga — a barra sólida mostra quando elas realmente ocorrem no cenário mais cedo, e a faixa tracejada mostra o quanto elas poderiam atrasar (a folga total) sem comprometer o prazo final.</li>
  <li><b>Atividades "empilhadas" na vertical</b> (como D, E, F, G, todas começando no mês 2): representam atividades que podem ocorrer em paralelo, já que todas dependem só de B ter terminado.</li>
</ul>

A folga total se mantém constante ao longo de um trecho sem ramificação — mas, no momento em que uma atividade converge com outro caminho (ou é predecessora de mais de um caminho diferente), a folga dali para trás (ou para os pontos de convergência) passa a refletir o caminho mais apertado entre os que se cruzam ali, não necessariamente o caminho que você estava seguindo.



<h2>3. Folga Livre vs. Folga Total no gráfico</h2>
<p>Repare em um padrão que fica bem visível agora:</p>
<ul>
  <li><b>C, L, M e N</b> têm a faixa de folga inteira preenchida em azul-claro — ou seja, toda a folga total delas é <b>livre</b>: elas podem atrasar sozinhas, sem empurrar mais nada.</li>
  <li><b>A, E, F, G, I e J</b> têm folga total, mas ela aparece só como contorno tracejado (sem preenchimento) — porque a folga livre delas é <b>zero</b>. Toda a margem que elas têm está, na prática, "guardada" na atividade seguinte (C, L, I ou M, por exemplo), não nelas mesmas.</li>
  <li><b>B, D, H, K, O</b> (caminho crítico) não têm nenhuma faixa — folga total e livre são as duas zero.</li>
</ul>
<p class="note">Isso confirma visualmente algo que já discutimos: folga total "espalhada" ao longo de um caminho pertence ao caminho como um todo, mas só se torna folga <i>livre</i> de fato no ponto final desse caminho (ou no ponto de convergência), não em cada atividade individual dele.</p>
<h2>4. Por que o Gantt é útil aqui</h2>
<p>Diferente da rede AON/AOA (que mostra a <b>lógica de precedência</b> entre atividades), o Gantt mostra a <b>linha do tempo real</b> do projeto — é o formato que normalmente se usa para acompanhar o andamento físico do cronograma, mês a mês, e para visualizar rapidamente quais atividades estão acontecendo em paralelo em um determinado momento. A rede (AON/AOA) responde "o que precisa terminar antes de quê"; o Gantt responde "o que está acontecendo quando".</p>
