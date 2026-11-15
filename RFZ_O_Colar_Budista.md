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

# O Colar Budista[^1]

[RFZ O Espírito Zombeteiro](RFZ_O_Espírito_Zombeteiro)

>RECICLAGEM
>
>Nem tudo que eu te digo
>Era originalmente pra você
>
>Muito já escrevi
>Pra outros endereços
>
>Você não é por isso
>Menos digno de apreço
>
>É que, por sermos humanos,
>Muita coisa é repetida
>
>E pra ser sustentável
>Economizo minhas linhas
>
>Conhece o japonês
>Que com outro emenda?
>
>Pensa nas minhas palavras
>Como os cacos dessa lenda
>
>E você, o motivo d'eu tentar
>O coração de novo emendar


### Encontro Com o Objeto

A "lenda" referida no poema acima é o *kintsugi* (金継ぎ). Quando os cacos de um vaso são emendados com ouro, o objeto ganha status novo devido a emenda dos cacos. Falarei em seguida de um objeto e um conceito cuja operação relaciona-se com a ideia do poema.
{: .capitular}
#### Descrição Concreta

É leve. Quando enrolado, posso contê-lo com uma mão. Posso também enrolá-lo no na mão ou no braço. É circular e possui contas de madeira. 108 contas, para ser mais exato. Uma delas é consideravelmente maior que as outras e tem um pingente verde de tecido leve ao toque, pendurado, verde escuro. O pingente tem vários fios desse tecido e brilha contra a luz como a seda. As contas também brilham contra a luz devido ao que parece ser verniz. A cor é de madeira, cor de mel meio acastanhado. A porosidade da madeira e algumas nódoas, poucas e pequenas, ainda se sente e se percebe ao toque. O cheiro também é de madeira. As contas produzem um "tec tec" baixo quando batem umas contra as outras. Pode-se mesmo dizer que é singelo e muito bonito.
{: .capitular}
#### Contexto De Circulação Contemporânea

Pedi meu Japamala pela internet. No *site* havia vários preços, formas, cores e descrições. Por digitar diretamente "Japamala" no buscador fui direcionado a uma seção já com vários materiais: pedras naturais, madeira, sementes, materiais sintéticos.
{: .capitular}

As descrições variavam como "Espiritual", "Rosário Budista", "Paz". Ocorre que também não recordava do nome exato do objeto. E, ao invés de digitar diretamente "Japamala" no buscador, o que fiz na segunda vez, digitei "Jamapala" e aí surgiram diversas descrições ainda mais ricas. A começar pelo departamento da loja, cujo mecanismo de busca enquadrou em dois: Moda e Espiritualidade. Os nomes dos produtos dessa vez também vinham com uma ligeira descrição: "Cordão sagrado para meditação", "Desbloqueio de Chakras", "Equilíbrio emocional", "Proteção espiritual", "Pulseira budista", "Decoração sala, quarto, adorno", "Decoração vaso garrafa".

Após algum tempo de busca, encontrei um de madeira e com uma espécie de pingente verde que me atraiu e por um bom preço. Aproximadamente R$ 20,00. Comprei-o e aguardei a entrega em casa.

Enquanto isso, resolvi buscar definições, funções e modo de uso em *sites* especializados e não especializados. O primeiro dedicava-se exclusivamente à produção e venda de Japamalas e fornecia uma breve descrição "Poderosas ferramentas para a meditação e a prática do mantra". Em seguida, um manual de uso.

O segundo *site* definia-o como "Cordão sagrado feito de contas, usado para ajudar o praticante a entrar no estado meditativo." E trazia também regras de uso. Que variavam de instruções "como energiza-lo" a proibições "Remova durante a visita ao funeral".

Fui mais a fundo e decidi pesquisar por "colar decorativo". Não o fiz por acaso. Já havia visto tal decoração em muitos lugares. Especialmente consultórios médicos e escritórios de *Design* e Arquitetura. 

E não fiquei surpreso ao encontrar peças idênticas ao Japamala em forma e estilo. Maiores, no entanto. Posicionadas sobre a mesa, em prateleiras, vasos, cumbucas. Geralmente em madeira e alguns com pequenas contas com palavras como "*Home*". Cheguei mesmo a encontrar um com um pingente em uma ponta e um crucifixo em outra. As descrições iam de "colar genérico" a "decoração estilo *boho*" ou "Ambientes estilo mediterrâneo".

O Japamala tem ainda alguma aura espiritual quando objeto decorativo e inspira no lugar em que é usado (sic) uma espécie de energia *zen*, calma, quietude. Geralmente acompanhada de desodorizadores e fontes de água artificiais.

O que chama a atenção é como um objeto cuja origem pertence a mosteiros isolados na Ásia tornou-se tão acessível às prateleiras das lojas virtuais. O que necessitaria uma iniciação a uma tradição religiosa com rito próprio agora pode ser entregue diretamente em minha casa e com um pequeno ritual de "limpeza" e "ativação" energética já substitui-se a iniciação. Além da versatilidade do que deixa de ser matéria para canalização de energia espiritual e torna-se objeto decorativo.
### Múltiplos Sentidos Atribuídos

Observa-se a partir do exposto que o Japamala parte de matéria devocional a objeto. Tal objeto agora tem vários usos possíveis que se aproximam e se distanciam do seu uso original. É sobre isso que tratará essa seção.
{: .capitular}
#### Uso Ritual

O Japamala tem em seu nome a sua origem. Japamala significa algo como a junção do espiritual com o material. E para isso é usado pelos monges: Canalizar a energia espiritual. Concentrar-se em sua prática central: O *zazen*, também conhecido como meditação.
{: .capitular}

O uso do Japamala implica uma pertença a uma comunidade, uma prática central constante e uma atitude específica diante do sagrado. Nada se faz com o Japamala em tal contexto que não seja enquadrado dentro dessa tradição.

Há reminiscências dessa origem quando o Japamala torna-se objeto mercantil e passa a circular sob o guarda-chuva de "religião e espiritualidade" nas lojas de departamento.

Quando o doutor, homem da ciência, assume que a presença do Japamala em seu escritório trará calma e paz aos seus pacientes. Ou quando o *site* de vendas descreve-o como "poderosa ferramenta espiritual". Ainda que de "proteção".

No entanto, já não é mais Jamapala. Nesses contextos é ferramenta.
#### Uso Estético

Há também uma relação do Japamala com a noção que se tem de que o exótico é belo e de que o belo é exótico. E, como vindo da Ásia, o Japamala é de alguma forma mágico, diferente, inefável. Tem uma aura e produz uma ambiência.
{: .capitular}

Essa ambiência, instrumentalizada, torna-o colar, decoração, objeto. O Japamala está presente em diversos modelos, cores, materiais, até mesmo sintéticos. E é usado para recobrir mesas de centro, prateleiras, escrivaninhas, mesas de jantar, pescoços, pulsos, tornozelos, vasos e tantos outros lugares que a imaginação do brasileiro conseguir designá-lo.

Por que, afinal, faz-se isso? Ora, pela simples justificativa de que o lugar onde o Japamala, tornado objeto, fica torna-se "bonito".
#### Uso Identitário

