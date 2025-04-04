# Topologia de Rede

Este documento descreve a topologia da rede, os dispositivos envolvidos, os endereços de rede utilizados e as interfaces de comunicação entre os nós.

## Componentes da Topologia

A rede é composta por múltiplos nós, interligados através de conexões diretas. Cada nó pode desempenhar diferentes funções:

- **Roteadores:** Responsáveis pelo encaminhamento de pacotes entre sub-redes.
- **Hosts:** Dispositivos finais conectados à rede.
- **Switches:** (se aplicável) Fazem a interconexão entre dispositivos dentro da mesma sub-rede.

## Esquema de Endereçamento e Interligações

Cada nó possui interfaces de rede conectadas a diferentes sub-redes. Abaixo, a descrição de cada um:

### Riachao_dos_Dantas (n2)  
- `eth0`: 192.0.2.1/24 (conexão com Boquim)  
- `eth1`: 192.0.3.1/24 (conexão externa ou outro nó)  

### Boquim (n9)  
- `eth0`: 192.0.2.2/24 (conectado a Riachao_dos_Dantas)  
- `eth1`: 192.0.4.1/24 (conexão com Estancia)  
- `eth2`: 192.0.5.1/24 (outra conexão)  

### Estancia (n1)  
- `eth0`: 192.0.4.2/24 (conectado a Boquim)  
- `eth1`: 192.0.7.2/24 (conexão com Araua)  
- `eth2`: 192.0.9.1/24 (conexão com Salgado)  
- `eth3`: 192.0.10.1/24 (conexão com Santa Luzia)  
- `eth4`: 192.0.12.1/24 (conexão com Pix)  

### Araua (n7)  
- `eth0`: 192.0.6.1/24  
- `eth1`: 192.0.7.1/24 (conectado a Estancia)  

### Salgado (n12)  
- `eth0`: 192.0.9.2/24 (conectado a Estancia)  
- `eth1`: 192.0.8.1/24  

### Santa Luzia (n17)  
- `eth0`: 192.0.10.2/24 (conectado a Estancia)  
- `eth1`: 192.0.11.1/24  

### Pix (n13)  
- `eth0`: 192.0.12.2/24 (conectado a Estancia)  
- `eth1`: 192.0.13.1/24  

## Portas Utilizadas

Caso existam serviços rodando nos dispositivos, seguem as portas associadas:

- **SSH (22/tcp)**: Acesso remoto aos nós para configuração e monitoramento.
- **HTTP (80/tcp)**: Caso algum servidor web esteja operando.
- **DNS (53/udp/tcp)**: Se houver um serviço de resolução de nomes na rede.

*(Adicione outras portas caso tenha mais serviços rodando.)*
