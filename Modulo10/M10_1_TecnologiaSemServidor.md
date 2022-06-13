# Escolher a melhor tecnologia sem servidor do Azure para seu cenário empresarial

A computação sem servidor é um termo usado para descrever um ambiente de execução configurado e gerenciado para você. Você só precisa especificar o que deseja que aconteça escrevendo código ou conectando e configurando componentes em um editor visual e, então, especificar as ações que disparam sua funcionalidade, como um temporizador ou uma solicitação HTTP. O melhor é que você não precisará se preocupar com uma interrupção; seu código pode ser dimensionado instantaneamente para atender à demanda, e você só paga pelo uso real dele.

## Identificar as opções de produto

> A computação sem servidor é um **ambiente de execução hospedado na nuvem que executa o código, mas abstrai o ambiente de hospedagem subjacente**.

O termo computação sem servidor é um nome inadequado. Afinal, há um servidor (ou um grupo de servidores) que executa seu código ou a funcionalidade desejada.

A ideia principal é que você não seja responsável por configurar nem por manter esse servidor. Você não precisará se preocupar em dimensioná-lo quando houver aumento da demanda, nem com interrupções. O fornecedor de nuvem cuida de todas as questões de manutenção e dimensionamento para você.

Você cria uma instância do serviço e adiciona seu código. Nenhuma configuração ou manutenção da infraestrutura é necessária, nem mesmo permitida. Você configura os aplicativos sem servidor para responder a eventos.

**Um evento pode ser um ponto de extremidade REST, um temporizador periódico ou até mesmo uma mensagem recebida de outro serviço do Azure**. Nesse caso, o aplicativo sem servidor é executado somente quando disparado por um evento. O dimensionamento e o desempenho são administrados automaticamente, e você é cobrado apenas pelos recursos que utiliza. Você nem precisa reservar recursos.

**A computação sem servidor é normalmente usada para lidar com cenários de back-end.** Em outras palavras, a computação sem servidor é responsável por enviar mensagens de um sistema para outro ou processar mensagens que foram enviadas de outros sistemas. Essa computação não é usada para sistemas voltados ao usuário; em vez disso, ela funciona em segundo plano.

### Funções do Azure

Com o serviço do Azure Functions, você pode hospedar um único método ou função usando uma linguagem de programação popular na nuvem que é executada em resposta a um evento. Um exemplo de evento pode ser uma solicitação HTTP, uma nova mensagem em uma fila ou uma mensagem em um temporizador.

Devido à sua natureza atômica, o Azure Functions pode atender a muitas finalidades no design de um aplicativo. As funções podem ser escritas em muitas linguagens de programação comuns, como C#, Python, JavaScript, Typescript, Java e PowerShell.

O Azure Functions é dimensionado automaticamente, e as cobranças são geradas apenas quando uma função é disparada. Essas qualidades tornam o **Azure Functions uma escolha sólida quando a demanda é variável**.

**A solução Azure Functions é ideal quando você está preocupado apenas com o código que está executando seu serviço, e não com a plataforma ou infraestrutura subjacente**. O Azure Functions **geralmente é usado quando você precisa realizar um trabalho em resposta a um evento**. Isso geralmente é feito por meio de uma solicitação REST, um temporizador ou uma mensagem de outro serviço do Azure e quando esse trabalho pode ser concluído rapidamente, em poucos segundos ou menos.

### Aplicativos Lógicos do Azure

Os Aplicativos Lógicos são uma plataforma de desenvolvimento de código baixo/sem código hospedada como um serviço de nuvem. O serviço ajuda a automatizar e orquestrar tarefas, processos empresariais e fluxos de trabalho quando você precisa integrar aplicativos, dados, sistemas e serviços em empresas ou organizações. Os Aplicativos Lógicos simplificam a maneira como você projeta e constrói soluções escalonáveis, seja na nuvem, no local ou em ambos. Essa solução abrange as integrações de aplicativos, dados, sistemas, EAI (integração de aplicativos empresariais) e B2B (entre empresas).

### Quais são as diferenças entre esses serviços?

Você pode chamar o Azure Functions de Aplicativos Lógicos do Azure e vice-versa. A principal diferença entre os dois serviços é a que eles se destinam. O **Azure Functions é um serviço de computação sem servidor**, enquanto os **Aplicativos Lógicos do Azure se destinam a ser um serviço de orquestração sem servidor**. Embora você possa usar o Azure Functions para orquestrar um processo empresarial de longa execução que envolva diversas conexões, esse não era o caso de uso principal dele quando foi projetado.

Os dois serviços também têm preços diferentes.

1. O preço do Azure Functions é baseado no número de execuções e no tempo de execução de cada uma.
2. O preço dos Aplicativos Lógicos é baseado no número de execuções e no tipo de conectores que elas utilizam.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/serverless-fundamentals/2-identify-product-options)

## Analisar os critérios de decisão

### Você precisa executar uma orquestração em APIs bem conhecidas?

O **serviço Aplicativos Lógicos do Azure foi projetado pensando em orquestração**, do configurador visual baseado na Web ao modelo de preços. Os Aplicativos Lógicos se destacam na conexão de uma ampla gama de serviços diferentes por meio das APIs para passar e processar dados em várias etapas em um fluxo de trabalho.

