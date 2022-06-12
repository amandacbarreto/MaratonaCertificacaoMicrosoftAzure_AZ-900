# Escolher o melhor serviço de monitoramento para visibilidade, insight e mitigação de interrupções

A Microsoft oferece várias soluções que podem ajudar você a reagir rapidamente a interrupções, pesquisar problemas intermitentes, otimizar o uso e ser proativo no tratamento de futuros tempos de inatividade planejados.

## Identificar suas opções de produto

Todas as empresas que usam a nuvem têm várias perguntas ou preocupações básicas.

- Estamos usando a nuvem corretamente? Podemos obter mais desempenho dos nossos gastos com a nuvem?
- Estamos gastando mais do que precisamos?
- Nossos sistemas estão protegidos adequadamente?
- Qual é o grau de resiliência dos nossos recursos? Se passássemos por uma interrupção regional, poderíamos fazer failover para outra região?
- Como é possível diagnosticar e corrigir problemas que ocorrem de modo intermitente?
- Como podemos determinar rapidamente a causa de uma interrupção?
- Como podemos aprender sobre o tempo de inatividade planejado?

O Azure oferece soluções de monitoramento pelas quais é possível obter respostas, insights e alertas para ajudar a garantir que tenha otimizado o uso da nuvem; verificar a causa raiz de problemas não planejados.; e,preparar-se antecipadamente para interrupções planejadas.

Há três ofertas principais de monitoramento do Azure.

### Assistente do Azure

> ### O Assistente do Azure avalia seus recursos do Azure e faz recomendações para ajudar a melhorar a confiabilidade, a segurança e o desempenho, alcançar a excelência operacional e reduzir os custos. O Assistente foi projetado para ajudar você a poupar tempo na otimização da nuvem. O serviço de recomendação inclui ações sugeridas que você pode adotar imediatamente, adiar ou ignorar.

As recomendações estão disponíveis por meio do portal do Azure e da API, e é possível configurar notificações para alertar você sobre novas recomendações.

Quando você estiver no portal do Azure, o painel do Assistente exibirá recomendações personalizadas para todas as suas assinaturas, e você poderá usar filtros para selecionar recomendações de serviços, grupos de recursos ou assinaturas específicas. As recomendações são divididas em cinco categorias:

- Confiabilidade: usada para garantir e aprimorar a continuidade dos seus aplicativos comercialmente críticos.
- Segurança: usada para detectar ameaças e vulnerabilidades que podem levar a violações de segurança.
- Desempenho: usado para aprimorar a velocidade de seus aplicativos.
- Custo: usado para otimizar e reduzir seus gastos gerais com o Azure.
- Excelência operacional: usada para ajudar você a obter eficiência de processo e fluxo de trabalho, gerenciamento de recursos e melhores práticas de implantação.

### Azure Monitor

> ### O Azure Monitor é uma plataforma para coleta, análise, visualização e potencial execução de ações com base dos dados de registro em log e de métrica de todo o ambiente do Azure e local.

Os dados podem ser usados para ajudar você a reagir a eventos críticos em tempo real, por meio de alertas entregues às equipes por SMS, email etc. Outra opção é usar limites a fim de disparar a funcionalidade de dimensionamento automático para aumentar ou reduzir conforme a demanda.

Alguns produtos populares, como o Application Insights do Azure, um serviço para envio de informações de telemetria do código-fonte do aplicativo para o Azure, usam o Azure Monitor nos bastidores. Com o Application Insights, os desenvolvedores de aplicativos podem aproveitar a poderosa plataforma de análise de dados no Azure Monitor para ter insights aprofundados sobre as operações de um aplicativo e diagnosticar erros sem ter que esperar que um usuário os relate.

### Integridade do Serviço do Azure

> ### A Integridade do Serviço do Azure fornece uma exibição personalizada da integridade dos serviços, regiões e recursos do Azure dos quais você depende.

O site status.azure.com, que exibe apenas os principais problemas que afetam amplamente os clientes do Azure, não fornece o panorama completo. Mas a Integridade do Serviço do Azure exibe os problemas localizados principais e menores que afetam você. Os problemas de serviço são raros, mas é importante estar preparado para o inesperado. Você pode configurar alertas que ajudam a fazer a triagem de interrupções e manutenção planejada. Após uma interrupção, a Integridade do Serviço fornece relatórios oficiais de incidentes, chamados de RCAs (análises de causa raiz), que podem ser compartilhados com os stakeholders.

A Integridade do Serviço ajuda você a ficar atento a vários tipos de evento:

- Problemas de serviço são problemas no Azure, como interrupções, que afetam você no momento. Você pode analisar detalhadamente o impacto em serviços e regiões, atualizações de suas equipes de engenharia e encontrar maneiras de compartilhar e acompanhar as informações mais recentes.

