## Observações

- Utilizar o DHCP nos permite atribuir endereços IP dinamicamente, sem a necessidade de configurar manualmente cada um.

## Configuração

```bash	
# Entrando no modo de configuração
enable

# Configurando o nome do roteador
configure terminal

# Adicionando portas
interface fastEthernet 0/0
no shutdown

# Configurando pool de IPs
ip dhcp pool CASA
network 192.168.0.0 255.255.255.0
default-router 192.168.0.1
exit

# Configurando o IP do roteador
interface fastEthernet 0/0
ip address 192.168.0.1 255.255.255.0
exit
```