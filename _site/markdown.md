# Bootcamp Santander 2025

## Aplicações Web

São programas que funcionam direto no navegador, sem a necessidade de instalar qualquer app. Esses programas se comunicam com o servidor, fazendo requisições pela internet, utilizando tecnologias como:

* HTTP/HTTPS
* APIs (REST, por exemplo)
* AJAX/fetch (no JavaScript)

## Requisição HTTP

Quando uma URL é digitada (ex: `google.com`), é feita uma requisição HTTP. Essa URL é então traduzida para um endereço IP pela rede.
A requisição vai até o servidor que hospeda o site.
No servidor, um programa (ex: Apache ou Nginx) processa a requisição, lê o que está sendo pedido (ex: a página principal), busca os arquivos necessários e envia de volta uma resposta.
O navegador recebe essa resposta e exibe o site na tela.
* Uma requisição GET pede informações para o servidor.
* Uma requisição POST envia informações para o servidor.

## Servidor Proxy

Um servidor proxy é um servidor que fica entre o Cliente e a Internet. Ele aplica regras de acesso e, com base nelas, permite ou bloqueia o acesso do cliente a determinadas páginas.

## Firewall

O firewall é um sistema/programa de segurança que protege a rede ou o computador. Ele analisa o que entra e sai pela internet e, se encontrar algo perigoso (como um arquivo malicioso), bloqueia o acesso para manter tudo seguro.

## Servidor DNS

O DNS é um servidor que pega o nome do site digitado, procura qual é o endereço IP correspondente e devolve esse IP para o navegador. Assim, o navegador pode fazer a requisição para o endereço certo e acessar o site. Por isso, quando contratamos uma hospedagem, também é necessário contratar um domínio.
* Hospedagem: Guarda os arquivos do site (HTML, imagens, etc.).
* Domínio: Nome que as pessoas digitam para chegar até o seu site. Ex: (`www.google.com`).

## Conexão FTP

FTP é um protocolo de transferência de arquivos. Ele permite que o cliente se conecte diretamente ao servidor para enviar ou baixar arquivos. Quando você contrata uma hospedagem, o provedor fornece os dados de acesso FTP (como host, usuário e senha), para que você consiga gerenciar os arquivos do seu site diretamente no servidor.
