# Planeje e gerencie seus custos do Azure

## Comparar custos usando a Calculadora de custo total de propriedade

### O que é a Calculadora de TCO?

> ### A [Calculadora de TCO](https://azure.microsoft.com/pt-br/pricing/tco/calculator/) ajuda a estimar a economia de custos de operar sua solução no Azure ao longo do tempo em comparação com a operação no datacenter local.

O termo custo total de propriedade normalmente é usado em finanças. Pode ser difícil ver todos os custos ocultos relacionados à operação de um recurso tecnológico local. As licenças de software e o hardware são custos adicionais.

Com a Calculadora de TCO, você insere os detalhes de suas cargas de trabalho locais. Em seguida, você examina o custo médio sugerido do setor (que pode ser ajustado) relativo aos custos operacionais relacionados. Esses custos incluem luz, manutenção de rede e pessoal de TI. Você verá um relatório lado a lado. Usando o relatório, você pode comparar esses custos com as mesmas cargas de trabalho em execução no Azure.

    Observação: Você não precisa de uma assinatura do Azure para trabalhar com a Calculadora de TCO.

### Como funciona a Calculadora de TCO?

Trabalhar com a Calculadora de TCO envolve três etapas:

- Definir suas cargas de trabalho
- Ajustar as suposições
- Exibir o relatório

#### **Etapa 1: Definir suas cargas de trabalho**

Primeiro, você insere as especificações da sua infraestrutura local na Calculadora de TCO com base nestas quatro categorias:

- Servidores: inclui sistemas operacionais, métodos de virtualização, núcleos de CPU e memória (RAM).

- Bancos de dados: inclui tipos de banco de dados, hardware de servidor e o serviço do Azure que você deseja usar, que inclui o máximo de credenciais de usuário simultâneos esperadas.

- Storage: inclui o tipo de armazenamento e a capacidade, que inclui backups ou armazenamentos de arquivos.

- Rede: inclui a quantidade de largura de banda de rede que você consome atualmente no seu ambiente local.

#### **Etapa 2: Ajustar as suposições**

Em seguida, especifique se suas licenças locais atuais estão inscritas para Software Assurance, o que pode economizar dinheiro reutilizando essas licenças no Azure. Você também especifica se precisa replicar o armazenamento para outra região do Azure para maior redundância.

Em seguida, você pode ver as principais suposições de custo operacional em várias áreas diferentes, que variam entre equipes e organizações. Esses custos foram certificados pela Nucleus Research, uma empresa de pesquisa independente. Por exemplo, esses custos incluem:

- Preço da eletricidade por quilowatts/hora (KWh)
- Taxa de pagamento por hora para a administração de TI
- Custo de manutenção de rede como um percentual de custos de hardware e software de rede

Para aumentar a precisão dos resultados da Calculadora de TCO, você pode ajustar os valores para que correspondam aos custos da sua infraestrutura local atual.

#### **Etapa 3: Exibir o relatório**

Escolha um período entre um e cinco anos. A Calculadora de TCO gera um relatório com base nas informações inseridas. Aqui está um exemplo:

Para cada categoria (computação, datacenter, rede, armazenamento e mão de obra de TI), você também pode exibir uma comparação lado a lado do detalhamento de custo de operar essas cargas de trabalho localmente, em vez de no Azure.

Você pode baixar, compartilhar ou salvar este relatório para examinar mais tarde.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/plan-manage-azure-costs/2-compare-costs-tco-calculator)

## Comprar serviços do Azure

### Que tipos de assinaturas do Azure posso usar?

Você provavelmente sabe que uma assinatura do Azure dá acesso aos recursos do Azure, como VMs (máquinas virtuais), armazenamento e bancos de dados. Os tipos de recursos que você usa afetam sua fatura mensal.

O Azure oferece opções de assinatura gratuitas e pagas para atender às suas necessidades e requisitos. Eles são:

- **Avaliação gratuita**: Uma assinatura de avaliação gratuita fornece 12 meses de serviços gratuitos populares, um crédito para explorar qualquer serviço do Azure por 30 dias e mais de 25 serviços que são sempre gratuitos. Os serviços do Azure são desabilitados quando a avaliação termina ou quando seu crédito expira para produtos pagos, a menos que você atualize para uma assinatura paga.

