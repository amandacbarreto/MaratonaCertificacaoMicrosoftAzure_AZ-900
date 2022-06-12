# Escolha as melhores ferramentas para ajudar as organizações a criar soluções melhores

## Entender as opções de produtos

Há três ofertas principais, cada uma delas voltada para um público-alvo e um caso de uso específicos, que fornecem um conjunto diversificado de ferramentas, serviços, APIs programáticas e muito mais.

### Azure DevOps Services

> ### O Azure DevOps Services é um conjunto de serviços que lidam com cada fase do ciclo de vida do desenvolvimento de software.

- O Azure Repos é um repositório de código-fonte centralizado no qual profissionais de desenvolvimento de software, engenharia de DevOps e documentação podem publicar código para revisão e colaboração.
- O Azure Boards é um pacote de gerenciamento de projetos ágil que inclui quadros Kanban, relatórios e acompanhamento de ideias e trabalho, de epics de alto nível a itens de trabalho e problemas.
- O Azure Pipelines é uma ferramenta de automação do pipeline de CI/CD.
- O Azure Artifacts é um repositório para hospedagem de artefatos, como o código-fonte compilado, que podem ser inseridos nas etapas dos pipelines de teste ou de implantação.
- O Azure Test Plans é uma ferramenta de teste automatizado que pode ser usada em um pipeline de CI/CD para garantir a qualidade antes da liberação de um software.

O Azure DevOps é uma ferramenta madura, com um grande conjunto de recursos, que começou como um software para servidores local e evoluiu para uma oferta de SaaS (software como serviço) da Microsoft.

## GitHub e GitHub Actions

O GitHub é, sem dúvida, o repositório de código mais popular do mundo para software livre. O Git é uma ferramenta de gerenciamento de código-fonte descentralizada, e o GitHub é uma versão hospedada do Git que serve como o remoto primário. O GitHub se baseia no Git para fornecer serviços relacionados para coordenar trabalhos, relatar e discutir problemas, fornecer documentação e muito mais.

> ### O GitHub Actions permite a automação do fluxo de trabalho com gatilhos para muitos eventos do ciclo de vida.
>
> Um exemplo seria automatizar uma cadeia de ferramentas de CI/CD.

Uma cadeia de ferramentas é uma combinação de ferramentas de software que auxiliam na entrega, no desenvolvimento e no gerenciamento de aplicativos de software durante o ciclo de vida de desenvolvimento de um sistema. A saída de uma ferramenta na cadeia de ferramentas é a entrada da próxima ferramenta na cadeia de ferramentas. Funções típicas das ferramentas vão desde executar atualizações de dependência automatizadas até a criação e a configuração do software, a entrega dos artefatos de build a vários locais, a realização de testes e assim por diante.

Diante dessa similaridade entre muitos recursos do GitHub e do Azure DevOps, você pode estar se perguntando qual produto escolher para sua organização. Infelizmente, a resposta pode não ser simples.

Embora o Azure DevOps e o GitHub permitam repositórios de código públicos e privados, o GitHub tem um longo histórico com repositórios públicos e conta com a confiança de dezenas de milhares de proprietários de projetos de software livre.

> O GitHub é uma ferramenta mais leve do que o Azure DevOps, com foco em desenvolvedores individuais que contribuem para o código de software livre.
>
> O Azure DevOps, por outro lado, é mais focado em desenvolvimento corporativo, com ferramentas de planejamento e gerenciamento de projeto mais pesadas e controle de acesso mais refinado.

### Azure DevTest Labs

> ### O Azure DevTest Labs fornece um meio automatizado de gerenciar o processo de criação, configuração e remoção de VMs (máquinas virtuais) que contêm builds de seus projetos de software.

Dessa maneira, desenvolvedores e testadores podem executar testes em uma variedade de ambientes e builds. E isso não fica limitado às VMs. Tudo o que você pode implantar no Azure por meio de um modelo do ARM pode ser provisionado pelo DevTest Labs. O provisionamento de ambientes de laboratório pré-criados com as ferramentas e as configurações necessárias já instaladas economiza muito tempo para desenvolvedores e profissionais de garantia de qualidade.

Suponha que você precise testar um novo recurso em uma versão antiga de um sistema operacional. O Azure DevTest Labs pode configurar tudo automaticamente após a solicitação. Depois que o teste for concluído, os DevTest Labs poderão desligar e desprovisionar a VM, o que economiza dinheiro quando ela não está em uso. A fim de controlar custos, a equipe de gerenciamento pode restringir quantos laboratórios podem ser criados, por quanto tempo eles são executados e assim por diante.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/serverless-fundamentals/2-identify-product-options)

## Analisar os critérios de decisão

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/serverless-fundamentals/2-identify-product-options)

