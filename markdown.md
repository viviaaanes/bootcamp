# Bootcamp Santander 2025

### Aplicações Web
São programas que funcionam direto no navegador, sem a necessidade de instalar qualquer app. Esses programas se comunicam com o servidor, fazendo requisições pela internet, utilizando tecnologias como:
* HTTP/HTTPS
* APIs (REST, por exemplo)
* AJAX/fetch (no JavaScript)


### Requisição HTTP
Quando uma URL é digitada (ex: `google.com`), é feita uma requisição HTTP. Essa URL é então traduzida para um endereço IP pela rede.
A requisição vai até o servidor que hospeda o site.
No servidor, um programa (ex: Apache ou Nginx) processa a requisição, lê o que está sendo pedido (ex: a página principal), busca os arquivos necessários e envia de volta uma resposta.
O navegador recebe essa resposta e exibe o site na tela.
* Uma requisição GET pede informações para o servidor.
* Uma requisição POST envia informações para o servidor.

  
### Servidor Proxy
Um servidor proxy é um servidor que fica entre o Cliente e a Internet. Ele aplica regras de acesso e, com base nelas, permite ou bloqueia o acesso do cliente a determinadas páginas.


### Firewall
O firewall é um sistema/programa de segurança que protege a rede ou o computador. Ele analisa o que entra e sai pela internet e, se encontrar algo perigoso (como um arquivo malicioso), bloqueia o acesso para manter tudo seguro.


### Servidor DNS
O DNS é um servidor que pega o nome do site digitado, procura qual é o endereço IP correspondente e devolve esse IP para o navegador. Assim, o navegador pode fazer a requisição para o endereço certo e acessar o site. Por isso, quando contratamos uma hospedagem, também é necessário contratar um domínio.
* Hospedagem: Guarda os arquivos do site (HTML, imagens, etc.).
* Domínio: Nome que as pessoas digitam para chegar até o seu site. Ex: (`www.google.com`).

### Conexão FTP
FTP é um protocolo de transferência de arquivos. Ele permite que o cliente se conecte diretamente ao servidor para enviar ou baixar arquivos. Quando você contrata uma hospedagem, o provedor fornece os dados de acesso FTP (como host, usuário e senha), para que você consiga gerenciar os arquivos do seu site diretamente no servidor.


### Banco de Dados
Um banco de dados é uma aplicação que serve para armazenar informações.
Ele pode estar no mesmo servidor que o site ou em um servidor separado.
É usado para guardar, organizar e recuperar dados como:
* Usuários cadastrados
* Produtos de uma loja
* Comentários, postagens, mensagens etc.


### Formulário
Um formulário é uma parte de código HTML que contém campos para o usuário inserir informações. Ele pode ter vários tipos de campos, como:
* Caixa de texto
* Botões de opção (radio)
* Caixas de seleção (checkbox)
* Campos de senha
* Botões de envio (submit)

---

### Atributos importantes em formulários

name → Dá um nome ao campo. 
Útil para acessar o valor com JavaScript ou enviar dados para o back-end.

```html
<input type="text" name="email" />
```

action → Define pra onde (qual URL) os dados do formulário vão ser enviados.

```html
<form action="/cadastro">
```

method → Define como os dados vão ser enviados:

- GET → Envia os dados pela URL. Não é seguro para senhas.
- POST → Envia os dados dentro do corpo da requisição. Mais seguro.

```html
<form method="post">
```

target → Diz onde abrir o resultado do envio do formulário:

- _self (padrão): mesma aba
- _blank: nova aba

```html
<form target="_blank">
```

autocomplete → Ativa ou desativa o autocompletar do navegador (sugestões de campos que já foram preenchidos antes).

```html
<form autocomplete="on">
```

Eventos (on...) → Tudo que começa com `on` é um evento HTML. 
Usado com JavaScript para reagir a ações.

- onsubmit → algo acontece quando o formulário é enviado.

```html
<form onsubmit="validarFormulario()">
```

### Checkbox e Radio – Como funcionam no envio de formulários

Checkbox → Checkboxes permitem múltiplas seleções.
Quando usamos o método GET, se você marcar vários checkboxes com o mesmo `name`, o navegador envia todos os valores com o mesmo nome — mas alguns servidores só pegam o último valor, e não entendem como lista.

