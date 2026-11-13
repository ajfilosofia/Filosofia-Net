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
</style>

![RFZ_autoretrato.jpg](RFZ_autoretrato.jpg)

> _Legenda para todos verem: um busto masculino sem qualquer pelo de olhos fechados contra um fundo com o mesmo tom de pele. O busto é meu._

# Rfz - O Espírito Zombeteiro

Caro leitor,
{: . Capitular}

Sou Rfz. Um preto norte, americano forte com um brinco de ouro na orelha... Brincadeira. Sou apenas um rapaz latino americano sem dinheiro no banco.

Sou comunicólogo e faço um monte de coisas, mas minha área não é a filosofia. Entrei pro grupo Filosofia-Net logo no começo, pois aprender e conhecer é minha paixão. Especialmente quando se faz isso em grupo.

Meus textos devem passar por muitos assuntos, pois eu sou meio de ter visão aérea sobre muitas coisas. Espero, de coração, que com a ajuda dos meus colegas do grupo eu possa entregar raciocínios ao menos de fácil compreensão e que lhes agrade o conteúdo aqui.

Forte abraço,

Rfz

Post Scriptum: para me conhecer melhor você pode acessar [https://rafaelmmilhomens.com](https://rafaelmmilhomens.com)
## Textos

> Não tão filosóficos, mas ainda reflexivos

1. [Kit De Socorros](Kit_De_Socorros)
	1. Guia para publicar no Filosofia-Net
2. [A Tecnologização Do Sagrado E A Crise Do Indivíduo Contemporâneo](RFZ_A_Tecnologização_do_Sagrado_e_a_Crise_do_Indivíduo_Contemporâneo.md)
	1. Algaravias bruxuleantes sobre a ideia de colocar um copo d'água na frente da TV para ser abençoado
3. [O Gênero Documental Como Discurso Científico - Educação E Linguagem Audiovisual](RFZ_O_Gênero_Documental.md)
	1. Literacia midiática e sua urgência
4. [Um País Cristão - Brasil E O Cruzeiro Do Sul](RFZ_Um_País_Cristão.md)
	1. Acerca do que vemos e ignoramos

## Laboratório

1. [Verso & Poesia](RFZ_Verso_&_Poesia.md)