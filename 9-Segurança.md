# Microsoft Entra ID

O Microsoft Entra ID, anteriormente conhecido como Azure Active Directory (Azure AD), é o serviço de gerenciamento de identidades e diretórios na nuvem da Microsoft. Ele oferece recursos para gerenciamento de identidade e acesso, permitindo que as organizações controlem quem tem acesso a seus recursos e informações.

### Principais Funcionalidades

1. **Gerenciamento de Identidade e Acesso**:
   - **Autenticação**: Verificação de identidades de usuários e dispositivos antes de conceder acesso.
   - **Autorização**: Definição de permissões e políticas de acesso aos recursos.

2. **Integração com Aplicações**:
   - Suporte para integração com milhares de aplicações SaaS, como Microsoft 365, Salesforce, e outras.
   - Aplicações personalizadas podem ser integradas para utilizar o Entra ID para autenticação e autorização.

3. **Segurança e Conformidade**:
   - **Autenticação Multifator (MFA)**: Adiciona uma camada extra de segurança, exigindo mais de uma forma de verificação.
   - **Gestão de Identidade e Acesso Privilegiado (PIM)**: Gerencia, controla e monitora acessos privilegiados dentro do ambiente.

4. **Autenticação Unificada (SSO)**:
   - Permite aos usuários acessarem várias aplicações e serviços com uma única autenticação, melhorando a experiência do usuário e a segurança.

5. **Gerenciamento de Dispositivos e Aplicações**:
   - Inclui ferramentas para gerenciar dispositivos e políticas de segurança para garantir que apenas dispositivos compatíveis e seguros possam acessar os recursos corporativos.

### Casos de Uso Comuns

- **Empresas que utilizam Microsoft 365**: Utilizam o Entra ID para autenticação de usuários e gerenciamento de acessos.
- **Desenvolvedores de Aplicações**: Integram o Entra ID para fornecer login seguro e gerenciamento de identidades em suas aplicações.
- **Organizações que Implementam BYOD (Bring Your Own Device)**: Gerenciam e protegem o acesso a recursos corporativos em dispositivos pessoais.

### Benefícios

- **Segurança Avançada**: Recursos como MFA e políticas de acesso condicional ajudam a proteger contra ameaças e acessos não autorizados.
- **Produtividade dos Usuários**: SSO e gerenciamento simplificado de identidade reduzem a necessidade de múltiplos logins e melhoram a eficiência.
- **Gerenciamento Centralizado**: Consolida o gerenciamento de identidades e acessos em uma plataforma unificada, facilitando a administração e conformidade.


# Acesso Condicional do Azure

O Acesso Condicional permite ou nega o acesso a recursos com base em sinais de identidade. Esses sinais podem incluir quem é o usuário, onde ele está e qual dispositivo ele está usando para solicitar acesso.

## Benefícios do Acesso Condicional

### Produtividade em Qualquer Lugar
Permite que os usuários acessem recursos da organização de qualquer lugar, mantendo a segurança.

### Proteção de Ativos
Garante que os ativos da organização estejam protegidos, aplicando políticas de acesso baseadas em condições específicas.

## Funcionamento do Acesso Condicional

O processo de Acesso Condicional envolve três etapas principais:

### 1. Coleta de Sinais

- **Exemplos de Sinais**: Localização do usuário, dispositivo utilizado, aplicativo acessado.
- **Objetivo**: Identificar o contexto do acesso.

### 2. Tomada de Decisões

- **Baseada em Sinais**: Decidir se o acesso deve ser permitido, negado ou se deve ser solicitado um segundo fator de autenticação.
- **Exemplo**: Permitir acesso completo de um local usual, bloquear ou solicitar MFA de um local incomum.

### 3. Imposição

- **Ação Executada**: Aplicar a decisão tomada.
- **Exemplo**: Conceder acesso, solicitar MFA ou negar acesso.

### Casos de Uso do Acesso Condicional

- **Exemplo**: Exigir MFA para administradores, mas não para usuários regulares, ou para usuários que acessam de fora da rede corpor

# Controle de Acesso Baseado em Função do Azure (RBAC)

É um sistema que permite gerenciar o acesso aos recursos do Azure de maneira detalhada, atribuindo permissões a usuários, grupos ou aplicativos com base em suas funções dentro de uma organização. Este modelo segue o princípio dos privilégios mínimos, garantindo que os indivíduos tenham apenas o acesso necessário para realizar suas tarefas.

## Benefícios do RBAC

### Segurança Aprimorada
- **Princípio dos Privilégios Mínimos**: Concede apenas as permissões necessárias para realizar uma tarefa específica, minimizando o risco de acesso indevido.

### Gerenciamento Simplificado
- **Atribuição de Funções**: Facilita a gestão de acesso ao agrupar permissões em funções e atribuí-las a grupos ou indivíduos.
- **Atualização Automática de Permissões**: Novos membros de uma equipe herdam automaticamente as permissões do grupo ao qual são adicionados.

## Funcionamento do RBAC

