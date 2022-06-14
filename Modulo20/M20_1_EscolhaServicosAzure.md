# Escolha os serviços do Azure certos examinando SLAs e ciclo de vida do serviço

## O que são SLAs (Contratos de Nível de Serviço)?

> ### **Um SLA (Contrato de Nível de Serviço) é um contrato formal entre uma empresa de serviços e o cliente.**
>
> No caso do Azure, esse contrato define os padrões de desempenho com os quais a Microsoft se compromete a fornecer para você, o cliente.

### Por que os SLAs são importantes?

Entender o SLA para cada serviço do Azure usado ajuda a entender que garantias você pode esperar.

Quando você cria aplicativos no Azure, a disponibilidade dos serviços usados afeta o desempenho do aplicativo. Entender os SLAs envolvidos pode ajudar a estabelecer o SLA definido com seus clientes.

### Em que local posso acessar os SLAs para os serviços do Azure?

Você pode acessar os SLAs em Contratos de Nível de Serviço.

    Observação: Você não precisa de uma assinatura do Azure para examinar os SLAs de serviço.

Cada serviço do Azure define o próprio SLA. Os serviços do Azure são organizados em categorias.

Abra o SLA para o Banco de Dados do Azure para MySQL, um banco de dados gerenciado que torna mais fácil para os desenvolvedores trabalharem com Banco de Dados MySQL. Você voltará a consultar esse SLA em instantes.

Para fazer isso:

    Acesse Contratos de Nível de Serviço.
    Na categoria Bancos de Dados, selecione Banco de Dados do Azure para MySQL.

### O que há em um SLA típico?

Um SLA típico divide-se nestas seções:

- **Introdução**: explica o que esperar desse SLA, incluindo o escopo e como as renovações de assinatura podem afetar os termos.

- **Termos gerais**: contém termos que são usados em todo o SLA para que ambas as partes (você e a Microsoft) tenham um vocabulário consistente. Por exemplo, esta seção pode definir o que significa tempo de inatividade, incidentes e códigos de erro.
  Também define os termos gerais do contrato, incluindo como enviar um requerimento, receber crédito por problemas de desempenho ou disponibilidade e limitações do contrato.

- **Detalhes de SLA** : define as garantias específicas para o serviço. Os compromissos de desempenho geralmente são medidos como um percentual. Essa porcentagem normalmente varia de 99,9% ("três noves") a 99,99% ("quatro noves").
  O principal compromisso de desempenho geralmente se concentra em tempo de atividade ou no percentual de tempo em que um produto ou serviço está funcionando com êxito. Alguns SLAs se concentram também em outros fatores, incluindo latência ou quão rápido o serviço deve responder a uma solicitação.
  Esta seção também define quaisquer termos adicionais específicos para esse serviço.

### Como os percentuais estão relacionados ao tempo de inatividade total?

O _tempo de inatividade_ refere-se à duração da indisponibilidade do serviço.

A diferença entre 99,9% e 99,99% pode parecer pequena, mas é importante entender o que esses números significam em termos de tempo de inatividade total.

Esses valores são cumulativos, o que significa que a duração de várias interrupções de serviço diferentes é combinada ou somada.

### O que são créditos de serviço?

Um crédito do serviço é o percentual dos valores pagos que são creditados de volta para você de acordo com o processo de aprovação da declaração.

Um SLA descreve como a Microsoft responde quando o desempenho de um serviço do Azure não cumpre as especificações. Por exemplo, você pode receber um desconto em sua fatura do Azure como compensação quando um serviço não tem desempenho de acordo com o SLA.

Normalmente, os créditos aumentam conforme o tempo de atividade diminui.

### Qual é o SLA para serviços gratuitos?

Produtos gratuitos normalmente não têm um SLA.

