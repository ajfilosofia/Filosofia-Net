---
title: Pré-Textuais
autor: rfz
data: 2026-11-09
---

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

# A Máquina Do Sentido[^1]

[RFZ O Espírito Zombeteiro](RFZ_O_Espírito_Zombeteiro)

A Máquina Do Sentido: Teoria Não Universal Pós-Secular Da Percepção

Ensaio sobre a crise na percepção do indivíduo pós-secular.

Brasília, D.F.

Início em 2026

## Dedicatoria

> Para todos que já amei.

## Epígrafe

> "Isso significa que, apesar de tudo, somos uma província da civilização ocidental. Uma nova Roma, uma matriz ativa da civilização neolatina. Melhor que as outras, porque lavada em sangue negro e em sangue índio, cujo papel, doravante, menos que absorver europeidades, será ensinar o mundo a viver mais alegre e mais feliz" Darcy Ribeiro. *O Povo Brasileiro: A Formação e Sentido do Brasil.* pg. 198

## Apresentação Do Autor

### O Problema Intelectual Que O Livro Ataca

Muito em breve o leitor conhecerá Maria. Personagem importante para. Maria é a persona que encarna e vive a realidade pós-secular.
{: .capitular}

Maria operando o mecanismo de "Purificação Simbólica" sem perceber tem muito a perder. Perde a capacidade de agir sobre os sistemas, ainda que pela recusa em participar deles. Afinal, ela desconhece a existência daqueles em que está inscrita, quiçá vários outros.

Quando Maria reconhece o mecanismo a partir da assimilação do conceito ela ainda o opera, mas sabe que o faz. Pode agora decidir de que forma operá-lo.

Uma vez que sua percepção não é mais a mesma e uma miríade virtualmente infinita de sistemas se revela à personagem, o real ganha nova dimensão, o espaço de ação, outrora delimitado por premissas específicas, ganha novas fronteiras. Maria agora pode decidir quais sistemas habitar e porquê.

Em nível social e político, Maria pode intervir sobre a operação do conceito coletivamente. O que vale para Maria, vale também para as instituições que ela participa. Uma instituição, nas pessoas de seus membros, consciente do mecanismo que opera como programa invisível tem agora, ao contrário, um amplo panorama do programa e, portanto, a capacidade de, via reflexão, escolher mudá-lo, otimizá-lo ou até mesmo abandoná-lo.

A percepção do indivíduo, exemplificado por Maria, não é fenômeno irrelevante ou menor à escala social. Tampouco o inverso. A escala social é também relevante à percepção do indivíduo. De modo que Maria desenvolve agência quando reconhece o potencial dialético das ações motivadas por sua percepção do real. E tal reconhecimento tem consequências indeléveis em nível pessoal e social: fraturam-se estruturas, e sistemas passam a emergir dessas fissuras.

Em outras palavras, este livro não tem como centro gravitacional o conceito de "Purificação Simbólica", mas a *assimetria entre habitar um sistema e conhecê-lo* e as consequências, portanto, de cada uma dessas coisas.

### Do Ensaio Brasileiro

É possível que o leitor questione a razão pela qual este livro se pretende fazer um discurso científico utilizando-se no entanto de um registro que à primeira vista pode parecer estranho à forma da publicação científica convencional: O ensaio.
{: .capitular}

No entanto, o Brasil, recorte necessário e importante para este exercício, tem longa tradição de teóricos, homens da ciência, que teceram seus conceitos, ferramentas metodológicas, descobertas com o registro ensaio. Dentre eles destaco os que acredito serem os mais relevantes para o panorama no qual este livro se insere quando propõe-se a discutir o caso Brasileiro: Sérgio Buarque de Holanda e Darcy Ribeiro.

O primeiro, Buarque de Holanda, escreve seu livro seminal "Raízes do Brasil" nesse mesmo registro: o ensaio. E o faz de forma magistral. O segundo, Ribeiro, em sua obra "O Povo Brasileiro" também o faz no trabalho que pode ser considerado como a pedra angular para perceber o Brasil. Ambos o fizeram, não de forma inconsciente, por capricho formal, mas por que reconheciam que há no ensaio, o gênero que não se dobra a forma alguma, a possibilidade de expressar em amplo espectro toda a vastidão de sentidos e conceitos que uma investigação recobre: seu objeto (O Brasil) exigia.

