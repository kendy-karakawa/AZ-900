# Descrever os serviços do armazenamento do Azure

## Redundância de Armazenamento do Azure

O armazenamento do Azure oferece várias opções de redundância para proteger seus dados contra falhas de hardware, interrupções de energia ou rede e desastres naturais. Essas opções garantem a alta disponibilidade e durabilidade dos dados, mesmo diante de falhas.

### Opções de Redundância

#### Redundância na Região Primária

- **LRS (Locally Redundant Storage)**:
  - **Replicação**: 3 cópias dos dados em um único data center na região primária.

  ![-](https://learn.microsoft.com/pt-br/training/wwl-azure/describe-azure-storage-services/media/locally-redundant-storage-37247957.png)

- **ZRS (Zone-Redundant Storage)**:
  - **Replicação**: Síncrona em 3 zonas de disponibilidade na região primária.

  ![-](https://learn.microsoft.com/pt-br/training/wwl-azure/describe-azure-storage-services/media/zone-redundant-storage-6dd46d22.png)

#### Redundância em uma Região Secundária

- **GRS (Geo-Redundant Storage)**:
  - **Replicação**: 3 cópias em um data center na região primária (LRS) e 3 cópias em um data center na região secundária (LRS).

  ![-](https://learn.microsoft.com/pt-br/training/wwl-azure/describe-azure-storage-services/media/geo-redundant-storage-3432d558.png)

- **GZRS (Geo-Zone-Redundant Storage)**:
  - **Replicação**: Síncrona em 3 zonas de disponibilidade na região primária (ZRS) e 3 cópias em um data center na região secundária (LRS).

  ![-](https://learn.microsoft.com/pt-br/training/wwl-azure/describe-azure-storage-services/media/geo-zone-redundant-storage-138ab5af.png)

#### Acesso de Leitura aos Dados na Região Secundária

- **RA-GRS (Read-Access Geo-Redundant Storage) e RA-GZRS (Read-Access Geo-Zone-Redundant Storage)**:
  - **Funcionalidade**: Permite acesso de leitura aos dados replicados na região secundária, mesmo que a região primária esteja operando normalmente.
  - **Benefícios**: Maior disponibilidade de dados, mesmo em caso de falhas regionais na região primária.

### Benefícios e Considerações

- **Confiabilidade e Desempenho**: A replicação garante alta disponibilidade e durabilidade dos dados. Opções como ZRS e GZRS proporcionam resiliência adicional ao replicar dados em várias zonas de disponibilidade.
- **Segurança**: Os dados são protegidos contra falhas de hardware, interrupções de energia e desastres naturais. A redundância geográfica (GRS, GZRS) protege contra falhas regionais.
- **Custo**: LRS é a opção mais econômica, mas oferece menor durabilidade em comparação com ZRS, GRS e GZRS. Escolher a opção correta depende do equilíbrio entre custo e necessidade de disponibilidade e durabilidade.

### Diagramas de Replicação

- **LRS**: Replicação em um único data center na região primária.
- **ZRS**: Replicação em três zonas de disponibilidade na região primária.
- **GRS**: Replicação em um data center na região primária e outro na região secundária.
- **GZRS**: Replicação em três zonas de disponibilidade na região primária e em um data center na região secundária.


# Serviços de Armazenamento do Azure

A plataforma de armazenamento do Microsoft Azure oferece diversos serviços de dados para atender a diferentes necessidades de armazenamento, escalabilidade e durabilidade. Vamos explorar cada um desses serviços em detalhes.

## 1. Blobs do Azure

### Descrição
Um serviço de armazenamento de objetos altamente escalável para armazenar grandes quantidades de dados não estruturados, como texto ou dados binários. Inclui suporte para análise de Big Data com o Data Lake Storage Gen2.

### Casos de Uso
- Fornecimento de imagens ou documentos diretamente a um navegador.
- Armazenamento de arquivos para acesso distribuído.
- Transmissão de áudio e vídeo por streaming.
- Armazenamento de dados de backup, restauração e arquivamento.
- Armazenamento de dados para análise por serviços locais ou no Azure.

### Camadas de Acesso
- **Camada de Acesso Frequente (Hot)**: Para dados acessados com frequência.
- **Camada de Acesso Esporádico (Cool)**: Para dados acessados com menos frequência e armazenados por pelo menos 30 dias.
- **Camada de Acesso Arquivo (Archive)**: Para dados raramente acessados e armazenados por pelo menos 180 dias.

## 2. Arquivos do Azure

### Descrição
Compartilhamentos de arquivos gerenciados acessíveis por meio dos protocolos SMB ou NFS, permitindo o acesso simultâneo por implantações locais ou na nuvem.

### Características Principais

- **Compatibilidade com SMB e NFS:** Suporte para os protocolos de compartilhamento de arquivos SMB (Server Message Block) e NFS (Network File System).
- **Gerenciamento Simples:** Fácil de configurar e gerenciar via Portal do Azure, CLI ou PowerShell.
- **Alta Disponibilidade:** Compartilhamentos de arquivos são replicados para garantir alta disponibilidade.

### Casos de uso
- **Ambientes de Desenvolvimento e Teste:** Compartilhamento de arquivos para equipes de desenvolvimento e teste.
- **Armazenamento de Dados de Aplicativos:** Armazenamento centralizado de arquivos para acesso por múltiplas instâncias de aplicativos.

## 3. Filas do Azure

### Descrição
Um serviço de armazenamento de mensagens que permite a comunicação assíncrona entre componentes de aplicativos.

### Casos de Uso
- Criação de listas de pendências de trabalho para processamento assíncrono.
- Integração com Azure Functions para executar ações automáticas quando mensagens são recebidas.
- Armazenamento de mensagens que podem ser acessadas globalmente via HTTP ou HTTPS.

## 4. Discos do Azure

### Descrição
Volumes de armazenamento em nível de bloco gerenciados pelo Azure para uso com VMs do Azure. Oferecem resiliência e disponibilidade superiores aos discos físicos.

### Benefícios
- Provisionamento fácil e gerenciamento automático pelo Azure.
- Suporte a diferentes tipos de discos (SSD, HDD) para atender a diversas necessidades de desempenho.

## 5. Tabelas do Azure

### Descrição
Um serviço de armazenamento NoSQL para grandes volumes de dados estruturados. Suporta chamadas autenticadas de dentro e fora da nuvem do Azure.

### Casos de Uso
- Armazenamento de dados estruturados não relacionais.
- Construção de soluções híbridas ou de várias nuvens com acesso constante aos dados.

## Benefícios do Armazenamento do Azure

- **Durável e Altamente Disponível**: Redundância para proteção contra falhas de hardware e desastres naturais, garantindo alta disponibilidade.
- **Seguro**: Criptografia de todos os dados gravados e controle refinado de acesso.
- **Escalonável**: Projetado para atender a demandas de armazenamento e desempenho de aplicativos modernos.
- **Gerenciado**: Manutenção de hardware, atualizações e problemas críticos são cuidados pelo Azure.
- **Acessível**: Acesso aos dados de qualquer lugar do mundo via HTTP ou HTTPS, com suporte a diversas linguagens e ferramentas de gerenciamento.

# Opções de Migração de Dados do Azure

O Azure oferece uma gama completa de ferramentas e serviços para migrar dados, aplicativos e infraestrutura para a nuvem. As opções de migração variam desde soluções online, que utilizam ferramentas integradas para avaliar e migrar ambientes locais, até soluções offline, como o Azure Data Box, que facilitam a transferência de grandes volumes de dados com segurança. A escolha da ferramenta e do método de migração depende das necessidades específicas de cada organização, incluindo volume de dados, conectividade de rede e requisitos de segurança.

## Ferramentas de Migração Online
- **Migrações para Azure: Descoberta e Avaliação**: Avalia ambientes locais para migração.
- **Migrações para Azure: Migração de Servidor**: Migra VMs e servidores para o Azure.
- **Assistente de Migração de Dados**: Avalia e prepara SQL Servers para migração.
- **Serviço de Migração de Banco de Dados do Azure**: Migra bancos de dados para o Azure.
- **Assistente de Migração do Serviço de Aplicativo do Azure**: Migra sites locais para o Serviço de Aplicativo do Azure.

## Ferramentas de Migração Offline
- **Azure Data Box**: Usa dispositivos físicos para transferir grandes volumes de dados de forma rápida e segura.


# Opções de Movimentação de Arquivos no Azure

O Azure oferece várias ferramentas para movimentação de arquivos que atendem a diferentes necessidades de transferência e gerenciamento de dados. O AzCopy é ideal para transferências rápidas de linha de comando, o Gerenciador de Armazenamento do Azure proporciona uma interface gráfica fácil de usar, e a Sincronização de Arquivos do Azure permite centralizar e sincronizar dados entre servidores locais e a nuvem de forma bidirecional.

### AzCopy
- **Carregamento de Arquivos**: Transferir grandes volumes de arquivos de um ambiente local para o Azure rapidamente.
- **Sincronização de Backups**: Manter backups locais sincronizados com o Azure de forma unidirecional.
- **Migração entre Nuvens**: Transferir dados entre diferentes provedores de nuvem.

### Limitação
- A sincronização com o AzCopy é unidirecional, ou seja, apenas em uma direção da origem para o destino.

### Gerenciador de Armazenamento do Azure
- **Gerenciamento de Arquivos**: Facilitar o upload, download e transferência de arquivos com uma interface gráfica.
- **Movimentação de Dados**: Transferir dados entre diferentes contas de armazenamento no Azure.

### Sincronização de Arquivos do Azure
- **Centralização de Dados**: Manter dados centralizados no Azure enquanto acessíveis localmente.
- **Sincronização bidirecional**: Mantém automaticamente os arquivos atualizados entre um servidor Windows local e um ambiente de nuvem do Azure
- **Continuidade de Negócios**: Recuperar rapidamente de falhas locais sincronizando novos servidores com o Azure.
- **Otimização de Armazenamento**: Armazenar localmente apenas os arquivos acessados com frequência e manter os menos acessados na nuvem.







