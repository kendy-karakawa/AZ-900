# Recursos do Azure

## Máquinas Virtuais do Azure

As Máquinas Virtuais (VMs) do Azure fornecem uma plataforma de Infraestrutura como Serviço (IaaS) que permite criar e usar VMs na nuvem, oferecendo controle total sobre o sistema operacional, software personalizado e configurações de hospedagem.

## Área de Trabalho Virtual do Azure

A Área de Trabalho Virtual do Azure (Azure Virtual Desktop - AVD) é um serviço de virtualização de áreas de trabalho e aplicativos executado na nuvem, permitindo que você acesse uma versão do Windows hospedada na nuvem de qualquer localização. Ele é compatível com diversos dispositivos e sistemas operacionais e pode ser acessado através de aplicativos para áreas de trabalho remotas ou navegadores modernos.

## Contêineres do Azure
Os contêineres são uma tecnologia de virtualização que permite executar várias instâncias de um aplicativo em um único host físico ou virtual. Eles são uma alternativa mais leve e ágil às máquinas virtuais (VMs), proporcionando maior flexibilidade e eficiência na gestão de aplicativos.

## Azure Functions
O Azure Functions é uma plataforma de computação sem servidor controlada por eventos, projetada para executar pequenas partes de código (funções) em resposta a eventos, sem a necessidade de gerenciar a infraestrutura subjacente.

## Serviço de Aplicativo do Azure
Permite criar e hospedar aplicativos web, APIs RESTful, back-ends de dispositivos móveis e trabalhos em segundo plano sem gerenciar a infraestrutura.

- Suporte para implantações automatizadas do GitHub, Azure DevOps ou qualquer repositório Git.
- Compatível com várias linguagens (como .NET, Java, Ruby, Node.js, PHP e Python) e ambientes (Windows e Linux).


# Beneficios da Nuvem. 
Estudos sobre os beneficios de se ter um ambiente em nuvem. 

## Alta Disponibilidade
Um sistema que está sempre funcionando com recursos disponiveis sempre que necessário. Se concentra em garantir a disponiblidae maxima, independente de interrupções ou eventos que possam ocorrer.

SLA = Um Acordo de Nível de Serviço (SLA) é um contrato que define o nível esperado de serviço entre um provedor de serviços e um cliente. No Azure, SLAs garantem a disponibilidade e o desempenho dos serviços.

### Pontos Principais:

- Disponibilidade: Expressa como porcentagem de tempo de atividade (por exemplo, 99.9%).
- Creditos de Serviço: Compensações oferecidas se o SLA não for cumprido.
- Monitoramento: Ferramentas como Azure Monitor ajudam a garantir que os SLAs sejam mantidos.

## Escalabilidade ou Elasticidade 
  - Refere-se a capacidade de ajustar recursos para atender a demanda, siginifica que você pode adicionar mais recursos para lidar melhor com o aumento da demanda.
  - Você não esta pagando alem do necessário pelos serviços.
  - Baseado em consumo, vocës só paga pelo que usa.
  - Se a demanda cair vocë poderá reduzir seus recursos e assim reduzir seus custos.

### Vertical X Horizontal 
  - Escala vertical, se você estivesse desenvolvendo um aplicativo e precisasse de amsi capacidade de processamento, poderia escalar verticalmente para adicionar mais CPUs ou RAM a VM.
  - Escala horizontal, se seu aplicativo web estiver recebendo mais tráfego do que uma única VM pode lidar, você pode escalar horizontalmente adicionando mais VMs para balancear a carga e melhorar o desempenho e a resiliência.

## Agilidade
- Agilidade refere-se à capacidade de responder rapidamente às mudanças nas necessidades do negócio e de implantar e configurar recursos em nuvem de forma rápida e eficiente.
  
## Confiabilidade 
  - A capacidade que um sistema tem de se recuperar de falhas e continuar funcionando.
  - Devido ao design descentralizado, a nuvem naturalmente da suporte a uma infraestrutura confiável e resiliente
  - A nuvem permite que você tenha recursos implantados em várias regiões do mundo. 

## Previsibilidade
  - A Previsibilidade na nuvem permite que você avance com confiança, seja no desempenho ou no custo. 

## Desempenho
-  A previsibilidade de desempenho se concentra em prever os recursos necessários para oferecer uma experiência positiva aos clientes. 
- O dimensionamento automático, o balanceamento de carga e a alta disponibilidade são apenas alguns dos conceitos de nuvem que dão suporte à previsibilidade de desempenho. 
- Se de repente você precisar de mais recursos, o dimensionamento automático poderá implantar recursos adicionais para atender à demanda e depois reduzir a implantação quando a demanda cair. 

## Custo
- A previsibilidade de custos se concentra em prever o custo dos gastos com a nuvem. 

## Segurança
  - A nuvem oferece ferramentas de segurança que atendem as necessidades dos clientes mas, é importante lembrar que a implementação de muitas delas devem ser realizadas pelo cliente.
  - Se você quiser que a aplicação de pathces e a manutenção sejam tratadas automaticamente, as implantações de plataforma como serviço ou software como serviço podem ser as melhores estratégias de nuvem para você. 

## Gerenciabiliade.
  - UM dos principais beneficios da computação em nuvem são as opções de capacidade de gerenciamento. Há dois tipos de capacidade de gerenciamento para computação em nuvem, pelo portal e Azure CLI ou power shell e APIs.
  - O gerenciamento da nuvem diz respeito a gerenciar seus recursos de nuvem. Por Exemplo: Escalar automaticamente a implantação de recursos com base na necessidade.
  - Implantar recursos com base em um modelo pré-configurado, removendo a necessidade de configuração manual. 

## Governança 
  - Como vamos gerir, os padrões que iremos adotar. Padrões da empresa e/ou padrões de mercado.
  - A auditoria baseaada em nuvem ajuda a sinalizar qualquer recurso que esteja fora de conformidade com seus padrões corporativos e fornece estratégias de mitigação.
  - Dependendo do modelo operacional, patches de software e atualizações tambem podem ser aplicados automaticamente, o que ajuda na governança e segurança.
  - Ao estabelecer uma presença de governança o mais cedo possivel, você poderá manter sua presença de nuvem atualizada, protegida e bem gerenciada. 
