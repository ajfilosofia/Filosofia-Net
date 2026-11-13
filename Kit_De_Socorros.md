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
# Kit De Socorros[^1]

![Filosofia-Net.jpg](Filosofia-Net.jpg)

> Para todos verem: cartaz em estilo arcade com os dizeres "Filosofia-net, um canal dedicado à filosofia via XMPP. filosofia-net@canais.xmpp.social.br . Acesse pelos apps: 1. conversations 2. Gajim"

# 1. O Que É Filosofia-Net?

Seja bem-vindo ao canal Filosofia-net!


Fique à vontade para conversar e trocar ideia sobre filosofia e áreas afins.

Lembre-se de ser respeitoso e tolerante com as diferenças, exceto com o que for intolerável:

1. qualquer forma de discurso de ódio;
2. racista;
3. machista; 
4. homofóbico ou transfóbico.

Além das boas conversas em nosso chat, também nos reunimos mensalmente para a discussão de algumas obras.

*A participação é voluntária e aberta a todos.*

Se inscreva em nossa plataforma de organização de leituras:

https://leituras.mimoprodutora.com.br

Também contamos com um site em que divulgamos nossos textos autorais. Avise no chat caso queira participar. O endereço é:

https://ajfilosofia.github.io/Filosofia-Net/

# 2. Como Publicar No Blog Do Filosofia-Net?

## 2.1. Fluxo Das Publicações

0. Escreva seu texto (em linguagem Markdown preferivelmente)
1. Faça uma conta no GitHub
2. Suba a proposta para o seu blog via pull request no GitHub, no diretório do Filosofia-Net
	1. Via formulário de novo texto (para quem não sabe usar o GitHub)
	2. Diretamente no editor do GitHub (mais mobilidade)
	3. Git direto do computador (para quem tem intimidade com as ferramentas)
3. Avise aos colegas no XMPP que subiu texto novo
4. Seu texto vai à apreciação dos colegas em branch própria
5. Os colegas comentam o seu texto proposto no próprio texto e lhe avisam no grupo do XMPP
6. Você corrige o que for pertinente e faz novo commit (sobe o texto novamente)
7. O colega responsável publica o texto (merge pull request)
8. A serpente estará na terra e seu texto estará no ar

## 2.2. Sugestões

1. Somos colegas, não há necessidade de editor-chefe
2. Aprovar não é concordar
3. Cada voz é própria e o texto só é assinado se vc quiser
4. Textos públicos são livres
5. Não há bastidores, comentários públicos são mais bacanas
6. Todos revisando todos é uma maneira bacana de melhorar nosso texto

# 3. O Que É Git?

Git é uma ferramenta que guarda versões de arquivos. Cada "commit" é uma forma de fotografar o estado atual do arquivo e comentá-lo. Isso permite "voltar no tempo" para os estados anteriores dos arquivos, se for necessário. Também é possível acompanhar quaisquer alterações feitas nos arquivos.

# 4. O Que É GitHub?

GitHub é uma página online que, dentre outras coisas, principalmente guarda arquivos git online. Assim várias pessoas podem colaborar em diferentes projetos.

# 5. Como Subir Textos No Blog?

## 5.1. "Não sei usar git"

(1) Você pode enviar seu arquivo no formato que lhe for mais conveniente para os colegas no XMPP e explicar a situação, mas a conta no GitHub será necessária para que você possa ter uma página no blog.

(2) Você pode seguir esse passo a passo aqui:

1. No repositório do blog, no GitHub, clique na aba "Issues"
2. Clique em "New Issue" e preencha com seu texto
3. Clique em "create" e avise os colegas no XMPP
4. Para corrigir seu texto, basta abrir o seu envio novamente, clicar em "..." mudar o que for necessário e salvar.
5. O texto será publicado após a revisão

## 5.2. "Quero subir direto no GitHub"

Tenha uma conta no GitHub e faça um pull request numa branch própria no diretório do blog diretamente do navegador, pelo editor de textos do proprio GitHub.

## 5.3. "Sei fazer commits, pulls and pushs"

Então é só commitar e fazer o pull request numa branch própria.

# 6. FAQ

1. Posso por imagens?
	1. Faz favor! Eu, Rafz, acho que fica uma graça!
	2. Lembre-se que é necessário deter os direitos da imagem
2. Como corrijo um texto já postado?
	1. Edite o texto postado no editor do GitHub e faça novo pull request. Ou converse com um colega.
3. Quanto custa?
	1. Nadica de nada. Só seu tempo e dedicação mesmo.


[^1]: Escrito por RFZ em 7/11/2026 e revisado por FJ no dia seguinte