## Usar o Azure DevOps para gerenciar o ciclo de vida do desenvolvimento de aplicativo

### Você precisa automatizar e gerenciar a criação de laboratórios de teste?

Caso seu objetivo seja **automatizar a criação e o gerenciamento de um ambiente de laboratório de teste, considere escolher o Azure DevTest Labs**. Das três ferramentas e serviços que descrevemos, este é o único que oferece essa funcionalidade.

No entanto, você pode automatizar o provisionamento de novos laboratórios como parte de uma cadeia de ferramentas usando o GitHub Actions ou o Azure Pipelines.

### Você está criando software livre?

Embora o Azure DevOps possa publicar repositórios de código públicos, **o GitHub é o host preferencial para software livre** há tempos. **Se você estiver criando software livre, provavelmente escolherá o GitHub devido à sua visibilidade e à aceitação geral da comunidade de desenvolvimento de software livre**.

### Com relação às ferramentas de gerenciamento de código-fonte e DevOps, que nível de granularidade você precisa ter para as permissões?

O GitHub funciona em um modelo simples de permissões de leitura/gravação para cada recurso. Já o Azure DevOps tem um conjunto muito mais granular de permissões que possibilita às organizações refinar quem pode executar a maioria das operações em todo o conjunto de ferramentas.

### Com relação ao gerenciamento de código-fonte e às ferramentas de DevOps, quão sofisticados o gerenciamento de projeto e os relatórios precisam ser?

Embora o GitHub tenha itens de trabalho, problemas e um quadro Kanban, o gerenciamento de projeto e os relatórios são as áreas de excelência do Azure DevOps. **O Azure DevOps é altamente personalizável**, o que permite que um administrador adicione campos personalizados para capturar metadados e outras informações junto com cada item de trabalho. Por outro lado, **o recurso de Problemas do GitHub usa marcações como o principal meio de ajudar uma equipe a categorizar os problemas**.

### Com relação ao gerenciamento de código-fonte e às ferramentas de DevOps, quão estreita você precisa que seja a integração com ferramentas de terceiros?

Embora não façamos recomendações específicas sobre ferramentas de terceiros, é importante que você entenda os investimentos existentes de sua organização em ferramentas e serviços e avalie como essas dependências podem afetar sua escolha. É provável que a maioria dos fornecedores que criam ferramentas de DevOps crie ganchos ou APIs que possam ser usados pelo Azure Pipelines e pelo GitHub Actions. Mesmo assim, provavelmente vale o esforço para validar essa suposição.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-devops-devtest-labs/3-analyze-decision-criteria)

## Usar o Azure DevOps para gerenciar o ciclo de vida do desenvolvimento de aplicativo

> **Cenário**
>
> A equipe de desenvolvimento de software na Tailwind Traders trabalha em vários projetos diferentes e eles precisam fornecer aos patrocinadores e gerentes do projeto relatórios de nível executivo, incluindo Gráficos de Burndown, acompanhar o progresso em relação a epics e acompanhar informações personalizadas específicas da Tailwind Traders em cada item de trabalho e relatório de bug.

### Quais serviços devemos escolher?

1. A Tailwind Traders precisa automatizar e gerenciar a criação de laboratório de teste?

   Não. Portanto, nesse cenário, o Azure DevTest Labs não é um candidato, pois ele não se destina a esse caso de uso específico.

2. A Tailwind Traders está criando software livre?
   Embora não seja mencionado especificamente, a Tailwind Traders está criando sistemas internos e externos, como o sistema de comércio eletrônico, que não é de software livre. Portanto, essa não é uma consideração nesse cenário.

3. Que nível de granularidade a Tailwind Traders precisa ter para as permissões?
   Anteriormente, afirmamos que a Tailwind Traders contratará funcionários e fornecedores temporários para trabalhos de curto prazo, o que faz das permissões granulares uma consideração importante para a alta gerência. Com base em nossa descrição na unidade anterior, esse recurso faria do **Azure DevOps** um dos principais candidatos. Usando o Azure DevOps, os administradores da Tailwind Traders também teriam um conjunto mais robusto de opções para controlar as permissões em todo o portfólio de trabalho.

4. A Tailwind Traders precisa de uma solução sofisticada de gerenciamento e relatórios de projetos?
   Sim, recursos robustos de gerenciamento e relatório de projetos são uma das principais considerações. Novamente, **devido à quantidade de personalização e de relatórios de itens de trabalho que a equipe de gerenciamento deseja, o Azure DevOps provavelmente seria uma boa opção**.

