# ferramentas de monitoramento no Azure

## Finalidade do Assistente do Azure (Azure Advisor)

O Assistente do Azure é uma ferramenta que avalia os recursos do Azure e oferece recomendações para melhorar a confiabilidade, segurança, desempenho, excelência operacional e reduzir custos. As recomendações são personalizadas e podem ser visualizadas no portal do Azure ou via API. É possível configurar notificações para alertar sobre novas recomendações.

### Categorias Principais

- **Confiabilidade**
- **Segurança**
- **Desempenho**
- **Excelência Operacional**
- **Custo**

### A imagem a seguir mostra o painel do Assistente do Azure.

![-](https://learn.microsoft.com/pt-br/training/wwl-azure/describe-monitoring-tools-azure/media/azure-advisor-dashboard-baca22e2.png)



## Serviço do Azure (Azure Service Health)

Azure Service Health combina três serviços para ajudar a gerenciar e monitorar a integridade dos recursos do Azure:

### Azure Status

- Visão global do status dos serviços do Azure em todas as regiões.
- Informa sobre interrupções de serviço.

### Integridade do Serviço (Service Health)

- Visão detalhada focada nos serviços e regiões específicos que você usa.
- Notifica sobre interrupções, manutenção planejada e avisos.
    - Ex: Analise de relatorios de interrupcao que ocorreu no passado.

### Integridade de recursos (Resource Health)

- Informações personalizadas sobre a integridade de recursos específicos, como VMs.
- Alertas configuráveis via Azure Monitor.


## Azure Monitor

Azure Monitor é uma plataforma de monitoramento abrangente que coleta, analisa e visualiza dados de recursos no Azure, em ambientes locais e multi-nuvem.

### Componentes Principais

- **Log Analytics**: Executa consultas de log para análise de dados.
- **Alertas**: Configura notificações automáticas e ações corretivas com base em métricas e logs.
- **Application Insights**: Monitora aplicativos web, oferecendo insights detalhados sobre desempenho e uso.

### Benefícios

- Monitoramento em tempo real e histórico.
- Alertas personalizados para eventos críticos.
- Integração com outras ferramentas como Power BI.