É possível criar o mesmo fluxo de trabalho usando o Azure Functions, mas isso pode levar um tempo considerável para pesquisar quais APIs chamar e como chamá-las. Os Aplicativos Lógicos do Azure já modelaram essas chamadas à API para que você forneça apenas alguns dados, abstraindo os detalhes da chamada às APIs necessárias.

### Você precisa executar algoritmos personalizados ou executar análises de dados especializadas e pesquisas de dados?

Com o **Azure Functions**, você pode usar a expressividade total de uma linguagem de programação de forma compacta. Isso **permite criar algoritmos complexos de maneira concisa ou operações de pesquisa e análise de dados**. Você seria responsável pela manutenção do código, manipulação de exceções de modo resiliente e assim por diante.

Embora os Aplicativos Lógicos do Azure possam executar lógica (loops, decisões e assim por diante), se você tiver uma orquestração de lógica intensiva que requeira um algoritmo complexo, implementar esse algoritmo poderá exigir maior detalhamento e parecer visualmente opressivo.

### Você tem tarefas automatizadas escritas em uma linguagem de programação imperativa?

Se você já tem sua orquestração ou lógica de negócios expressa em C#, Java, Python ou em outra linguagem de programação popular, talvez seja mais fácil portar seu código para o corpo de um aplicativo de funções do **Azure Functions** do que recriá-lo usando os Aplicativos Lógicos do Azure.

### Você prefere um fluxo de trabalho visual (declarativo) ou escrever código (imperativo)?

Em última análise, sua escolha se resume a definir se você prefere trabalhar em um ambiente declarativo ou imperativo. Os desenvolvedores que têm experiência com linguagem de programação imperativa podem preferir pensar na automação e orquestração com uma mentalidade imperativa. Os profissionais de TI e analistas de negócios podem preferir trabalhar em um ambiente mais visual de código baixo/sem código (declarativo).

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/serverless-fundamentals/3-analyze-decision-criteria)

## Usar o Azure Functions

> **Cenário**:
>
> A Tailwind Traders deseja atualizar seu site de comércio eletrônico para incluir rastreamento de estoque em tempo real. Atualmente, o site atualiza a disponibilidade do produto à noite às 2h.
>
> Na maioria das vezes, esse sistema funciona bem. No entanto, alguns produtos estão em alta demanda e outros produtos são mantidos em pequenas quantidades em cada loja. Várias vezes por dia, os clientes vão até a loja para comprar um item e descobrem que ele não está mais em estoque.
>
> Em vez de executar o algoritmo todas as noites, a empresa deseja executar o atualizador de estoque cada vez que um produto é comprado.

### Qual serviço escolher?

Como a equipe de desenvolvedores da empresa já escreveu a lógica em C#, faria sentido copiar o código C# relevante do serviço Windows e portá-lo para uma função do Azure. Os desenvolvedores devem associar a função para ser disparada sempre que uma nova mensagem aparecer em uma fila específica.

### Por que não escolher Aplicativos Lógicos do Azure?

É possível implementar a mesma lógica nos Aplicativos Lógicos do Azure. No entanto, como a equipe já investiu tempo na construção do serviço em C#, ela pode usar o mesmo código em uma função do Azure.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/serverless-fundamentals/4-use-azure-functions)

## Usar os Aplicativos Lógicos do Azure

> **Cenário**:
>
> A empresa envia a seus clientes um convite para participar de uma pesquisa de satisfação aleatoriamente após uma compra. Atualmente, os resultados da satisfação do cliente são agregados, calculados e colocados em gráfico. No entanto, seu departamento de atendimento ao cliente vê uma oportunidade de alcançar de forma proativa os clientes que fornecem notas baixas e deixam comentários com um sentimento negativo.
>
> Idealmente, as pontuações negativas de satisfação dos clientes disparariam um fluxo de trabalho de retenção. Primeiro, uma análise de sentimentos seria gerada com base nos comentários em forma livre, um email seria enviado ao cliente com um pedido de desculpas e um código de cupom, e a mensagem seria encaminhada à equipe de atendimento ao cliente do Dynamics 365, para que ela pudesse agendar um email de acompanhamento.

### Qual serviço escolher?

Nesse cenário, **os Aplicativos Lógicos do Azure** são provavelmente a melhor solução. Um profissional de TI ou de nuvem poderia **empregar conectores existentes para executar uma análise de sentimentos usando o conector de Serviços Cognitivos do Azure, enviar um email usando o conector do Outlook para Office 365 e criar um registro e email de acompanhamento usando o conector de atendimento ao cliente do Dynamics 365**.

Como os Aplicativos Lógicos do Azure são um serviço de código baixo/sem código, nenhum desenvolvedor é necessário. Um profissional de TI ou de nuvem deve conseguir criar e dar suporte a esse fluxo de trabalho.

### Por que não escolher o Azure Functions?

Embora seja possível criar a solução inteira usando o Azure Functions, essa abordagem poderá ser desafiadora se nenhum desenvolvedor de software puder se comprometer com esse projeto.
Esse é um cenário ideal para os Aplicativos Lógicos do Azure. **Os conectores já existem para cada uma das etapas descritas no fluxo de trabalho**. Seria necessário um pouco de pesquisa, desenvolvimento e teste para um desenvolvedor criar uma solução que utilizasse todos esses sistemas de software diferentes.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/ai-machine-learning-fundamentals/6-use-bot-services)

> ## [Próximo](./M10_2_Resumo.md)