Há ainda aqueles que se identificam ou querem ser identificados pela imagem reminescente de monge budista secular através da relação pública com o objeto. O doutor é calmo, o arquiteto tem o estilo viajante, *Boho*, a jovem que usa-o como colar *gosta do budismo* e é sempre paciente.
{: .capitular}

Ser visto como detentor do Japamala é ser visto como alguém que em alguma medida se assemelha às suas qualidades exóticas. Mas na medida, e somente na medida, em que essas qualidades não ameaçam a realidade vigente.

O doutor segue sendo um homem da ciência cujo método é estritamente rigoroso, seu escritório é apenas um ambiente de espera para que se inicie a verdadeira consulta recheada de termos de origem grega "anamnese, diagnóstico". O arquiteto tem o estilo viajante, mas esse é seu estilo, é como é, não implica uma religião específica ou a falta dela. Não pertence a tradição alguma: sua casa é o mundo. E seu escritório o microcosmo harmônico e arquitetado em detalhe para servir ao propósito de vendê-lo como competente ao cliente. Já a jovem não tem preconceitos. Mas não necessariamente frequenta o mosteiro, não pratica o *zazen* e não tem interesse algum e raspar os cabelos.

Não se trata de moralizar tais personagens com sua exposição. São imagens, exemplos. Caricatos e insuficientes por natureza. Se estão aqui é para demonstrar o que revelam: o interesse pelo Japamala está restrito à imagem que transmite ao outro e que se contrói de si. Não implica necessariamente uma pertença à uma comunidade ou a uma tradição. O que não impede que seja um primeiro contato com as mesmas. Daí que não se afirma que isso é certo ou errado, mas um fenômeno corrente neste momento do tempo.
#### Uso Mercantil

Este é, sem dúvida, o uso que viabiliza a maioria dos usos no território geográfico brasileiro, mas não necessariamente os explica. Direta ou indiretamente, o interesse do capital e pelo capital (simbólico ou material) é uma grande motivação para a transformação do Japamala em objeto.
{: .capitular}

Os exemplos: o doutor precisa agregar valor simbólico ao seu trabalho de doutor dando ao paciente uma experiência total de cura, da chegada ao consultório à grafia da receita. Tal movimento tem a intenção de legitimá-lo, e também de agregar valor material ao seu serviço. Mantém os pacientes interessados pela sua consulta e não pela de outro médico.

O Arquiteto faz o mesmo movimento. Legitima-se simbólica e materialmente por meio do uso do Japamala. Com os mesmos objetivos. E a jovem faz com o grupo de pessoas que deseja fazer parte, para afirmar-se, para pertencer. Agrega valor simbólico e cultural à persona social que apresenta.

Por último há ainda a facilidade de encontrar o Japamala em *sites* e lojas a preços acessíveis a grande parte do mercado consumidor brasileiro. Tal facilitação não necessariamente reflete a conversão do Brasil em um país budista.
### Deslocamento Semântico

Nesta seção falarei mais detalhadamente sobre o que até o momento apenas ilustrei a partir dos exemplos. Esta seção tem o objetivo de mitigar interpretações moralizantes ou aglutinação dos conceitos futuros por assimilação a conceitos de outros campos do conhecimento pelo leitor.
{: .capitular}
#### Mudança De Função Percebida

Façamo-nos uma pergunta muito simples: O que Maria perde ao não saber o que é o que está fazendo com o Japamala, ou seja, reenquadrando-o conforme o seu sistema simbólico dominante?
{: .capitular}

Antes da reposta, preciso definir o que é exatamente a ação de "enquadrar" para esta obra. "Enquadramento" é um conceito desenvolvido pelo pesquisador Canadense Erving Goffman, muito utilizado nos estudos em Comunicação Social. E defini-se, de maneira operacional para este contexto, da seguinte maneira: Enquadramento é a forma subjetiva de interpretação conceitual que precede a experiência e determina o comportamento do sujeito dentro de um contexto. Definido em maior detalhe, com seus efeitos e consequências, por Goffman, enquadramento não deve ser confundido com um dispositivo material. Enquadramento não é a máquina de sentido, o suporte ou a mídia. Mas a reação do indivíduo diante de uma extensão mcluhaniana (uma tecnologia ou, simplesmente, um objeto). Para McLuhan, as tecnologias eram extensões do ser humano. Portanto, não as diferenciava, essencialmente, entre eletrônicas (o que se pensa correntemente quando a palavra é mencionada) ou analógicas. Nesse contexto, portanto, uma extensão mcluhaniana é tanto um lápis quando um computador da IBM. E enquadramento é o mecanismo pelo qual a extensão, doravante "Máquina de sentido", opera no nível do indivíduo. Enquadramento é o ponto de contato entre um "sistema simbólico", que será ainda definido e o comportamento concreto.

Por exemplo, as frases clássicas "Eu derrubei a garrafa" e "A garrafa caiu" podem ser utilizadas para enquadrar o mesmo fato, mas não são atitudes subjetivas iguais. Diz-se que há dois enquadramentos diferentes em cada postura refletida pelas frases.

Por fim, respondendo à questão inicial sobre Maria. Há efeitos deletérios e graves. Quando não há sistemas, não há concorrência e não há percepção desses sistemas e dessa concorrência. E, consequentemente, não há noção de que certos sistemas são mais privilegiados em relação a outros. Quando todas essas conjunturas se encontram, não há a possibilidade de acesso aos outros sistemas simbólicos de maior prestígio, pois eles não existem na perceção de Maria. Na medida em que Maria desconhece até mesmo a existência de um sistema simbólico, portanto não sabe que há diferença e concorrência entre eles, Maria perde capacidade de agência sobre a própria vida. Maria, no momento em que observa o Japamala como ameaça a sua estabilidade cognitiva, quando não sabe o que é ou o que está fazendo, perde a oportunidade de dar nome ao que sente.

Maria, o doutor, o arquiteto, a jovem fashionista passam a acreditar que seu destino é estrutura e não sistema. E, então, o seu destino passa a ser a estrutura do sistema. Eles não podem escolher permanecer ou não em um sistema que para eles é invisível e do qual podem ser preteridos e não criadores.
#### Permanência Da Forma Material

Em praticamente todos os casos e usos do Japamala mencionados até aqui, sua forma material permanece a mesma quando re-enquadrado. Não me refiro aqui à forma "pura", platônica, do objeto. Pois essa é modificada a cada nova reinterpretação. O Japamala pode variar em cor, tamanho, material, pode até ter pingentes de cruz e outros símbolos. Trata-se aqui do objeto em si. Já presente na percepção do indivíduo. Concreto. Palpável. Diante dos seus olhos.
{: .capitular}

Esse objeto, mesmo quando re-enquadrado como parte de um sistema simbólico prévio ao indivíduo, não muda de forma. É ainda o mesmo objeto materialmente. Mas seu novo uso, prática, e atitude diante dele, revelam algo mais profundo: o objeto é o mesmo em matéria, mas já não é o mesmo em essência. Como um livro que serve de peso de papel. Ou um prêmio Oscar que serve como aparador de porta.

