# Resumo

A computação sem servidor é um termo usado para descrever um ambiente de execução configurado e gerenciado para você. É um **ambiente de execução hospedado na nuvem que executa o código, mas abstrai o ambiente de hospedagem subjacente**.

A ideia principal é que você não seja responsável por configurar nem por manter esse servidor. Você não precisará se preocupar em dimensioná-lo quando houver aumento da demanda, nem com interrupções. O fornecedor de nuvem cuida de todas as questões de manutenção e dimensionamento para você.

### Azure Functions (Funções do Azure)

Com o serviço do Azure Functions, você pode hospedar um único método ou função usando uma linguagem de programação popular na nuvem que é executada em resposta a um evento. Um exemplo de evento pode ser uma solicitação HTTP, uma nova mensagem em uma fila ou uma mensagem em um temporizador.

Devido à sua natureza atômica, o Azure Functions pode atender a muitas finalidades no design de um aplicativo. As funções podem ser escritas em muitas linguagens de programação comuns, como C#, Python, JavaScript, Typescript, Java e PowerShell.

**A solução Azure Functions é ideal quando você está preocupado apenas com o código que está executando seu serviço, e não com a plataforma ou infraestrutura subjacente**. O Azure Functions **geralmente é usado quando você precisa realizar um trabalho em resposta a um evento**.

Com o **Azure Functions**, você pode usar a expressividade total de uma linguagem de programação de forma compacta. Isso **permite criar algoritmos complexos de maneira concisa ou operações de pesquisa e análise de dados**. Você seria responsável pela manutenção do código, manipulação de exceções de modo resiliente e assim por diante.

Se você já tem sua orquestração ou lógica de negócios expressa em C#, Java, Python ou em outra linguagem de programação popular, talvez seja mais fácil portar seu código para o corpo de um aplicativo de funções do **Azure Functions** do que recriá-lo usando os Aplicativos Lógicos do Azure.

Os desenvolvedores que têm experiência com **linguagem de programação imperativa** podem preferir pensar na automação e orquestração com uma mentalidade **imperativa**.

Quando a empresa precisou criar uma solução que efetuasse pull da lógica de código de um serviço Windows em C# existente, nós a ajudamos a escolher o Azure Functions.

### Aplicativos Lógicos do Azure

Os Aplicativos Lógicos são uma plataforma de desenvolvimento de código baixo/sem código hospedada como um serviço de nuvem. O serviço ajuda a automatizar e orquestrar tarefas, processos empresariais e fluxos de trabalho quando você precisa integrar aplicativos, dados, sistemas e serviços em empresas ou organizações. Os Aplicativos Lógicos simplificam a maneira como você projeta e constrói soluções escalonáveis, seja na nuvem, no local ou em ambos. Essa solução abrange as integrações de aplicativos, dados, sistemas, EAI (integração de aplicativos empresariais) e B2B (entre empresas).

O **serviço Aplicativos Lógicos do Azure foi projetado pensando em orquestração**, do configurador visual baseado na Web ao modelo de preços.

Os profissionais de TI e analistas de negócios podem preferir trabalhar em um **ambiente mais visual de código baixo/sem código (declarativo)**.

Quando ela precisou orquestrar um fluxo de trabalho para melhorar a retenção do cliente após uma experiência de compra negativa, nós a ajudamos a escolher os Aplicativos Lógicos do Azure.

### Quais são as diferenças entre esses serviços?

Você pode chamar o Azure Functions de Aplicativos Lógicos do Azure e vice-versa. A principal diferença entre os dois serviços é a que eles se destinam. O **Azure Functions é um serviço de computação sem servidor**, enquanto os **Aplicativos Lógicos do Azure se destinam a ser um serviço de orquestração sem servidor**.

Os dois serviços também têm preços diferentes.

1. O preço do Azure Functions é baseado no número de execuções e no tempo de execução de cada uma.
2. O preço dos Aplicativos Lógicos é baseado no número de execuções e no tipo de conectores que elas utilizam.

> Azure Functions: quando já há uma solução pré-produzida em alguma linguagem de programação. Mais indicado para quem prefere trabalhar em um ambiente imperativo (escrever código).
>
> > _"Os desenvolvedores que têm experiência com linguagem de programação imperativa podem preferir pensar na automação e orquestração com uma mentalidade imperativa_"

> Aplicativos Lógicos do Azure: quando a solução vai ser elaborada do zero e pode utilizar recursos já disponíveis no Azure, de modo que bastaria "conectá-los". Indicado para quem prefere um fluxo de trabalho visual (declarativo)
>
> > _"Os profissionais de TI e analistas de negócios podem preferir trabalhar em um ambiente mais visual de código baixo/sem código (declarativo)._"

> Você precisa processar mensagens de uma fila, analisá-las usando alguma lógica imperativa existente escrita em Java e enviá-las para uma API de terceiros. Qual opção sem servidor você deve escolher?
>
> > O Azure Functions é a opção correta porque você pode usar o código Java existente com modificação mínima.

> Você quer orquestrar um fluxo de trabalho usando APIs de vários serviços conhecidos. Qual é a melhor opção para este cenário?
>
> > O serviço Aplicativos Lógicos do Azure facilita a criação de um fluxo de trabalho entre serviços conhecidos com menos esforço do que escrever código e orquestrar manualmente todas as etapas por conta própria.

> Sua equipe tem experiência limitada em escrever código personalizado, mas vê um enorme valor na automação de vários processos empresariais importantes. Qual das opções a seguir é a melhor opção para a sua equipe?
>
> > O serviço de Aplicativos Lógicos do Azure é mais adequado para usuários que se sentem mais à vontade em um ambiente visual que permite automatizar processos empresariais. Os Aplicativos Lógicos são a melhor opção nesse cenário.

> Quando a empresa precisou criar uma solução que efetuasse pull da lógica de **código** de um serviço Windows em C# **existente**, nós a ajudamos a escolher o **Azure Functions**.

> Quando ela precisou **orquestrar um fluxo de trabalho** para melhorar a retenção do cliente após uma experiência de compra negativa, nós a ajudamos a escolher os **Aplicativos Lógicos do Azure**.

> Sem a computação sem servidor, a empresa seria forçada a configurar e gerenciar a própria infraestrutura de computação para esses cenários empresariais. A equipe precisaria monitorar de perto os serviços para determinar se era necessário dimensioná-los. E provavelmente teria desperdiçado dinheiro no processo, com muitos ou poucos recursos de computação dedicados à solução.
>
> Além disso, talvez ela precisasse projetar, escrever, testar e manter um código personalizado para obter resultados semelhantes.
