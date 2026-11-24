<style>
:root {
  --preto: #000;
  --verde-fundo: #0b2e1b;
  --verde-painel: #061c10;
  --concreto: #b9b8ae;
  --concreto-claro: #e4e3d8;
  --concreto-escuro: #6e7069;
  --texto: #dcdbd0;
  --mono: ui-monospace, "SFMono-Regular", Menlo, Consolas, "Courier New", monospace;
  --pesado: "Arial Black", "Helvetica Neue", Arial, sans-serif;
  --sombra: 12px 12px 0 var(--preto);
  --granulado: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='3' stitchTiles='stitch'/%3E%3CfeColorMatrix values='0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 .25 0'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
}
/* base */
html { background: var(--preto); }
body { background: var(--verde-fundo); color: var(--texto); font: 17px/1.7 var(--mono); }
.wrapper { max-width: 1100px; }
.page-content { padding: 2.5rem 0; }
::selection { background: var(--concreto); color: var(--preto); }
/* títulos */
h1, h2, .site-title, .v, .placa, .sigla { font-family: var(--pesado); font-weight: 900; text-transform: uppercase; }
h1, h2 { color: var(--concreto-claro); line-height: 1.15; }
h1 { text-align: center !important; font-size: 2.3rem; letter-spacing: -0.02em; padding-bottom: 0.4em; margin-bottom: 0.6em; border-bottom: 8px solid var(--concreto); }
h2 { font-size: 1.15rem; letter-spacing: 0.02em; padding-bottom: 0.35em; margin-top: 1.5em; border-bottom: 4px solid var(--concreto); }
.subtitulo { text-align: center; color: var(--concreto); font-size: 1.05rem; letter-spacing: 0.05em; margin-bottom: 2.5rem; }
/* logo */
.site-title::before, .site-title::after, h1::before, h1::after { content: "φ"; display: inline-block; vertical-align: middle; font-family: Georgia, "Times New Roman", serif; font-weight: 700; font-size: 1.15em; text-transform: none; }
.site-title::before, h1::before { margin-right: 0.35em; }
.site-title::after, h1::after { margin-left: 0.35em; }
/* cabeçalho e rodapé */
.site-header { background: var(--preto); border: 0; }
.site-header::after { content: ""; display: block; height: 16px; background: repeating-linear-gradient(90deg, var(--concreto-escuro) 0 8px, #3d3f3a 8px 16px); }
.site-title, .site-title:visited { color: var(--concreto-claro); }
.site-nav .page-link { color: var(--texto); text-transform: uppercase; }
.site-nav .page-link:hover { color: var(--preto); }
@media (max-width: 600px) { .site-nav { background: var(--preto); border: 3px solid var(--concreto); border-radius: 0; } }
.site-footer { background: var(--preto); border-top: 8px solid var(--concreto-escuro); margin-top: 2rem; }
.site-footer a, .site-footer a:visited { color: var(--concreto-claro); }
/* links */
a, a:visited { color: var(--concreto-claro); font-weight: 700; text-decoration: underline; text-decoration-thickness: 2px; text-underline-offset: 4px; }
a:hover { color: var(--preto); background: var(--concreto); text-decoration: none; }
a:focus-visible { outline: 3px solid var(--concreto-claro); outline-offset: 3px; }
/* painéis */
.fachada, .coluna-texto, .coluna-lateral, .placa, .laje { box-shadow: var(--sombra); }
.fachada, .intro, .placas, .conjunto { margin-bottom: 3.5rem; }
.duas-colunas { display: flex; gap: 2rem; align-items: flex-start; margin-bottom: 2rem; }
.coluna-texto { flex: 2; min-width: 0; background: var(--verde-painel); border: 5px solid var(--concreto); padding: 1.75rem; }
.coluna-lateral { flex: 1; color: var(--preto); border: 5px solid var(--preto); padding: 1.25rem 1.5rem; background: var(--granulado) var(--concreto); }
.coluna-lateral h2 { text-align: center; color: var(--preto); border-bottom: 5px solid var(--preto); margin-top: 0.2em; }
.coluna-lateral ul { list-style: square; }
@media (max-width: 700px) { .duas-colunas { flex-direction: column; } }
/* fachada: o Verbo em três estágios (pedra, ranhura, pixel) */
.fachada { background: var(--verde-painel); border: 5px solid var(--concreto); padding: 2.5rem 2rem 1.5rem; overflow: hidden; }
.fachada .v { font-size: clamp(1.7rem, 6vw, 4.4rem); line-height: 1.08; letter-spacing: -0.02em; margin: 0 0 0.3em; }
.v1 { color: var(--concreto-claro); text-shadow: 4px 4px 0 var(--preto); }
.v2, .v3 { color: transparent; -webkit-background-clip: text; background-clip: text; }
.v2 { background-image: repeating-linear-gradient(to bottom, var(--concreto-claro) 0 5px, transparent 5px 8px); }
.v3 { background-color: var(--concreto); background-image: linear-gradient(90deg, var(--verde-painel) 3px, transparent 3px), linear-gradient(0deg, var(--verde-painel) 3px, transparent 3px); background-size: 8px 8px; }
@keyframes descer { from { transform: translateY(-48px); opacity: 0; } to { transform: none; opacity: 1; } }
@media (prefers-reduced-motion: no-preference) {
  .fachada .v { animation: descer 0.6s steps(6, end) both; }
  .fachada .v2 { animation-delay: 0.35s; }
  .fachada .v3 { animation-delay: 0.7s; }
}
/* placas: as perguntas em escala de cartaz */
.placa { width: 100%; margin: 0 0 1.75rem; padding: 1.4rem 1.6rem; font-size: clamp(1.35rem, 4.2vw, 2.9rem); line-height: 1.12; letter-spacing: -0.01em; background: var(--preto); color: var(--concreto-claro); border: 5px solid var(--concreto); }
.placa:nth-child(odd) { background: var(--granulado) var(--concreto); color: var(--preto); border-color: var(--preto); }
@media (min-width: 701px) {
  .placa { width: var(--w, 92%); }
  .placa:nth-child(even) { --w: 80%; margin-left: auto; }
  .placa:nth-child(3) { --w: 100%; }
  .placa:nth-child(4) { --w: 68%; }
}
/* blogs: blocos do mesmo tamanho (4 por linha) */
.titulo-bloco { margin: 0 0 1.75rem; }
.conjunto { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1.5rem; }
.laje { position: relative; display: flex; flex-direction: column; justify-content: flex-end; min-height: 220px; padding: 1rem 1.1rem 1.1rem; background: var(--granulado) var(--concreto); border: 5px solid var(--preto); overflow: hidden; }
a.laje, a.laje:visited { text-decoration: none; }
.sigla { position: relative; font-size: clamp(2rem, 3.4vw, 2.7rem); line-height: 0.95; letter-spacing: -0.04em; }
.nome { position: relative; font-weight: 700; font-size: 0.95rem; text-transform: uppercase; margin-top: 0.6rem; padding-top: 0.45rem; border-top: 4px solid currentColor; }
/* blocos reservados (ainda sem blog) */
.laje.vazia { color: var(--concreto-escuro); }
@media (max-width: 800px) { .conjunto { grid-template-columns: 1fr 1fr; } .sigla { font-size: clamp(2.2rem, 8vw, 3rem); } }
@media (max-width: 520px) { .conjunto { grid-template-columns: 1fr; } }
/* links sobre concreto */
a.laje, a.laje:visited, .coluna-lateral a, .coluna-lateral a:visited { color: var(--preto); }
a.laje:hover, .coluna-lateral a:hover { color: var(--concreto-claro); background-color: var(--preto); }
/* produções das leituras coletivas */
.producoes { margin-bottom: 2rem; }
.producoes h2 { margin-top: 0; }
.producoes ul { list-style: square; margin-bottom: 0; }
/* rodapé: φ, atalhos e carimbo */
.rodape { display: grid; grid-template-columns: auto 1fr auto; align-items: center; gap: 2.5rem; margin-top: 1.5rem; padding: 1.75rem 2rem; background: var(--preto); border: 5px solid var(--concreto); box-shadow: var(--sombra); }
.phi { font: 700 clamp(6rem, 14vw, 10rem)/0.8 Georgia, "Times New Roman", serif; color: var(--concreto-escuro); }
.atalhos { display: grid; width: 100%; max-width: 340px; justify-self: center; }
.atalhos a, .atalhos a:visited { padding: 0.6rem 0.3rem; border-bottom: 3px solid var(--concreto-escuro); text-decoration: none; text-transform: uppercase; }
.atalhos a:last-child { border-bottom: 0; }
.carimbo { transform: rotate(-2deg); padding: 0.9rem 1.3rem; border: 4px solid var(--concreto); outline: 2px solid var(--concreto); outline-offset: 4px; text-align: center; text-transform: uppercase; color: var(--concreto); }
.carimbo small { display: block; font-size: 0.78rem; letter-spacing: 0.15em; }
.carimbo b { display: block; margin: 0.25rem 0; font-family: var(--pesado); font-weight: 900; font-size: 1.6rem; color: var(--concreto-claro); }
@media (max-width: 700px) { .rodape { grid-template-columns: 1fr; justify-items: center; gap: 1.75rem; } }
</style>

<h2 class="subtitulo">Um ciberespaço para trocar uma ideia descontraída sobre filosofia</h2>

<section class="fachada" aria-label="Abertura">
  <p class="v v1">No princípio era o Verbo.</p>
  <p class="v v2">E o Verbo se fez carne.</p>
  <p class="v v3">Depois o Verbo se fez dígito.</p>
</section>

<div class="coluna-texto intro" markdown="1">

O Ser que surge no pensamento.  
O Ser que compreende o ser humano.  
O Ser que é absorvido pelo dígito.  
Eis onde estamos: na era do ciberespaço.  
Mundo híbridos de seres ciborgues.  
Onde as fronteiras entre natural e o artificial são borradas.  
Onde tudo foi deslocado, desde a cultura até a política,  
passando pela economia e os afetos.  
Mas há algo que não mudou!  
Algo que não se esgota, por mais que possa ser adormecido.  
O pensamento!  
É preciso pensar.  
É preciso responder as perguntas que seguem surgindo:

</div>

<div class="placas">
  <p class="placa">“O que significa ser humano na época do ciborgue?”</p>
  <p class="placa">“Existe algo que ainda é natural?”</p>
  <p class="placa">“As tecnologias modificam o pensamento?”</p>
  <p class="placa">“A máquina pode pensar?”</p>
</div>

<h2 class="titulo-bloco" id="blogs">Blogs</h2>

<nav class="conjunto" aria-label="Blogs">
  <a class="laje" href="DA_Dio_Anfibio"><span class="sigla">DA</span><span class="nome">Dio Anfibio</span></a>
  <a class="laje" href="FJ_O_Louco"><span class="sigla">FJ</span><span class="nome">O Louco</span></a>
  <a class="laje" href="RFZ_O_Espírito_Zombeteiro"><span class="sigla">RFZ</span><span class="nome">O Espírito Zombeteiro</span></a>
  <a class="laje" href="Sant'_Um_Único"><span class="sigla">SANT’</span><span class="nome">Um Único</span></a>
  <!-- Blocos reservados: para ativar, troque <div> por <a href="..."> (e </div> por </a>), remova a classe "vazia" e preencha sigla e nome. -->
  <div class="laje vazia"><span class="sigla">···</span><span class="nome">Em breve</span></div>
  <div class="laje vazia"><span class="sigla">···</span><span class="nome">Em breve</span></div>
  <div class="laje vazia"><span class="sigla">···</span><span class="nome">Em breve</span></div>
  <div class="laje vazia"><span class="sigla">···</span><span class="nome">Em breve</span></div>
</nav>

<div class="duas-colunas">

<div class="coluna-texto" markdown="1">

Enfim, inúmeras perguntas que emergem do grande problema filosófico de estar vivo.  
Algo que ainda nos atravessa (deixará de o fazê-lo? outra pergunta a ser respondida).  
Este espaço é um espaço de trocas de ideias. Diálogo intensivo e descontinuado entre pessoas que habitam o ciberespaço e se ocupam com as grandes questões da existência. É um espaço caótico, de atravessamentos, em que temas emergem e imergem com velocidades infinitas. O que resulta? o impossível em sua imprevisibilidade.  

</div>

<aside class="coluna-lateral" markdown="1">

## LISTA DE LEITURA DO FILOSOFIA-NET

- [Lista De Leitura Oficial](Lista_De_Leitura_Oficial)

</aside>

</div>

<section class="coluna-texto producoes" id="producoes" markdown="1">

## Produções das leituras coletivas

- [“Manuscritos Econômico-Filosóficos” de Karl Marx](https://ajfilosofia.github.io/Filosofia-Net/RUP-Marx1)

</section>

<footer class="rodape">
  <div class="phi" aria-hidden="true">φ</div>
  <nav class="atalhos" aria-label="Atalhos">
    <a href="{{ '/' | relative_url }}">Início</a>
    <a href="#blogs">Blogs</a>
    <a href="Lista_De_Leitura_Oficial">Lista de leitura</a>
    <a href="#">Voltar ao topo ↑</a>
  </nav>
  <div class="carimbo"><small>Última atualização</small><b>{{ site.time | date: "%d/%m/%Y" }}</b><small>Filosofia-Net</small></div>
</footer>
