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
</style>

# Um País Cristão - Brasil E O Cruzeiro Do Sul

![navegante](navegante.jpg)
> Para todos verem: um homem adulto com a mão no peito por debaixo do colete, como fez Napoleão, e um barquinho de papel na cabeça.

# Preâmbulo

Dentre várias teorias, destaca-se uma para o seguinte texto a teoria do enquadramento de Goffman que trata da ideia de que indivíduos comportam-se segundo a sua perspectiva de determinado fato. Para que isso ocorra, é necessário que exista o que Goffman chamou de "chave", que pode ser tanto física (um objeto) quanto mental (um conceito). Essa chave dará o tom para o comportamento. Pode-se pensar também no teórico da psicologia comportamental Skinner, para quem o objeto de estudo da psicologia deveria ser o comportamento somente. Em outras palavras: aquilo que se pode descrever de forma objetiva. Obviamente, o presente texto não dispõe de extensão hábil para defender analiticamente a complementação que, à primeira vista, parece óbvia entre uma teoria e outra. No entanto, observe como a ideia de chave, no aspecto mental, está bem complementada pelo conceito de "comportamento". Com isso em vista, tem-se o seguinte exemplo: uma cruz e uma roda gigante são elementos completamente diferentes. Onde um está, comporta-se muito diferentemente de onde está o outro. O espaço que coloca-se um é muito diferente do que põe-se o outro. E ambos criam uma espécie de atmosfera própria de cada um. Ora: uma igreja e um parque de diversões, é claro! Essa explanação inicial é necessária para que se compreenda o que vem a seguir.

# Nomes E Enquadramentos

Tendo sob a lupa a história do conceito do nome "Brasil" e que, como conceito visto acima, implica em um determinado comportamento de quem o detém, por assim dizer. Tem-se que tal nome não era o que gostariam os portugueses de colocar neste território do hemisfério sul. A ideia de nome original seria "Terra de Vera Cruz". Para os povos convencionados a ser chamados como "conquistadores", o último nome não se tornou popular, mas o primeiro sim. Contudo, para os povos que já habitavam este continente, o próprio chamava-se "Abya Yala". Tome-se então "Brasil" e "Abya Yala" como chaves para enquadramentos que suscitam comportamentos dos indivíduos. Ora, são comportamentos completamente distintos. Pois a história que um povo carrega consigo tem a ver com a história de sua cultura e portanto, a história de seus conceitos e objetos. Chaves para seus comportamentos. Afinal, a postura de um sujeito que nasce em Abya Yala em relação à sociedade que constrói e faz parte é muito diferente da postura de um sujeito que chama-a de "América" em relação a mesma sociedade.

Culturas convencionadas a serem chamadas como "indígenas" tinham visões e comportamentos diferentes dos povos convencionados "conquistadores". E um exemplo disso é o próprio calendário. Que requer uma discussão mais aprofundada, mas que será abordado aqui _en passant_: é dado conhecido que o calendário gregoriano está apoiado sob fortes bases dos povos tidos como "pagãos" e que tem nas datas comemorativas do calendário católico uma ressonância profunda. Como é o caso da relação entre a festa do Natal e a Saturnália. Ou o Dia de Todos os Santos e o *Samhaim.*.. Assim por diante. O problema que se revela aqui é que esse calendário simbólico, conceitual e, por assim dizer, também em certa medida "mítico", está todo voltado para o passar das estações dos territórios do hemisfério norte. Ainda, está voltado para como as estações se refletem naquele território. Assim, estão trocados em relação aos territórios do hemisfério sul e causam uma certa dissonância nas pessoas em relação ao espaço em que ocupam. Um exemplo: no Brasil, comemora-se o natal com neve artificial em pinheiros de plástico. O comercial da Coca-Cola é de um urso polar (!) e há neve falsa por toda parte. Todavia, o natal brasileiro realiza-se em pleno solstício de verão. E não é raro ouvir dos cidadãos que no país não é clara a divisão entre as estações do ano. Quando, na verdade, tampouco as estações tem divisão obscura, tampouco elas manifestam-se no território do mesmo modo que as estações europeias. Além disso, a divisão das estações em quatro partes também não é absolutamente necessária. Há calendários, como alguns calendários japoneses, com mais de 50 estações. Totalmente voltado para o território japonês, sua fauna e flora. Nesse caso, cada estação representa um estágio da arvore de cerejeira, por exemplo. Veja a importância dos conceitos e das narrativas míticas que a história chamada "oficial" tem sobre o comportamento das pessoas.

# Astrolábios

A história "oficial" conta que os conquistadores, ao chegarem em Abya Yala, utilizavam-se de estrelas para guiar seus navios. E que tinham o hábito de "pesá-las", isto é, o hábito de dar nomes a elas conforme o discernimento do astrólogo responsável. E foi pesando as estrelas que deram o nome de "Cruzeiro do Sul" a um conjunto de cinco estrelas. Observe que este é apenas um exemplo, há muitos outros, como a ideia que lhes ocorreu de rezar a primeira missa em solo. Pois, como se pode notar pela nota do inquisidor no prefácio da obra de Camões, o pensamento português é, ou transformou-se por algum momento, em cristão.

