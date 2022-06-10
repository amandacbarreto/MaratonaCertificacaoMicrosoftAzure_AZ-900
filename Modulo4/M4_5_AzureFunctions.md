# Decidir quando usar o Azure Functions

> ### **A computação sem servidor é a abstração de servidores, infraestrutura e sistemas operacionais**.
>
> Com a computação sem servidor, o Azure cuida do gerenciamento da infraestrutura de servidor e da alocação e desalocação de recursos com base na demanda. Você não precisa se preocupar com a infraestrutura. A colocação em escala e o desempenho são manipulados automaticamente. Você é cobrado apenas pelos recursos exatos que usa. Não é necessário ter capacidade reserva.

A computação sem servidor inclui a abstração de servidores, uma escala controlada por eventos e uma microcobrança:

- **Abstração de servidores**: a computação sem servidor abstrai os servidores em que você executa. Você nunca reserva instâncias de servidor explicitamente. A plataforma gerencia isso para você. A execução de cada função pode ser executada em uma instância de computação diferente. Esse contexto de execução é transparente para o código. Com a arquitetura sem servidor, você implanta seu código, que, por sua vez, é executado com alta disponibilidade.

- **Escala controlada por eventos**: A computação sem servidor é uma opção excelente para cargas de trabalho que respondem a eventos de entrada. Os eventos incluem gatilhos por:

  - Temporizadores, por exemplo, se uma função precisar ser executada todos os dias às 10h00 UTC.
  - HTTP, por exemplo, em cenários com API e webhook.
  - Filas, por exemplo, com o processamento em ordem.
  - E muito mais.

  Em vez de escrever um aplicativo inteiro, o desenvolvedor cria uma função, que contém o código e os metadados sobre seus gatilhos e associações. A plataforma agenda automaticamente a função para execução e dimensiona o número de instâncias de computação com base na taxa de eventos de entrada. Gatilhos definem como uma função é invocada. As associações fornecem uma forma declarativa de conectar-se a serviços de dentro do código.

- **Microcobrança**: a computação tradicional cobra por um bloco de tempo, por exemplo, com o pagamento de uma taxa mensal ou anual pela hospedagem de sites. Esse método de cobrança é conveniente, mas nem sempre é econômico. Mesmo que o site de um cliente receba apenas uma visita por dia, ele ainda pagará pela disponibilidade de um dia inteiro. Com a computação sem servidor, ele paga apenas pelo tempo em que seu código é executado. Se nenhuma execução de função ativa ocorrer, ele não será cobrado. Por exemplo, se o código for executado uma vez por dia por dois minutos, ele será cobrado por uma execução e dois minutos de tempo de computação.

### Computação sem servidor no Azure

O Azure tem duas implementações de computação sem servidor:

- **Azure Functions**: o Functions pode executar o código praticamente em qualquer linguagem de programação moderna.
- **Aplicativos Lógicos do Azure**: os aplicativos lógicos foram desenvolvidos em um designer baseado na Web e podem executar a lógica disparada pelos serviços do Azure sem escrever nenhum código.

# Azure Functions

O Azure Functions é ideal para você caso esteja preocupado apenas com o código do serviço, não com a plataforma nem com a infraestrutura subjacente. As funções costumam ser usadas quando você precisa executar um trabalho em resposta a um evento (geralmente por meio de uma solicitação REST), um temporizador ou uma mensagem de outro serviço do Azure e quando esse trabalho pode ser concluído dentro de segundos.

As funções são dimensionadas automaticamente com base na demanda; assim sendo, trata-se de uma boa opção quando a demanda é variável. Por exemplo, você pode receber mensagens de uma solução de IoT (Internet das Coisas) usada para monitorar uma frota de veículos de entrega. Provavelmente, a maioria dos dados é recebida durante o horário comercial.

Usando uma abordagem baseada em máquina virtual, você incorreria em custos mesmo quando a máquina virtual estivesse ociosa. Com funções, o Azure executa o código quando este é disparado e desaloca os recursos automaticamente quando a função é concluída. Neste modelo, você só é cobrado pelo tempo de CPU usado durante a execução da função.

As funções podem ser sem estado ou com estado. Quando são sem estado (o padrão), elas se comportam como se fossem reiniciadas sempre que respondem a um evento. Quando são com estado (chamadas de Durable Functions), um contexto é passado pela função para acompanhar a atividade anterior.

As funções são um componente chave da computação sem servidor. Elas também são uma plataforma de computação geral para executar qualquer tipo de código. Se as necessidades do aplicativo do desenvolvedor forem alteradas, você poderá implantar o projeto em um ambiente que não seja sem servidor. Essa flexibilidade permite gerenciar o dimensionamento, executar em redes virtuais e até mesmo isolar completamente as funções.

## Aplicativos Lógicos do Azure

Os aplicativos lógicos são semelhantes às funções. Ambos permitem que você dispare lógica com base em um evento. Enquanto as funções executam código, os aplicativos lógicos executam fluxos de trabalho criados para automatizar cenários de negócios com base em blocos de lógica predefinida.

Cada fluxo de trabalho de aplicativo lógico do Azure começa com um gatilho, que é acionado quando um evento específico ocorre ou quando novos dados disponíveis atendem a critérios específicos. Vários gatilhos incluem recursos básicos de agendamento, para que os desenvolvedores possam especificar a regularidade das execuções das suas cargas de trabalho. Cada vez que o gatilho é acionado, o mecanismo de Aplicativos Lógicos cria uma instância de aplicativo lógico que executa as ações no fluxo de trabalho. Essas ações também podem incluir conversões de dados e controles de fluxo, como instruções condicionais, instruções de comutação, loops e ramificações.

Você cria fluxos de trabalho de aplicativo lógico usando um designer visual no portal do Azure ou no Visual Studio. Os fluxos de trabalho são mantidos como um arquivo JSON com um esquema de fluxo de trabalho conhecido.

O Azure fornece mais de 200 conectores e blocos de processamento para você interagir com diferentes serviços. Esses recursos incluem os aplicativos empresariais mais populares. Você também pode criar etapas de fluxo de trabalho e conectores personalizados caso o serviço com o qual precisa interagir não esteja coberto. Em seguida, você usa o designer visual para vincular conectores e blocos. Você passa dados pelo fluxo de trabalho para fazer o processamento personalizado, geralmente sem escrever nenhum código.

Por exemplo, digamos que chegou um tíquete no Zendesk. Você pode:

* Detectar a intenção da mensagem com os serviços cognitivos.
* Criar um item no SharePoint para acompanhar o problema.
* Adicionar o cliente ao seu sistema de CRM do Dynamics 365 caso ele não esteja no banco de dados.
* Envie um email de acompanhamento para confirmar a solicitação.

Todas essas ações podem ser criadas em um designer visual, o que facilita a visualização do fluxo lógico. Por esse motivo, ele é ideal para uma função de analista de negócios.

# Functions vs. Aplicativos Lógicos

O Functions e os Aplicativos Lógicos podem criar orquestrações complexas. Uma orquestração é uma coleção de funções ou etapas que são executadas para realizar uma tarefa complexa.

    Com o Functions, você escreve código para concluir cada etapa.
    Com os Aplicativos Lógicos, você usa uma GUI para definir as ações e como elas se relacionam entre si.

Você pode combinar serviços ao compilar uma orquestração, chamando funções de aplicativos lógicos e chamando aplicativos lógicos de funções. No entanto, há algumas diferenças entre essas implementações.


###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-compute-fundamentals/azure-functions)

> ## [Próximo](./M4_6_AreaTrabalhoVirtual.md)