- Os eventos de manutenção planejada podem afetar sua disponibilidade. Você pode analisar detalhadamente os serviços, as regiões e os detalhes afetados para mostrar como um evento afetará você e o que é necessário fazer. A maioria desses eventos ocorre sem nenhum impacto a você e não é mostrada aqui. No caso raro em que uma reinicialização seja necessária, a Integridade do Serviço permite que você escolha quando realizar a manutenção para minimizar o tempo de inatividade.

- Os avisos de integridade são problemas que exigem que você aja para evitar a interrupção do serviço, incluindo descontinuações de serviço e alterações significativas. Os comunicados de integridade são anunciados com antecedência para permitir que você se planeje.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/monitoring-fundamentals/2-identify-product-options)

## Analisar os critérios de decisão

### Você precisa analisar como está usando o Azure para reduzir custos, aumentar a resiliência ou proteger a segurança?

Escolha **o Assistente do Azure quando estiver procurando uma análise de seus recursos implantados**. O Assistente do Azure analisa a configuração e o uso de seus recursos e dá sugestões de como otimizar a confiabilidade, a segurança, o desempenho, os custos e as operações com base nas melhores práticas de especialistas.

### Deseja monitorar os serviços do Azure ou seu uso do Azure?

**Se quiser acompanhar o próprio Azure, especialmente os serviços e as regiões dos quais você depende, escolha a Integridade do Serviço do Azure**. Confira o status atual dos serviços do Azure dos quais você depende, as futuras interrupções planejadas e os serviços que serão descontinuados. É possível configurar alertas que ajudam você a ficar a par de incidentes e tempos de inatividade futuros sem precisar acessar o painel regularmente.

**No entanto, se quiser acompanhar o desempenho ou os problemas relacionados a suas VMs ou instâncias de contêiner específicas, bancos de dados, aplicativos etc., acesse o Azure Monitor e crie relatórios e notificações para ajudar você a entender o desempenho dos seus serviços ou diagnosticar problemas relacionados ao uso do Azure**.

### Deseja medir eventos personalizados em conjunto com outras métricas de uso?

**Escolha o Azure Monitor quando quiser medir eventos personalizados com outros dados de telemetria coletados**. Eventos personalizados, como aqueles adicionados ao código-fonte de seus aplicativos de software, podem ajudar a identificar e diagnosticar por que seu aplicativo está se comportando de determinada maneira.

### Você precisa configurar alertas de interrupções ou quando o dimensionamento automático está prestes a implantar novas instâncias?

Mais uma vez, você usaria o **Azure Monitor a fim de configurar alertas para eventos importantes relacionados a seus recursos específicos**.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/monitoring-fundamentals/3-analyze-decision-criteria)

## Usar o Assistente do Azure

> **Cenário**:
>
> A Tailwind Traders deseja **otimizar os gastos com a nuvem**. Além disso, a organização está preocupada com violações de segurança, pois armazena dados do cliente e dados de compra históricos em bancos de dados baseados em nuvem. À medida que ganha experiência em nuvem, a organização deseja entender melhor seu uso da nuvem e as melhores práticas e identificar "ganhos fáceis" em que pode aprimorar seus gastos com a nuvem e suas práticas de segurança.

### Qual serviço escolher?

1. Nesse cenário, a Tailwind Traders precisa analisar o próprio uso do Azure para fins de otimização?
   Sim. A Tailwind Traders entende que pode estar gastando muito e está preocupada com as próprias práticas de segurança. Ela **deseja analisar o uso que faz da nuvem em relação às melhores práticas do setor. Portanto, o Assistente do Azure é a opção perfeita para esse cenário**.

Embora você possa ter encontrado a opção de produto adequada, vamos continuar avaliando os critérios de decisão para esse cenário.

2. Nesse cenário, a Tailwind Traders deseja monitorar a integridade dos serviços do Azure que afetam todos os clientes ou os recursos implantados no Azure?

Nesse cenário, não há preocupação com operações. No entanto, **o Assistente do Azure analisa e dá recomendações para excelência operacional**.

3. Nesse cenário, a Tailwind Traders quer medir eventos personalizados em conjunto com outras métricas de uso?

Não, a medição de eventos personalizados não é mencionada como um requisito e não é uma consideração nesse cenário.

4. Neste cenário, a Tailwind Traders quer configurar alertas para interrupções ou quando o dimensionamento automático está prestes a implantar novas instâncias?

Novamente, não há preocupação com operações nesse cenário. No entanto, **o Assistente do Azure analisa e dá recomendações para excelência operacional**.

O Assistente do Azure é a opção de produto adequada para ajudar a Tailwind Traders a compreender e otimizar melhor os gastos com a nuvem e sua postura de segurança na nuvem. O produto também pode ajudar a organização com outras áreas de seu uso da nuvem.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/monitoring-fundamentals/4-use-azure-advisor)