- **Pago conforme o uso**: Uma assinatura com Pagamento Conforme o Uso permite que você pague pelo que usar vinculando um cartão de crédito ou débito à sua conta. As organizações podem se candidatar a descontos por volume e a faturamento pré-pago.

- **Ofertas de membro**: Sua associação existente a determinados produtos e serviços da Microsoft pode fornecer créditos para sua conta do Azure e taxas reduzidas nos serviços do Azure. Por exemplo, ofertas de membros estão disponíveis para assinantes do Visual Studio, membros da Microsoft Partner Network, membros da Microsoft para Startups e membros do Microsoft Imagine.

### Como comprar serviços do Azure?

Há três maneiras principais de comprar serviços no Azure. Eles são:

- **Por meio de um Contrato Enterprise**: Clientes maiores, conhecidos como clientes corporativos, podem assinar um Contrato Enterprise com a Microsoft. Esse contrato os obriga a gastar um valor predeterminado nos serviços do Azure durante um período de três anos. O valor de serviço geralmente é pago anualmente. Como um cliente com Contrato Enterprise, você receberá o melhor preço personalizado conforme os tipos e as quantidades de serviços que planeja usar.

- **Diretamente da Web**: Aqui, você pode comprar os serviços do Azure diretamente do site do portal do Azure e pagar os preços padrão. Você é cobrado mensalmente, como um pagamento de cartão de crédito ou por uma fatura. Esse método de compra é conhecido como Web Direct.

- **Por meio de um Provedor de Soluções na Nuvem**: Um CSP (Provedor de Soluções na Nuvem) é um parceiro da Microsoft que ajuda você a criar soluções com base no Azure. Seu CSP cobra seu uso do Azure a um preço que ele determina. Ele também responde às suas perguntas de suporte e as encaminha à Microsoft conforme a necessidade.

Você pode abrir ou provisionar, recursos do Azure do portal do Azure ou da linha de comando. O portal do Azure organiza produtos e serviços em categorias. Você pode selecionar os serviços que atendem às suas necessidades. Sua conta é cobrada de acordo com o modelo "pagar pelo que usar" do Azure.

No final de cada mês, você será cobrado pelo que usou. A qualquer momento, você pode verificar a página Gerenciamento de Custos e Cobrança no portal do Azure para obter um resumo do uso atual e examinar faturas de meses anteriores.

### Quais fatores afetam o custo?

A maneira como você usa recursos, seu tipo de assinatura e preços de fornecedores de terceiros são fatores comuns. Vamos dar uma olhada rápida em cada um.

#### **Tipo de recurso**

Vários fatores influenciam o custo dos recursos do Azure. Eles dependem do tipo de recurso ou de como você o personaliza.

Por exemplo, com uma conta de armazenamento, você especifica um tipo (como armazenamento de blobs de blocos ou de tabelas), um nível de desempenho (Standard ou Premium) e uma camada de acesso (frequente, esporádico ou arquivos). Essas seleções apresentam custos diferentes.

#### **Medidores de uso**

Quando você provisiona um recurso, o Azure cria medidores para acompanhar o uso desse recurso. O Azure usa esses medidores para gerar um registro de uso que depois é usado para ajudar a calcular sua fatura.

Considere os medidores de uso como semelhantes a como você usa a eletricidade ou a água em sua casa. Você pode pagar um preço base por mês para o serviço de energia ou água, mas sua fatura final é baseada no valor total que você consumiu.

Vamos examinar uma única VM como exemplo. Os seguintes tipos de medidores são relevantes para acompanhar seu uso:

- Tempo geral da CPU
- Tempo gasto com um endereço IP público
- Tráfego de rede de entrada (ingresso) e saída (egresso) da VM
- Tamanho do disco e quantidade de operações de leitura e gravação no disco

Cada medidor rastreia um tipo específico de uso. Por exemplo, um medidor pode acompanhar o uso de largura de banda (tráfego de rede de entrada ou saída em bits por segundo), o número de operações ou seu tamanho (capacidade de armazenamento em bytes).