É verdade que todo objeto e sua matéria estão sujeitos às intempéries do tempo e do uso, portanto mudam. Mas o material, o formato, seguem sendo ligeiramente o mesmo. O suficiente a ponto de identificar sua origem. Esse é o ponto: há sempre uma espécie de remanescente da função primeira daquela máquina de sentido.

As consequências de tudo o que foi mencionado nesta seção são as seguintes: a Máquina de sentido não precisa necessariamente ter alguma espécie de movimento para agir em um sistema simbólico. A Máquina de sentido pode ser um vasto leque de tecnologias. E a percepção do indivíduo é a área na qual a Máquina de sentido atuará.

O que não é Máquina de sentido, então? Objetos da natureza, como uma pedra, uma árvore, não são tecnologia e não pertencem à ordem de extensão do homem, exceto quando instrumentalizados por ele. A Máquina de sentido não é qualquer signo ou objeto, mas a parte material expressa *em larga escala* de um sistema simbólico. Ou seja, A Máquina de sentido é produto de um sistema simbólico e precisa atender a estes requisitos: parte material e expressão em larga escala. Larga escala varia conforme a comunidade, mas em tempos pós-industriais, larga escala é tudo aquilo que alcança um replicabilidade técnica ou ritualística e é de fato replicado. Ou seja, que passa pelo processo  industrial. O Davi, de Michelangelo, não é uma Máquina de sentido, mas os *souvenirs* baseados nele são.
### Ruptura Entre Origem E Prática Atual

Tal ruptura é proporcionada pela Máquina de sentido. Mas só é ruptura de fato quando permite ao indivíduo a compreensão de que há ali uma fronteira de sistemas materializado pela Máquina e representado pela estranheza diante dela. A contraparte dessa ruptura é o que chamo "Homeostase". Para definir homeostase: É quase o mesmo que equilíbrio, mas é um equilíbrio ativamente buscado pela percepção do indivíduo e pelos sistemas em geral.
{: .capitular}

A busca pela homeostase significa a sobrevivência do sistema no estado em que se encontra, ou seja, a perpetuação de sua matriz: sua replicação torna-se possível. Será mencionado mais à frente que o indivíduo não suportaria a presença "total" da Máquina de sentido, ou ao menos da tecnologia da qual foi derivada a Máquina. Há ainda uma dimensão cosmológica do que chamo homeostase. Eliade, teórico das religiões, dirá: "Numa palavra, sejam quais forem as dimensões do espaço que lhe é familiar e no qual ele se sente situado - seu país, sua cidade, sua aldeia, sua casa - o homem religioso experimenta a necessidade de existir sempre num mundo total e organizado." (Eliade, p. 43.) Ou seja, o ser humano não busca apenas o equilíbrio: seu espírito deseja o *cosmos*, a ordem. E, portanto, a homeostase sistêmica é apenas uma forma de descrever esse fenômeno em nível sistêmico e semiológico.

Em outras palavras, o mecanismo que opera na percepção do indivíduo para re-enquadrar a Máquina conforme o seu sistema simbólico não pode ter uma implicação moral direta. Pois é um mecanismo estrutural do sistema. No entanto, é necessário que se faça uma estratificação de níveis nos quais tal mecanismo pode ocorrer e sua implicação, não moral, mas ética. É essa diferenciação de níveis que invalida a ideia de que "conhecer o mecanismo" não seria suficiente. São eles: Intra-indivíduo (percepção individual), institucional (percepção coletiva enquadrada) e inter-institucional (mecanismo como projeto político de hegemonia). Cada um deles implica uma postura ética diferente. Tratarei disso em detalhe no próximo capítulo. Agora é chegada a hora de desvelar o mecanismo e seu funcionamento.
### Emergência Do Conceito

Nesta seção tratarei do conceito central para a compreensão desta obra: Purificação Simbólica. Antes de qualquer prosa sobre o mecanismo que Purificação simbólica é, é necessário definir o que não é o conceito: Purificação simbólica não denota "sacralização", consagração ritual, ou purificação cultural normativa. O termo não deve ser confundido com noções de Eliade sobre consagração tampouco com debates contemporâneos sobre "Apropriação cultural". O conceito de "Purificação simbólica" opera estritamente em nível epistemológico. Consagração, em Eliade, torna algo sagrado. Apropriação cultural disputa posse simbólica. Já Purificação simbólica suspende pressupostos interpretativos.
{: .capitular}

Tenho usado, ao longo de todo o capítulo, os conceitos "Sistema" e "Individuo". Definirei cada um com detalhe apropriado nos seguintes capítulos, mas, ao apresentar o conceito de Purificação e suas implicações, fica imperioso mencionar isso: sistema e indivíduo não são a mesma coisa e não equivalem a completude do que significa "Ser Humano". O ser humano é, por definição, indefinível. Especialmente dentro do contexto desta obra. Pois esta obra considera a dimensão do sagrado e do espírito. Experiência religiosa e contato com o sagrado são características humanas cuja matéria é por si inexplicável, incompreensível. Eliade bem postulou e deixou o sagrado equivalente ao *Ganz andere*. Portanto, se o ser humano é capaz dessa experiência e a compreende, ele também não é completamente definível, descritível, compreensível. O que esta obra faz, portanto, é operacionaliza-lo. Torna o humano um indivíduo. Que é uma modulação do humano, uma matriz, um *mainframe* que agora o torna compreensível. O ser humano não é necessariamente um sistema, mas um indivíduo é como uma espécie de sistema dotado de consciência de si, um sistema especial, autônomo e, redundantemente, individual. É como o humano se apresenta no tempo pós-secular. Mas ele pode ser comunidade, sujeito, plebeu, monarca, povo, cidadão, devoto. E muitas outras coisas conforme o tempo, a história, e o espírito.

A partir dessa ótica, é possível compreender o indivíduo como um sistema em contato com outros sistemas. Um sistema que outros sistemas habitam e que habita outros sistemas. Uma espécie de nó. Um ponto de intersecção que é, devido a qualidade relativamente consciente, o "centro de controle" dessas intersecções. Um organismo pode ser compreendido como um sistema, na medida em que suas partes estabelecem relações para determinado contexto, mas a substância da qual é feito não está limitada a esse enquadramento. Desse modo, não é o interesse deste trabalho esgotar o sentido de "Humano", pois isso além de impossível é temerário e redutivo. Por fim, como propriedade do indivíduo, a purificação simbólica é executada. Como propriedade do sistema, ele fornece categorias (valores) para que ela seja operacional, executável. Tal distinção é importante e necessária.

Ainda. Há o risco de conclusões tautológicas sobre a relação sistema-indivíduo-mecanismo. "O sistema existe por que parece natural e se parece natural é sistema". O erro nesse raciocínio é assumir que o sistema não existe se o indivíduo não o percebe. No entanto, o sistema está sempre lá. Ao percebê-lo o indivíduo constata sua existência. Há, então três níveis distintos: o sistema que existe, o mecanismo que produz naturalidade do sistema e o reconhecimento individual de que o sistema existe. Como identificar um sistema simbólico, então? Ele tem replicabilidade social (é reconhecido por mais de um indivíduo como tal), coerção normativa observável (ele tenta definir os próprios limites de pertencimento e não pertencimento), penalidade por desvio (aqui também há três níveis de penalidade de indivíduo a instituição a inter-institucional. Em ordem: sentimento de culpa ou desorientação, exclusão do sistema por parte dos que nele estão e sanções em todos os níveis anteriores mais o não reconhecimento em relação às instituições como parte do sistema). As questões que ficam sobre o que é um sistema e como ele se relaciona com os símbolos nesta obra serão tratadas mais à frente, em capítulo próprio.

