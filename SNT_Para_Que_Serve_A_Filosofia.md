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

![Livro antigo](/img/Livro_antigo.jpg)
# "Para que serve a filosofia?" — Uma investigação literalmente inútil.

[Sant' Um Único](Sant'_Um_Único)

> "No fim, a longa linha de sua disputa chega a este ponto: que um [o filósofo] dá o preceito, e o outro [o historiador] o exemplo. (...)" — Sir Phillip Sidney [Em Defesa da Poesia]

**Escritas Preliminares**
Digo a cada pessoa que desgasta do seu tempo que lhe é próprio como Chico Buarque que "Meu caro amigo, eu não pretendo provocar". Pois o que pretendo é mais que isso, eu pretendo queimar as certezas e ascender a luz da verdade. 
Bom, imagino que saibamos que na filosofia, antes de tentarmos responder uma pergunta, precisamos primeiro discernir os compromissos internalizados nela que nesse caso é: todo conhecimento válido deve servir para um interesse humano.
Contudo, essa sentença tem compromissos internalizados também, pois o que é um conhecimento válido e qual interesse humano estamos falando?
Bom, não irei estender sobre a validade do um conhecimento, pois o que importa é: que interesse humano está validando o conhecimento? Já que essa é a questão central da sentença internalizada na pergunta do título.

**Iniciação ao conteúdo**
Quando tratamos do _interesse humano_ sabemos claramente que trata-se de uma inclinação, de um mover a um objetivo tal qual é descrito o mover do agir ético humano à eudaimonia em Aristóteles. Mais que um interesse individual, é um interesse que reconhece-se na espécie e nos indivíduos na convivência social, considerando que Marx [no _manuscritos econômicos-filosóficos_] e Feuerbach definem o Homem como _ser-espécie_ (Gattungswesen) por sua existência ser genérica e se realiza plenamente na espécie. No caso, não podemos desconsiderar que esses interesses são mediados para o homem pelas instituições e sua relação econômica e social com seus iguais. Então quando ouvimos essa pergunta, devemos lembrar que na sociedade capitalista e técnica ela significa "Qual é o lucro ou facilitação ao lucro que a filosofia é capaz de entregar?", pois sabemos que essa armadilha alcança até as ciências devido sua abstração que naturalmente atinge sua existência pós-filosófica e invalida diversos conhecimentos científicos no pensamento popular. Até agora, notamos que o interesse humano é **historicamente localizado** e **socialmente mediado** e que quem pergunta isso está em uma sociedade capitalista, portanto, ela quer saber a utilidade mercantil. Para esse interesse em específico digo: Não. A filosofia é o antônimo de qualquer interesse imediato ou útil. "Que interesse a filosofia suprime?", "Ela suprime um interesse?" ou como um filósofo perguntaria: "Ela deve suprimir um interesse?"

**A filosofia**
Gosto de dizer que a filosofia é a "arte de fabricar contexto", é uma roteirização do mundo que indica como ele deve ser a partir do que o filósofo pensar que é o mundo.
A filosofia busca as leis universais, o ser enquanto ser: investigar a natureza, o agir e o pensar.
Quando perguntamos para que serve a filosofia, devemos pensar em maneiras de responder e eu vou dar a resposta de um historiador, um poeta e um filósofo e suas perguntas — pois nenhum deles perguntaria dessa maneira, mas sim da que eles podem pensar.

O historiador provavelmente iria perguntar "Para que a filosofia serviu?" e logo teria a resposta em seus livros: A Filosofia iniciou o pensamento lógico e racional sobre a natureza e o agir, começando a dividir os conhecimentos da matemática, da física e da lógica. Depois desdobrou historicamente em suas próprias rupturas, na ciência moderna, no renascimento, no iluminismo... Na revolução francesa, nas constituições... ou seja, ela serviu para iniciar e proporcionar as descobertas mais recentes das ciências, dando o método e até para transformarmos a nossa política ao longo da história.