### Definição de Funções
- **Funções Internas**: O Azure fornece funções predefinidas que cobrem cenários comuns, como Proprietário, Contribuidor e Leitor.
- **Funções Personalizadas**: É possível definir funções personalizadas com um conjunto específico de permissões.

### Atribuição de Funções
- **Indivíduos ou Grupos**: Funções podem ser atribuídas a usuários individuais ou a grupos do Azure AD.
- **Permissões Associadas**: Ao atribuir uma função, os indivíduos ou grupos recebem todas as permissões associadas a essa função.

## Escopos de Aplicação

O RBAC é aplicado a diferentes níveis de escopo, que definem onde as permissões são válidas:

### Grupo de Gerenciamento
- **Abrange várias assinaturas.**
- **Exemplo**: Um proprietário no escopo do grupo de gerenciamento pode gerenciar todos os recursos em todas as assinaturas desse grupo.

### Assinatura
- **Engloba todos os grupos de recursos e recursos dentro de uma assinatura.**
- **Exemplo**: Um leitor no escopo da assinatura pode visualizar todos os recursos nessa assinatura.

### Grupo de Recursos
- **Contém múltiplos recursos relacionados.**
- **Exemplo**: Um contribuidor no escopo do grupo de recursos pode criar e gerenciar todos os recursos dentro desse grupo.

### Recurso Individual
- **Permissões aplicadas a um recurso específico.**
- **Exemplo**: Um usuário pode ter permissões de leitura apenas para um banco de dados específico.

## Hierarquia do RBAC

O RBAC do Azure é hierárquico, permitindo que as permissões atribuídas a um escopo pai sejam herdadas por todos os escopos filho. Por exemplo:
- **Função de Proprietário em um Grupo de Gerenciamento**: Permite gerenciar todos os recursos em todas as assinaturas dentro desse grupo.
- **Função de Leitor em uma Assinatura**: Permite visualizar todos os grupos de recursos e recursos dentro dessa assinatura.

## Imposição do RBAC

O RBAC é imposto pelo Azure Resource Manager (ARM), que organiza e protege os recursos de nuvem do Azure. As ações iniciadas no portal do Azure, Azure Cloud Shell, Azure PowerShell e CLI do Azure são sujeitas às permissões definidas pelo RBAC. No entanto, o RBAC não controla permissões no nível do aplicativo ou dos dados, que devem ser gerenciadas separadamente.

## Exemplo de Uso do RBAC

### Gestão de Acesso Granular
- **Cenário**: Uma equipe de engenharia precisa de acesso de leitura a logs de armazenamento, mas não de escrita.
- **Implementação**: Criar uma função personalizada que concede apenas permissões de leitura e atribuí-la ao grupo de engenharia.

### Automação e Eficiência
- **Cenário**: Um novo desenvolvedor é contratado.
- **Implementação**: Adicionar o novo desenvolvedor ao grupo de RBAC do Azure para engenheiros, concedendo automaticamente as mesmas permissões que os outros engenheiros.

# Modelo de Confiança Zero

A Confiança Zero é um modelo de segurança que pressupõe o pior cenário e protege os recursos com essa expectativa. A Confiança Zero pressupõe uma violação desde o início e verifica cada solicitação como se ela tivesse sido originada em uma rede não controlada.

## Princípios Orientadores da Confiança Zero

### Verificar de Modo Explícito
- **Descrição**: Sempre autenticar e autorizar com base em todos os pontos de dados disponíveis, como identidade do usuário, localização, integridade do dispositivo, classificação do serviço ou carga de trabalho e anomalias.
- **Objetivo**: Garantir que cada solicitação de acesso seja rigorosamente verificada independentemente de sua origem.

### Usar o Acesso com o Mínimo de Privilégios
- **Descrição**: Limitar o acesso dos usuários e recursos ao mínimo necessário para realizar suas tarefas, utilizando métodos como Just-In-Time (JIT) e Just-Enough-Access (JEA), políticas adaptáveis baseadas em risco e proteção de dados.
- **Objetivo**: Reduzir a superfície de ataque minimizando os privilégios e acessos concedidos.

### Pressupor a Violação
- **Descrição**: Operar com a expectativa de que uma violação já ocorreu. Minimizar o raio de alcance e segmentar o acesso, verificar a criptografia de ponta a ponta e usar análises avançadas para detectar ameaças e fortalecer as defesas.
- **Objetivo**: Proteger proativamente os recursos e mitigar os efeitos de uma possível violação.


# Defesa em Profundidade

A defesa em profundidade é uma estratégia de segurança que utiliza várias camadas de proteção para salvaguardar informações contra acessos não autorizados e ataques. Essa abordagem garante que, se uma camada de segurança for comprometida, outras camadas ainda estejam em vigor para mitigar a exposição adicional e fornecer alertas para ações corretivas.

## Camadas da Defesa em Profundidade

### Segurança Física
- **Descrição**: Protege o hardware de computação nos datacenters.
- **Objetivo**: Prevenir acesso físico não autorizado aos equipamentos e garantir a segurança dos ativos físicos.