5. A Tailwind Traders requer uma forte integração com ferramentas de DevOps de terceiros?
   A integração de ferramentas não foi listada como uma consideração principal para esse cenário. Como você aprendeu na unidade anterior, **a maioria das ferramentas de DevOps de terceiros se integra ao Azure DevOps e ao GitHub**, o que torna provável que a equipe encontre as ferramentas de que precisa.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-devops-devtest-labs/4-use-azure-devops)

## Usar o GitHub para contribuir com software livre

> **Cenario**:
>
> A Tailwind Traders espera publicar uma API que permita que terceiros integrem os próprios inventários de itens novos e usados.
>
> Embora a implementação interna da API seja de código-fonte fechado, a Tailwind Traders quer criar um conjunto de exemplos que chamam a API para executar várias ações. A equipe precisa de uma plataforma para compartilhar código de exemplo, coletar comentários sobre a API, permitir que os colaboradores relatem problemas e criar uma comunidade em torno de solicitações de recursos.

### Qual serviço escolher?

1. A Tailwind Traders precisa automatizar e gerenciar a criação de laboratório de teste?
   Não. Nesse cenário, o Azure DevTest Labs não é um candidato, pois ele não se destina a esse caso de uso.

2. A Tailwind Traders está criando software livre?
   Sim. Como observamos em uma unidade anterior, os desenvolvedores estão acostumados a ver esse tipo de conteúdo disponível no GitHub. **Com o GitHub, os desenvolvedores da Tailwind Traders podem publicar código, aceitar contribuições da comunidade para aprimorar os exemplos de código, aceitar comentários e relatórios de bugs e muito mais**. Como esse cenário envolve software livre, o GitHub é um dos principais candidatos.

3. Que nível de granularidade a Tailwind Traders precisa ter para atribuir permissões?
   Embora não seja afirmado explicitamente, **pelo fato de que a Tailwind Traders aceitará contribuições da comunidade, emitirá relatórios e tentará, de modo geral, criar uma comunidade de desenvolvedores com seus exemplos de API, as necessidades de permissão da empresa são básicas: os usuários podem ser somente exibição ou exibição e gravação**. Esse é outro motivo pelo qual o **GitHub seria um bom candidato para esse cenário**.

4. A Tailwind Traders precisa de uma solução sofisticada de gerenciamento e relatórios de projetos?
   Mais uma vez, devido à natureza do projeto, **a equipe não precisa de uma solução sofisticada de relatórios e gerenciamento de projetos**. Nesse cenário, **a potência do Azure DevOps Services não é necessária**.

5. A Tailwind Traders requer uma forte integração com ferramentas de DevOps de terceiros?
   A integração de ferramentas não foi listada como uma consideração principal para esse cenário e não qualifica nem desqualifica nenhuma das ferramentas.

**O GitHub é a melhor opção para esse cenário. Embora você possa usar o Azure DevOps para tornar o repositório público, alguns dos outros recursos que envolvem a comunidade de desenvolvimento, como comentários ou relatórios de bugs, seriam menos acessíveis**.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-devops-devtest-labs/5-use-github)

## Usar o Azure DevTest Labs para gerenciar ambientes de teste

> **Cenario**:
>
> A Tailwind Traders quer ser mais metódica e cuidadosa ao efetuar push de novas versões de seu site de comércio eletrônico para produção. A empresa expandirá sua equipe de QA (garantia de qualidade) e usará a nuvem para criar e hospedar VMs (máquinas virtuais). Com essa abordagem, eles criarão ambientes de teste correspondentes ao ambiente de produção.
>
> A equipe de gerenciamento tem preocupações relativas aos custos de um ambiente de teste mais automatizado. Por exemplo, eles querem ter certeza de que os profissionais de garantia de qualidade não estejam desperdiçando tempo configurando o ambiente de teste para que ele corresponda ao ambiente de produção. A equipe deseja garantir que as VMs sejam destruídas quando não estiverem mais em uso. Eles querem limitar o número de VMs que cada profissional de garantia de qualidade tem permissão para ativar. Além disso, a equipe quer garantir que cada ambiente esteja configurado de modo correto e consistente com o ambiente de produção.

### Qual serviço escolher?

1. A Tailwind Traders precisa automatizar e gerenciar a criação de laboratório de teste?
   Sim. Esse parece ser um trabalho para o **Azure DevTest Labs**, pois ele **pode fazer tudo que a equipe precisa realizar nesse cenário**.

Poderíamos continuar avaliando os critérios de decisão, mas nem o Azure DevOps nem o GitHub é necessário para esse cenário. Lembre-se de que o Azure DevOps ou o GitHub pode ser usado para criar versões de produtos que podem ser incluídas automaticamente em VMs criadas para fins de teste.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-devops-devtest-labs/6-use-azure-devtest-labs)

> ## [Próximo](./M11_2_Resumo.md)