O que é, então, finalmente, Purificação Simbólica? Trata-se de um mecanismo pelo qual um sistema simbólico dominante sobrescreve a espiritualidade ou o significado de objetos, práticas ou pessoas de outros sistemas, apresentando-se a si mesmo como neutro, natural ou vazio de sentido. Ora, não é difícil observar a partir do exemplo do objeto budista sua reinscrição em diversos sistemas. Ora funciona como objeto decorativo, ora como objeto ritual, ora como adorno corporal. Todos esses usos apresentam o Japamala não pela origem ou pela história do que é, poucas vezes pelo seu nome de origem também, mas pela definição que agora carrega dentro do sistema ao qual foi inscrito. O Japamala não é mais um Japamala, mas um "colar" que vem a ser budista. Isso quando vem a ser budista e não somente um colar "diferente".

É importante observar que tal mecanismo não ocorre necessariamente em todos os indivíduos presentes em um espaço, região ou território: Há budistas no Brasil. Que certamente reconheceriam o Japamala pela função original e não pelas funções atribuídas por similitude. A formalização que o mecanismo de Purificação promove somente é partilhada pelos indivíduos que habitam o mesmo sistema simbólico. A partilha de mesmo sistema não é também absolutamente necessária para que o mecanismo ocorra. Na verdade, cada brasileiro é em si um conjunto de sistemas simbólicos disputados. Haverá sempre uma hierarquia dentro desses sistemas que auxiliará a percepção do indivíduo a orientar-se. E é a partir dessa hierarquia que o indivíduo perceberá "valor" da máquina de sentido, o objeto, e também dos sistemas simbólicos que o habitam. Seu impulso será reprogramar o objeto com a similitude de qualquer outro que houver dentro do sistema simbólico percebido por ele como de maior prestígio ou dominância.

Exemplifico: uma jovem adolescente aficionada em moda reconhecerá no Japamala diversos usos e funções, decoração, adorno e até mesmo objeto devocional, cada um representando um sistema simbólico diferente que a jovem habita. No entanto, será aquele de maior prestígio ou dominância que vencerá e logo a jovem estará reconhecendo o Japamala como um colar e atribuindo-lhe função conforme.

Tal definição pode e é provável que mude conforme o contexto, essa é a lógica de um sistema: ele muda conforme suas relações mudam. No entanto, aqueles de maior prestígio ou dominância tendem a ter certa estabilidade em suas relações. A jovem pode usá-lo como colar, se for católica, por exemplo, mas dificilmente o verá como objeto devocional. Exceto se confundi-lo com uma variação de um terço, o que é em si o mecanismo operando novamente.

Agora, quando não há purificação simbólica? Quando o sistema não é estratificado. Quando é homogêneo. Quando uma máquina de sentido é produzida e operacionalizada pelo próprio sistema. Um católico compra um terço, produzido ou não por católicos, e reza com ele. Não há purificação. Não há estranhamento. Não há fratura no sistema. Há continuidade ritual, reprodução interna e reforço identitário.

Surge então uma questão: Como reconhecer o sistema simbólico de maior dominância e/ou prestígio no estrato subjetivo individual, social e político? Essa questão se adianta e será tratada no capítulo seguinte.

Há na gênese do brasileiro uma propensão história e cultural ao desenvolvimento da linguagem em sistemas estratificados. Não se afirma que não haja linguagem em outras culturas, afirma-se no entanto que o modo pelo qual a linguagem é estruturada é outro: desde sua emergência, o estrato brasileiro é um conjunto disputado e heterogêneo de sistemas simbólicos díspares. É nessa gênese de marco zero que o mecanismo da Purificação passará a atuar. E o indivíduo agirá conforme o sistema simbólico que primeiro o integrar. Consciente ou inconscientemente.

A partir daí haverá uma cascata de Purificações extrínsecas e intrínsecas. Desde a semelhança da criança com o avô "Veja, o Enzo tem as pernas do meu pai... Será bom atacante!" até "Eu não sou mais criança, mãe. Não vou usar esse corte de cabelo de neném!". No primeiro caso, Enzo é purificado: antes pareça seu avô do que qualquer outro indivíduo. No segundo, Enzo purifica: o novo corte de cabelo que mamãe não aprova pertence ao sistema simbólico de quem não é neném e portanto pode ser integrado ao meu sistema simbólico.

Embora Enzo não saiba o que é exatamente "não ser neném" ou "adulto". Assimila o novo corte de cabelo adaptando-o aos valores que já conhece: opondo-o à figura do neném. São esses valores, herdados do sistema primeiro no marco zero da linguagem durante o desenvolvimento, que servem de base estrutural para o julgamento de qualquer outra espécie de sistema simbólico que vir a encontrar.

Tal mecanismo nem sempre, e quase nunca, é operado de maneira consciente. O indivíduo não sabe que está fazendo. Tem como percepção o mecanismo como sua opinião ou apenas um fato. Um dado da natureza. Natural, não interpretado.

Enzo não diz "Mãe, interpreto esse corte de cabelo como um sinal de infantilização incompatível com os valores dos sistemas simbólicos com os quais me identifico e aos quais quero pertencer. Assumo isso como uma postura, não como um fato. Pode ser que um adulto também o utilize e não torne-se neném por isso". Enzo afirma categoricamente "esse corte é de neném" ponto final.

Enzo é uma criança, naturalmente, e quando está diante de um mágico profissional acredita testemunhar os poderes mágicos do mesmo. O coelho literalmente saiu da cartola que estava vazia. Enzo não percebe que havia já um mecanismo de ocultação do coelho e *quando perceber cessarão os poderes do mágico*. Tal atitude não é diferente para Maria, a personagem que encarna o estrato de maior quantidade de pessoas no território brasileiro. Maria tem entre 35 e 40 anos de idade. Mas não abandona a atitude metodológica de Enzo diante dos sistemas simbólicos, que lhe são invisíveis. A primeira atitude "acreditar testemunhar os poderes do mágico" é o que chamo aqui de "crença inocente" e a segunda atitude, quando os poderes do mágico cessam, "crença reflexiva".

Barthes descreve em certa medida o que chamei de "crença inocente" ao utilizar o termo "naturalização". O que difere os conceitos é que, para Barthes, a naturalização se dá, dentro de seu sistema semiológico, a partir da força intencionada do mito. Ou seja, do projeto do emissor. Que o faz de forma consciente. É assim que opera: Ele busca significantes (a essência) para o significado (a forma). Situação na qual a forma precede a essência. Pouco importa o objeto, desde que ele signifique o mito. Em outras palavras: quero um colar, pouco importa se é budista, umbandista, judeu ou católico.

