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
/* ===== PALETA ===== */
:root {
  --preto: #000000;
  --verde-fundo: #0d3b21;
  --verde-painel: #082315;
  --amarelo: #f5c400;
  --amarelo-claro: #ffe066;
  --texto: #efe9c8;
  --mono: ui-monospace, "SFMono-Regular", Menlo, Consolas, "Courier New", monospace;
}
/* ===== BASE: tudo reto, sem cantos arredondados ===== */
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
/* ===== CABEÇALHO: bloco preto com faixa de alerta ===== */
.site-header {
  background: var(--preto);
  border-top: 0;
  border-bottom: 0;
}
.site-header::after {
  content: "";
  display: block;
  height: 12px;
  background: repeating-linear-gradient(-45deg, var(--amarelo) 0 12px, var(--preto) 12px 24px);
}
.site-title, .site-title:visited {
  color: var(--amarelo);
  font-family: var(--mono);
  font-weight: 800;
  letter-spacing: 0.04em;
  text-transform: uppercase;
}
.site-title:hover { color: var(--amarelo-claro); background: none; text-decoration: none; }
.site-nav .page-link { color: var(--texto); font-family: var(--mono); text-transform: uppercase; }
.site-nav .page-link:hover { color: var(--preto); background: var(--amarelo); text-decoration: none; }
@media screen and (max-width: 600px) {
  .site-nav { background: var(--preto); border: 3px solid var(--amarelo); }
}
/* ===== TÍTULOS ===== */
h1, h2, h3, h4, h5, h6 {
  color: var(--amarelo);
  font-family: var(--mono);
  font-weight: 800;
  line-height: 1.2;
  letter-spacing: -0.01em;
}
h1 {
  font-size: 2.4rem;
  text-transform: uppercase;
  padding-bottom: 0.4em;
  margin-bottom: 0.6em;
  border-bottom: 6px solid var(--amarelo);
}
h2 {
  font-size: 1.3rem;
  text-transform: uppercase;
  padding-bottom: 0.3em;
  margin-top: 1.5em;
  border-bottom: 3px solid var(--amarelo);
}
.subtitulo {
  color: var(--amarelo-claro);
  font-size: 1.05rem;
  letter-spacing: 0.06em;
}
/* ===== LINKS ===== */
a, a:visited {
  color: var(--amarelo);
  text-decoration: underline;
  text-decoration-thickness: 2px;
  text-underline-offset: 4px;
}
a:hover { color: var(--preto); background: var(--amarelo); text-decoration: none; }
a:focus-visible { outline: 3px solid var(--amarelo-claro); outline-offset: 3px; }
/* ===== PAINÉIS: borda grossa e sombra dura ===== */
.coluna-texto {
  background: var(--verde-painel);
  border: 4px solid var(--amarelo);
  box-shadow: 10px 10px 0 var(--preto);
  padding: 1.75rem;
}
.coluna-lateral {
  flex: 1;
  background: var(--amarelo);
  color: var(--preto);
  border: 4px solid var(--preto);
  box-shadow: 10px 10px 0 var(--preto);
  padding: 1.25rem 1.5rem;
}
.coluna-lateral h2 { color: var(--preto); border-bottom: 4px solid var(--preto); margin-top: 0.2em; }
.coluna-lateral a, .coluna-lateral a:visited { color: var(--preto); }
.coluna-lateral a:hover { color: var(--amarelo); background: var(--preto); }
.coluna-lateral hr { border-top-color: var(--preto); }
/* ===== LISTAS, CITAÇÕES, DIVISÓRIAS ===== */
ul, ol { margin-left: 1.5em; }
ul { list-style: square; }
li::marker { color: var(--amarelo); }
.coluna-lateral li::marker { color: var(--preto); }
blockquote {
  color: var(--texto);
  background: var(--preto);
  border-left: 8px solid var(--amarelo);
  padding: 0.8em 1.2em;
}
hr { border: 0; border-top: 4px solid var(--amarelo); margin: 2rem 0; }
img { border: 3px solid var(--amarelo); }
code, pre { background: var(--preto); color: var(--amarelo); border: 2px solid var(--amarelo); }
::selection { background: var(--amarelo); color: var(--preto); }
/* ===== RODAPÉ ===== */
.site-footer {
  background: var(--preto);
  color: var(--texto);
  border-top: 6px solid var(--amarelo);
  margin-top: 2rem;
  padding-bottom: 2rem;
}
.site-footer a, .site-footer a:visited, .footer-heading { color: var(--amarelo); }
.site-footer a:hover { color: var(--preto); }
.svg-icon { fill: var(--amarelo); }
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
