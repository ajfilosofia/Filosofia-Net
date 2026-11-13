<!-- ===== Estilo da Lista de Leitura (minimalista, coletivo) — colar no <head>, junto do outro =====
     Só age em páginas que contenham <div class="lista-leitura">. O resto do blog não muda. -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300..600&display=swap" rel="stylesheet">

<style>
  /* ---------- Página inteira: neutra, sem a identidade do blog ---------- */
  html:has(.lista-leitura),
  body:has(.lista-leitura) {
    background: #FFFFFF;
  }
  body:has(.lista-leitura) {
    --ll-tinta: #222222;
    --ll-cinza: #8A8A8A;
    --ll-linha: #E6E6E6;
    color: var(--ll-tinta);
    font-family: "Inter", "Helvetica Neue", Helvetica, Arial, sans-serif;
    font-size: 1rem;
    font-feature-settings: "tnum";     /* números alinhados */
    line-height: 1.5;
    max-width: 40em;
    margin: 0 auto;                    /* centraliza a coluna */
    padding: 5em 1.5em 0;
  }
  body:has(.lista-leitura) h1,
  body:has(.lista-leitura) h2,
  body:has(.lista-leitura) h3 {
    font-family: inherit;
    font-variant: normal;
    font-style: normal;
    color: var(--ll-tinta);
    text-align: left;
    letter-spacing: -0.02em;
  }
  body:has(.lista-leitura) h1 {
    font-size: 1.75em;
    font-weight: 400;
    margin: 0 0 1.5em;
  }
  body:has(.lista-leitura) h1::after { content: none; }
  body:has(.lista-leitura) p {
    text-align: left;
    text-indent: 0;
    hyphens: manual;
  }
  body:has(.lista-leitura) p::first-letter,
  body:has(.lista-leitura) p::first-line {
    all: unset;
  }
  body:has(.lista-leitura) a,
  body:has(.lista-leitura) strong {
    color: inherit;
    border-bottom-color: var(--ll-linha);
  }
  body:has(.lista-leitura) ::selection {
    background: var(--ll-tinta);
    color: #FFFFFF;
  }

  /* Legenda (o "> Legenda: ..." do Markdown) */
  body:has(.lista-leitura) blockquote {
    margin: 0 0 3em;
    padding: 0;
    border: none;
    font-style: normal;
    font-size: 0.8em;
    color: var(--ll-cinza);
  }

  /* ---------- A lista ---------- */
  .lista-leitura > ol {
    list-style: none;
    counter-reset: obra;
    padding: 0;
    margin: 0;
    border-top: 1px solid var(--ll-linha);
  }
  .lista-leitura > ol > li {
    counter-increment: obra;
    position: relative;
    padding: 1.1em 4em 1.1em 3em;     /* espaço à direita para o total de votos */
    border-bottom: 1px solid var(--ll-linha);
    line-height: 1.4;
  }
  .lista-leitura > ol > li::before {      /* a numeração da própria lista: 01, 02, 03… */
    content: counter(obra, decimal-leading-zero);
    position: absolute;
    left: 0;
    top: 1.6em;
    font-size: 0.75em;
    color: var(--ll-cinza);
    letter-spacing: 0.04em;
  }

  /* Linha "VOTOS  nome · nome" */
  .lista-leitura > ol > li > ol {
    list-style: none;
    padding: 0;
    margin: 0.35em 0 0;
  }
  .lista-leitura > ol > li > ol > li {
    display: flex;
    flex-wrap: wrap;
    align-items: baseline;
    gap: 0.9em;
    font-size: 0.68em;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    color: var(--ll-cinza);
  }
  .lista-leitura > ol > li > ol > li > ol {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;            /* elimina espaços soltos entre os nomes */
    flex-wrap: wrap;
    counter-reset: votos;
    font-size: 1.15em;
    text-transform: none;
    letter-spacing: 0.01em;
  }
  .lista-leitura > ol > li > ol > li > ol > li {
    counter-increment: votos;
  }
  .lista-leitura > ol > li > ol > li > ol > li + li::before {
    content: "·";
    margin: 0 0.6em;
  }

  /* Total de votos (contado automaticamente), à direita da linha do título */
  .lista-leitura > ol > li > ol > li > ol::after {
    content: counter(votos);
    position: absolute;
    right: 0;
    top: 0.75em;
    font-size: 1.6em;
    font-weight: 300;
    color: var(--ll-tinta);
    letter-spacing: 0;
  }

  /* Anula o espaço que o tema Primer põe entre itens (desalinhava os nomes) */
  .lista-leitura li + li { margin-top: 0; }

  /* Obra concluída: ~~ ~~ no Markdown */
  .lista-leitura del {
    color: var(--ll-cinza);
    text-decoration-thickness: 1px;
  }

  @media (max-width: 600px) {
    body:has(.lista-leitura) { padding: 2.5em 1em 0; }
    .lista-leitura > ol > li { padding: 1em 2.5em 1em 2.3em; }
  }
