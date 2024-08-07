# Infraestrutura Física do Azure

A infraestrutura física do Azure é composta por datacenters, regiões, zonas de disponibilidade e pares de regiões. Vamos explorar cada um desses componentes em detalhes.

## Datacenters

### Descrição
Os datacenters do Azure são instalações físicas que abrigam recursos organizados em racks, com infraestrutura dedicada para energia, refrigeração e rede. Eles são semelhantes aos grandes datacenters corporativos, mas não são acessíveis diretamente aos usuários.

### Importância
Os datacenters formam a base da infraestrutura global do Azure, proporcionando os recursos necessários para executar serviços em nuvem.

## Regiões

### Descrição
Uma região é uma área geográfica que contém pelo menos um, mas geralmente vários, datacenters próximos e conectados por uma rede de baixa latência.

### Funcionalidade
- **Seleção de Região**: Ao implantar recursos no Azure, você escolhe a região onde deseja que eles sejam hospedados.
- **Disponibilidade de Serviços**: Alguns serviços e tipos de VMs estão disponíveis apenas em determinadas regiões.

### Exemplos
- Leste dos EUA
- Europa Ocidental
- Sudeste Asiático

## Zonas de Disponibilidade

### Descrição
Zonas de disponibilidade são datacenters fisicamente separados dentro de uma mesma região, cada um com infraestrutura independente de energia, resfriamento e rede.

### Funcionalidade
- **Resiliência**: Se uma zona ficar inativa, as outras continuam funcionando.
- **Alta Disponibilidade**: Projetadas para hospedar aplicativos críticos, replicando recursos entre zonas.

### Exemplos de Serviços Suportados
- VMs
- Discos Gerenciados
- Balanceadores de Carga
- Bancos de Dados SQL

## Pares de Regiões

### Descrição
A maioria das regiões do Azure é emparelhada com outra região na mesma geografia, separada por pelo menos 300 milhas (cerca de 480 km), permitindo a replicação de recursos.

### Funcionalidade
- **Redundância Geográfica**: Reduz a probabilidade de interrupções devido a desastres naturais ou outros eventos regionais.
- **Failover Automático**: Em caso de falha em uma região, os serviços podem fazer failover para a região emparelhada.

### Exemplos
- Oeste dos EUA e Leste dos EUA
- Sudeste Asiático e Leste Asiático

### Vantagens dos Pares de Regiões
- **Restaurar Prioridade**: Em caso de interrupção ampla, uma região de cada par é priorizada para restauração.
- **Atualizações Planejadas**: As atualizações são distribuídas de forma a minimizar o tempo de inatividade.
- **Conformidade Jurisdicional**: Os dados permanecem na mesma geografia para fins de conformidade com regulamentações locais.

## Regiões Soberanas

### Descrição
São instâncias do Azure isoladas da instância principal, usadas para fins legais ou de conformidade.

### Exemplos
- **Azure Gov**: Regiões para parceiros e órgãos do governo dos EUA, operadas por cidadãos dos EUA com certificações de conformidade adicionais.
- **Azure China**: Operadas pela 21Vianet, isoladas da rede principal do Azure.

# Infraestrutura de Gerenciamento do Azure

A infraestrutura de gerenciamento do Azure organiza recursos, grupos de recursos, assinaturas e contas de forma hierárquica para facilitar a administração, cobrança e controle de acesso. Aqui estão os componentes principais:

## 1. Recursos e Grupos de Recursos do Azure

### Recursos
Elementos básicos do Azure, como VMs, redes virtuais, bancos de dados, etc.

### Grupos de Recursos
Contêineres que agrupam recursos relacionados para gerenciamento mais fácil. Um recurso pode estar apenas em um grupo de recursos por vez, e os grupos de recursos não podem ser aninhados.

### Benefícios
- **Ações em Massa**: Aplicar ações (como excluir ou conceder acesso) a todos os recursos dentro do grupo.
- **Organização**: Facilita a organização lógica dos recursos por projeto, aplicação ou departamento.

### Exemplo de Uso
- Configurar um ambiente de desenvolvimento temporário e desprovisionar todos os recursos ao excluir o grupo de recursos correspondente.

## 2. Assinaturas do Azure

### Assinaturas
Unidades de gerenciamento, cobrança e escala. Uma assinatura fornece acesso autenticado e autorizado aos serviços do Azure e permite provisionar recursos. Cada assinatura é vinculada a uma conta do Azure.

### Benefícios
- **Cobrança**: Diferentes assinaturas podem ser usadas para separar e gerenciar custos.
- **Controle de Acesso**: Aplicar políticas de gerenciamento de acesso no nível da assinatura.

### Exemplo de Uso
- Criar assinaturas separadas para desenvolvimento/teste, produção e diferentes departamentos dentro da organização.

## 3. Grupos de Gerenciamento do Azure

### Grupos de Gerenciamento
Contêineres que organizam assinaturas em um nível superior. Facilitam a aplicação de políticas de governança e controle de acesso em grande escala.

### Benefícios
- **Políticas Unificadas**: Aplicar políticas de governança a várias assinaturas simultaneamente.
- **Acesso Centralizado**: Gerenciar permissões de acesso de maneira centralizada para múltiplas assinaturas.

### Exemplo de Uso
- Limitar locais de VM a uma região específica (como Oeste dos EUA) para todas as assinaturas de produção.

## Hierarquia da Infraestrutura de Gerenciamento

1. **Recursos**: Elementos individuais como VMs, bancos de dados.
2. **Grupos de Recursos**: Contêm múltiplos recursos.
3. **Assinaturas**: Contêm múltiplos grupos de recursos.
4. **Grupos de Gerenciamento**: Contêm múltiplas assinaturas.