A crença inocente, ao contrário, não vê necessariamente o indivíduo que opera o mecanismo como motivado a fazê-lo de forma consciente do sistema simbólico. Em outras palavras, o indivíduo não age conforme um programa deliberado.

Para Barthes, tratar o Japamala como colar é um projeto pequeno-burguês de dominação contra os budistas. Esta obra não exclui tal possibilidade, mas lhe dá também outras dimensões: usar o Japamala como colar é, em nível subjetivo, uma estratégia defensiva de estabilização cognitiva. Os sistemas simbólicos que habitam o indivíduo não seriam capazes de suportar a cascata de contradições e implicações decorrentes da aura do Japamala percebido tal qual o é no sistema simbólico do qual provém sem transformar-se em sistemas outros, desconexos e mesmo disfuncionais para o contexto em que operam. As relações são o que dá coesão, coerência e estabilidade ao sistema. O indivíduo, na presença "total" do Japamala, teria seus sistemas simbólicos alterados radicalmente em curto espaço de tempo. E um sistema cujas relações entre suas partes muda é já um novo sistema. O indivíduo, que se orienta pelos sistemas que nele habitam, colapsaria junto a eles na presença de qualquer artefato diverso desses mesmos sistemas.

Barthes afirma que a naturalização (mecanismo correlato, mas não idêntico à Purificação) é um projeto deliberado de dominação do emissor e a solução do dominado para tal problema seria desmontar o resultado do projeto, que ele chama "mitificação", destruir o mito barthesiano. No entanto, ao perceber a Purificação simbólica como mecanismo do receptor a solução para o problema que se impõe, quando em nível político, é torná-la consciente. Pois um é escolha e o outro é condição passível de manejo.
#### Condições De Ocorrência

Na seção em que falei sobre a emergência do conceito central para esta obra, tratei também de algumas condições para que o mecanismo ocorresse. Vou agora detalhar estas condições. Antes de qualquer coisa é preciso reforçar: A Purificação Simbólica opera em nível epistemológico. E ocorre na fronteira entre sistemas simbólicos, que definirei com mais detalhe na seção "limites do conceito". É uma prevenção de uma fratura cognitiva e, portanto, acontece nos sistemas simbólicos já assimilados pelo indivíduo.
{: .capitular}

 Hoje, na contemporaneidade, a Purificação Simbólica ocorre nos estratos dos sistemas simbólicos brasileiros em uma quantidade de situações admirável. Refiro-me a "hoje", pois o mecanismo é limitado pela história: pode evoluir, mudar, nascer e até mesmo deixar de ocorrer. Assunto que também tratarei com mais detalhe na seção "limites do conceito".
 
 Retomando. Para que a purificação simbólica ocorra é necessário que haja sistemas simbólicos díspares, no qual um deles será dominante, por já estar assimilado, e contato entre esses sistemas, na presença de uma Máquina de sentido.
 
 A Purificação Simbólica pressupõe a existência de Sistemas Simbólicos. E para que saibamos que um sistema simbólico existe é preciso reconhecê-lo. No entanto, o indivíduo que desconhece o mecanismo desconhece o sistema como tal, embora possa reconhecer de alguma forma parte de sua natureza estrutural, mas não sua natureza sistêmica. Ou seja, o sistema está lá. Existe antes da percepção do indivíduo. O indivíduo enxerga "isso aqui é o teatro", mas desconhece a natureza da fronteira entre o que é e o que não é teatro. Para ele, o que "não é o teatro" é uma implicação natural do teatro que ele conhece, ou seja, do sistema que têm assimilado. Ou seja, se "isso é teatro" aquilo outro "não pode ser teatro". É natural.
 
 Outro pressuposto é que haja no mínimo dois sistemas simbólicos e que sejam díspares. A Purificação se manifestará na fronteira entre esses sistemas. Ou seja, quando o indivíduo classifica o que é o teatro por exclusão, toda a parte negativa não é teatro. Em certa medida, esticando a situação ao limite, se o teatro for apenas a *comedia del arte*, o resto do universo não será teatro, pois tudo aquilo que não caracterizar a *comedia del arte* não será teatro.
 
 Pode-se identificar, no entanto, muitas outras formas de teatro e artes cênicas. Mas, para o exemplo do indivíduo que consideraria o Teatro apenas a *comedia del arte*, essas artes cênicas seriam qualquer outra coisa. Poderíamos circunscrever a disparidade em dois sistemas diferentes: "A *comedia del arte* não é o carnaval". Esse indivíduo, em uma viagem talvez, pode visitar um baile de carnaval e encontrar uma máscara do Brás (Uma máquina de sentido). O sistema *comedia del arte* por ser o sistema já assimilado é dominante para esse indivíduo e agora encontramos a última condição para que a purificação ocorra.
 
 O encontro entre dois sistemas no objeto de uma máquina de sentido. O indivíduo da *comedia del arte* localizará logo no baile as máscaras e os motivos do que considera a *comedia del arte*. E, ao agregar tais máscaras e motivos em seu sistema "comediadelartiano", a máscara do Brás já não será mais carnaval.
 
 As máscaras e fantasias de carnaval, embora muitas vezes confeccionadas de maneira artesanal, são em si, em ato e intenção, uma máquina replicável. Não a fantasia em si, mas o fantasiar-se para o carnaval: o produzir uma fantasia. Uma máscara do Brás, uma rua de comércio de São Paulo, torna-se então uma máquina de sentido por representar sozinha um símbolo do carnaval. Que, se re-introduzida e purificada, tornar-se-á uma máscara somente. Mais uma, dentre tantas outras, no arsenal da *Comedia del arte*. O que era carnaval, torna-se uma máscara carnavalesca. Uma máscara que foi comprada no carnaval brasileiro. Ou apenas uma máscara.
#### Efeitos Observáveis

Os efeitos da purificação simbólica são muitos. O mais observável, em nível individual, é a percepção de que não é possível orientar-se sem que o mecanismo ocorra. Mas, ao ocorrer, o mecanismo apaga vestígios de uma possível fratura em um sistema estanque. Ou seja, que já não produz novos sentidos. Essa é a causa do principal efeito observável: a aparente perda de sentido.

O indivíduo pós-secular brasileiro não encontra mais contato com aquilo que proporciona um sentido, comunitário, geral e individual: O sagrado, nos termos de Eliade, *Ganz andere*. Hoje, esse indivíduo está fragmentado em diversos sistemas que habita e que nele habitam. Ao hierarquizar tais sistemas e buscar organizá-los de modo a privilegiar aquele que reforça a sua identidade, o indivíduo encontra-se auto-referenciado.

O diálogo com o diferente não é mais possível, pois o diferente é uma ameaça a ser neutralizada, colonizada, purificada e re-introduzida no sistema com a forma caricata e redutora que lhe cabe ali. E não um "irmão" que faz parte do seu cosmos, onde a ordem e o sentido estão estabelecidos, mas admite o diferente com qualidades manejáveis e deveras mais profundas do que o indivíduo pós-secular é capaz de tolerar.

