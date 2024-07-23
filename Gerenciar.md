# Ferramentas para gerenciar e implantar recursos do Azure

## Ferramentas para Interagir com o Azure

### Portal do Azure

- Interface gráfica para gerenciar assinaturas, criar dashboards personalizados e configurar acessibilidade.
- Resiliente e atualizado continuamente, sem necessidade de tempo de inatividade.

### Azure Cloud Shell

- Ferramenta baseada em navegador que suporta Azure PowerShell e CLI do Azure (Bash).
- Não requer instalação local e é autenticada com suas credenciais do Azure.

### Azure PowerShell

- Usa cmdlets para executar tarefas de gerenciamento.
- Suporta scripts para automação de processos complexos.

### CLI (Interface de Linha de Comando) do Azure

- Funcionalmente equivalente ao Azure PowerShell, mas usa sintaxe Bash.
- Ideal para quem prefere linguagem Bash.


## Azure Arc

Azure Arc estende a gestão e governança do Azure para ambientes híbridos e multi-nuvem. Com o Azure Arc, você pode gerenciar servidores, clusters do Kubernetes, serviços de dados, SQL Server e VMs como se estivessem no Azure.

### Funcionalidades

- **Gerenciamento Centralizado**: Projeta recursos não-Azure no Azure Resource Manager (ARM).
- **Consistência de Ferramentas**: Usa as ferramentas de gerenciamento do Azure em qualquer lugar.
- **Suporte a ITOps e DevOps**: Integra práticas tradicionais e novas no mesmo ambiente.

### Exemplo

- Com o Azure Arc, é possível aplicar o Azure Policy em recursos em outras nuvens como AWS.

## Azure Resource Manager (ARM)

Serviço para organizar, implantar e gerenciar recursos no Azure por meio de grupos de recursos.
Permite a implementação de "Infraestrutura como Código" (IaC) para controle centralizado de infraestrutura.

### Benefícios do ARM

- **Implantações Consistentes**: Automatiza a implantação de recursos.
  - *Exemplo*: Implantar infraestrutura de rede com VMs e bancos de dados de forma padronizada.
- **Orquestração Automática**: Determina a ordem de implantação.
  - *Exemplo*: Implantar VMs após configurar a rede.
- **Modularidade e Extensibilidade**: Reutilização de modelos.
  - *Exemplo*: Usar modelos para aplicações web em diferentes ambientes.

### Bicep

- Linguagem simplificada para escrever modelos ARM.

### Infraestrutura como Código (IaC)

Infraestrutura como Código (IaC) é a prática de gerenciar e provisionar recursos de TI por meio de arquivos de definição legíveis por máquina, em vez de configuração manual. Isso é feito através de ferramentas de automação e scripts que descrevem a infraestrutura desejada.

### Benefícios

- **Consistência e Repetibilidade**: Garantia de que a infraestrutura seja configurada da mesma forma, sempre.
- **Automação**: Redução de erros humanos e aumento da eficiência.
- **Versionamento**: Controle de versões da infraestrutura como qualquer outro código de software.

### Exemplo no Azure

Usar modelos ARM para descrever e automatizar a implantação de redes, VMs e outros recursos, garantindo que cada implantação seja idêntica e conforme as especificações definidas no código.