- Use o método POST e coloque colchetes no `name`
- O `[]` no `name="adicionais[]"` indica ao servidor que deve tratar isso como uma lista/array de valores.

```html
<input type="checkbox" name="adicionais[]" value="bacon">
<input type="checkbox" name="adicionais[]" value="queijo">
<input type="checkbox" name="adicionais[]" value="ovo">
```

Radio → Radios servem para escolher apenas uma opção entre várias. Para isso funcionar, todos os radios do mesmo grupo precisam ter o mesmo `name`. Com o mesmo nome, o navegador entende que só uma opção pode ser escolhida.

```html
<input type="radio" name="pagamento" value="pix">
<input type="radio" name="pagamento" value="cartao">
```

### Formatações de texto no HTML

| **TAG** | **Função** |
| --- | --- |
| `<i>` | Deixa o texto em itálico (não tem significado semântico). |
| `<u>` | Sublinha o texto |
| `<b>` | Deixa o texto em negrito (estética, sem significado semântico). |
| `<mark>` | Destaca o texto como se fosse marca-texto. |
| `<sup>` | Coloca o texto acima da linha (ex: expoente `10<sup>2</sup>`). |
| `<sub>` | Coloca o texto abaixo da linha (ex: fórmula química `H<sub>2</sub>O`). |
| `<blockquote>` | Destaca uma citação ou trecho, com recuo à esquerda. |
| `<strong>` | Deixa o texto em negrito, com significado semântico de ênfase. (Usado por leitores de tela e acessibilidade). |
| `<em>` | Deixa o texto em itálico, mas com ênfase semântica (tipo “destaque verbal”). |
| `<font>` | era usada antigamente para mudar a cor, o tipo e o tamanho da fonte direto no HTML. Hoje em dia, não é mais recomendada, porque essa função deve ser feita com CSS. (ex: `<font color=”red” face =”Arial”>`Texto em vermelho e Arial`</font>`). |

### Semântica no HTML

Semântica → Semântica é escrever o HTML de forma que o código faça sentido por si só, tanto para humanos quanto para máquinas (navegadores, leitores de tela e etc).

### Estruturando HTML

`<div>` → Usada para estruturar blocos do seu código HTML.

Por padrão, ela tem um `display: block`, ou seja, ocupa toda a largura disponível e quebra linha automaticamente. Usada para:

- Agrupar conteúdos (textos, imagens, formularios etc).
- Criar seções.
- Trabalhar com layout (CSS).

`<span>` → Usada para selecionar partes pequenas e específicas do texto ou elementos inline, quando queremos aplicar algum estilo ou comportamento sem quebrar a linha.
Por padrão, tem `display: inline`, ou seja, não quebra a linha.

`<fieldset>` → Como tudo no HTML, ela é uma tag estrutural.
Ela é usada dentro de formulários para agrupar campos relacionados e dar uma aparência visual diferenciada, com uma borda ao redor do grupo.

`<legend>` → Usada junto com o `<fieldset>`, ela serve como título do grupo de campos. Aparecendo por padrão acima da borda do fieldset.

`<iframe>` → É uma evolução do antigo `<embed>`.

Ela permite carregar conteúdos de outros sites dentro da sua página, como vídeos do YouTube, mapas, formulários, entre outros.

- src → Define qualpágina será carregada dentro do iframe.
- width e height -: Definem o tamanho da janela

```html
<iframe width="560" height="315"
  src="https://www.youtube.com/embed/dQw4w9WgXcQ"
  title="Vídeo do YouTube"
  frameborder="0"
  allowfullscreen>
</iframe>
```

- Quando você coloca um vídeo do youtube via `<iframe>`, quem recebe o view é o criador do vídeo, não você.
Isso acontece porque o vídeo ainda está sendo hospedado e servido pelo youtube, e o `<iframe>` só está mostrando uma “janela” para o conteúdo. Ou seja, você está “pegando emprestado” o conteúdo externo.
- Nem todo site permite ser carregado via iframe (pode bloquear via `X-Frame-Options`).
- Não é indicado para conteúdo muito importante ou interações críticas (segurança e acessibilidade).
- Muito útil para conteúdo externo não essencial: vídeos, mapas, calendários etc.

