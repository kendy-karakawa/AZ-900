# Descrever o gerenciamento de custos no Azure

## Fatores que Afetam os Custos no Azure

1. **Tipo de Recurso**: Máquinas virtuais, bancos de dados, armazenamento, etc.
2. **Configuração de Recurso**: Tamanho e capacidade de recursos, como vCPUs e RAM.
3. **Consumo de Recursos**: Medido por uso, como horas de VM, transações de armazenamento.
4. **Localização Geográfica**: Regiões diferentes têm preços diferentes.
5. **Tipo de Assinatura**: Planos de pagamento como Pay-As-You-Go, Reserved Instances.
    - **Pay-As-You-Go**: Paga-se apenas pelos recursos consumidos. É flexível, mas pode ser mais caro para uso prolongado.
    - **Reserved Instances**: Descontos significativos ao reservar recursos por um período (1 ou 3 anos). Ideal para cargas de trabalho previsíveis.
    - **Enterprise Agreements**: Contratos personalizados para grandes organizações, oferecendo descontos e benefícios adicionais.
6. **Azure Marketplace**: Serviços de terceiros podem aumentar os custos.

## Comparação das Calculadoras de Preço e Custo Total de Propriedade (TCO)

### Calculadora de Preços

- Fornece estimativas de custos para provisionar recursos no Azure.
- Permite configurar cenários com recursos individuais ou soluções completas.
- Útil para prever custos de computação, armazenamento, e rede.

### Calculadora de TCO

- Compara custos de infraestrutura local versus nuvem Azure.
- Insere configuração atual e calcula a diferença de custo ao migrar para o Azure.
- Considera fatores como energia e mão de obra de TI.


## Ferramenta de Gerenciamento de Custos do Azure

### Análise de Custos

- Monitora e analisa gastos em várias perspectivas (ciclo de cobrança, região, recurso).
- Oferece visualizações detalhadas dos gastos.
- Facilita a compreensão dos padrões de consumo e identificação de áreas de economia.

### Alertas de Custo

- Configura alertas para quando os gastos se aproximarem ou ultrapassarem limites definidos.
- Notificações automáticas por email ajudam a manter o controle em tempo real.

### Orçamentos

- Define limites de gastos mensais ou anuais.
- Permite criar orçamentos para monitorar e controlar os custos, garantindo que não haja surpresas na fatura.

## Finalidade das Marcas no Azure (tags)

### Marcas de Recursos

- Adicionam metadados aos recursos para facilitar o gerenciamento e a organização.

### Principais Usos

- **Gerenciamento de Recursos**: Localizam e gerenciam recursos específicos.
- **Otimização de Custos**: Agrupam recursos para relatórios e controle de orçamento.
- **Operações**: Agrupam recursos por importância e ajudam a definir SLAs.
- **Segurança**: Classificam recursos pelo nível de segurança.
- **Conformidade**: Identificam recursos que atendem aos requisitos regulatórios.
- **Automação**: Facilitam a execução de tarefas automatizadas.

### Gerenciamento de Marcas

- Feito via PowerShell, CLI do Azure, modelos do Resource Manager, API REST ou portal do Azure.
- Não é necessário impor a presença de uma marca específica em todos os recursos.
