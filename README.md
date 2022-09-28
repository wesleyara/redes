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

### Classes de IP
---
As classes de IP separam os endereços de IP em intervalos, preferinindo também suas máscara de rede. Essa análise é feita com base no primeiro valor, os intervalos são:
 
- Classe A: 1-126 (Máscara: 255.0.0.0)
- Classe B: 128-191 (Máscara: 255.255.0.0)
- Classe C: 192-223 (Máscara: 255.255.255.0)
- Classe D: 224-239
- Classe E: 240-255

A IETF (Internet Engineering Task Force) determinou que existiriam ao todo 5 classes de endereços IP, indo de ordem alfabética da classe A até a classe E. Porém as duas últimas classes não são usadas para serem endereçadas as máquinas. A classe D seria usada para multicast (termo usado quando queremos nos comunicar com somente algumas máquinas de nossa rede) e a classe E seria uma classe experimental. Portanto as classes de IP que podem ser endereçadas para máquinas seriam a classe A, B e C.


### IP 127.0.0.1
---
O endereço 127.0.0.1 seria uma faixa de endereço IP reservada, esse seria um endereço interno da placa de rede para realizar testes e verificar se ela está de fato validando os protocolos TCP/IP.

### IP Privado
---
Os endereços IP privados são usados para comunicação somente em minha rede local, de acordo com a especificação, eles não podem ser usados para comunicação na internet por exemplo. Os endereços IP privados são:

![ip privado](/assets/ip-privado.png)

### IPv6
---
O endereço IPv6 foi necessário porque os endereços IPv4 públicos chegaram a um fim por conta da grande popularidade da internet, smartphones, tablets, etc.

### Endereço de rede
---
O endereço de rede é feito com base no primeiro intervalo do endereço de IP, ou seja, no IP 192.168.1.3, o endereço de rede seria 192.168.1.0.

### Endereço de broadcast
---
O endereço de broadcast é feito com base no endereço de rede, por exemplo, em redes com máscara 192.168.1.0, vamos ter como endereço de broadcast 192.168.1.255.

### DHCP
---
O DHCP (Dynamic Host Configuration Protocol) é um protocolo que realiza a configuração dinâmica de endereços IP. Ele é responsável por realizar a atribuição de endereços IP para os dispositivos que estão conectados na rede.
