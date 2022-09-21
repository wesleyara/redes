# Redes

Conteúdo aprendido durante uma formação de Redes, tida como pré-requisito para dar seguimento nos estudos sobre Linux. Entender melhor como funciona as redes, comandos, testes e outros detalhes que norteiam esse mundo de TI.

## Sumário

- [Notas Gerais](#notas-gerais)
- [Hub](/docs/001-hub/)
- [Switch](/docs/002-switch/)
- [Router](/docs/003-router/)

## Notas Gerais

Alguns conteúdos relevantes serão documentados de forma mais direta, criando uma lógica dentro de minhas anotações.

### ICMP
---
Dentro da ferramenta administrativa do ping temos o protocolo ICMP, sendo ele o responsável por mandar uma requisição (Echo Request) para máquina remota e esperar um retorno dessa máquina remota (Echo Reply). O ping é um comando que envia pacotes ICMP para o destino, e o destino responde com um pacote ICMP.

### TLL
---
O TTL é uma informação dentro do pacote do IP que informa qual é a máxima quantidade de hops que minha informação pode passar antes de ser descartada. É a quantidade de máquinas que ela vai poder passar no caminho. Se o TTL chegar a 0, o pacote é descartado.

### DNS
---
Os servidores DNS são chamados de Domain Name Servers e sua função é realizar o “mapeamento” entre endereço IP e url (ex: www.google.com). Dessa forma, se estamos digitando www.google.com no browser, o servidor DNS está fazendo a tradução entre o nome da url e o endereço IP.

### ARP
--- 
O ARP é o protocolo utilizado para fazer o mapeamento entre o endereço IP e o endereço MAC de um dispositivo. Isso é necessário porque o MAC encontra-se um nível abaixo do IP e eu preciso dele para poder transmitir as informações.

### Cabos de conexão
---
Para conexão entre computadores e dispostivos de rede temos dois tipos de cabos, o cabo direto e o cabo cruzando. Quando temos um padrão de cores iguais nas duas pontas do cabo, teremos o que chamamos de cabo direto. Quando temos um padrão de cores diferentes nas duas pontas do cabo, teremos o que chamamos de cabo cruzado. Essa troca de cores é feita nas entradas 1, 2, 3 e 6.

### TCP
---
O protocolo TCP encontra-se acima da camada onde o IP está localizado e ele é responsável por realizar o transporte da minha informação. Além do protocolo TCP, essa camada possui também outro protocolo bastante conhecido, o UDP.

### TLS
---
TLS (Transport Layer Security) seria um protocolo de criptografia utilizado para segurança da informação. Ele seria a evolução do protocolo SSL (Secure Sockets Layer).

### HTTPS
---
O youtube usa em seu site um sistema de criptografia das informações, onde o protocolo TLS é responsável por essa atividade. Pelo fato das informações, estarem criptografadas não foi possível reconstruir a informação e visualizar o que o usuário estava digitando.

### Máscara de rede
---
A máscara de rede é usada como forma de comparação para determinar se dois equipamentos estão na mesma rede. Para isso ela vai dividir o endereço IP em dois grupos, de rede e hosts (máquinas). Tendo um padrão 255.255.255.0, onde o 255 se refere a rede e o 0 ao host.
