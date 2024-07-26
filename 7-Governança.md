# ferramentas de governança e conformidade no Azure

## Microsoft Purview

Microsoft Purview é uma solução para governança, risco e conformidade de dados, oferecendo uma visão unificada dos dados em ambientes locais, multinuvem e SaaS.

### Principais Funcionalidades

- **Descoberta Automatizada**: Localiza dados em diferentes ambientes.
- **Classificação de Dados**: Identifica e classifica dados confidenciais.
- **Linhagem de Dados**: Mapeia o fluxo de dados de ponta a ponta.

### Benefícios

- Proteção de dados confidenciais.
- Gerenciamento de conformidade regulatória.
- Governança de dados centralizada.


## Finalidade do Azure Policy

Azure Policy é um serviço do Azure que permite criar, atribuir e gerenciar políticas para garantir a conformidade dos recursos com os padrões corporativos. 

Além disso, as Políticas do Azure são herdadas, se você definir uma política em um nível superior, ela será aplicada automaticamente a todos os herdeiros.

### Componentes Principais

- **Definições de Políticas**: Impõem regras sobre as configurações dos recursos.
  - *Exemplo*: "Os recursos devem estar em uma região específica."
- **Iniciativas**: Grupos de políticas relacionadas.
  - *Exemplo*: Monitorar um banco de dados SQL não criptografado na Central de Segurança. Essa política monitora servidores e bancos de dados SQL não criptografados.
- **Avaliação de Conformidade**: Identifica e corrige automaticamente recursos fora de conformidade.
  - *Exemplo*: "Nenhum IP público deve ser permitido em VMs."

### Benefícios

- Assegura que os recursos estejam sempre em conformidade.
- Automatiza a correção de configurações de recursos.


## Finalidade dos Bloqueios de Recursos no Azure

Bloqueios de Recursos ajudam a proteger recursos críticos de exclusões ou alterações acidentais, mesmo com políticas RBAC (Controle de Acesso Baseado em Função).

### Tipos de Bloqueios

- **Delete (Excluir)**: Permite leitura e modificação, mas impede exclusão.
- **ReadOnly (Somente Leitura)**: Permite apenas leitura, impedindo exclusão ou modificação.

### Gerenciamento

- Pode ser gerenciado via portal do Azure, PowerShell, CLI do Azure, ou Azure Resource Manager.
- Para alterar um recurso bloqueado, primeiro remova o bloqueio.

## Finalidade do Portal de Confiança do Serviço

Microsoft Service Trust Portal oferece acesso a conteúdos, ferramentas e recursos sobre segurança, privacidade e conformidade da Microsoft. Contém detalhes sobre os controles e processos que protegem os serviços em nuvem e dados dos clientes. 

### Recursos Incluídos

- Documentos sobre conformidade que podem ser salvos e notificados quando atualizados.