Esta obra também o faz não somente por discutir o Brasil e honrar a tradição dos estudiosos que a inauguraram, mas também por um imperativo metodológico. Ao me inscrever no objeto que analiso tenho uma única opção: me implicar no discurso sobre tal objeto. O que não é compatível com o uso da terceira pessoa tão cara e necessária ao discurso acadêmico, quando este se pretende neutro (sic), objetivo e fora do objeto, por exemplo.

Por fim, o gênero ensaio além de ferramenta tradicional, plástica, versátil, conforme a tradição e imperativa ao método desta obra é também um caminho do meio entre a literatura e a aridez da linguagem acadêmica. Sabe-se que ambas tem grande valor para a percepção do indivíduo (nosso objeto). De maneira que tal estilo se mostra perfeitamente aderente à pena e ao leitor. Que pode doravante fruir das benesses do registro literário sem, no entanto, perder o rigor do método.

### Trajetória do Autor

Iniciei meus estudos na Universidade de Brasília em 2015, com dezoito anos então. Comecei pelos estudos de Jornalismo, que não concluí e formei-me bacharel em Comunicação Social habilitado em Audiovisual com o Trabalho de Conclusão de Curso Intitulado "O Conceito de Linguagem Audiovisual na Pesquisa em Comunicação". Desde os primeiros anos do curso já me causava interesse a percepção e os efeitos da mesma nas realidades coletiva e subjetiva.
{: .capitular}

A fratura necessária para a minha percepção e insights acerca do tema deu-se não somente pela formação e o conhecimento de cada novo autor, teórico, pesquisador, mas também pela vivência na fronteira de realidades muito distintas: entre a universidade e ser o primeiro universitário de uma instituição federal da família. 

A formação em Audiovisual na Universidade de Brasília com os mestres que dispus equipou-me com o rigor técnico e metodológico que disponho. A vivência universitária com muito mais que isso, mas também com o *drive* para o estudo auto-dirigido. Não se forma um universitário única e exclusivamente através do estudo orientado por um professor. Como defendia Darcy Ribeiro, fundador da Universidade e nome do seu principal *campus*. Através do tripé essencial: Ensino, pesquisa e extensão.

A síntese dessa fratura causada pelo estranhamento do viver em fronteira se deu pelo interesse acerca da linguagem. Daí o tema do Trabalho de Conclusão de Curso e agora desta obra: Do estranhamento à fratura, da fratura à linguagem, da linguagem à percepção, da percepção à pesquisa independente.

E é daí, da pesquisa independente equipada com o rigor universitário adquirido que descobri o Audiovisual não como mero fato social relevante para os cadernos da crítica jornalística de cultura, mas como aparato simbólico sofisticado cuja operação e funcionamento interessam muito a todos aqueles que desejam compreender a percepção, a cultura, e tantos outros objetos.

O Audiovisual é objeto, mas sua pesquisa também é campo legítimo para a investigação científica em todo nível que se dispôr: de matéria jurídica (câmeras de segurança) ao estudo da Biologia (observação indireta da fauna e flora) a pesquisa em Audiovisual se faz necessária por não bastar ouvir e ver, deve-se perceber, interpretar, assimilar, recordar e transmitir.

É preciso que o pesquisador em Audiovisual trate de filmes somente? quando vive-se na realidade uma profusão de imagem e audio. Perceber, interpretar, assimilar, recordar e transmitir são cada verbo um campo específico cujo estudo o Audiovisual suporta e compreende.

De modo que não seria necessária a existência de um Cinema sequer na história da humanidade para que a pesquisa em Audiovisual fosse possível. Enquanto o homem dispuser de sentidos (ver e ouvir são a ponta do *iceberg* comunicacional) haverá justificativa plausível para que se busque compreender as operações mencionadas e tantas outras que implicam o Audiovisual.
### Do Alcance Da Hipótese De Trabalho