O uso que um medidor acompanha está correlacionado a uma quantidade de unidade cobráveis. Essas unidades são cobradas em sua conta para cada período de cobrança. A taxa por unidade faturável depende do tipo de recurso que você está usando.

#### **Uso de recursos**

No Azure, você sempre será cobrado conforme o que usa. Como exemplo, vejamos como essa cobrança se aplica à desalocação de uma VM.

No Azure, você pode excluir ou desalocar uma VM. A exclusão de uma VM significa que você não precisa mais dela. A VM é removida da assinatura e é preparada para outro cliente.

A desalocação de uma VM significa que a VM não está mais em execução, mas os discos rígidos e os dados associados ainda são mantidos no Azure. A VM não está atribuída a uma CPU ou rede no datacenter do Azure e, portanto, não gera os custos associados ao tempo de computação ou ao endereço IP da VM. Como os discos e os dados ainda estão armazenados e o recurso está presente em sua assinatura do Azure, você ainda será cobrado pelo armazenamento em disco.

Desalocar uma VM quando você não planeja usá-la por algum tempo é apenas uma forma de minimizar os custos. Por exemplo, você pode desalocar as VMs usadas para teste nos finais de semana quando sua equipe de teste não as usa. Você aprenderá outras maneiras de minimizar o custo mais adiante neste módulo.

#### **Tipos de assinaturas do Azure**

Alguns tipos de assinatura do Azure também incluem as concessões de uso, que afetam os custos.

Por exemplo, uma assinatura de avaliação gratuita do Azure fornece acesso a vários produtos do Azure gratuitos por 12 meses. Ele também inclui crédito a ser gasto em seus primeiros 30 dias de inscrição. Você também obtém acesso a mais de 25 produtos que sempre são gratuitos (com base na disponibilidade de recursos e regiões).

#### **Azure Marketplace**

Você também pode comprar soluções e serviços baseados no Azure de fornecedores terceirizados por meio do Azure Marketplace. Os exemplos incluem dispositivos de firewall de rede gerenciados ou conectores para serviços de backup de terceiros. As estruturas de cobrança são definidas pelo fornecedor.

### O local ou o tráfego de rede afeta o custo?

Ao provisionar um recurso no Azure, você precisa definir o local (conhecido como a região do Azure) de onde ele será implantado. Vamos ver por que essa decisão pode ter consequências de custo.

#### **Location**

A infraestrutura do Azure é distribuída globalmente, o que permite que você implante serviços centralmente ou os provisione mais perto de onde os clientes os usam.

Regiões diferentes podem ter preços associados diferentes. Como as regiões geográficas podem afetar o local em que o tráfego de rede flui, o tráfego de rede é uma influência de custo a ser considerada também.

Por exemplo, digamos que a Tailwind Traders decida provisionar seus recursos do Azure nas regiões do Azure que ofereçam os preços mais baixos. Essa decisão economizaria algum dinheiro para a empresa. No entanto, se a empresa precisar transferir dados entre essas regiões ou se os usuários estiverem em diferentes partes do mundo, qualquer economia potencial poderá ser contrabalançada pelos custos de uso de rede adicionais da transferência de dados entre esses recursos.

#### **Zonas para cobrança de tráfego de rede**

As zonas de cobrança são um fator para determinar o custo de alguns serviços do Azure.

A largura de banda refere-se aos dados que entram e saem dos datacenters do Azure. Algumas transferências de dados de entrada (dados que entram em datacenters do Azure) são gratuitas. Para transferências de dados de saída (dados que saem de data centers do Azure), o preço de transferência de dados é baseado em zonas.

Uma zona é um agrupamento geográfico de regiões do Azure para fins de cobrança. As seguintes zonas incluem algumas das regiões, como mostrado aqui:

- Zona 1: Austrália Central, Oeste dos EUA, Leste dos EUA, Oeste do Canadá, Oeste da Europa, França Central e outros
- Zona 2: Leste da Austrália, Oeste do Japão, Índia Central, Sul da Coreia e outros
- Zona 3: Sul do Brasil, Norte da África do Sul, Oeste da África do Sul, EAU Central, Norte dos EAU
- Alemanha Zona 1: Alemanha Central e Nordeste da Alemanha

