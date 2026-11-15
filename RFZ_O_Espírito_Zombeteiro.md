<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400..800;1,400..800&display=swap" rel="stylesheet">

<style>
  :root {
    --papel: #F3EEDF;       
    --papel-escuro: #E8E0CB; 
    --tinta: #2A2520;       
    --tinta-suave: #5A5148;
    --vermelho: #D90416;
  }

  /* ---------- Página ---------- */
  html { background: var(--papel); }

  body {
    background: var(--papel);
    color: var(--tinta);
    font-family: "EB Garamond", Garamond, "Times New Roman", serif;
    font-size: 1.25rem;
    line-height: 1.55;
    font-feature-settings: "kern", "liga", "onum"; /* algarismos de estilo antigo */
    font-kerning: normal;
    text-rendering: optimizeLegibility;
    -webkit-font-smoothing: antialiased;
    max-width: 36em;
    margin: 0 auto;
    padding: 3em 1.5em 5em;
  }

  /* ---------- Parágrafos à moda de livro ---------- */
  p {
    margin: 0;
    text-align: justify;
    hyphens: auto;
    -webkit-hyphens: auto;
  }
  p + p { text-indent: 1.5em; }  /* recuo em vez de espaço entre parágrafos */

  /* ---------- Títulos ---------- */
  h1, h2, h3, h4 {
    font-family: "EB Garamond", Garamond, serif;
    font-weight: 500;
    color: var(--vermelho);
    text-align: center;
    line-height: 1.2;
    margin: 2em 0 1em;
  }
  h1 {
    font-size: 2.3em;
    font-variant: small-caps;
    letter-spacing: 0.04em;
    margin-top: 0.5em;
  }
  h1::after {               /* ornamento sob o título principal */
    content: "☤";
    display: block;
    font-size: 0.5em;
    margin-top: 0.4em;
    color: var(--vermelho);
  }
  h2 { font-size: 1.5em; font-variant: small-caps; letter-spacing: 0.05em; }
  h3 { font-size: 1.2em; font-style: italic; }
  h4 { font-size: 1em; font-variant: small-caps; letter-spacing: 0.08em; }

  /* ---------- Letra capitular ----------
     Automática no 1º parágrafo do post (nas plataformas mais comuns)
     ou manual: <p class="capitular">...</p> */
  .capitular::first-letter,
  article > p:first-of-type::first-letter,
  .post-body > p:first-of-type::first-letter,
  .entry-content > p:first-of-type::first-letter,
  .post-content > p:first-of-type::first-letter {
    float: left;
    font-size: 4.1em;
    line-height: 0.82;
    font-weight: 500;
    color: var(--vermelho);
    padding: 0.06em 0.08em 0 0;
  }
  .capitular::first-line,
  article > p:first-of-type::first-line,
  .post-body > p:first-of-type::first-line,
  .entry-content > p:first-of-type::first-line,
  .post-content > p:first-of-type::first-line {
    font-variant: small-caps;   /* primeira linha em versaletes, como nos livros */
    letter-spacing: 0.03em;
  }
  .capitular,
  article > p:first-of-type,
  .post-body > p:first-of-type,
  .entry-content > p:first-of-type,
  .post-content > p:first-of-type { text-indent: 0; }

  /* ---------- Destaques em vermelho ---------- */
  a {
    color: var(--vermelho);
    text-decoration: none;
    border-bottom: 1px solid rgba(217, 4, 22, 0.35);
  }
  a:hover { border-bottom-color: var(--vermelho); }

  strong, b { font-weight: 600; color: var(--vermelho); }
  em, i { font-style: italic; }
  mark {
    background: none;
    color: var(--vermelho);
    font-variant: small-caps;
    letter-spacing: 0.03em;
  }
  ::selection { background: var(--vermelho); color: var(--papel); }

  /* ---------- Citações ---------- */
  blockquote {
    margin: 1.5em 1.5em;
    padding: 0 0 0 1em;
    border-left: 2px solid var(--vermelho);
    font-style: italic;
    color: var(--tinta-suave);
  }
  blockquote p { text-indent: 0; }
  blockquote cite, blockquote footer {
    display: block;
    text-align: right;
    font-style: normal;
    font-variant: small-caps;
    margin-top: 0.5em;
  }

  /* ---------- Separador ornamental (use <hr>) ---------- */
  hr {
    border: none;
    text-align: center;
    margin: 2.5em 0;
    height: 1.5em;
  }
  hr::before {
    content: "⁂";
    color: var(--vermelho);
    font-size: 1.3em;
  }

  /* ---------- Listas, notas, código ---------- */
  ul, ol { padding-left: 1.5em; margin: 1em 0; }
  li::marker { color: var(--vermelho); }
  small, sup, figcaption { font-size: 0.8em; color: var(--tinta-suave); }
  figcaption { text-align: center; font-style: italic; margin-top: 0.5em; }
  sup a { border: none; }
  code, pre {
    background: var(--papel-escuro);
    font-size: 0.85em;
    padding: 0.1em 0.3em;
  }
  pre { padding: 1em; overflow-x: auto; }
  img {
    max-width: 100%;
    height: auto;
    border-radius: 12px; 
    filter: sepia(0.15);
  }
  p:has(> img) {
    text-indent: 0;
    text-align: center;
    margin: 1.5em 0;
  }
  p:has(> img)::first-letter { all: unset; }

  /* ---------- Celular ---------- */
  @media (max-width: 600px) {
    body { font-size: 1.1rem; padding: 1.5em 1.1em 3em; }
    h1 { font-size: 1.9em; }
    p { text-align: left; } /* justificado em tela estreita abre "rios" de espaço */
  }
  /* Corpo do texto em EB Garamond (o tema Primer sobrescrevia) */
  .markdown-body {
    font-family: "EB Garamond", Garamond, "Times New Roman", serif;
    font-size: 1.25rem;
    line-height: 1.55;
    color: var(--tinta);
  }
    .markdown-body p { margin: 0; }
  /* ---------- 1. Abertura: retrato menor, cantos arredondados, legenda discreta ---------- */
  .markdown-body > p:first-of-type:has(> img) {
    text-align: center;
    margin: 1em 0 0.6em;
  }
  .markdown-body > p:first-of-type:has(> img) img {
    width: 240px;
    max-width: 70%;
    height: auto;
    border-radius: 10px;
    padding: 0;
    background: none;
  }

  /* Legendas das imagens (o "Para todos verem") */
  .markdown-body > p:has(> img) + blockquote {
    max-width: 28em;
    margin: 0 auto 2.5em;
    padding: 0;
    border: 0;
    text-align: center;
    font-size: 0.78em;
    line-height: 1.45;
    color: var(--tinta-suave);
  }
  .markdown-body > p:has(> img) + blockquote p { text-align: center; text-indent: 0; hyphens: manual; }

  /* Título logo depois do retrato */
  .markdown-body > h1:not(:first-child) { margin-top: 0.2em; }

  /* ---------- 2. Epígrafes: todas as outras citações ---------- */
  .markdown-body > blockquote:not(p:has(> img) + blockquote) {
    max-width: 30em;
    margin: 0 auto 2.5em;
    padding: 0;
    border: 0;
    font-size: 0.9em;
    line-height: 1.5;
    color: var(--tinta-suave);
  }
  .markdown-body > blockquote:not(p:has(> img) + blockquote)::before {
    content: "";
    display: block;
    width: 2.5em;
    margin: 0 auto 0.8em;
    border-top: 2px solid var(--vermelho);
  }
  .markdown-body > blockquote p { text-indent: 0; text-align: left; hyphens: manual; }
  /* epígrafe que vem depois de um parágrafo precisa de ar acima */
  .markdown-body > p + blockquote:not(p:has(> img) + blockquote) { margin-top: 1.8em; clear: both; }

  /* ---------- 3. Índice: uma linha de navegação, como num sumário de livro ---------- */
  .markdown-body > h2:has(+ ol > li > a[href^="#"]) {
    font-size: 0.75em;
    letter-spacing: 0.25em;
    color: var(--tinta-suave);
    margin: 2.5em 0 0.6em;
  }
  .markdown-body > ol:has(> li > a[href^="#"]) {
    list-style: none;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 0.2em 0;
    padding: 0.6em 0;
    margin: 0 0 1em;
    border-top: 1px solid var(--papel-escuro);
    border-bottom: 1px solid var(--papel-escuro);
    font-variant: small-caps;
    letter-spacing: 0.06em;
  }
  .markdown-body > ol:has(> li > a[href^="#"]) li { margin: 0; }
  .markdown-body > ol:has(> li > a[href^="#"]) li + li::before {
    content: "·";
    color: var(--vermelho);
    margin: 0 0.8em;
  }
  .markdown-body > ol:has(> li > a[href^="#"]) a { border-bottom: 0; }

  /* ---------- 4. Textos: catálogo numerado, com título e resumo ---------- */
  .markdown-body > ol:has(> li > ol) {
    list-style: none;
    counter-reset: texto;
    padding: 0;
    margin: 1em 0 3em;
    border-top: 1px solid var(--papel-escuro);
  }
  .markdown-body > ol:has(> li > ol) > li {
    counter-increment: texto;
    position: relative;
    padding: 0.9em 0 0.9em 2.8em;
    margin: 0;
    border-bottom: 1px solid var(--papel-escuro);
    line-height: 1.35;
  }
  .markdown-body > ol:has(> li > ol) > li::before {
    content: counter(texto, upper-roman) ".";
    position: absolute;
    left: 0;
    top: 0.9em;
    width: 2.2em;
    text-align: right;
    color: var(--vermelho);
    font-variant: small-caps;
  }
  .markdown-body > ol:has(> li > ol) > li > a { font-size: 1.08em; }
  .markdown-body > ol:has(> li > ol) > li > ol {
    list-style: none;
    padding: 0;
    margin: 0.25em 0 0;
    font-style: italic;
    font-size: 0.88em;
    color: var(--tinta-suave);
  }
  .markdown-body > ol:has(> li > ol) > li > ol li { margin: 0; }

  /* ---------- 5. Imagens no meio do texto: menores, centralizadas ---------- */
  .markdown-body > p:has(> img):not(:first-of-type) {
    text-align: center;
    margin: 1.5em 0 0.6em;
  }
  .markdown-body > p:has(> img):not(:first-of-type) img {
    max-width: min(100%, 340px);
    padding: 0;
    background: none;
    border-radius: 10px;
  }

  /* ---------- 6. Contato: o último parágrafo vira uma linha destacada ---------- */
  .markdown-body > p:last-of-type {
    clear: both;
    text-align: center;
    text-indent: 0;
    margin: 1.8em auto 0;
    padding: 0.6em 0;
    border-top: 1px solid var(--papel-escuro);
    border-bottom: 1px solid var(--papel-escuro);
  }

  /* ---------- 7. Ritmo entre seções ---------- */
  .markdown-body > h2 { margin-top: 3.2em; }