Ora, uma constelação não tem desenho certo. É como uma nuvem. Assume a forma que a imaginação lhe dá. E, não raramente, a forma dada é aquela importante para a sociedade na qual o indivíduo responsável por nomeá-la está inserido. Por exemplo, não haveria a constelação de "mesa" se o objeto mesa não existisse como referente. Do mesmo modo, se não houvesse uma cruz, não haveria referência para o "Cruzeiro do Sul". Povos de Abya Ayala poderiam dar nomes diferentes para aquele conjunto de estrelas. Ou talvez sequer teriam aquele conjunto de estrelas como uma constelação notável. Poderiam ser quatro ou cinco, ou várias outras constelações diferentes.

Existe uma noção, trazida por Buarque de Holanda, que o povo brasileiro constitui-se na relação de três culturas: Africana, Indígena e Portuguesa. Entretanto, apesar dessa imagem de três culturas distintas ter se cristalizado no imaginário do brasileiro, nem o próprio é de uma dessas culturas apenas, nem essas culturas eram monolíticas e harmônicas em si mesmas. De modo que há uma profusão de culturas diferentes em território africano e em território de Abya Yala, antes dos portugueses. Mesmo os portugueses eram latinos e celtíberos. E mesmo o brasileiro de hoje não é monolítico. Ele não é nem português, nem africano, nem indígena. Ele é o resultado dessa aventura, na falta de encontrar outro nome.

# Consequências

A Europa deixou para o hemisfério sul de Abya Yala algumas coisas que ficaram: quase toda sua herança cultural e também uma cruz perene pairando sob o céu e a grande consequência de que essa cruz é um sinal: o pensamento de que o Brasil é um país cristão. Retomando o pensamento de Goffman e tendo o Cruzeiro do Sul como uma chave, as pessoas acabam se comportando, queiram ou não, sob a perspectiva cristã, por ser a cruz um símbolo cristão por excelência. Poucos pensam sobre a origem do Cruzeiro do Sul e muitos assumem-o como um dado da natureza somente. Em outras palavras, assumem que é tão evidente o desenho de uma cruz entre aquelas estrelas que não poderia haver qualquer desenho outro. Por exemplo, o Brasil é um país que contemporaneamente comporta uma vastidão de denominações religiosas cristãs. E muitos outros países questionam: Em um mundo cada vez mais secular, no qual a religião desempenha um papel cada vez mais particular na vida de uma sociedade, por que razão o Brasil ainda leva tão consigo presente o pensamento quase medieval de uma política cristã? Naturalmente, não há resposta absoluta, mas o exposto até o momento pode contribuir para a colcha de retalhos que comporá a resposta. Ainda, no Brasil, há aqueles que inflam os pulmões para dizer que "O Brasil é um país cristão!".

Muitos dos que afirmam isso fazem-no com três disposições mentais diferentes: 1. País cristão como um dado da natureza. 2. País cristão como constatação de sua realidade. 3. Como vontade de tornar-lo cristão e apagar tudo aquilo que não o é do território (catequizar os gentios). Outra coisa se apresenta nesse contexto: aqueles indivíduos que se veem como separados em "três raças" já não o são a muito tempo. Estão relativamente misturados, ao menos geneticamente, pois a sociedade é, cada vez mais, estratificada. O produto disso é que o campo no qual a catequização dos gentios se dá não é mais externa ao indivíduo. Pois é ele próprio "Cristão e gentio". Descende de ambos. A briga é interna à psiquê, que querem catequizar-se a si mesmos até o fim dos tempos. Um país que busca por inimigos internos a todo o tempo. Um país que destrói imagens de orixás e santos, que o crime organizado e o corpo político se proclama muitas vezes como de determinada religião, como se isso estivesse essencialmente relacionado às suas atividades.

O psiquiatra suiço, Carl G. Jung afirmava que na psiquê nada se apaga e que também ela é histórica. Mesmo que um indivíduo queira catequizar a si... e os outros grupos que fazem parte de seu espírito e sua história? Qual é o local que essas "forças" vão ocupar nessa sociedade e nessas psiquês? Esse é o grande problema do sujeito chamado, constituído, identificado sob o conceito de "Brasileiro". 

# Conclusão

Este texto tem como objetivo demonstrar como algo aparentemente simples como a ideia de olhar para o céu e dizer "aquilo será uma cruz" vai ressoar na psiquê de quem virá séculos depois. Diante do exposto, torna-se evidente que a identidade brasileira foi construída segundo uma herança simbólica densa, como a do Cruzeiro do Sul. Cuja interpretação se reflete pelo comportamento cristão da sociedade. Não é preciso, no entanto, construir um país laicista, mas um país verdadeiramente laico e rico em expressão religiosa.

RFZ