### Como posso estimar o custo total?

Como você aprendeu, uma estimativa de custo preciso leva todos os fatores anteriores em conta. Felizmente, a [calculadora de preços do Azure](https://azure.microsoft.com/pt-br/pricing/calculator/) ajuda nesse processo.

A calculadora de preços exibe produtos do Azure em categorias. Você pode adicionar essas categorias à sua estimativa e configurar de acordo com seus requisitos específicos. Em seguida, você receberá um preço estimado consolidado, com uma análise detalhada dos custos associados a cada recurso que adicionou à sua solução. Você pode exportar ou compartilhar essa estimativa ou salvá-la para depois. Você pode carregar uma estimativa salva e modificá-la conforme os requisitos atualizados.

Você também pode acessar os detalhes de preços, os detalhes do produto e a documentação de cada produto de dentro da calculadora de preços.

As opções que você pode configurar na calculadora de preços variam entre os produtos, mas podem incluir:

- **Região**: Uma região é a localização geográfica na qual você pode provisionar um serviço. Sudeste da Ásia, Canadá Central, Oeste dos Estados Unidos e Norte da Europa são alguns exemplos.

- **Camada**: Camadas, como a Camada gratuita, a Camada básica e assim por diante, têm níveis diferentes de disponibilidade ou desempenho e custos associados diferentes.

- **Opções de cobrança**: As opções de cobrança realçam as diferentes maneiras de pagar por um serviço. As opções podem variar com base no tipo de cliente e no tipo de assinatura e podem incluir alternativas para economizar custos.

- **Opções de suporte**: Essas opções permitem que você selecione alternativas de preços de suporte adicionais para determinados serviços.

- **Programas e ofertas**: Seu tipo de cliente ou assinatura pode permitir que você escolha programas de licenciamento específicos ou outras ofertas.

- **Preço de Desenvolvimento/Teste do Azure**: Essa opção lista os preços disponíveis para cargas de trabalho de desenvolvimento e teste. O preço de Desenvolvimento/Teste se aplica quando você executa recursos dentro de uma assinatura do Azure que se baseia em uma oferta de desenvolvimento/teste.

Lembre-se de que a calculadora de preços fornece estimativas, não cotações de preços reais. Os preços reais podem variar conforme a data de compra, a moeda de pagamento que você está usando e o tipo de cliente do Azure que é.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/plan-manage-azure-costs/4-purchase-azure-services)

## Gerenciar e minimizar o custo total no Azure

### Entenda os custos estimados antes de implantar

Para ajudá-lo a planejar sua solução no Azure, considere cuidadosamente os produtos, serviços e recursos de que você precisa. Leia a documentação pertinente para entender como cada uma das suas escolhas é medida e cobrada.

Calcule os custos projetados usando a calculadora de preços e a Calculadora de TCO (custo total de propriedade). Adicione somente os produtos, os serviços e os recursos necessários para sua solução.

### Use o Assistente do Azure para monitorar seu uso

Idealmente, você deseja que os recursos provisionados correspondam ao uso real.

O Assistente do Azure identifica recursos não utilizados ou subutilizados e recomenda recursos não utilizados que podem ser removidos. Essa informação ajuda a configurar seus recursos para que correspondam à carga de trabalho real.

As recomendações são classificadas por impacto: alto, médio ou baixo. Em alguns casos, o Assistente do Azure pode corrigir o problema subjacente de modo automático. Outros problemas, como os dois listados como alto impacto, exigem intervenção humana.

### Use limites de gastos para restringir seus gastos

Se você tiver uma avaliação gratuita ou uma assinatura do Azure baseada em crédito, poderá usar limites de gastos para evitar excesso inadvertido.

Por exemplo, quando você gasta todo o crédito incluído com sua conta gratuita do Azure, os recursos do Azure implantados são removidos da produção e as VMs (máquinas virtuais) do Azure são interrompidas e desalocadas. Os dados em suas contas de armazenamento ficam disponíveis como somente leitura. Neste ponto, você pode atualizar sua assinatura de avaliação gratuita para uma assinatura com Pagamento Conforme o Uso.

