## Rede Virtual do Azure

### Definição

As redes virtuais (VNet) do Azure permitem que recursos, como VMs, aplicativos web e bancos de dados, se comuniquem entre si, com usuários na Internet e com redes locais. Elas funcionam como uma extensão da rede local, oferecendo várias funcionalidades essenciais de rede.

### Funcionalidades Principais

#### Isolamento e Segmentação

- Redes virtuais isoladas podem ser criadas, cada uma com seu próprio espaço de endereço IP privado.
- Divisão do espaço de endereços IP em sub-redes.
- Uso do serviço de resolução de nomes interno do Azure ou configuração de um servidor DNS interno/externo.

#### Comunicação pela Internet

- Conexões de entrada podem ser habilitadas atribuindo um endereço IP público ou utilizando um balanceador de carga público.
- Para que as máquinas virtuais acessem a Internet, é necessário configurar um gateway de Internet na rede virtual e definir regras apropriadas no NSG para permitir o tráfego de saída para a Internet.

#### Comunicação entre Recursos do Azure

Recursos do Azure, podem se comunicar entre si das seguintes maneiras:

- **Rede Virtual**: Recursos dentro da mesma VNet podem se comunicar diretamente.
- **Pontos de Extremidade de Serviço**: Conectam recursos do Azure com segurança, otimizando o encaminhamento.
- **Emparelhamento de Redes Virtuais**: Conecta duas VNets diretamente, permitindo tráfego privado na rede de backbone da Microsoft.

#### Comunicação com Recursos Locais

- **Ponto a Site**: Conexão VPN criptografada de computadores clientes para a rede virtual.
- **Site a Site**: Conexão VPN entre dispositivos locais e o Gateway de VPN do Azure.
- **ExpressRoute**: Conectividade privada dedicada para o Azure, fora da Internet, para maior largura de banda e segurança.

#### Roteamento de Tráfego de Rede

- O roteamento de tráfego é realizado automaticamente entre sub-redes, redes locais e Internet.
- **Tabelas de Rotas**: Definem regras para o tráfego entre sub-redes.
- **BGP (Border Gateway Protocol)**: Propaga rotas BGP locais para redes virtuais do Azure.

#### Filtragem de Tráfego de Rede

- **Grupos de Segurança de Rede (NSGs)**: Contêm regras para permitir ou bloquear tráfego baseado em IPs, portas e protocolos.
- **Soluções de Virtualização de Rede**: VMs especializadas para funções de rede específicas, como firewalls.

#### Conectar Redes Virtuais

- **Emparelhamento de Redes Virtuais**: Conecta duas VNets diretamente, com tráfego privado na rede de backbone da Microsoft.
- **Rotas Definidas pelo Usuário (UDR)**: Controle sobre tabelas de roteamento entre sub-redes e VNets.

#### Pontos de Extremidade

- **Pontos de Extremidade Públicos**: Têm um endereço IP público, acessível globalmente.
- **Pontos de Extremidade Privados**: Existentes dentro da VNet, com um endereço IP privado.


## Redes Virtuais Privadas do Azure (VPN)

### O que é uma VPN?

Uma VPN (Virtual Private Network) usa um túnel criptografado dentro de outra rede, geralmente a Internet pública, para conectar duas ou mais redes privadas confiáveis. Isso permite que redes compartilhem informações de maneira segura, protegendo o tráfego contra interceptação e outros ataques.

### Gateways VPN

Um gateway de VPN é um tipo de gateway de rede virtual no Azure. Esses gateways são implantados em uma sub-rede dedicada e permitem diferentes tipos de conectividade:

- **Conexão Site a Site**: Conecta datacenters locais a redes virtuais.
- **Conexão Ponto a Site**: Conecta dispositivos individuais a redes virtuais.
- **Conexão Rede a Rede**: Conecta redes virtuais entre si.
- Todas as transferências de dados são criptografadas durante o tráfego pela Internet.

### Tipos de VPNs

Existem dois tipos principais de VPNs no Azure:

- **VPN Baseada em Política**:
  - Especifica estaticamente os endereços IP dos pacotes que precisam ser criptografados.
  - Avalia cada pacote de dados em relação aos conjuntos de endereços IP para escolher o túnel adequado.
  
- **VPN Baseada em Rota**:
  - Modela túneis IPSec como adaptadores de rede ou interfaces de túnel virtual.
  - Usa o roteamento IP para decidir qual túnel usar.
  - Preferida para conectar dispositivos locais devido à sua resiliência a alterações de topologia.


### Alta Disponibilidade em Gateways VPN

Para garantir que a VPN seja resiliente e tolerante a falhas, existem algumas configurações de alta disponibilidade:

- **Ativo/Em Espera**:
  - Dois gateways são implantados, um ativo e outro em espera.
  - Em caso de manutenção ou falha, o gateway em espera assume automaticamente, com interrupções mínimas.

- **Ativo/Ativo**:
  - Utiliza o protocolo de roteamento BGP.
  - Dois endereços IP públicos são atribuídos, um para cada instância.
  - Permite criar túneis redundantes e estender a alta disponibilidade com dispositivos VPN adicionais.

- **Failover do ExpressRoute**:
  - Configura um gateway de VPN como caminho de failover para conexões ExpressRoute.
  - Garante conectividade alternativa via Internet em caso de falhas no ExpressRoute.

- **Gateways com Redundância de Zona**:
  - Implantação em zonas de disponibilidade do Azure para maior resiliência.
  - Protege contra falhas no nível da zona.
  - Exige SKUs de gateway diferentes e utiliza endereços IP públicos Standard.

Essas configurações e tipos de VPN ajudam a garantir a segurança, resiliência e continuidade do serviço ao conectar redes e dispositivos por meio de redes virtuais privadas no Azure.

## Express Route

Se você precisa trafegar uma quantidade muito grande de dados emtre sua infra local e o Azure(ou qualquer outro cloud), você pode estar fazendo o uso do Express Route, que basicamente é uma forma de fazer um link direto do seu ponto até o data center do Azure, esse passo custa um pouco caro, mas é mais fácil que trafegar pela internet.

### Tipos de Conectividade:

 - VPN de IP (any-to-any): Rede de qualquer para qualquer.
 - Rede Ethernet ponto a ponto.
 - Conexão cruzada virtual por meio de um provedor de conectividade em uma colocação.

Essas conexões não passam pela Internet pública, oferecendo mais confiabilidade, maior velocidade, latências consistentes e maior segurança.

## DNS do AZure

O **DNS do Azure** é um serviço de hospedagem para domínios DNS, permitindo que você gerencie e resolva nomes de domínio em infraestrutura do Azure. Ele fornece alta disponibilidade e desempenho, juntamente com a capacidade de gerenciar registros DNS de forma fácil e segura.


## Características Principais
- **Alta Disponibilidade:** O serviço é distribuído globalmente, garantindo alta disponibilidade.
- **Desempenho Rápido:** Resolução de nomes rápida utilizando a infraestrutura global da Microsoft.
- **Segurança:** Integração com o Azure Active Directory para controle de acesso baseado em funções.
- **Facilidade de Gerenciamento:** Gerenciamento de registros DNS através do portal do Azure, CLI, ou API REST.

Obs.: DNS, ou Domain Name System (Sistema de Nomes de Domínio), é um sistema que traduz nomes de domínio legíveis por humanos (como www.exemplo.com) em endereços IP numéricos que os computadores utilizam para se comunicar entre si na rede.