Diferentemente um poeta perguntaria se " a filosofia poderia servir para algo?" e com seus versos e estrofes o poeta talvez responderia tal qual _Buarque_: "O mundo me condena
E ninguém tem pena
Falando sempre mal do meu nome
Deixando de saber
Se eu vou morrer de sede
Ou se vou morrer de fome
Mas a filosofia, hoje, me auxilia
A viver indiferente assim
Nesta prontidão sem fim
Vou fingindo que sou rico
Pra ninguém zombar de mim
Não me incomodo
Que você me diga
Que a sociedade é minha inimiga
Pois cantando neste mundo
Vivo escravo do meu samba
Muito embora vagabundo
Quanto a você
Da aristocracia
Que tem dinheiro
Mas não compra alegria
Há de viver eternamente
Sendo escrava dessa gente
Que cultiva hipocrisia" [música: Filosofia]. Talvez responderia de outra maneira, mas enfim, poetas. Amáveis e confusos.

O filósofo perguntaria "A Filosofia deve servir para algo?" e a resposta espanta, talvez, como responderia Heiddegger: ""É perfeitamente exato e da mais completa justeza dizer: 'Com a filosofia não se pode fazer nada.' O único erro é julgar que, com tal afirmação, se encerrou o julgamento sobre a filosofia. Pois resta ainda um pequeno aditamento sob a forma da contra-pergunta: se nós não podemos fazer nada com a filosofia, não poderá ela, porventura, fazer algo conosco, contanto que nos entreguemos a ela?"" — _Língua de Tradição e Língua Técnica_ (pp. 8–13). e "A filosofia é, por sua própria essência, intempestiva, porque pertence àquelas poucas coisas cujo destino é nunca poderem encontrar ressonância imediata no seu próprio presente, e nem sequer terem o direito de a encontrar. Quando parece acontecer tal coisa, quando uma filosofia vira moda, ou não há aí nenhuma filosofia real, ou ela é mal interpretada e abusivamente aproveitada para quaisquer fins estranhos a ela, segundo as necessidades do dia."
— _Introdução à Metafísica_ (Capítulo I: A questão fundamental da metafísica).

A filosofia, portanto, não pode ser avaliada a partir dos critérios que avaliamos as outras ciências, as técnicas... pois são os próprios filósofos na sua produção imediatamente inútil quem produzem o contexto em que esses sistemas fazem sentido.

**Considerações finais**
Não temos uma resposta clara de "para que a filosofia serve?", mas uma coisa temos "para que a filosofia não serve?". A filosofia não serve a nada e a ninguém, é irreverente e sustenta-se a partir de uma característica essencialmente humana que não pode homem algum desvincular-se: o espanto (ou a admiração) diante do ser dos entes. Como diria Farias Brito em _A Base Física do Espírito_:
 "Já sabemos que a filosofia é a paixão do conhecimento. Como paixão é necessidade e como necessidade é força que leva à ação. É assim que a primeira manifestação da filosofia é a curiosidade natural que nos leva a indagar da significação das coisas. É o que poderia se chamar o instinto do conhecimento, instinto que é a vida mesma do espírito; que começa com as primeiras revelações da consciência e vai continuamente crescendo à proporção que a consciência se alarga. A filosofia é, pois, a atividade mesma do espírito: atividade permanente, por se tratar de uma necessidade que jamais poderá ser satisfeita de todo, de uma necessidade que a todo momento se renova; o que justifica em absoluto a fórmula de Leibniz: perennis philosophia.
Podemos, pois, concluir: a filosofia é uma atividade permanente do espírito humano; é o espírito interrogando a realidade, o espírito em ação, lançando o seu olhar sobre as coisas e procurando explicá-las, investigando o desconhecido e elaborando o conhecimento."

> "Trata-se de livro inacabado porque lhe falta a resposta." — Clarice Lispector [A Hora da Estrela]"

[Sant' Um Único](Sant'_Um_Único)