### Identidade e Acesso
- **Descrição**: Controla o acesso à infraestrutura e às alterações de configuração.
- **Objetivo**: Garantir que apenas identidades autorizadas tenham acesso aos recursos necessários, utilizando SSO e autenticação multifator.
- **Práticas**:
  - Implementação de logon único (SSO).
  - Uso de autenticação multifator (MFA).
  - Auditoria de eventos e alterações.

### Perímetro
- **Descrição**: Protege contra ataques baseados na rede, como ataques DDoS.
- **Objetivo**: Filtrar e mitigar ataques antes que eles impactem os recursos internos.
- **Práticas**:
  - Implementação de proteção contra DDoS.
  - Uso de firewalls de perímetro para detecção e alerta de ataques.

### Rede
- **Descrição**: Limita a comunicação entre recursos na rede.
- **Objetivo**: Reduzir a disseminação de ataques dentro da rede.
- **Práticas**:
  - Limitar a comunicação entre recursos.
  - Negar por padrão e permitir somente quando necessário.
  - Restringir acesso à Internet e implementar conectividade segura com redes locais.

### Computação
- **Descrição**: Protege máquinas virtuais e outros recursos de computação.
- **Objetivo**: Garantir que os sistemas estejam protegidos contra malware e vulnerabilidades.
- **Práticas**:
  - Proteção de acesso a máquinas virtuais.
  - Implementação de proteção de endpoint.
  - Manter sistemas atualizados e com patches.

### Aplicativo
- **Descrição**: Garante que os aplicativos sejam desenvolvidos e operem de forma segura.
- **Objetivo**: Reduzir vulnerabilidades no código dos aplicativos.
- **Práticas**:
  - Integrar segurança no ciclo de vida de desenvolvimento do aplicativo.
  - Armazenar segredos de aplicativos em mídia segura.
  - Adotar segurança como um requisito de design.

### Dados
- **Descrição**: Protege o acesso e armazenamento dos dados.
- **Objetivo**: Garantir a confidencialidade, integridade e disponibilidade dos dados.
- **Práticas**:
  - Controle de acesso rigoroso aos dados.
  - Criptografia de dados em trânsito e em repouso.
  - Implementação de políticas de conformidade regulatória.


# Microsoft Defender para Nuvem

O Microsoft Defender para Nuvem é uma ferramenta abrangente de monitoramento e gerenciamento da postura de segurança que oferece proteção contra ameaças em ambientes de nuvem, locais, híbridos e de várias nuvens. Ele fornece diretrizes e notificações para fortalecer a postura de segurança e proteger recursos contra ataques cibernéticos.

## Funcionalidades Principais

### Proteção Multinuvem e Híbrida

- **Descrição**: Monitora ambientes do Azure, locais, híbridos e outras nuvens como AWS e GCP.
- **Implantação**: Pode implantar automaticamente um agente do Log Analytics para coletar dados de segurança. Para ambientes híbridos e de várias nuvens, utiliza o Azure Arc para extensão das proteções.

### Proteções Nativas do Azure

- **Serviços PaaS do Azure**: Detecta ameaças em serviços como o Serviço de Aplicativo do Azure, SQL do Azure e Conta de Armazenamento do Azure.
- **Serviços de Dados do Azure**: Classifica automaticamente dados e fornece avaliações de vulnerabilidades e recomendações.
- **Redes**: Limita a exposição a ataques com proteção de portas de VMs usando acesso Just-In-Time (JIT).

### Proteção de Ambientes Híbridos

- **Descrição**: Adiciona recursos de proteção para servidores não Azure e fornece alertas de ameaças personalizados.
- **Implantação**: Utiliza o Azure Arc para proteger servidores locais com recursos aprimorados do Defender para Nuvem.

### Recursos em Outras Nuvens

- **AWS**:
  - Avalia recursos da AWS com recomendações de segurança específicas e padrões de conformidade (AWS CIS, AWS PCI DSS).
  - Microsoft Defender para Contêineres e Servidores adiciona detecção de ameaças em clusters EKS e instâncias EC2.
- **GCP**: Proteções similares são estendidas para recursos na Google Cloud Platform.

## Avaliar, Proteger e Defender

### Avaliação Contínua

- **Descrição**: Avalia continuamente a postura de segurança e identifica vulnerabilidades.
- **Ferramentas**: Inclui soluções de avaliação de vulnerabilidade para VMs, registros de contêiner e servidores SQL, integrando-se com o Microsoft Defender para Ponto de Extremidade.

### Proteger

- **Descrição**: Implementa políticas de segurança baseadas no Azure Security Benchmark, garantindo que as cargas de trabalho estejam configuradas de acordo com as melhores práticas de segurança.
- **Políticas**: Definidas para grupos de gerenciamento, assinaturas e locatários inteiros.

### Defender

- **Descrição**: Fornece alertas de segurança e recursos avançados de proteção contra ameaças.
- **Alertas de Segurança**: Detalham recursos afetados, sugerem etapas de correção e, em alguns casos, permitem acionar aplicativos lógicos.
- **Proteção Avançada**: Inclui proteção de portas de VMs, controle de aplicativos adaptáveis e análise de cadeia de encerramento de fusão para entender a origem e impacto de ataques.
