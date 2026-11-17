<style>
/* ===== SEU CSS ATUAL (mantido) ===== */
.site-title::before,
h1::before {
  content: "";
  display: inline-block;
  width: 40px;
  height: 40px;
  margin-right: 10px;
  vertical-align: middle;
  background: url("/Filosofia-Net/img/logo-phi.jpg") no-repeat center / contain;
}
h1 { text-align: center !important; }
.subtitulo { text-align: center; }
.duas-colunas {
  display: flex;
  gap: 2rem;
  align-items: flex-start;
}
.coluna-texto { flex: 2; min-width: 0; }
.coluna-lateral h2 { text-align: center; }
@media (max-width: 700px) {
  .duas-colunas { flex-direction: column; }
}
/* ===== PALETA: verde escuro, preto e concreto ===== */
:root {
  --preto: #000000;
  --verde-fundo: #0b2e1b;
  --verde-painel: #061c10;
  --concreto: #b9b8ae;
  --concreto-claro: #e4e3d8;
  --concreto-escuro: #6e7069;
  --texto: #dcdbd0;
  --mono: ui-monospace, "SFMono-Regular", Menlo, Consolas, "Courier New", monospace;
  --pesado: "Arial Black", "Helvetica Neue", Arial, sans-serif;
  --granulado: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='3' stitchTiles='stitch'/%3E%3CfeColorMatrix values='0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 .25 0'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
}
/* ===== BASE ===== */
* { border-radius: 0 !important; }
html { background: var(--preto); }
body {
  background: var(--verde-fundo);
  color: var(--texto);
  font-family: var(--mono);
  font-size: 17px;
  line-height: 1.7;
}
.wrapper { max-width: 1100px; }
.page-content { background: var(--verde-fundo); padding: 2.5rem 0; }
/* ===== CABEÇALHO ===== */
.site-header { background: var(--preto); border-top: 0; border-bottom: 0; }
.site-header::after {
  content: "";
  display: block;
  height: 16px;
  background: repeating-linear-gradient(90deg, var(--concreto-escuro) 0 8px, #3d3f3a 8px 16px);
}
.site-title, .site-title:visited {
  color: var(--concreto-claro);
  font-family: var(--pesado);
  font-weight: 900;
  letter-spacing: -0.01em;
  text-transform: uppercase;
}
.site-title:hover { color: var(--preto); background: var(--concreto); text-decoration: none; }
.site-nav .page-link { color: var(--texto); font-family: var(--mono); text-transform: uppercase; }
.site-nav .page-link:hover { color: var(--preto); background: var(--concreto); text-decoration: none; }
@media screen and (max-width: 600px) {
  .site-nav { background: var(--preto); border: 3px solid var(--concreto); }
}
/* ===== TÍTULOS ===== */
h1, h2, h3, h4, h5, h6 {
  color: var(--concreto-claro);
  font-family: var(--pesado);
  font-weight: 900;
  line-height: 1.15;
  text-transform: uppercase;
}
h1 {
  font-size: 2.3rem;
  letter-spacing: -0.02em;
  padding-bottom: 0.4em;
  margin-bottom: 0.6em;
  border-bottom: 8px solid var(--concreto);
}
h2 {
  font-size: 1.15rem;
  letter-spacing: 0.02em;
  padding-bottom: 0.35em;
  margin-top: 1.5em;
  border-bottom: 4px solid var(--concreto);
}
.subtitulo { color: var(--concreto); font-size: 1.05rem; letter-spacing: 0.05em; margin-bottom: 2.5rem; }
/* ===== LINKS ===== */
a, a:visited {
  color: var(--concreto-claro);
  font-weight: 700;
  text-decoration: underline;
  text-decoration-thickness: 2px;
  text-underline-offset: 4px;
}
a:hover { color: var(--preto); background: var(--concreto); text-decoration: none; }
a:focus-visible { outline: 3px solid var(--concreto-claro); outline-offset: 3px; }
/* ===== PAINÉIS ===== */
.coluna-texto {
  background: var(--verde-painel);
  border: 5px solid var(--concreto);
  box-shadow: 14px 14px 0 var(--preto);
  padding: 1.75rem;
}
.intro { margin-bottom: 3.5rem; }
.coluna-lateral {
  flex: 1;
  color: var(--preto);
  background:
    var(--granulado),
    repeating-linear-gradient(to bottom, transparent 0 158px, rgba(0,0,0,.4) 158px 162px),
    var(--concreto);
  border: 5px solid var(--preto);
  box-shadow: 14px 14px 0 var(--preto);
  padding: 1.25rem 1.5rem;
}
.coluna-lateral h2 { color: var(--preto); border-bottom: 5px solid var(--preto); margin-top: 0.2em; }
.coluna-lateral a, .coluna-lateral a:visited { color: var(--preto); }
.coluna-lateral a:hover { color: var(--concreto-claro); background: var(--preto); }
.duas-colunas { margin-bottom: 2rem; }
/* ===== LISTAS, CITAÇÕES, DIVISÓRIAS ===== */
ul, ol { margin-left: 1.5em; }
ul { list-style: square; }
li::marker { color: var(--concreto); }
.coluna-lateral li::marker { color: var(--preto); }
blockquote { color: var(--texto); background: var(--preto); border-left: 10px solid var(--concreto-escuro); padding: 0.8em 1.2em; }
hr { border: 0; border-top: 5px solid var(--concreto); margin: 2rem 0; }
img { border: 3px solid var(--concreto); }
code, pre { background: var(--preto); color: var(--concreto-claro); border: 2px solid var(--concreto-escuro); }
::selection { background: var(--concreto); color: var(--preto); }
/* ===== RODAPÉ ===== */
.site-footer { background: var(--preto); color: var(--texto); border-top: 8px solid var(--concreto-escuro); margin-top: 2rem; padding-bottom: 2rem; }
.site-footer a, .site-footer a:visited, .footer-heading { color: var(--concreto-claro); }
.site-footer a:hover { color: var(--preto); }
.svg-icon { fill: var(--concreto-claro); }
/* ===== FACHADA: o Verbo em três estágios (pedra, ranhura, pixel) ===== */
.fachada {
  background: var(--verde-painel);
  border: 5px solid var(--concreto);
  box-shadow: 14px 14px 0 var(--preto);
  padding: 2.5rem 2rem 2rem;
  margin-bottom: 3.5rem;
  overflow: hidden;
}
.fachada .v {
  font-family: var(--pesado);
  font-weight: 900;
  text-transform: uppercase;
  font-size: clamp(1.7rem, 6vw, 4.4rem);
  line-height: 1.08;
  letter-spacing: -0.02em;
  margin: 0 0 0.3em;
  overflow-wrap: break-word;
}
.fachada .v:last-child { margin-bottom: 0; }
.fachada .v1 { color: var(--concreto-claro); text-shadow: 4px 4px 0 var(--preto); }
.fachada .v2, .fachada .v3 { color: var(--concreto); }
.fachada .v2 { background-image: repeating-linear-gradient(to bottom, var(--concreto-claro) 0 5px, transparent 5px 8px); }
.fachada .v3 {
  background-color: var(--concreto);
  background-image: linear-gradient(90deg, var(--verde-painel) 3px, transparent 3px), linear-gradient(0deg, var(--verde-painel) 3px, transparent 3px);
  background-size: 8px 8px;
}
@supports ((-webkit-background-clip: text) or (background-clip: text)) {
  .fachada .v2, .fachada .v3 { color: transparent; -webkit-background-clip: text; background-clip: text; }
}
@keyframes descer {
  from { transform: translateY(-48px); opacity: 0; }
  to { transform: none; opacity: 1; }
}
@media (prefers-reduced-motion: no-preference) {
  .fachada .v { animation: descer 0.6s steps(6, end) both; }
  .fachada .v2 { animation-delay: 0.35s; }
  .fachada .v3 { animation-delay: 0.7s; }
}
/* ===== PLACAS: as perguntas em escala de cartaz ===== */
.placas { margin-bottom: 3.5rem; }
.placa {
  font-family: var(--pesado);
  font-weight: 900;
  text-transform: uppercase;
  font-size: clamp(1.35rem, 4.2vw, 2.9rem);
  line-height: 1.12;
  letter-spacing: -0.01em;
  margin: 0 0 1.75rem;
  padding: 1.4rem 1.6rem;
  width: 92%;
}
.placa:nth-child(odd) {
  background-color: var(--concreto);
  background-image: var(--granulado);
  color: var(--preto);
  border: 5px solid var(--preto);
  box-shadow: 12px 12px 0 var(--preto);
}
.placa:nth-child(even) {
  background: var(--preto);
  color: var(--concreto-claro);
  border: 5px solid var(--concreto);
  width: 80%;
  margin-left: auto;
}
.placa:nth-child(3) { width: 100%; }
.placa:nth-child(4) { width: 68%; }
@media (max-width: 700px) {
  .placa, .placa:nth-child(n) { width: 100%; }
}
/* ===== CONJUNTO: cada blog é um bloco, alinhados pela base ===== */
.titulo-bloco { margin: 0 0 1.75rem; }
.conjunto {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 1.5rem;
  align-items: end;
  margin-bottom: 3.5rem;
}
a.laje, a.laje:visited {
  --janela: rgba(0, 0, 0, 0.55);
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 1rem 1.1rem 1.1rem;
  color: var(--preto);
  background-color: var(--concreto);
  background-image: var(--granulado);
  border: 5px solid var(--preto);
  box-shadow: 10px 10px 0 var(--preto);
  text-decoration: none;
  overflow: hidden;
}
a.laje::before {
  content: "";
  position: absolute;
  top: 1.1rem;
  left: 1.1rem;
  right: 1.1rem;
  height: calc(100% - 9rem);
  background-image: repeating-linear-gradient(90deg, transparent 0 8px, var(--janela) 8px 20px, transparent 20px 22px);
  -webkit-mask-image: repeating-linear-gradient(to bottom, #000 0 16px, transparent 16px 30px);
  mask-image: repeating-linear-gradient(to bottom, #000 0 16px, transparent 16px 30px);
}
a.laje:hover {
  --janela: var(--concreto-claro);
  background-color: var(--preto);
  background-image: var(--granulado);
  color: var(--concreto-claro);
}
.laje .sigla {
  position: relative;
  font-family: var(--pesado);
  font-weight: 900;
  font-size: clamp(2.6rem, 7vw, 4.8rem);
  line-height: 0.95;
  letter-spacing: -0.04em;
}
.laje .nome {
  position: relative;
  font-family: var(--mono);
  font-weight: 700;
  font-size: 0.95rem;
  text-transform: uppercase;
  margin-top: 0.6rem;
  padding-top: 0.45rem;
  border-top: 4px solid currentColor;
}
.l1 { grid-column: span 4; min-height: 300px; }
.l2 { grid-column: span 2; min-height: 200px; }
.l3 { grid-column: span 3; min-height: 360px; }
.l4 { grid-column: span 3; min-height: 240px; }
.l2 .sigla { font-size: clamp(2rem, 4.2vw, 3.2rem); }
.l4 .sigla { font-size: clamp(1.8rem, 4.2vw, 3rem); }
@media (max-width: 800px) {
  .conjunto { grid-template-columns: 1fr 1fr; }
  .conjunto .laje { grid-column: span 1; }
  .conjunto .l1 { min-height: 230px; }
  .conjunto .l2 { min-height: 170px; }
  .conjunto .l3 { min-height: 270px; }
  .conjunto .l4 { min-height: 200px; }
  .conjunto .laje .sigla { font-size: clamp(2.2rem, 8vw, 3.4rem); }
}
@media (max-width: 520px) {
  .conjunto { grid-template-columns: 1fr; }
}
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

<h2 class="titulo-bloco">Blogs</h2>

<nav class="conjunto" aria-label="Blogs">
  <a class="laje l1" href="DA_Dio_Anfibio"><span class="sigla">DA</span><span class="nome">Dio Anfibio</span></a>
  <a class="laje l2" href="FJ_O_Louco"><span class="sigla">FJ</span><span class="nome">O Louco</span></a>
  <a class="laje l3" href="RFZ_O_Espírito_Zombeteiro"><span class="sigla">RFZ</span><span class="nome">O Espírito Zombeteiro</span></a>
  <a class="laje l4" href="Sant'_Um_Único"><span class="sigla">SANT’</span><span class="nome">Um Único</span></a>
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