### Trabalhando com mídias (imagens)

`<img>` → Exibe uma imagem na página.

```html
<img src="imagem.jpg" alt="Descrição da imagem" title="Título da imagem" width="300">
```

`<svg>` → Representa imagens vetoriais (gráficos baseados em pontos e formas, não em pixels. Você pode ampliar ou reduzir sem perder qualidade.

- src → Caminho da imagem (local ou URL da web).
- alt → Texto alternativo (usado para leitores de tela e mostrado se a imagem não carregar).
- title → Mostra um balão com texto ao passar o mouse.
- width → Define a largura (a altura se ajusta automaticamente para não distorcer).
- height → Pode ser definido, mas cuidado para não esticar a imagem.

### formatos de imagem

| **Formato** | **Vantagens** | **Desvantagens** | **Ideal para…** |
| --- | --- | --- | --- |
| **JPG** | Leve | Perde qualidade (compressão) | Fotos, galerias de imagem |
| **PNG** | Alta qualidade + Transparência | Mais pesado | Logos, ícones, labels |
| **GIF** | Animação simples | Baixa resolução, pesado | Figurinhas animadas, memes |
| **SVG** | Vetorial (não perde qualidade) | Mais dificil de editar sem ferramenta  | Logos, ícones, graficos |

### Trabalhando com mídias (audio)

`<audio>` → É uma tag nativa do HTML5, usada para inserir e tocar arquivos de áudio diretamente no navegador.

```html
<audio controls>
  <source src="musica.mp3" type="audio/mpeg">
  Seu navegador não suporta áudio.
</audio>
```

`<source>` → É  a tag filha da tag `<audio>` e define o caminho e o tipo do arquivo de áudio.
Você pode colocar vários `<source>` com formatos diferentes para compatibilidade.

```html
<source src="musica.mp3" type="audio/mpeg">
<source src="musica.ogg" type="audio/ogg">
```

### Atributos comuns:

| **Atributo** | **Função** |
| --- | --- |
| **controls** | Mostra os controles padrão do navegador (play, pause, volume…) |
| **autoplay** | O áudio começa a tocar automaticamente ao carregar a página (nem sempre funciona por questões de privacidade) |
| **loop** | O áudio recomeça automaticamente quando termina |
| **muted** | Começa o áudio com o som desligado |
| **preload** | Controla o pré-carregamento (auto, metadata, none) |
- Com JavaScript você pode criar seus próprios botões, controlar o tempo da música, volume etc.

### Trabalhando com mídias (video)

`<video>` → É uma tag nativa do HTML5 que permite exibir videos diretamente no navegador, sem precisar de plugins.

```html
<video controls width="640" height="360">
  <source src="meuvideo.mp4" type="video/mp4">
  Seu navegador não suporta vídeos.
</video>
```

- A tag `<source>` define a origem do vídeo e o tipo (type). Você pode incluir vários `<source>` com formatos diferentes (mp4. ogg, webm).

`<track>` → É usada dentro do `<video>` para adicionar legendas, trascrições, capítulos e descrições.

- Normalmente usa o formato `.vtt` (WebVTT)
- É um arquivo de texto que marca o tempo exato de cada parte da legenda ou capítulo.

```html
<video controls width="640" height="360">
  <source src="aula.mp4" type="video/mp4">
  <track src="legenda.vtt" kind="subtitles" srclang="pt" label="Português" default>
</video>
```

### Atributos do `<track>`:

| **Atributo** | **Função** |
| --- | --- |
| **src** | Caminho do arquivo `.vtt` |
| **kind** | Tipo do conteúdo: `subtitles`, `captions`, `chapters`, `descriptions` |
| **srclang** | Linguagem da legenda (`pt`, `en`, `es`…) |
| **label** | Nome que vai aparecer no seletor de legendas |
| **default** | Define que essa legenda ja vem ativada automaticamente. |

Exemplo do conteúdo .vtt:

```html
WEBVTT

00:00:00.000 --> 00:00:04.000
Bem-vindo à nossa aula de HTML!

00:00:05.000 --> 00:00:09.000
Hoje vamos aprender sobre a tag <video>.
```