Por exemplo, muitos serviços do Azure fornecem uma camada gratuita ou compartilhada que fornece funcionalidade mais limitada. Serviços como o Assistente do Azure sempre são gratuitos. O SLA para o Assistente do Azure declara que, por ser gratuito, ele não tem um SLA com suporte financeiro.
Como saber quando há uma interrupção?

O status do Azure fornece uma exibição global da integridade dos serviços e regiões do Azure. A suspeita de uma interrupção geralmente é um bom ponto de partida para a investigação.

O status do Azure fornece um RSS feed de alterações à integridade dos serviços do Azure que você pode assinar. Você pode conectar esse feed a um software de comunicação, como o Microsoft Teams ou o Slack.

Na página de status do Azure, você também pode acessar a Integridade do Serviço do Azure. Ela fornece uma exibição personalizada da integridade dos serviços e das regiões do Azure que você está usando diretamente no portal do Azure.

### Como posso solicitar um crédito de serviço da Microsoft?

Normalmente, você precisa registrar um requerimento com a Microsoft para receber um crédito de serviço. Se você comprar os serviços do Azure de um parceiro CSP (Provedor de Soluções na Nuvem), o CSP normalmente gerenciará o processo de reivindicações.

Cada SLA especifica o prazo até o qual você deve enviar seu requerimento e quando a Microsoft o processará. Para muitos serviços, você deve enviar seu requerimento até o final do mês do calendário após o mês em que o incidente ocorreu.

Em seguida, vamos analisar alguns outros fatores que a Tailwind Traders precisa considerar que podem afetar as metas de desempenho do SLA.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/choose-azure-services-sla-lifecycle/2-what-are-service-level-agreements)

## Definir o SLA do aplicativo

Um SLA aplicativo define os requisitos de SLA para um aplicativo específico. Esse termo geralmente se refere a um aplicativo que você compilar no Azure.

### Impacto aos negócios

Se o aplicativo falhar, qual será o impacto aos negócios?

### Efeito sobre outras operações de negócios

O aplicativo afeta outras operações? A maioria dos negócios da empresa continuaria a funcionar normalmente se o aplicativo em questão ficasse inoperante?

### Padrões de uso

Os padrões de uso definem quando e como os usuários acessam seu aplicativo.

Uma questão a ser considerada é se o requisito de disponibilidade é diferente entre períodos críticos e não críticos. Por exemplo, um aplicativo de declaração de imposto não pode falhar durante um prazo de entrega da declaração.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/choose-azure-services-sla-lifecycle/3-define-application-sla)

## Projetar seu aplicativo para atender ao seu SLA

### Identificar suas cargas de trabalho

> ### **Uma carga de trabalho é uma funcionalidade ou tarefa distinta logicamente separada de outras tarefas em termos de requisitos de armazenamento de dados e lógica de negócios**. Cada carga de trabalho define um conjunto de requisitos de disponibilidade, escalabilidade, consistência de dados e recuperação de desastres.

Depois de identificar o SLA para as cargas de trabalho individuais no aplicativo, você pode observar que esses SLAs não são todos iguais. Como isso afeta nosso requisito geral de SLA de aplicativo de 99,9%? Para resolver isso, você precisará fazer alguns cálculos.

O processo de combinar SLAs ajuda a computar o SLA composto para um conjunto de serviços. A computação do SLA composto exige que você multiplique o SLA de cada serviço individual.

Em Contratos de Nível de Serviço, você descobre o SLA para cada serviço do Azure de que precisa.

Observe que, embora todos os serviços individuais tenham SLAs iguais ou melhores que o SLA de aplicativo, a combinação deles resulta em um número geral menor do que o percentual de 99,9% necessário. Por quê? Isso acontece por que usar vários serviços adiciona um nível de complexidade e aumenta levemente o risco de falha.

### O que acontece quando o SLA composto não atende às suas necessidades?

#### Escolher as opções de personalização que atendam ao SLA necessário

Cada uma das cargas de trabalho definidas anteriormente tem o próprio SLA, e as opções de personalização feitas ao provisionar cada carga de trabalho afetam o SLA. Por exemplo:

