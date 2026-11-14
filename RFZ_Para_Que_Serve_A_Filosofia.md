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

![questão](/img/questão.jpeg)
> Para todos verem: homem peludo sem camisa, com barba encarando um pomo de uma fruta qualquer. Como que perguntasse "Ser ou não ser?"


# Para Que Serve A Filosofia? Sobre Os Privilégios Nas Torres De Marfim[^1]

[RFZ O Espírito Zombeteiro](RFZ_O_Espírito_Zombeteiro)

> Escrevi esse texto ouvindo Funk e não quis parar de ouvir para escrever

## Sumário

1. [Jogo no fresstyle](#1-jogo-no-freestyle)
2. [O que é filosofia?](#2-o-que-é-filosofia)
	1. [O nome não é a coisa](#21-o-nome-não-é-a-coisa)
	2. [O nome não é só comida. É comida, diversão e arte](#211-o-nome-não-é-só-comida-é-comida-diversão-e-arte)
	3. [A perspectiva síncrona](#212-a-perspectiva-síncrona)
	4. [A perspectiva assíncrona](#213-a-perspectiva-assíncrona)
	5. [Frigir dos ovos](#214-frigir-dos-ovos)
3. [Dois planos (concreto e etéreo)](#3-dois-planos-concreto-e-etéreo)
4. [Serve para algo?](#4-serve-para-algo)
	1. [Sim](#41-sim)
	2. [Mas também não](#42-mas-também-não)
	3. [No plano concreto, é possível que não sirva?](#43-no-plano-concreto-é-possível-que-não-sirva)
5. [Conclusão](#5-conclusão)

## 1. Jogo No *Freestyle*

Caro leitor, como vai? Dizem que um homem com um defeito é mais charmoso... Essa é minha esperança, pois meu defeito é que não sou filósofo e o texto a seguir não vêm de reflexões calcadas em literatura especializada em filosofia, mas em literatura de outras ciências, também prática filosófica e vivência própria. Essas últimas frases ao invés de desqualificar, justificam este texto, vide-o à conclusão.
{: .capitular}

Costumo dizer que, ao contrário dos meus colegas do grupo, eu jogo no *freestyle* filosófico. Pois muito do que escrevo vêm da minha formação não especializada.  E poderia ser diferente, afinal? Feito o *disclaimer*, espero que lhe seja aprazível a leitura.

## 2. O Que É Filosofia?

Creio que antes de dizer para o que algo serve é necessário definir bem o que é esse algo. E definir filosofia é de uma pretensão tão megalomaníaca que chega mesmo a ser estúpida. Portanto, digamos que a discussão aqui não é sobre o que é filosofia, mas sobre o que ela poderia ser considerando minha história, meu percurso, minha conjuntura.
{: .capitular}

Eu não sou um homem universal. Conhece essa expressão? É a ideia de um homem que representa todos os outros. Não, eu tenho recorte, eu tenho lugar, eu tenho endereço, CPF, eu tenho nome... (qualquer menção ao meme do *Grindr* é mera coincidência).

O que quero dizer é que tudo sobre mim e que vem de mim é circunscrito e condicionado a tudo o que já me atravessou e me atravessa. E com a filosofia que conheço também. O primeiro problema está aí: as pessoas se degladeiam  para definir coisas pelo nome e pelas características possíveis daquilo, mas essa não é uma boa estratégia.

### 2.1. O Nome Não É A Coisa

Venho das ciências sociais. E muitas vezes encontro pessoas, mesmo as que são dessas ciências, que confundem um pouco as coisas. As ciências sociais estudam a sociedade, um grande coletivo, em detrimento de indivíduos isolados. Quem faria algo assim seria a antropologia ou mesmo a psicologia e até em relação a isso tenho minhas reservas.
{: .capitular}

Acontece que para a sociologia nomes não são nada mais nada menos que "tipos". Tipos são categorias usadas para classificar grupos. Caixas nas quais se depositam coisas. O problema disso? É que não existem sujeitos isolados que sejam contemplados por todas as características de um único tipo. Daí que o tipo é só uma etiqueta, uma categoria operacional para facilitar a análise. Pode ser que você seja considerado "amarelo" pelo Instituto Brasileiro de Geografia e Estatística (IBGE), mas você não é só isso. Só que para o IBGE o que interessa é isso, na verdade.

Não se pode definir o indivíduo como amarelo a partir do IBGE se a ideia não for fazer um Censo. E nem se pode definir o Censo a partir de um indivíduo.

Vejo muitas vezes pessoas que entendem classificações como "gay, bi, hétero" como leis calcadas em pedra sob as quais o indivíduo não pode fluir por entre e através, pois isso além de "caracterizar um crime" também caracterizaria uma "transgressão desses tipos". Ora, somos humanos. Não cabemos em conceitos. E isso é potência para ser além. Quero dizer que o nome serve como uma bandeira, um indicador de "você pode se juntar a nós e agir como um grupo em determinado contexto, pois isso será socialmente benéfico para você e para nós". Mas o sujeito não define o grupo nem o grupo define o sujeito.

Os conceitos são assim. As palavras, no geral, trazem coisas à mente, mas não presentificam aquilo em matéria. Se eu digo "garfo" você pensa num gargo, mas não surge um garfo a partir da palavra na minha mão. E nem o garfo que você imagina é exatamente igual ao que eu me refiro.

Com a filosofia a coisa acontece de maneira semelhante. É uma palavra com contexto de mais ou menos uns 8 mil anos de história. Talvez muito mais que isso, dependendo do critério. Pode-se considerar filosofia como a surgida dos gregos, que cunharam o termo, e parte-se daí. Pode-se considerar filosofia como qualquer coisa que se aproxime do que é contemplado pelo termo e parte-se de um lugar muito diferente.

### 2.1.1. O Nome Não É Só Comida. É Comida, Diversão E Arte

Com esse título quero dizer que ainda que haja um nome tentando definir uma coisa e um ponto de partida, o nome ainda não será suficiente. É preciso dar alma ao corpo: uma tradição. Filosofia ou cozinha são nomes para coisas diferentes, mas ambas requerem práticas, métodos, disposições específicas do espírito, rituais, aprendizado, ensino etc.
{: .capitular}

Portanto, pensar no que é o termo filosofia é também pensar no corpo de coisas que fazem parte do conceito. Muito mais do que em sua definição. E aí esbarramos em outro problema. Partindo do ponto A (filosofia surgida dos gregos) ou do ponto B (filosofia como algo que se assemelha à filosofia)  ainda teremos que definir o que entra e o que não entra nesse corpo de coisas que vou me limitar a chamar de tradições. Se formos ortodoxos ao extremo, haverá uma filosofia por cabeça.

### 2.1.2. A Perspectiva Síncrona

Ainda há que se pensar que as tradições mudam e se renovam. Daí que o termo tem história. E, por vezes, em momentos diferentes da história, o termo toma valores muito diferentes. Por isso, filosofia hoje em Creta é muito diferente de filosofia ontem em Macedônia.
{: .capitular}

### 2.1.3. A Perspectiva Assíncrona

E, por último, temos a ideia de filosofia como toda a história do nome e de suas tradições. E isso dá muito pano pra manga. Pois o contexto disso é enorme. É literalmente *Lato sensu*. Mas essa última ideia é bacana, pois engloba muitas coisas diferentes a partir de um único referencial, que permite que se amarre tudo na mesma caixinha e, a partir da mesma etiqueta, consiga-se reunir mais pessoas à mesa. Ao menos aquelas que quiserem participar da refeição no mesmo palácio. Pois certamente haverá quem julgue que não precisa desse referencial e chamará a filosofia grega, na verdade, de uma variação da sua Bíblia, por exemplo.
{: .capitular}

### 2.1.4. Frigir Dos Ovos

Para este texto filosofia é um nome, uma etiqueta, uma referencia, uma caixa gigante na qual cabem religião, tradição, brincadeiras, manufatura, escrita, leitura, analfabetismo, oralidade, pão de queijo, sua receita e forma de fazer, goiabada cascão, gosto, forma e arte de corte, dentre outras coisas... É uma perspectiva *lato sensu*, assíncrona, que não começa nos gregos, mas toma emprestado o nome que utilizaram para batizá-la. É uma salada de frutas mesmo.
{: .capitular}

## 3 Dois Planos (Concreto E Etéreo)

Mas agora só resolvemos parte do problema. Sabemos o que é filosofia para este contexto. Mas para que serve isso tudo? Aí eu te direi: além de haver a etiqueta, que é o nome e o conceito, há a função da etiqueta. Ora, quem faz etiquetas quer organizar coisas a partir de alguma perspectiva e com alguma finalidade. Pode-ser organizar peças Lego, por exemplo, de várias formas: cor, cheiro, textura, tamanho, forma...
{: .capitular}

Mas há aqueles que desejam chegar à raíz das coisas. O que seria discutir o conceito si: a etiqueta. O que é? Quem criou? Quando? Para quê? Esse é o plano etéreo da coisa. Onde cabe toda a investigação do que é que nos leva a pensar como pensamos.

A primeira forma é o plano concreto, que diz "já que pensamos assim, que faremos com isso?". Ambas as formas têm suas vantagens e desvantagens. E ambas válidas e necessárias. O problema é quando tentamos confundir uma com a outra e misturar as duas. Chamo isso de fazer regras. "Chamo filosofia de x e x é assim, portanto, todos que fazem x devem fazer assim". Calma lá!

O preciosismo benéfico de investigar o etéreo é a ilusão de que o etéreo pode se manifestar sem um concreto. O que não é verdade. Meu colega, [Sant' Um Único](Sant'_Um_Único) em seu texto sobre o tema ([O filosofar é o mesmo que roteirizar](SANT_filosofar-roteirizar)), demonstra que pensar e fazer são coisas difíceis de separar. Da mesma forma, não existe o concreto absoluto sem o etéreo.

Mas é mesmo necessário que o etéreo reclame por liberdade de ser. Em outras palavras, que o conceito de "filosofia" seja defendido pelos partidário do "filosofia não serve pra nada". É isso que permite que o conceito continua vivo e prenhe de possibilidades. E também é necessário que o concreto clame por "filosofia sem programa é masturbação mental".  Afinal, é isso que pressiona o filósofo e o pensamento a assumirem o que sempre esteve ali: o programa por detrás da investigação aparentemente despretensiosa. E responsabilizem-se por tal. Pois não sois deuses, filósofos. Há que lembrá-los de que estamos todos no mesmo barco. Ainda que seu iate possua uma torre de marfim.

## 4. Serve Para Algo?

Chegamos agora na resposta à questão do título. Filosofia, nos termos colocados aqui. Serve para algo?
{: .capitular}

### 4.1. Sim

É claro que serve! É óbvio. É política em sua carne, ossos e tutano. É sobre fazer, não fazer e desfazer. É sobre guardar a potência de uma ação qualquer e decidir quando e se realizá-la. Filosofia sem programa é abandonar o mundo e viver de algaravias bruxuleantes e charutos.  É dizer aos irmãos "vão sem mim que eu vou lá ler um bocado". 
{: .capitular}

### 4.2. Mas Também Não

Só que a Filosofia com F maiúsculo não pertence a um indivíduo. É maior, muito maior. É um coletivo inteiro e o ultrapassa. É tudo o que a humanidade e quem sabe até o não humano já foi capaz de testemunhar e transmitir da forma que conseguiu. Essa filosofia não se submete a nenhum ego tresloucado. E não é possível que o faça. Ainda que se tente. 
{: .capitular}

### 4.3. No Plano Concreto, É Possível Que Não Sirva?

Acho difícil. Pois todo deus precisa de um veículo para se manifestar. Mas nenhum veículo é puro, pois não é o deus. A Filosofia precisa do filósofo, mas o filósofo é só mais um ser humano no meio da multidão. E ele precisa fazer o banal: comer, beber, pagar as contas, sobreviver e viver... A pitonisa ou a vestal que fosse, seria ainda necessário dedicá-las algum alimento. E fica a questão: os deuses se manifestam quando estamos no banheiro? Em nosso ato de mais alta vulnerabilidade e necessidade humana?
{: .capitular}

## 5. Conclusão

Daí minha resposta é "filosofia serve pra algo?". Serve sim. Vai servir sempre. Mas e a Filosofia? Essa não tem obrigação com nada e com ninguém. Morre-se e vive-se por ela. Mas eu sou humano e, saudando [Sant' Um Único](Sant'_Um_Único) mais uma vez, como dizia Raul Seixa s "Eu não sou besta pra tirar onda de herói", quem quiser que tome sua cicuta (não literal) em nome de seus ideais. Eu ainda tenho de lavar minhas louças.
{: .capitular}

[RFZ O Espírito Zombeteiro](RFZ_O_Espírito_Zombeteiro)


[^1]: Rfz é pesquisador independente baseado em Brasília, Brasil. Bacharel em Comunicação – Audiovisual (Universidade de Brasília – UnB). Interesses de pesquisa incluem sistemas simbólicos pós-seculares, semiótica, teoria cultural, e os mecanismos pelos quais tecnologias de sentido organizam a percepção coletiva. Atualmente desenvolvendo o conceito de “**Purificação Simbólica**”: uma matriz para compreender como sistemas simbólicos dominantes sobrescrevem outros enquanto apresentam-se como neutros (rafzmilhomens@proton.me).