Se você tiver uma assinatura baseada em crédito e alcançar seu limite de gastos configurado, o Azure suspenderá sua assinatura até que um novo período de cobrança comece.

Um conceito relacionado é de cotas, ou limites ao número de recursos semelhantes que você pode provisionar em sua assinatura. Por exemplo, você pode alocar até 25.000 VMs por região. Esses limites ajudam principalmente a Microsoft a planejar a capacidade do datacenter.

### Usar Reservas do Azure para pagar antecipadamente

As Reservas do Azure oferecem preços com desconto em determinados serviços do Azure. As Reservas do Azure podem economizar até 72% em comparação aos preços pagos conforme o uso. Para receber um desconto, você pode reservas serviços e recursos pagando com antecedência.

Por exemplo, você pode pagar antecipadamente por um ano ou três anos de uso de VMs, capacidade de computação de banco de dados, taxa de transferência de banco de dados e outros recursos do Azure.

As Reservas do Azure estão disponíveis para clientes com um Contrato Enterprise, provedores de soluções na nuvem e assinaturas com Pagamento Conforme o Uso.

### Escolher regiões e locais de baixo custo

O custo de produtos, serviços e recursos do Azure pode variar em locais e regiões. Se possível, você deve usá-los nos locais e nas regiões onde custam menos.

Porém, lembre-se de que alguns recursos são medidos e cobrados de acordo com a quantidade de largura de banda de rede de saída (egresso) que consomem. Você deve provisionar recursos conectados que são medidos por largura de banda na mesma região do Azure para reduzir o tráfego de saída entre eles.

### Pesquisar ofertas econômicas disponíveis

Mantenha-se atualizado com as ofertas de cliente e assinatura do Azure mais recentes e mude para ofertas que ofereçam o maior benefício de economia de custo.

Use o Gerenciamento de Custos e Cobranças da Microsoft para controlar os gastos

O Gerenciamento de Custos é um serviço gratuito que ajuda você a entender sua fatura do Azure, gerenciar sua conta e assinaturas, monitorar e controlar os gastos do Azure e otimizar o uso de recursos.

Os recursos de Gerenciamento de Custos incluem:

- Relatórios: Use dados históricos para gerar relatórios e prever o uso e as despesas futuras.

- Enriquecimento de dados: Melhore a responsabilidade classificando os recursos com marcas que correspondam a unidades organizacionais e de negócios do mundo real.

- Orçamentos: Crie e gerencie orçamentos de custo e uso monitorando tendências de demanda de recursos, taxas de consumo e padrões de custo.

- Alertas: Obtenha alertas conforme seus orçamentos de custo e uso.

- Recomendações: Receba recomendações para eliminar recursos ociosos e otimizar os recursos do Azure que você provisiona.

Aplique marcas para identificar os proprietários de custo

As marcas ajudam a gerenciar os custos associados aos diferentes grupos de produtos e recursos do Azure. Você pode aplicar marcas a grupos de recursos do Azure para organizar dados de cobrança.

Por exemplo, se você executar várias VMs para equipes diferentes, poderá usar marcas para classificar os custos por departamento, como recursos humanos, marketing ou financeiro, ou por ambiente, como teste ou produção.

As marcas facilitam a identificação dos grupos que geram os maiores custos do Azure, o que pode ajudar você a ajustar seus gastos de acordo.

### Redimensionar máquinas virtuais subutilizadas

Uma recomendação comum que você encontrará no Gerenciamento de Custos e no Assistente do Azure é redimensionar ou desligar as VMs que estão subutilizadas ou ociosas.

Por exemplo, digamos que você tenha uma VM cujo tamanho seja Standard_D4_v4, um tipo de VM de uso geral com quatro vCPUs e 16 GB de memória. Você pode descobrir que essa VM fica ociosa 90% do tempo.

Os custos de máquinas virtuais são lineares, custando o dobro para cada tamanho maior da mesma série. Nesse caso, se você reduzir o tamanho da VM de Standard_D4_v4 para Standard_D2_v4, que é o próximo menor tamanho, reduzirá o custo de computação em 50%.

