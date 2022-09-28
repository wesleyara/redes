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

# Configurando endereço IP do roteador
ip address 8.8.8.1 255.0.0.0 

# Informando o servidor DNS
ctrl+z
configure terminal
ip dhcp pool CASA
dns-server 8.0.0.11
```