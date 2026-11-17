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
  --verde-linha: #1a4a2e;
  --concreto: #b9b8ae;
  --concreto-claro: #e4e3d8;
  --concreto-escuro: #6e7069;
  --texto: #dcdbd0;
  --mono: ui-monospace, "SFMono-Regular", Menlo, Consolas, "Courier New", monospace;
  --pesado: "Arial Black", "Helvetica Neue", Arial, sans-serif;
  --granulado: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='3' stitchTiles='stitch'/%3E%3CfeColorMatrix values='0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 .25 0'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
}
/* ===== BASE: tudo reto, massa e peso ===== */
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
/* ===== CABEÇALHO: laje preta sobre fachada de concreto estriado ===== */
.site-header {
  background: var(--preto);
  border-top: 0;
  border-bottom: 0;
}
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
/* ===== TÍTULOS: peso monumental ===== */
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
.subtitulo {
  color: var(--concreto);
  font-size: 1.05rem;
  letter-spacing: 0.05em;
}
/* ===== LINKS: sublinhado grosso, hover em bloco de concreto ===== */
a, a:visited {
  color: var(--concreto-claro);
  font-weight: 700;
  text-decoration: underline;
  text-decoration-thickness: 2px;
  text-underline-offset: 4px;
}
a:hover { color: var(--preto); background: var(--concreto); text-decoration: none; }
a:focus-visible { outline: 3px solid var(--concreto-claro); outline-offset: 3px; }
/* ===== PAINÉIS: lajes pré-moldadas ===== */
.coluna-texto {
  background: var(--verde-painel);
  border: 5px solid var(--concreto);
  box-shadow: 14px 14px 0 var(--preto);
  padding: 1.75rem;
}
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
.coluna-lateral hr { border-top-color: var(--preto); }
/* ===== LISTAS, CITAÇÕES, DIVISÓRIAS ===== */
ul, ol { margin-left: 1.5em; }
ul { list-style: square; }
li::marker { color: var(--concreto); }
.coluna-lateral li::marker { color: var(--preto); }
blockquote {
  color: var(--texto);
  background: var(--preto);
  border-left: 10px solid var(--concreto-escuro);
  padding: 0.8em 1.2em;
}
hr { border: 0; border-top: 5px solid var(--concreto); margin: 2rem 0; }
img { border: 3px solid var(--concreto); }
code, pre { background: var(--preto); color: var(--concreto-claro); border: 2px solid var(--concreto-escuro); }
::selection { background: var(--concreto); color: var(--preto); }
/* ===== RODAPÉ ===== */
.site-footer {
  background: var(--preto);
  color: var(--texto);
  border-top: 8px solid var(--concreto-escuro);
  margin-top: 2rem;
  padding-bottom: 2rem;
}
.site-footer a, .site-footer a:visited, .footer-heading { color: var(--concreto-claro); }
.site-footer a:hover { color: var(--preto); }
.svg-icon { fill: var(--concreto-claro); }
</style>


<h2 class="subtitulo">Um ciberespaço para trocar uma ideia descontraída sobre filosofia</h2>

<div class="duas-colunas">

<div class="coluna-texto" markdown="1">

No princípio era o Verbo.  
E o Verbo se fez carne.  
Depois o Verbo se fez dígito.  
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
"O que significa ser humano na época do ciborgue?"  
"Existe algo que ainda é natural?"  
"As tecnologias modificam o pensamento?"  
"A máquina pode pensar?"

Enfim, inúmeras perguntas que emergem do grande problema filosófico de estar vivo.  
Algo que ainda nos atravessa (deixará de o fazê-lo? outra pergunta a ser respondida).  
Este espaço é um espaço de trocas de ideias. Diálogo intensivo e descontinuado entre pessoas que habitam o ciberespaço e se ocupam com as grandes questões da existência. É um espaço caótico, de atravessamentos, em que temas emergem e imergem com velocidades infinitas. O que resulta? o impossível em sua imprevisibilidade.  

</div>

<aside class="coluna-lateral" markdown="1">

## BLOGS

- [Dio Anfibio](DA_Dio_Anfibio)
- [FJ O Louco](FJ_O_Louco)
- [RFZ O Espírito Zombeteiro](RFZ_O_Espírito_Zombeteiro)
- [Sant' Um Único](Sant'_Um_Único)

---

## LISTA DE LEITURA DO FILOSOFIA-NET

- [Lista De Leitura Oficial](Lista_De_Leitura_Oficial)

</aside>

</div>