É preciso que se reconheça desde já que este livro trata do Brasil pelo brasileiro. Delimita-se a isso e o faz por ser o Brasil já saturado de Brasil pelo estrangeiro. Não somente por isso, mas também por que o estrangeiro pode não dispor de Brasil suficiente para compreendê-lo. Suas ferramentas, em geral, não são apropriadas à realidade, que se impõe a cada novo exercício.
{: .capitular}

As mitologias do pequeno burguês de Barthes (falo disso adiante) não explicam suficientemente o Brasil nem o Brasileiro. São ferramentas insuficientes para esses sistemas simbólicos suas relações e interações. O indivíduo que dessas ferramentas se serve corre alguns riscos e deles o principal: não realizar o trabalho conforme, devido à percepção errônea que a ferramenta pode lhe proporcionar.

Como um açougueiro que dispõe de uma pequena faca de plástico: se, para esse exemplo a faca de plástico é o conceito importado, o boi é o Brasil e o açougueiro o pesquisador, até mesmo o exemplo é insuficiente. O Brasil é deveras mais complexo e amplo que um boi. E a obra de Barthes mais valiosa que uma faca de plástico.

Portanto, por implicações lógicas que serão desenvolvidas no corpo do livro com maior detalhe, mas que já se anteveem, o conceito proposto aqui não se pretende universal. Assume a possibilidade de correlatos que se adaptam a cada situação, mas não é replicável fora da realidade brasileira. O Brasil é matriz e espelho dessa matriz. De modo que aqui o Brasil é recorte metodológico, mas não é modelo exportável.

E tratando sobre a percepção do indivíduo brasileiro pós-secular a postura assumida reconhece também tal indivíduo como único, inscrito em sistemas únicos e que é capaz de perceber a si com conceitos próprios. Tal postura não implica isolamento metodológico, ao contrário: é na fronteira dos sistemas, no contato com o estranho, a máquina de sentido, que vive a possibilidade de nova compreensão de interpretação, adaptação e re-interpretação. Coisas, inclusive, impossíveis de serem obliteradas em qualquer contato semelhante.

Em suma, o Brasil e o brasileiro admitem aqui correlatos, mas não se pretendem universais. Como alguém que tem amigos, até mesmo irmãos gêmeos, mas que, apesar das afinidades, são diversos e assim convivem.

### Da Poesia

Cada capítulo está aberto com um poema como epígrafe. Por quê? É também uma escolha de método. Ao iniciar com uma epígrafe diversa, mas que dialoga com o conteúdo do capítulo tenho o objetivo de causar uma fratura na percepção, que é diferente de fissura, a fratura implica uma cicatriz, uma marca, uma memória e uma diferença. Ao estranhar o capítulo em relação ao poema e vice-versa, pode-se compreender bem o mecanismo aqui descrito: o primeiro impulso do leitor.
{: .capitular}

O final do livro pretende-se uma fratura de percepção profunda o suficiente para deixar a cicatriz do que chamo "Crença reflexiva" como método e postura diante de cada poema. Não há óbice para que sejam revisitados, redescobertos e re-interpretados à nova luz... Sugestão dada.

Conforme a obra avança, o leitor perceberá que ele mesmo é indivíduo já inscrito no objeto deste livro e que estranhar o registro no qual escrevo foi condição *sine qua non* para a fratura na percepção tão necessária à apreensão do mecanismo central aqui descrito.

[RFZ O Espírito Zombeteiro](RFZ_O_Espírito_Zombeteiro)

[^1]: Rfz é pesquisador independente baseado em Brasília, Brasil. Bacharel em Comunicação – Audiovisual (Universidade de Brasília – UnB). Interesses de pesquisa incluem sistemas simbólicos pós-seculares, semiótica, teoria cultural, e os mecanismos pelos quais tecnologias de sentido organizam a percepção coletiva. Atualmente desenvolvendo o conceito de “**Purificação Simbólica**”: uma matriz para compreender como sistemas simbólicos dominantes sobrescrevem outros enquanto apresentam-se como neutros (rafzmilhomens@proton.me).