O indivíduo busca o sentido, mas ao afirmar-se, este lhe escapa pelos dedos. E ele recorre ao sistema que corresponde a ele como o grande gerador de sentido: A religião institucional. Mas esta nada mais é do que, diferente de outrora, mais um sistema simbólico possível para encontrar o *ganz andere* a partir da experiência religiosa. Não o único. E, ao afirmar-se, a religião institucional, opera, em nível inter-sistêmico, político, como um grande reprodutor do mecanismo de purificação simbólica. Que o fixa em cada indivíduo do estrato que é compreendido por ela. Mas o indivíduo não é mais unicamente religioso. Ele é atravessado por uma multiplicidade de sistemas que precisam encontrar a homeostase: ele é, ao mesmo tempo, fiel, secular, colega de trabalho, eleitor, pai.

Cada um dos sistemas que essas palavras implicam podem fornece-lhe a experiência religiosa que lhe devolveria o sentido. Mas nenhuma, hoje, o faria em absoluto. E o indivíduo se desmancha na profusão de sistemas que reclamam parte da unicidade do indivíduo em um tempo que já não mais é uno, e reclamam a própria legitimidade de sistema único possível. O indivíduo fica atomizado: solitário e desorientado. Reclama o sentido à Ciência, à Religião, à Arte e à Máquina. Fanatiza-se. Encontra no outro o bode expiatório para a perda de sentido do mundo. Pois o outro não pode ser mais do que a caricatura tolerável que o sistema de maior prestígio fez dele. As relações se tornam manejáveis, quantificáveis, comerciáveis, mas não relacionáveis, exceto se em um quadro de *networking* dos *stakeholders* da empresa, da família ou do indivíduo.

E aqui revelo uma manobra brusca: talvez o leitor tenha detectado a variação de escala nos efeitos observáveis. Passamos de indivíduo à instituição à política. E afirmamos que o mecanismo é incontornável em uma situação de estratificação de sistemas simbólicos. Pode parecer nesse momento que o que está sendo discutido se fecha sobre si e não há saída. No entanto, há posturas metodológicas possíveis, alternativas. Também há limites para o mecanismo e para o conceito. Abordo alguns desses limites a seguir.

#### Limites do Conceito

Começo pela questão ética. Devido ao fato do mecanismo ser operado pelo indivíduo em uma máquina de sentido como uma espécie de reflexo, uma estratégia para defender sua homeostase sistêmica, não se pode afirmar que é realizado em nível individual com intenção. Também por isso, não se pode afirmar que é necessariamente malicioso. No entanto, o mecanismo da purificação alcança ainda dois níveis além do indivíduo: o social (instituições) e o político (inter-institucional). Nesses dois níveis a situação ética deve ser avaliada. Pois o mecanismo pode tornar-se projeto consciente de um grupo de pessoas, e portanto replicável com intenção definida: sobrescrever outro sistema simbólico. A diferença entre níveis está na capacidade auto-reflexiva que as instituições possuem quando comportam uma variedade de indivíduos. Tais indivíduos podem raciocinar e verificar os programas institucionais conforme seus objetivos. O mecanismo pode não ser evitado, mas pode ser direcionado e motivado a situações e um sistema simbólico alvo. Por exemplo: Nas comunidades do Rio de Janeiro há um fenômeno no qual algumas são comandadas por entidades estranhas à legalidade. Algumas delas declaram-se como pertencentes a uma religião (sistema simbólico) específica, como a evangélica, e isso tem implicações diversas. Dentre elas, o apagamento e, muitas vezes, a destruição de tudo que remeta a outras religiões. Quando a destruição e o apagamento não são possíveis, purifica-se.
{: .capitular}

Outra limitação para o conceito é a limitação histórica. O indivíduo anterior à secularização desconhecia uma postura profana do mundo. Desconhecia a realidade estritamente objetiva motivada pela ciência e a economia. Em tempos anteriores, um sistema simbólico era claramente o único a fazer o que se propunha. A religião, o Estado. Hoje, a religião institucional é um exemplo muito propício. Em outros tempos era caso de nascimento, destino, não se imaginava escolher uma religião e a mudança de tradição religiosa, quando possível, implicava um rompimento dramático, sério, muitas vezes irreversível com o sistema simbólico da religião anterior. Hoje, pode-se escolher a religião conforme a impressão que se tem da igreja e do culto. Não é estranho no Brasil ir a um culto evangélico pela manhã e visitar esporadicamente um terreiro de umbanda ou candomblé pela tarde. Se a religião a qual o indivíduo faz parte já não o atrai, isso não implica necessariamente uma crise de fé e um caminho de evolução e fortalecimento para a mesma, basta que se visite o templo da religião do vizinho. Hoje, a religião institucional não se difere de uma marca de margarina em uma prateleira de supermercado: escolhe-se aquela que o atrai, cujo sabor e consistência agradam o paladar do indivíduo.
1. Devido a essa profusão de sistemas concorrentes no território, o indivíduo brasileiro sofisticou o mecanismo de purificação. Que passou a se generalizar depois da atitude pós-secular. Eis a razão para o limite histórico.
2. Outros limites estão relacionados à definição, finalmente, do que são sistemas simbólicos. Faço primeiro a definição de sistema, conforme Meadows, pesquisadora do MIT, sistemas são "[...] um conjunto *interconectado* de elementos organizados coerentemente de modo a obter alguma coisa." (Meadows, p. 25. Grifo meu). Uma vez que Donella Meadows define como não sistema tudo aquilo que não tem *correlação* explícita ou implícita (grãos de areia), a definição de Barthes para sistema semiológico é certeira. Abaixo, a descrição perfeita do que é um sistema semiológico.

> "[...] pois o que se apreende não é absolutamente um termo, um após o outro, mas a *correlação* que os une: Temos, portanto, o significante, o significado e o signo, que é o total associativo dos dois primeiros termos." Barthes, Mitologias, p. 203. Grifo meu.


Quando Meadows afirma que um sistema é um conjunto interconectado de elementos e Barthes afirma que um sistema semiológico está na apreensão da correlação entre signo, significado e significante, temos que a correlação é a chave que liga os dois conceitos. Produzindo assim a definição de Sistema simbólico. De maneira formal, o sistema simbólico terá características tanto sistêmicas quanto semiológicas: Estrutura não estanque e organizada de signos, práticas e valores que produz coerência e sentido para um grupo e que opera com máxima eficácia quando percebida como natural pelos seus membros. Um sistema simbólico precisa respeitar a quatro critérios: replicabilidade social, coerção normativa observável, penalidade por desvio e estabilidade histórica.

Ou seja, para definir o que é e o que não é um sistema simbólico a *coerência* de suas relações é muito importante. E os critérios para a identificação da coerência de um sistema simbólico está descrito acima. Exemplifico: replicabilidade social pode ser quando Maria ensina aos filhos os bons modos de comer à mesa. Coerção normativa observável pode ser a obrigação de aprender tais modos para participar do sistema simbólico da refeição, especialmente a social, naquele grupo familiar. Penalidade por desvio pode ser o que normalmente se caracteriza pela vergonha de Maria ao falhar em ensinar esses bons modos, mas também pode ser uma penalidade física (Umas palmadas não são atípicas em alguns contextos), condicional ("Só vai sair depois que comer") ou mesmo social (Não vai ser convidada a visitar os parentes, pois os filhos não tem "educação"). Por último, estabilidade histórica: os bons modos à mesa existem já há quanto tempo? Come-se com garfo e faca no Brasil há quantas gerações em algumas famílias?