- **Discos**: Com as Máquinas Virtuais, você pode escolher entre um disco gerenciado HDD Standard, um disco gerenciado SSD Standard, um SSD Premium ou um Disco Ultra. O SLA para uma única VM seria de 95%, 99,5% ou 99,9%, dependendo da escolha do disco.

- **Camadas**: Alguns serviços do Azure são oferecidos como um produto de camada gratuita e como um serviço pago padrão. Por exemplo, a Automação do Azure fornece 500 minutos de runtime de trabalho em uma conta gratuita do Azure, mas não tem o suporte de um SLA. O SLA da camada Standard para a Automação do Azure é de 99,9%.

Suas decisões de compra devem levar em conta o impacto sobre o SLA para os serviços do Azure escolhidos. Isso garante que o SLA dê suporte ao SLA de aplicativo necessário.

### Insira requisitos de disponibilidade no design

Há considerações de design de aplicativo que você pode usar com relação à infraestrutura de nuvem subjacente.

Por exemplo, para melhorar a disponibilidade do aplicativo, evite pontos únicos de falha. Assim, em vez de adicionar mais máquinas virtuais, você pode implantar uma ou mais instâncias adicionais da mesma máquina virtual em diferentes zonas de disponibilidade na mesma região do Azure.

Uma zona de disponibilidade é um local físico exclusivo dentro de uma região do Azure. Cada zona é composta por um ou mais datacenters equipados com energia, resfriamento e rede independentes. Essas zonas usam agendas diferentes para manutenção, ou seja, se uma zona for afetada, sua instância de máquina virtual na outra zona não será afetada.

A implantação de duas ou mais instâncias de uma máquina virtual do Azure em duas ou mais zonas de disponibilidade eleva o SLA da máquina virtual a 99,99%.

### Incluir redundância para aumentar a disponibilidade

Para garantir alta disponibilidade, você pode planejar que seu aplicativo tenha componentes duplicados em várias regiões, o que é conhecido como redundância. Por outro lado, para minimizar os custos durante períodos não críticos, você pode executar o aplicativo somente em uma única região. A Tailwind Traders poderá considerar isso se houver uma tendência de que as taxas de pedidos especiais sejam muito maiores durante determinados meses ou estações.

Para alcançar a disponibilidade máxima em seu aplicativo, adicione redundância a cada parte do aplicativo. Essa redundância inclui o próprio aplicativo, bem como os serviços e a infraestrutura subjacentes. No entanto, esteja ciente de que isso pode ser difícil e caro e, muitas vezes, resulta em soluções desnecessariamente complexas.

Considere a importância da alta disponibilidade para seus requisitos antes de adicionar redundância. Pode haver maneiras mais simples de cumprir o SLA do aplicativo.

### É difícil alcançar um desempenho muito alto

Metas de desempenho acima de 99,99% são muito difíceis de alcançar. Um SLA de 99,99% significa ter 1 minuto de tempo de inatividade por semana. É difícil seres humanos responderem a falhas com rapidez suficiente para cumprir metas de desempenho de SLA superiores a 99,99%. Em vez disso, seu aplicativo deve ser capaz de realizar os próprios diagnósticos e reparos durante uma interrupção.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/choose-azure-services-sla-lifecycle/4-design-application-meet-sla)

## Acessar versões prévias dos recursos e dos serviços

Como os serviços do Azure passam da fase de visualização para o produto em disponibilidade geral no Azure.

### O que é o ciclo de vida do serviço?

> ### O ciclo de vida do serviço define como cada serviço do Azure é liberado para uso público.

Cada serviço do Azure começa na fase de desenvolvimento. Nesta fase, a equipe do Azure coleta e define seus requisitos e começa a criar o serviço.

