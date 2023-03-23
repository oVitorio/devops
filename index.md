# Criando um Servdidos linux 

## Disbruição Linux

A escolha da distribuição Ubuntu para um servidor é uma decisão comum devido a sua estabilidade, segurança e suporte de longo prazo. O Ubuntu é baseado no sistema operacional Debian e é conhecido por sua facilidade de uso, ampla comunidade de suporte e atualizações regulares de segurança.

Além disso, o Ubuntu tem uma grande variedade de pacotes disponíveis em seus repositórios, o que permite a instalação de diferentes serviços e aplicativos de forma rápida e fácil. Ele também é altamente personalizável e pode ser configurado de acordo com as necessidades específicas do servidor.

O Ubuntu Server vem com diversas ferramentas de gerenciamento, como o sistema de gerenciamento de pacotes APT e o utilitário de configuração do sistema, o systemd. Essas ferramentas permitem que os administradores de sistema gerenciem facilmente o servidor e realizem tarefas como atualizações de software, monitoramento de desempenho e configuração de serviços.


## Criando o Pendriver Bootavel 

 Após a escolha da disbuição linux para  a criação do servidor é necessario criar um Pendriver Bootavel com esse sistema operacional.

 - Baixando a iso do sistema escolhido:
    -  para o server em questão sera o Ubuntu server e clicando [aqui](https://ubuntu.com/download/server)  ira ser redicionado para o site oficial do Ubunto para o dowloand 
    - Com a ISO baixa agora é o momento  de cria o pendrivel bootavel `RECOMENDAVEL O USO DE UM PENDRIVEL PELO MENOS 8GB`, para a criação do bootavel é nessario é o uso do [Rufus](http://rufus.ie/pt_BR/)

    <img src="assets\screenshot2_en.png" width="400">

## Configurando o Servidor 

1. setar a ordem de boot para que a bios possa inicializar primeiro o pendriver bootavel 

    <img src="assets\boot-from-usb-bios.png" width="400">

2. configurações basicas 

    nesse passo você ira setar as configurações basicas do servidor, como  Idioma do sistema layout do teclado, data e hora 
    - setando o Idioma. infelismente o idiam portugês Brasil não se encontra.

        <img src="assets\set-language.png" width="400">

    -  asgora setando o padrão do teclado. por padrão o instalador ja indefica o padrão então nessa parte apenas de o done. mas caso não apresente a configuração que deseje é o configurar com a sersão que deseje.

        <img src="assets\set-keyboard.png" width="400">


3. configurando o IP estatico para o servidor 
    
    quando terminar  de setar o Idioma e o layout do teclado.  a tela `NETWORK CONNECTIONS` vai aparecer  e por padrão é para já reconhecer um endereço de IP.
     <img src="assets\ip-page-padrao.png">

     mas não é isso que queremos. necessitamos de um IP estático para o servidor. 

     para configurar o IP estático precione a telca ent ***enter*** er no endereço de ip existente. um menu ira aparecer depois navege até opção `EDIT IPV4` e de  um ***enter***

    <img src="assets\ip-select.png">

    de novamente um ***enter***.
    E um outro menu ira aparecer navege até a opção manual e de um ***enter***

    <img src="assets\ip-select2.png">

    se voce fez tudo coreto voce estara vendo essa tela: 

    <img src="assets\ip-select-manual-vazia.png">

    temos que preencher todos os dados 
    - `SUBNET`:  nesse campo voce vai colocar o IP da rua rede com a mascara exempo: **192.198.1.0/24**
    - `ADDRESS`: nessa parte vai ser o ip do servidor exempo: **192.168.1.10**
    - `GATEWAY`: vamos setar o gateway é o ponto de entrada ou saída de uma rede, que conecta diferentes redes ou dispositivos exemplo : **192.168.1.1**
    - `NAME SERVERS`: nesse campo vamos setar o DNS (Domain Name System) é um sistema que converte nomes de domínio em endereços IP para permitir a comunicação entre dispositivos em uma rede. pdoe adicionar mais de 1 só lembrar de colocar um `,` entre cada um exemplo  **208.67.222.222, 208.67.220.220**
    - `SEARCH DOMAINS`: são configurações em um sistema de rede que permitem aos usuários digitar apenas o nome do host em vez do nome de domínio completo para acessar um recurso em uma rede local. Essas configurações permitem que os dispositivos procurem automaticamente o nome de domínio completo quando um nome de host simples é inserido em uma solicitação de rede. exemplo: **zer01ti.intra**

apos preencher todos clique em **SAVE**
<img src="assets\ip-select-manual.png">