Há ainda uma limitação do conceito em relação a extensão do mesmo. Mas isso será tratado em profundidade na seção "extensibilidade do mecanismo" mais à frente. Agora é o momento de tratar da estrutura do mesmo.
### Estrutura Da Purificação Simbólica

Pode-se objetar que o mecanismo muda conforme cada caso e, por não ser estável, não se caracteriza como mecanismo. No entanto, o mecanismo é o mesmo; o que muda é o material sobre o qual opera. É estável, pois, a matéria de operação é modulada pelo valor que o sistema de maior dominância imprime na máquina de sentido do outro sistema simbólico. Isso para explicar que a forma do mecanismo é estável, mas a substância sobre a qual o mecanismo opera é variável. De modo que os valores que ele sobrescreve adaptam-se conforme os valores do sistema a ser sobrescrito.
{: .capitular}

Quando à estrutura do mecanismo, há dois níveis com respectivos sub-níveis. (1) O nível de ocorrência. (2) O modo de ocorrência. Começo pelo nível de ocorrência.

Há três níveis muito claros de serem identificados: (1) o nível do indivíduo, o mais elementar e o que possibilita os outros níveis. Pois tudo ocorre a partir da percepção dos indivíduos. São eles quem operam os mecanismos. (2) O nível social, representado por uma instituição: um corpo de indivíduos que pertencem e compartilham o mesmo enquadramento do mundo. Tal nível é identificado a partir da estrutura sistêmica e, especialmente pelos critérios de identificação e coerência dos sistemas simbólicos. (3) O nível inter-sistêmico. Aqui já não se fala diretamente da relação de indivíduos, mas de instituições, que se utilizarão de indivíduos para a produção e replicação de máquinas de sentido a fim de reproduzir o mecanismo de purificação com o objetivo expresso ou não expresso de sobrescrever sistemas simbólicos díspares.

Na verdade, o que Barthes atribui à burguesia como projeto (a mitificação) pode ser colocado como categoria dentro do mecanismo de Purificação Simbólica quando processo coletivo, inter-institucional. É quando a Purificação Simbólica atinge o nível inter-institucional e político que ela pode receber status equivalente ao da mitificação burguesa. Sendo, no entanto, mecanismo não necessariamente burguês, mas do indivíduo brasileiro. No entanto, o mecanismo pode assumir o caráter de qualquer ideologia dentro do sistema de maior prestígio social para aquela comunidade. Por exemplo, se a instituição é de pintores dadaístas, o mecanismo tornado projeto institucional refletirá a ideologia dadaísta. Mas se a instituição for de freiras franciscanas, os valores franciscanos serão refletidos pelo mesmo mecanismo. Não havendo óbice algum para a interação, competição e purificação simbólica nas fronteiras entre os sistemas simbólicos que essas instituições habitam. Ainda, o mecanismo reflete, independentemente da ideologia, quando projeto político, uma atitude diante de um sistema outro e tal atitude pode se caracterizar como algo de colonizadora. Tal implicação será detalhada em capítulo seguinte, pois é deveras importante para esta obra. Há, portanto, três níveis de ocorrência da Purificação simbólica: (1) Intra-indivíduo, sua percepção em relação à máquina de sentido. (2) Institucional, social, a percepção coletiva enquadrada pela instituição. (3) inter-institucional, política, o mecanismo como projeto de busca por hegemonia.

Agora descreverei como o mecanismo ocorre. A partir do (1) apagamento da origem. O japamala tem sua origem budista apagada. O indivíduo que opera o mecanismo não vê o japamala mais como budista, mas como qualquer outra coisa que se assemelhe ao seu sistema de maior dominância. O japamala perde profundidade histórica. De onde veio e porque foi confeccionado não importa, desde que sirva ao propósito do indivíduo que purifica-o. Para que o apagamento seja possível, é necessário que o japamala seja despido de toda carga simbólica, especialmente espiritual, e, consequentemente, expurgado de tudo aquilo que não for considerado útil ao novo sistema.

A partir daí haverá a (2) reinscrição no sistema simbólico de maior dominância para a percepção do indivíduo. O japamala agora torna-se "decoração zen". A reinscrição em novo sistema acontece dessa mesma forma: o máquina de sentido é transformada em caricatura de algo semelhante ao sistema que irá integrar e a partir daí é hierarquizada a partir dos valores desse mesmo sistema. Quando hierarquizada, reflete a persistência dos signos de origem da máquina de sentido, mas já neutralizados por caberem em um nível hierárquico com papel definido no novo sistema.

Ainda haverá a (3) naturalização do novo regime simbólico. O Japamala será exótico, bonito. Mas não será mais o japamala. Muitas vezes, perdendo todos os signos aparentes de sua origem, como o nome. E é replicado no sistema com sua nova colocação. Para participar da nova hierarquia, ignora-se a história do objeto e a caricatura passa a ser a regra. 

Segue-se para a (4) invisibilização. Como a caricatura já tem um lugar no sistema, faz-se parecer que a máquina de sentido purificada sempre esteve ali como parte do sistema.

Como consequência da invisibilização, ocorre a (5) neutralização da máquina de sentido. Em outras palavras, o japamala não é mais budista, mas um objeto qualquer, um dado do mundo natural que é, naturalmente, dotado de objetos. Objetos ordinários, comuns.

Por último, a (6) legitimação. A máquina de sentido é reconhecida e utilizada conforme os valores do novo sistema sem qualquer tipo de constrangimento ou perturbação do mesmo. Ela foi purificada simbolicamente.

O mecanismo, portanto, apaga, re-inscreve, naturaliza, invisibiliza, neutraliza e legitima. O que varia é o material sobre o qual opera: o conteúdo simbólico de cada máquina de sentido, em cada contexto. Tal processo será, doravante, resumido pelo termo "sobrescrever".
### Generalização Controlada

Após a apresentação do mecanismo e suas características. Descreverei um teste de estresse do conceito a fim de compreender melhor seus limites. Retomarei pontos anteriores com maior detalhe.
{: .capitular}
#### Outros Tipos Possíveis De Objetos

O que determina o critério de seleção para uma Máquina de sentido tornar-se apta ao método abdutivo? Uma vez que não há "sistema puro", no sentido de sistema cuja fronteira não entra em contato com outro sistema simbólico. A resposta está na sensação de estranhamento. A necessidade de tentar explicar a si ou a outrem o que é aquela máquina de sentido é um indício de que aquilo não pertence ao sistema simbólico de maior dominância do indivíduo. Portanto, o estranhamento é o indício necessário e suficiente para a reprodução do método abdutivo. Pois é o estranhamento que possibilita a fratura na percepção. E, consequentemente, a consciência de que o sistema simbólico não só existe, mas que há dois deles e que são diferentes e concorrente entre si na percepção do individuo. Respeitadas essas condições, pode-se afirmar que qualquer coisa pode ser uma máquina de sentido apta ao método e passível de purificação simbólica.
{: .capitular}

