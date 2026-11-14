<!-- ===== Sant' Um Único — estilo gótico: fundo grafite, tinta vermelha.
     Colar no topo de cada .md dele (a página principal e cada texto). ===== -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bodoni+Moda:ital,opsz,wght@0,6..96,400..900;1,6..96,400..900&family=Libre+Caslon+Text:ital,wght@0,400;0,700;1,400&family=Grenze+Gotisch:wght@400..800&family=Noto+Serif+JP:wght@400;700&display=swap" rel="stylesheet">

<style>
  :root {
    --fundo: #1F1E20;     /* grafite */
    --vermelho: #EF4B4B;  /* texto: vermelho legível sobre o escuro */
    --sangue: #E8323A;    /* títulos */
    --osso: #E9DCD3;      /* links */
    --fio: #5A1A1E;       /* fios e bordas, vermelho apagado */
    --cinza: #8E878A;
  }

  html, body { background: var(--fundo); }

  body, .markdown-body {
    color: var(--vermelho);
    font-family: "Libre Caslon Text", "Noto Serif JP", Georgia, serif;
  }
  .markdown-body {
    font-size: 18px;
    line-height: 1.75;
    max-width: 38em;
    margin: 0 auto !important;
    padding: 3em 1.5em 4em !important;
  }

  /* Nome do site, discreto no alto */
  .markdown-body > h1:first-child {
    font-family: "Bodoni Moda", Georgia, serif;
    font-size: 0.95em;
    font-weight: 400;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    text-align: center;
    border: 0;
    border-bottom: 1px solid var(--fio);
    padding-bottom: 0.8em;
    margin: 0 0 3em;
  }
  .markdown-body > h1:first-child a { color: var(--cinza); text-decoration: none; }

  /* Demais títulos: Bodoni em caixa-alta espaçada */
  .markdown-body h1:not(:first-child),
  .markdown-body h2,
  .markdown-body h3 {
    font-family: "Bodoni Moda", "Noto Serif JP", Georgia, serif;
    font-weight: 600;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--sangue);
    border: 0;
    border-bottom: 1px solid var(--fio);
    padding-bottom: 0.3em;
    margin: 2.2em 0 1em;
  }
  .markdown-body h1:not(:first-child) { font-size: 1.4em; }
  .markdown-body h2 { font-size: 1.2em; }
  .markdown-body h3 { font-size: 1em; border: 0; }

  /* Título da página: letra gótica */
  .markdown-body > h1:nth-of-type(2) {
    font-family: "Grenze Gotisch", "Bodoni Moda", serif;
    font-weight: 600;
    text-transform: none;
    letter-spacing: 0;
    font-size: 3.4em;
    line-height: 1.1;
    text-align: center;
    color: var(--sangue);
    border: 0;
    margin: 0 0 1.2em;
    text-shadow: 0 0 22px rgba(232, 50, 58, 0.25);
  }

  /* Texto */
  .markdown-body p {
    text-align: left;       /* texto dele é em frases curtas: justificado abriria buracos */
    margin: 0 0 1.1em;
    white-space: pre-line; /* poesia: cada Enter no Obsidian vira quebra de verso no site */
  }
  .markdown-body strong { color: var(--osso); }
  .markdown-body em { color: var(--osso); }

  /* Links em cor de osso, sublinhados em vermelho */
  .markdown-body a {
    color: var(--osso);
    text-decoration: underline;
    text-decoration-color: var(--sangue);
    text-underline-offset: 0.2em;
  }
  .markdown-body a:hover { color: var(--fundo); background: var(--sangue); text-decoration: none; }

  /* Listas com cruz no lugar do marcador */
  .markdown-body ul { list-style: none; padding-left: 1.6em; }
  .markdown-body ul li { position: relative; margin: 0.5em 0; }
  .markdown-body ul li::before {
    content: "†";
    position: absolute;
    left: -1.3em;
    color: var(--sangue);
  }
  .markdown-body ol li::marker { color: var(--sangue); }

  /* Citações */
  .markdown-body blockquote {
    color: var(--osso);
    font-style: italic;
    border-left: 2px solid var(--sangue);
    padding: 0 0 0 1.2em;
    margin: 1.5em 0;
  }

  /* Separador (---): três cruzes */
  .markdown-body hr {
    height: auto;
    background: none;
    border: 0;
    text-align: center;
    margin: 3em 0;
  }
  .markdown-body hr::before {
    content: "† † †";
    color: var(--sangue);
    letter-spacing: 0.6em;
  }

  .markdown-body img { max-width: 100%; filter: grayscale(1) contrast(1.2); border: 1px solid var(--fio); }
  .markdown-body code, .markdown-body pre { background: #2A282B; color: var(--osso); }
  .markdown-body table td, .markdown-body table th { border-color: var(--fio); }
  .markdown-body table tr { background: transparent; }

  /* Notas e rodapé */
  .markdown-body .footnotes { color: var(--cinza); font-size: 0.85em; border-top: 1px solid var(--fio); }
  .markdown-body .footer { border-top: 1px solid var(--fio) !important; color: var(--cinza) !important; }

  ::selection { background: var(--sangue); color: var(--fundo); }

  @media (max-width: 600px) {
    .markdown-body { font-size: 17px; padding: 2em 1.1em 3em !important; }
    .markdown-body > h1:nth-of-type(2) { font-size: 2.5em; }
  }
</style>
<!-- ===== fim do estilo ===== -->
# Sant' Um Único

# Textos

- [Sobre A Gênese "発生について"](Sobre_A_Gênese)
- [O filosofar é o mesmo que roteirizar](SANT_filosofar-roteirizar)