Em seguida, o serviço é liberado para a fase de versão prévia pública. Durante essa fase, o público pode acessá-lo, experimentá-lo e fornecer comentários reais. Seus comentários ajudam a Microsoft a melhorar os serviços. O mais importante é que fornecer comentários lhe dá a oportunidade de solicitar funcionalidades novas ou diferentes para que os serviços atendam melhor às suas necessidades.

Depois que um novo serviço do Azure for validado e testado, ele será liberado a todos os clientes como um serviço pronto para produção. Isso é conhecido como GA (disponibilidade geral).

### Quais termos e condições posso esperar?

Cada versão prévia do Azure define os próprios termos e condições. Todos os termos e condições específicos da versão prévia estão excluídos dos contratos de nível de serviço e da garantia limitada.

Algumas versões prévias podem não estar cobertas pelo suporte ao cliente e podem estar sujeitas a compromissos de segurança, conformidade e privacidade reduzidos ou diferentes. Por esses motivos, as versões prévias não são recomendadas para cargas de trabalho comercialmente críticas.
Como posso acessar as versões prévias dos serviços?

Você pode acessar as versões prévias dos serviços pelo portal do Azure.

É assim que você pode ver quais versões prévias dos serviços estão disponíveis. Você poderá acompanhar se tiver uma assinatura do Azure.

1. Acesse o portal do Azure e entre.
2. Selecione Criar um recurso.
3. Insira versão prévia na caixa de pesquisa e selecione Enter.
4. Selecione um serviço de versão prévia para saber mais sobre ele. Você também poderá iniciar o serviço se quiser experimentá-lo.

### Como posso acessar novos recursos para um serviço?

Algumas versões prévias dos recursos estão relacionadas a uma área específica de um serviço do Azure. Por exemplo, um serviço de computação ou banco de dados que você usa diariamente pode fornecer funcionalidade aprimorada. Essas versões prévias dos recursos podem ser acessadas quando você implanta, configura e gerencia o serviço.

Embora seja possível um recurso de versão prévia do Azure em produção, esteja ciente das limitações antes de implantá-lo em um ambiente de produção.

### Como posso acessar as versões prévias dos recursos para o portal do Azure?

Você pode acessar as versões prévias dos recursos específicas para o portal do Azure em Microsoft Azure (versão prévia).

As versões prévias de recursos do portal típicas fornecem aprimoramentos de desempenho, navegação e acessibilidade para a interface do portal do Azure.

Quando você estiver usando a versão prévia do portal do Azure, o elemento Microsoft Azure (versão prévia) será exibido no cabeçalho da página para lembrar qual versão do portal do Azure você está usando. As versões prévias públicas dos recursos que estão disponíveis opcionalmente também são rotuladas com (versão prévia) nas páginas do Azure.

### Como posso fornecer comentários sobre o portal do Azure?

Você pode fornecer comentários:

1. Em um dos 124 fóruns dos serviços do Azure, acesse a página de ideias da comunidade de comentários do Azure
2. Na guia Comentários no portal do Azure.
3. Screenshot of the Azure portal showing the Feedback tab.

### Como posso ficar atualizado sobre os comunicados mais recentes?

A página de atualizações do Azure oferece informações sobre as atualizações mais recentes de produtos, serviços e recursos do Azure, bem como roteiros de produto e anúncios.

Na página Atualizações do Azure, você pode:

- Exibir detalhes sobre todas as atualizações do Azure.
- Veja quais atualizações estão disponíveis, em versão prévia ou em desenvolvimento no momento. Screenshot of the Azure updates page showing how to filter services by now available, in preview, or in development.
- Procurar atualizações pela categoria de produto ou pelo tipo de atualização.
- Pesquisar atualizações por palavra-chave.
- Assinar um RSS feed para receber notificações.
- Acesse a página do Microsoft Connect para ler anúncios e notícias sobre os produtos do Azure.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/choose-azure-services-sla-lifecycle/5-access-preview-services)

> ## [Próximo](./M20_2_Resumo.md)