</style>

![RFZ_autoretrato.jpg](/img/RFZ_autoretrato.jpg)

> _Legenda para todos verem: um busto masculino sem qualquer pelo de olhos fechados contra um fundo com o mesmo tom de pele. O busto é meu._

# Rfz - O Espírito Zombeteiro

> “Então escrever é o modo de quem tem a palavra como isca: a palavra pescando o que não é palavra. Quando essa não-palavra —a entrelinha —morde a isca, alguma coisa se escreveu. Uma vez que se pescou a entrelinha, poder-se ia com alívio jogar a palavra fora. Mas aí cessa a analogia: a não palavra, ao morder a isca, incorporou-a. O que salva então é escrever distraidamente.” - Clarice Lispector, Água Viva

## Índice

1. [Caro Leitor](#caro-leitor)
2. [Textos](#textos)
3. [Verso & Poesia](https://lacra.ia.br/rafzmilhomens/)
4. [Correio Elegante](#correio-elegante)

## Caro leitor

Sou comunicólogo e faço um monte de coisas, mas minha área não é a filosofia. Entrei pro grupo Filosofia-Net logo no começo, pois aprender e conhecer é minha paixão. Especialmente quando se faz isso em grupo.
{: .capitular}

Meus textos devem passar por muitos assuntos, pois eu sou meio de ter visão aérea sobre muitas coisas. Espero, de coração, que com a ajuda dos meus colegas do grupo eu possa entregar raciocínios ao menos de fácil compreensão e que lhes agrade o conteúdo aqui.

Forte abraço.

P.S.: para me conhecer melhor, você pode acessar [minha página](https://rafaelmmilhomens.com).
## Textos

> Não tão filosóficos, mas ainda reflexivos

1. [Kit De Socorros](Kit_De_Socorros)
	1. Guia para publicar no Filosofia-Net
2. [A Tecnologização Do Sagrado E A Crise Do Indivíduo Contemporâneo](RFZ_A_Tecnologização_do_Sagrado_e_a_Crise_do_Indivíduo_Contemporâneo)
	1. Algaravias bruxuleantes sobre a ideia de colocar um copo d'água na frente da TV para ser abençoado
3. [O Gênero Documental Como Discurso Científico - Educação E Linguagem Audiovisual](RFZ_O_Gênero_Documental)
	1. Literacia midiática e sua urgência
4. [Para Que Serve A Filosofia? Sobre Os Privilégios Nas Torres De Marfim](RFZ_Para_Que_Serve_A_Filosofia)
	1. Uma viagem sobre nomes imagens, nomes imagens nomes.
5. [Um País Cristão - Brasil E O Cruzeiro Do Sul](RFZ_Um_País_Cristão)
	1. Acerca do que vemos e ignoramos

## [Verso & Poesia](https://lacra.ia.br/rafzmilhomens/)

![frágil](/img/frágil.jpeg)
> Para todos verem: um homem careca e barbudo com o peito aberto. No buraco há um coração vítreo. Sou eu sendo dramático

Também escrevo poesia. Mas em outro blog. Se você tiver interesse o título é o link para o blog. Só clicar. Talvez eu poetize melhor do que filosofe...
{: .capitular}

> "[...] Todo bairro tem um louco
> que o bairro trata bem
> só falta mais um pouco
> pra eu ser tratado também"
> Paulo Leminski


## Correio Elegante

>Recebo o crack, colante, dinheiro parco, embrulhado em papel carbono e barbante, até cabelo cortado, retrato de 3x4, pra batizado distante, recebo até, meu senhor, uma carta de amor

Quer falar comigo? Eu também quero falar com você! Temos muito o que conversar...
{: .capitular}

Meu e-mail: rafzmilhomens@proton.me