## Usar o Azure Monitor

> **Cenário**:
>
> O site de comércio eletrônico da Tailwind Traders está apresentando erros intermitentes, e a equipe não tem certeza da causa. Devido à natureza dos erros, ela suspeita que seja um problema de banco de dados ou de cache. Quais são as circunstâncias relativas aos erros? Eles ocorrem somente nos horários de pico de uso? Qual é o estado da instância SQL do Azure da equipe? Qual é o estado do servidor de cache Redis? Como ela pode rastrear os problemas até a causa raiz?

### Qual serviço escolher?

1. Nesse cenário, a Tailwind Traders precisa de uma análise do uso que faz do Azure para fins de otimização?

Não, a otimização não é o objetivo da equipe nesse cenário; portanto, o Assistente do Azure não é um candidato.

2. Nesse cenário, a Tailwind Traders deseja monitorar a integridade dos serviços do Azure que afetam todos os clientes ou os recursos implantados no Azure?

Considerando que esse problema ocorre de forma intermitente, é improvável que ele afete uma região ou um serviço do Azure por completo. É mais provável que haja um problema lógico em alguma parte no código do site de comércio eletrônico ou que algum outro problema esteja causando falhas de banco de dados ou bloqueios de cache. **Nesse cenário, a equipe poderia usar o Azure Monitor para identificar uma sessão de usuário específica e examinar o desempenho de cada serviço envolvido no problema**.

3. Nesse cenário, a Tailwind Traders quer medir eventos personalizados em conjunto com outras métricas de uso?

Sim. Os desenvolvedores de software podem enviar informações adicionais sobre o estado do aplicativo Web por meio do Application Insights para ajudar a localizar a causa raiz do problema. O Application Insights se baseia na plataforma do Azure Monitor para armazenar informações de evento personalizado.

4. Nesse cenário, a Tailwind Traders quer configurar alertas para interrupções ou para quando o dimensionamento automático estiver prestes a implantar novas instâncias?

Não, o alerta não é o objetivo dela nesse cenário.

**O Azure Monitor é a melhor opção para ajudar a Tailwind Traders a rastrear esse problema intermitente**. A equipe pode usar uma infinidade de ferramentas para obter informações sobre o desempenho do aplicativo em um alto nível e se aprofundar em problemas específicos.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/monitoring-fundamentals/5-use-azure-monitor)

## Usar a Integridade do Serviço do Azure

> **Cenário**:
>
> A Tailwind Traders deseja operacionalizar seu ambiente de nuvem. Especificamente, a equipe de operações de nuvem deseja permitir que os stakeholders saibam sobre o futuro tempo de inatividade planejado com antecedência. A equipe também quer que seus arquitetos de solução sejam avisados com antecedência sobre quaisquer planos da Microsoft de descontinuar serviços para que possam rearquitetar seus produtos de software de maneira adequada.
>
> Em caso de interrupções, a equipe quer verificar rapidamente se o problema é específico de seus serviços ou se é uma interrupção de serviço que afeta muitos clientes do Azure. Ela também deseja fornecer relatórios aos principais stakeholders explicando como e por que o incidente ocorreu e assim por diante.

### Qual serviço escolher?

1. Nesse cenário, a Tailwind Traders precisa analisar o próprio uso do Azure para fins de otimização?

Não. Portanto, o Assistente do Azure não é um candidato para esse cenário.

2. A Tailwind Traders deseja monitorar a integridade dos serviços do Azure que afetam todos os clientes ou os recursos implantados no Azure?

Nesse cenário, **o requisito é manter-se atualizado sobre o tempo de inatividade planejado futuro. Além disso, a equipe deseja capturar relatórios oficiais de incidentes. Por esse motivo, a Integridade do Serviço do Azure é o candidato mais forte a ser escolhido para esse cenário**.

3. Nesse cenário, a Tailwind Traders quer medir eventos personalizados em conjunto com outras métricas de uso?

Não, a medição de eventos personalizados não é mencionada como um requisito e não é uma consideração nesse cenário.

4. Neste cenário, a Tailwind Traders quer configurar alertas para interrupções ou quando o dimensionamento automático está prestes a implantar novas instâncias?

A configuração de alertas para interrupções é um requisito nesse cenário, mas a criação de alertas para outros eventos, como o dimensionamento automático, não está no escopo.

**Use a Integridade do Serviço do Azure para configurar alertas específicos para interrupções do Azure que afetam todos os clientes do Azure.**

**Use o Azure Monitor para configurar alertas para interrupções e outros eventos que afetam apenas seus recursos específicos.**

Nesse cenário, a Integridade do Serviço do Azure é a opção correta a escolher.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/monitoring-fundamentals/6-use-azure-service-health)

> ## [Próximo](./M13_2_Resumo.md)
