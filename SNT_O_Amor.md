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

# O Amor: princípio dos princípios filosóficos

[Sant' Um Único](Sant'_Um_Único)

![stirner](citação_stirner.jpg)

_"Um gole de conhaque
Aquele toque em teu cetim
Que coisa adolescente
James Dean" — Belchior (Medo de Avião)_

O amor aparece das maneiras mais joviais que podemos imaginar. Em O Banquete, Diotima o apresenta como uma escada que parte da sensibilidade para alcançar o amor pela Ideia — isto é, pelo fundamento perene e necessário de todas as coisas.
Esse despertar pelo sensível, como atração pelo corpo, emerge de um efeito natural de espanto diante do diferente e do mistério interno que existe ali. Percebemos, assim, que habitamos um corpo, mas que nossos sentimentos, pensamentos e crenças transcendem a nossa imediata e efêmera carne, isso expande no reconhecimento da mente e da existência do outro. A música do Belchior é sobre esse espanto _(thaumazein)_, esse primeiro contato sensual com o outro que leva-nos à curiosidade acerca de sua interioridade: o degrau da beleza da Alma (o segundo degrau foi ignorado momentaneamente).
Toda essa questão nasce também de um afeto concebido a partir daquele corpo e daquele acesso parcial de suas concepções mediado pelos comportamentos, é perceptível um acesso a algo que parece muito maior que toda aquela simples relação entre corpos, uma conexão naturalmente formada em uma admiração à alma d'outro, como diz Colón:

_"No se puede negar la existencia de algo palpado
Por más etéreo que sea" — Willie Colón (Oh que sera)_

Não podemos negar aquela afecção, apenas crer ou não e nós cremos nela, óbvio!
Como poderíamos não acreditar?
Nós somos envolvidos numa presença, beleza e admiração que supera até as nossas vontades mais individuais, nossas crenças... muitas coisa fragiliza diante tal mistério, diante tal poder!

_"Quando a gente ama, brilha mais que o Sol
É muita luz, é emoção" — Arlindo Cruz (O Que É o Amor)_

É desse sentimento que Arlindo Cruz tenta dizer mas que não sabe explicar que nós estamos partindo. Estamos partindo dessa emoção que dá forma a tudo, como um tecelão que ao tecer conecta os mais diversos fios (que aqui representam as sensações) em uma obra final mais poderosa que cada fio, que antes frágeis, agora persistem em uma existência quase infinitamente maior que em sua simples singularidade.
É do espanto inicialmente dado pelo corpo que percebemos aquilo em outros corpos, é percebendo na nossa alma a existência de um mistério interno no outro corpo, que percebemos a vastidão das almas... todas livres! Isso é o que espanta mais: a vastidão de mistérios. Todos apaixonantes! Não para uma só alma, mas certamente para alguma. Tudo isso é o fundamento da filosofia, é aí que nasce a estética, a psicologia até as curiosidades sobre o mundo natural. 
Sabemos não é agradável às almas mais confusas toda essa liberdade e fuga de suas soberania, tal coisa dá forma à uma corrupção muito difícil de perceber: a tirania. Isso é uma morte para tudo que pensamos sobre o amor, o amor é o oposto da tirania, é a aceitação da liberdade daquela alma ante sua própria liberdade, a liberdade de não ser íntegra contigo e muito menos de te obedecer. Isso é o que permite o amor persistir temporalmente em si mesmo, pois levanta o espanto e permite sua continuidade na caminhada até patamares maiores: o nosso quarto degrau, o do amor pela ação e pelas leis.

_"O amor só dura em liberdade" — Raul Seixas (A Maçã)_

Todo o espanto pelo interior sensível no corpo e nas crenças do outro, que também só é permitido por perceber a beleza dos outros corpos é certamente também permitida pela reflexão das práticas e das leis. Pensar na corrupção e na virtude das ações, pensar no que é certo recorrer em todos os casos que se amparam naquele espanto, começamos a discursar sobre a defesa pela liberdade, sobre o que move os corpos e dá forma aos pensamentos mais belos. A filosofia é baseada no mesmo princípio do amor, pois é com esse mover natural da nossa alma para a vida comum a partir do seu espanto com o outro que permite a ética, a moral, as ciências naturais e até a matemática.
O amor é o promotor da razão às coisas, mas também é por amor que não permite que a razão esgote o mistério do amor, dos corpos e das almas, pois a cláusula do amor é a liberdade.
Toda a vida, em forma e conteúdo só é razoável por causa do Amor, tal que na eternidade, o Amor é causa do nascimento dos deuses a partir do informe.
O amor é a:
"_Razón eterna de vivir_" — Frank Sark (Amor Mío)
E este é o último degrau: O amor em si.

[Sant' Um Único](Sant'_Um_Único)