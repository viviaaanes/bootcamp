# Bootcamp Santander 2025

## Aplicações Web

São programas que funcionam direto no navegador, sem a necessidade de instalar qualquer app. Esses programas se comunicam com o servidor, fazendo requisições pela internet, utilizando tecnologias como:

* **HTTP/HTTPS**
* **APIs** (REST, por exemplo)
* **AJAX/fetch** (no JavaScript)

## Requisição HTTP

Quando uma URL é digitada (ex: `google.com`), é feita uma **requisição HTTP**. Essa URL é então traduzida para um **endereço IP** pela rede.

1.  A requisição vai até o servidor que hospeda o site.
2.  No servidor, um programa (ex: Apache ou Nginx) processa a requisição, lê o que está sendo pedido (ex: a página principal), busca os arquivos necessários e envia de volta uma resposta.
3.  O navegador recebe essa resposta e exibe o site na tela.

### Tipos de Requisição

* Uma requisição **GET** pede informações para o servidor.
* Uma requisição **POST** envia informações para o servidor.

## Servidor Proxy

Um **servidor proxy** é um servidor que fica entre o **Cliente** e a **Internet**. Ele aplica regras de acesso e, com base nelas, permite ou bloqueia o acesso do cliente a determinadas páginas.

## Firewall

O **firewall** é um sistema/programa de segurança que protege a rede ou o computador. Ele analisa o que entra e sai pela internet e, se encontrar algo perigoso (como um arquivo malicioso), bloqueia o acesso para manter tudo seguro.

## Servidor DNS

O **DNS** é um servidor que pega o nome do site digitado, procura qual é o **endereço IP** correspondente e devolve esse IP para o navegador. Assim, o navegador pode fazer a requisição para o endereço certo e acessar o site. Por isso, quando contratamos uma hospedagem, também é necessário contratar um domínio.

### Termos Importantes

* **Hospedagem**: Guarda os arquivos do site (HTML, imagens, etc.).
* **Domínio**: Nome que as pessoas digitam para chegar até o seu site. Ex: (`www.google.com`).

## Conexão FTP

**FTP** é um **protocolo de transferência de arquivos**. Ele permite que o cliente se conecte diretamente ao servidor para enviar ou baixar arquivos. Quando você contrata uma hospedagem, o provedor fornece os dados de acesso FTP (como host, usuário e senha), para que você consiga gerenciar os arquivos do seu site diretamente no servidor.

Banco de Dados → Um banco de dados é uma aplicação que serve para armazenar informações.
Ele pode estar no mesmo servidor que o site ou em um servidor separado.
É usado para guardar, organizar e recuperar dados como:

- Usuários cadastrados
- Produtos de uma loja
- Comentários, postagens, mensagens etc.

Formulário → Um formulário é uma parte de código HTML que contém campos para o usuário inserir informações. Ele pode ter vários tipos de campos, como:

- Caixa de texto
- Botões de opção (radio)
- Caixas de seleção (checkbox)
- Campos de senha
- Botões de envio (submit)

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