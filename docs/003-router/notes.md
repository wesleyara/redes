## Observações

- O Router é um equipamento utilizado para interconectar diversos dispositivos finais.
- O Router possibilita a comunicação entre diferentes redes.


## Conexão

- O Router é conectado aos computadores utilizando o cabo cruzado;
- O router necessita de um computador para ser configurado;
- Todos computadores das redes devem ter o endereço de IP configurado manualmente;

## Configuração

```bash	
# Entrando no modo de configuração
enable

# Configurando o nome do roteador
configure terminal

# Adicionando portas
interface fastEthernet 0/0
no shutdown
exit

interface fastEthernet 0/1
no shutdown
exit

# Configurando o IP do roteador
interface fastEthernet 0/0
ip address 192.168.3.100 255.255.255.0
exit 

interface fastEthernet 0/1
ip address 191.168.3.100 255.255.255.0
exit

# Listando os IPs das interfaces
show ip interface brief

# Agora é só adicionar o default gateway em cada máquina e testar a conexão
```