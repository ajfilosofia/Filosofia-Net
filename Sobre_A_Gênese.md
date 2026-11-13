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
# Sobre a Gênese "発生について"

P

(1) Estava relaxado,  — pleno? — não,

(2) mas muito concentrado seria encontrado no lago.

(3) Escuridão comum a todos os mortais, razão turva e a emoção em clarão.

(4) Pulsando forte naquele azul escurecido pelos mistérios da noite e inclinado no verde dos arredores, fui arrastado. Nem pensava como tal estado, bem cultivado, podia me ser furtado.

(5) — ... quê?

(6) o vermelho aos meus olhos que queimava a vista mas me permitia agora no lago ver o que não se vê,

(7) aquilo que ninguém, mesmo em várias vidas, veria!

(8) pois quem vê jamais esqueceria essa coisa bonita, indescritível e que preenchia minha mente como fosse uma jazida.

D1

(1) O estado furtado de calma de minha excelente meditação muito me irava.

(2) Raiva.

D2 

(1) — O que me queima os olhos, se não acendi fogueira alguma e nem sinto cheiro de fumaça?

(2) Como cego, não podia enxergar em nenhuma instância.

(3) Ignorância.

D3 — O homem

(1) O vermelho era do céu!

(2) Amanhecia com um homem assentado ao meu lado e bem sorridente que vinha com simplicidade... amigável, afável...

(3) A raiva foi cortada, a mente parecia ter sido adocicada pelo mais doce mel...

(4) Não tinha capacidade de ver nada além do sorriso, o homem era misterioso, inacessível e sua presença era imensurável.

(5) — que fazes, homem, parecia tão calmo... sua meditação parecia agradável, contudo, que fazes, homem, com essa ira e turvez... acaso o Abençoado não ensinara corretamente a prática que salva? — Disse Ele.

(6) Fui surpreendido por um Bodhisattva! — pensei corretamente.

(7) — O Abençoado nunca falharia! Cresci ouvindo as Nobres Verdades. Infalíveis!

(8) — Ouviu retamente?

D4 — O sermão do Buda

(1) Acaso podes ouvir o que não se fala, homem?

(2) O Tathagata te disse algo?

(3) Sua meditação ainda ilude sua mente pequena, confundindo o despertar com o desprezo, pensa que será como fidalgo?

(4) Suas respostas não me valerão palavras! Ouça o que diz o abençoado.

(5) Nada professa a Nobre-Boca do Buda, seu Amor revela fora das palavras, suas palavras se revelam no corpo e consomem.

(6) Tu vieste arrastado pelo desejo, homem. Não percebes que sua mente, tentando negar sua existência enquanto ser que sofre, ainda deseja alguém?

(7) O desejo significa que você não está sozinho, implica que há uma unidade mais fundamental para além da ilusão do Eu que tem te enganado.

(8) Purifique a mente, os olhos queimam, mas só pode ver quem tem luz. O fogo revela o mundo n'O mistério e Além.

(9) A Gênese de tudo vem do Infalível Amor, na Compaixão Incondicional. Hão duas vias que tu verás para conhecer o Amor: a Via do Sukha e a Via do Dukkha.

(10) Contudo é verdadeiro que todo amor é tomado pela Via do Sukha, pois pode haver atração na insatisfação?

D5 — O que está havendo no ambiente?

(1) O tempo não passa, o sol não aparece, o Buda fala, gesticula, me convence e nada sai do lugar!

(2) Aquilo me assustou, afinal o que estava havendo com o lago que logo havia tanta imensidão que o confundi com o mar?

(3) Pensar, deixar, amar deixar pensar...

D6

(1) A verdade do Amor é que ele se apresenta sempre na atração, como o imã com o metal,

(2) o Amor enquanto força no mundo, ilude, parece leve e bom,

(3) Porém é furtador da atenção, a concentração é seu inimigo mortal.

(4) Os amores dos mortais carregam sua condição inteira, que é a insatisfação, pois é verdade que o maculado não pode negar seu dom.

(5) Como acreditar no maculado para libertar?

(6) O Livre pode purificar a mácula, mas a mácula jamais pode libertar o maculado.

(7) Por isso a mente deve se atentar.

(8) Escute o Abençoado, pois no Futuro virei e tu não serás mais escravizado.

D7

(1) Pode no mundo algo nascer se não pelo Amor?

(2) Desconheço homem que nasça, animal que reproduza, sem que haja o papel do Amor neles.

(3) Invariável verdade é que o Amor une e se separa, mas só se separa daquele que nega ser amado.

(4) Pode alguém amar a Dor?

(5) Livre-se deles.

(6) Imutável é a palavra do Tathagata, mestre de demônios e deuses, incomparável é o puro e o impuro e incomparável é o Livre e o Maculado.

(7) Agora sei que o Amor é Maitreya! A verdade do Dharma é que o Amor é Bom e Amigável! Tu, misterioso homem, és o Amor. — Disse eu, intervindo a fala que ele articula.

(8) Homem, há vários amores e há o Amor, o Amor é conhecido na Via do Sukha que apenas o Abençoado pode ensinar. Dizer sobre o nascimento é dizer sobre o amor é vice-versa, contudo lembre-se: O livre liberta e o maculado macula.

E

(1) E então acordei: sentado e desperto.