Como exemplo, tomarei do próprio livro de Barthes, uma evidência incontornável de que o mecanismo foi detectado por ele, mas ignorado. Como um banhista que devolve uma esmeralda ao rio por ver ali somente uma pedra qualquer. Tal evidência não comprova a existência do mecanismo no território francês, mas torna-se um correlato plausível que possibilita a investigação de outras máquinas de sentido.

A certa altura do livro de Mitologias (pg. 166), o ensaio sobre "O Continente Perdido", Barthes observa exatamente um mecanismo correlato ao que eu chamo de Purificação Simbólica, no entanto, não nomeia o mecanismo, descreve-o e não parece consciente de que seja um mecanismo. Chega mesmo a dizer que as relações simbólicas são estratificadas: há uma categoria superior (logo, uma inferior):

> "[...]É certo que são sempre as "formas" que acusam com mais perfeição a identidade das religiões; mas, aqui, esta identidade, em vez de desmascará-las, as entroniza e lança crédito de uma catolicidade superior.


Já na página 167, Barthes descreve o mecanismo operando. No entanto, não dá a noção estatigráfica de sistemas simbólicos concorrentes. Ele sugere apenas uma atitude moral por parte do indivíduo. Não explica o seu funcionamento, suas causas, tampouco suas consequências. Aqui, Barthes parece ter tropeçado em uma evidência incontornável, mas reserva-lhe uma condição de ensaio isolado. Barthes chega mesmo a falar de inocência.

> "Em suma, o exotismo revela perfeitamente a sua justificação profunda, que consiste em negar qualquer situação da História. *Vacina-se* infalivelmente a realidade oriental contra qualquer conteúdo de responsabilidade, afetando-a com alguns bons signos indígenas. Um pouco de "situação", o mais superficial possível, fornece um álibi necessário e dispensa uma situação mais profunda. Em face do estrangeiro, a Ordem apresenta apenas dois tipos de comportamentos, ambos *mutilantes*: reconhece-a como um teatro de marionetes ou considera-a o mais puro reflexo do Ocidente, tirando-lhe assim toda a força. De qualquer modo, o essencial é retirar-lhe a história. Vê-se, pois, que as "belas imagens" de *O Continente Perdido* não são absolutamente inocentes: não se pode, inocentemente, perder o continente que se reencontrou em Bandoeng." Barthes, Mitologias, p. 167. Grifos meus.


Algo que difere a percepção de Barthes sobre o mecanismo descrito e o torna correlato, mas não idêntico, é que Barthes descreve o mecanismo como uma atitude moral do francês embebido da mitologia burguesa. Isso tem diversas implicações contrárias ao mecanismo da Purificação. Uma delas é que o mitólogo, categoria descrita por Barthes, tem a função de destruir o mito do qual está isolado, mas o indivíduo que pensa reflexivamente, como será ainda proposto em detalhe, está dentro do sistema simbólico que descreve. Uma segunda percepção sobre o mecanismo é que Barthes entende o mito pequeno-burguês como algo estrutural da França. Tanto que deve ser destruído, pois não é possível modificá-lo. A diferença entre estrutura e sistema está aí: um deles é estático o outro evolui. É como se a estrutura fosse a fotografia do sistema.

Por fim, é preciso que haja estranhamento do objeto. O momento de estranhamento é a fratura que expõe o sistema simbólico a que se pertence como tal. O que não ocorre em Barthes. Veja, então, porque Barthes vê mecanismo correlato e não o nomeia: Ao ilustrar a estrutura do mito a partir do método abdutivo, Barthes lança mão de mecanismos que lhe parecem menores diante da grande importância do desmonte da mitologia pequeno-burguesa. O que é essencial para seu livro. Não nomeia porque não assume a posição de dentro do sistema que aponta. Em suma, Barthes não percebe que ao afirmar que o sistema é estrutura, não se vê dentro da mesma. Ele é apenas o analista de um objeto exterior. Para Barthes, a estrutura tem valor inferior à importância de destruí-la. É como se ele dissesse: Ora, para que compreender como algo que produz efeito deletério funciona? Devemos destruir somente.

Por fim, caracteriza-se como essencial a necessidade de explicar o objeto, compreendê-lo para que possa-se então estranhá-lo, identificar nele a operação da purificação (ou aplicar o método abdutivo). Essas características mais aquelas que definem uma máquina de sentido são condicionais e necessárias para que o mecanismo ocorra e para que o objeto seja elegível à análise.

#### Extensibilidade Do Mecanismo

Quanto à extensibilidade do mecanismo, me limitarei a algumas palavras: A hipótese de que o mecanismo de Purificação Simbólica ou correlato possa ocorrer em territórios estranhos ao brasileiro é razoável devido a própria natureza do mecanismo: o encontro de sistemas simbólicos distintos. No entanto, o mecanismo de Purificação Simbólica é uma postura possível diante de uma máquina de sentido, mas não necessariamente única. Para que tal hipótese seja respondida, é necessária observação em condições semelhantes intra-sistema simbólico diverso do apresentado aqui.
{: .capitular}

A ideia de que o mecanismo possa ser universalizado encontra ainda óbice de natureza paradoxal: o conceito de "Purificação Simbólica" ao entrar em contato com outro sistema simbólico pode ele próprio sofrer o efeito do mecanismo que descreve. Daí que a única solução possível é encontrar mecanismo correlato, mas não idêntico, em sistemas simbólicos distintos.

Portanto, é possível identificar mecanismos correlatos, que não são completamente semelhantes, mas não um mecanismo universal, com as mesmas características. Pois isso planificaria a noção de cultura e de sistemas simbólicos. Esvaziaria o humano também. A própria atitude universalista é uma forma de operar o mecanismo e seus correlatos. Além disso, há condições em que o mecanismo não ocorre. Mais uma vez: aquelas de homogeneidade de sistema.
### Historicização

O Brasil é, como afirma Ribeiro, a aventura entre três matrizes étnicas. Cada uma implica seus próprios sistemas simbólicos. Mas, além dessas matrizes há também hoje, no tempo presente, a presença de muitas outras etnias e sistemas simbólicos no território. Todos passíveis de disputar a percepção do brasileiro.
{: .capitular}

O mecanismo descrito no objeto individual, o japamala, exige agora uma compreensão da formação que o tornou possível: a história brasileira. Ela é necessária para a compreensão do fenômeno pois ele exige história para existir de maneira relevante à análise. É a partir de dado período que o mecanismo torna-se geral no território. E tal generalização acontece devido à formação do mesmo.

[RFZ O Espírito Zombeteiro](RFZ_O_Espírito_Zombeteiro)

[^1]: Rfz é pesquisador independente baseado em Brasília, Brasil. Bacharel em Comunicação – Audiovisual (Universidade de Brasília – UnB). Interesses de pesquisa incluem sistemas simbólicos pós-seculares, semiótica, teoria cultural, e os mecanismos pelos quais tecnologias de sentido organizam a percepção coletiva. Atualmente desenvolvendo o conceito de “**Purificação Simbólica**”: uma matriz para compreender como sistemas simbólicos dominantes sobrescrevem outros enquanto apresentam-se como neutros (rafzmilhomens@proton.me).