</style>
<!-- ===== fim do estilo ===== -->
# Lista De Leitura Oficial


> Legenda: Nome Da Obra (Nome do autor) {Quem sugeriu} - data/de/conclusão

<div class="lista-leitura" markdown="1">

1. Manuscritos Econômicos Filosóficos de 1844 (Karl Marx) {santanista}
	1. Votos
		1. fjnet
		2. rafzmilhomens
		3. santanista
2. A Categoria Político-Cultural De Amefricanidade (Lélia Gonzalez) {fjnet}
	1. Votos
		1. fjnet
		2. rafzmilhomens
3. A Ideologia Alemã (Karl Marx) {santanista}
	1. Votos
		1. rafzmilhomens
		2. santanista
4. As Veias Abertas Da América Latina (Galeano) {rafzmilhomens}
	1. Votos
		1. fjnet
		2. rafzmilhomens
5. Crítica Da Razão Pura (Kant) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
		2. santanista
6. Futuro Ancestral (Krenak) {rafzmilhomens}
	1. Votos
		1. fjnet
		2. rafzmilhomens
7. História Do Sexo (Foucault) {rafzmilhomens}
	1. Votos
		1. fjnet
		2. rafzmilhomens
8. O Capital (Marx) {rafzmilhomens}
	1. Votos
		1. fjnet
		2. rafzmilhomens
9. Pedagogia Do Oprimido (Freire) {rafzmilhomens}
	1. Votos
		1. fjnet
		2. rafzmilhomens
10. Peles Negras, Máscaras Brancas (Fanon) {rafzmilhomens}
	1. Votos
		1. fjnet
		2. rafzmilhomens
11. A República (Platão) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
		2. santanista
12. A Economia Das Trocas Simbólicas (Bourdieu) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
13. A Riqueza Das Nações (Smith) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
14. A Ética Protestante E O Espírito Do Capitalismo (Weber) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
15. As Formas Elementares Da Vida Religiosa (Durkheim) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
16. Casa Grande & Senzala (Freyre) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
17. Do Ensino De Filosofia Para O Ensino De Filosofi@: Tessituras Possíveis E Necessárias (Andrews Jobim) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
18. Do Espírito Das Leis (Montesquieu) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
19. Ensino De Filosofia Hipermidiático: Guia Do Docente {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
20. História Agrária Romana (Weber) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
21. Jamais Fomos Modernos (Latour) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
22. Leviatã (Hobbes) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
23. O Pensamento Selvagem (Lévi-Strauss) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
24. O Poder Simbólico (Bourdieu) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
25. O Único E Sua Propriedade (Max Stirner) {santanista}
	1. Votos
		1. santanista
26. Os Donos Do Poder (Faoro) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
27. Sermões (Pe. Antônio Vieira) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens
28. Tristes Trópicos (Lévi-Strauss) {rafzmilhomens}
	1. Votos
		1. rafzmilhomens

</div>