Lembre-se de que redimensionar uma VM exige que ela seja interrompida, redimensionada e então reiniciada. Esse processo pode levar alguns minutos, dependendo de quão significativa é a alteração de tamanho.

Planeje-se adequadamente uma interrupção ou desloque o tráfego para outra instância enquanto executa operações de redimensionamento.

### Desalocar máquinas virtuais durante horas de inatividade

Lembre-se de que desalocar uma VM significa não executar mais a VM, mas preservar os discos rígidos e os dados associados no Azure.

Se você tem cargas de trabalho de VM usadas apenas durante determinados períodos, mas está executando-as durante todas as horas de todos os dias, está perdendo dinheiro. Essas VMs são excelentes candidatas a serem desligadas quando não estão em uso e reiniciadas conforme necessário, economizando custos de computação enquanto a VM fica desalocada.

Essa abordagem é uma excelente estratégia para ambientes de desenvolvimento e teste, em que as VMs são necessárias somente no horário comercial. O Azure oferece, inclusive, uma forma de iniciar e parar automaticamente suas VMs conforme um agendamento.

### Excluir recursos não utilizados

Essa recomendação pode parecer óbvia, mas se você não estiver usando um recurso, deverá desativá-lo. Não é incomum encontrar sistemas de não produção ou de prova de conceito que não sejam mais necessários após a conclusão de um projeto.

Analise regularmente seu ambiente e trabalho para identificar esses sistemas. Desligar esses sistemas pode ter um benefício duplo, economizando custos de infraestrutura e, possivelmente, custos de licenciamento e operações.

### Migrar de IaaS para serviços PaaS

À medida que você move as cargas de trabalho para a nuvem, uma evolução natural é começar com serviços de IaaS (infraestrutura como serviço) porque eles são mapeados mais diretamente para conceitos e operações com as quais você já está familiarizado.

Ao longo do tempo, uma forma de reduzir os custos é migrar gradualmente as cargas de trabalho de IaaS para serem executadas em serviços PaaS (plataforma como serviço). Embora você possa considerar IaaS como acesso direto à infraestrutura de computação, PaaS fornece ambientes de desenvolvimento e implantação prontos que são gerenciados para você.

Por exemplo, digamos que você execute o SQL Server em uma VM em execução no Azure. Essa configuração exige que você gerencie o sistema operacional subjacente, configure uma licença do SQL Server, gerencie atualizações de software e segurança e assim por diante. Você também paga pela VM esteja o banco de dados processando consultas ou não. Uma forma de potencialmente economizar custos é mover o banco de dados do SQL Server em uma VM para o Banco de Dados SQL do Azure. O Banco de Dados SQL do Azure é baseado em SQL Server.

A execução de serviços de PaaS, como o Banco de Dados SQL do Azure, muitas vezes tem um menor custo, porém, como eles são gerenciados para você, não é preciso se preocupar com atualizações de software, patches de segurança ou otimização do armazenamento físico para operações de leitura e gravação.

### Reduzir os custos de licenciamento

O licenciamento é outra área que pode afetar drasticamente seus gastos com a nuvem. Vejamos algumas maneiras para reduzir seus custos com licenciamento.
Escolher sistemas operacionais econômicos

Muitos serviços do Azure fornecem uma opção de execução no Windows ou no Linux. Em alguns casos, o custo depende do que você escolhe. Quando você tem opção e seu aplicativo não depende do sistema operacional subjacente, é útil comparar preços para ver se é possível economizar dinheiro.

### Usar o Benefício Híbrido do Azure para realocar licenças de software no Azure

Se você comprou licenças para o Windows Server ou o SQL Server e elas são cobertas pelo Software Assurance, poderá realocá-las para VMs no Azure.

Alguns dos detalhes variam entre o Windows Server e o SQL Server. No final deste módulo, forneceremos recursos para você saber mais.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/plan-manage-azure-costs/6-manage-minimize-total-cost)

> ## [Próximo](./M19_2_Resumo.md)
