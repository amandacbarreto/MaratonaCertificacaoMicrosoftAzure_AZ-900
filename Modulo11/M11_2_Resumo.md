# Resumo

## Azure DevOps Services

O Azure DevOps Services é um conjunto de serviços que lidam com cada fase do ciclo de vida do desenvolvimento de software.

- O Azure Repos é um repositório de código-fonte centralizado no qual profissionais de desenvolvimento de software, engenharia de DevOps e documentação podem publicar código para revisão e colaboração.
- O Azure Boards é um pacote de gerenciamento de projetos ágil que inclui quadros Kanban, relatórios e acompanhamento de ideias e trabalho, de epics de alto nível a itens de trabalho e problemas.
- O Azure Pipelines é uma ferramenta de automação do pipeline de CI/CD.
- O Azure Artifacts é um repositório para hospedagem de artefatos, como o código-fonte compilado, que podem ser inseridos nas etapas dos pipelines de teste ou de implantação.
- O Azure Test Plans é uma ferramenta de teste automatizado que pode ser usada em um pipeline de CI/CD para garantir a qualidade antes da liberação de um software.

O Azure DevOps é uma ferramenta madura, com um grande conjunto de recursos, que começou como um software para servidores local e evoluiu para uma oferta de SaaS (software como serviço) da Microsoft.

Caso seu objetivo seja **automatizar a criação e o gerenciamento de um ambiente de laboratório de teste, considere escolher o Azure DevTest Labs**. Das três ferramentas e serviços que descrevemos, este é o único que oferece essa funcionalidade.

No entanto, você pode automatizar o provisionamento de novos laboratórios como parte de uma cadeia de ferramentas usando o GitHub Actions ou o Azure Pipelines.

Embora o GitHub tenha itens de trabalho, problemas e um quadro Kanban, o gerenciamento de projeto e os relatórios são as áreas de excelência do Azure DevOps. **O Azure DevOps é altamente personalizável**, o que permite que um administrador adicione campos personalizados para capturar metadados e outras informações junto com cada item de trabalho.

O o Azure DevOps tem um conjunto muito mais granular de permissões que possibilita às organizações refinar quem pode executar a maioria das operações em todo o conjunto de ferramentas.

## GitHub e GitHub Actions

O GitHub é, sem dúvida, o repositório de código mais popular do mundo para software livre. O Git é uma ferramenta de gerenciamento de código-fonte descentralizada, e o GitHub é uma versão hospedada do Git que serve como o remoto primário. O GitHub se baseia no Git para fornecer serviços relacionados para coordenar trabalhos, relatar e discutir problemas, fornecer documentação e muito mais.

Embora o Azure DevOps possa publicar repositórios de código públicos, **o GitHub é o host preferencial para software livre** há tempos. **Se você estiver criando software livre, provavelmente escolherá o GitHub devido à sua visibilidade e à aceitação geral da comunidade de desenvolvimento de software livre**.

O GitHub funciona em um modelo simples de permissões de leitura/gravação para cada recurso.

## Azure DevTest Labs

O Azure DevTest Labs fornece um meio automatizado de gerenciar o processo de criação, configuração e remoção de VMs (máquinas virtuais) que contêm builds de seus projetos de software. Dessa maneira, desenvolvedores e testadores podem executar testes em uma variedade de ambientes e builds. E isso não fica limitado às VMs. Tudo o que você pode implantar no Azure por meio de um modelo do ARM pode ser provisionado pelo DevTest Labs. O provisionamento de ambientes de laboratório pré-criados com as ferramentas e as configurações necessárias já instaladas economiza muito tempo para desenvolvedores e profissionais de garantia de qualidade.

Suponha que você precise testar um novo recurso em uma versão antiga de um sistema operacional. O Azure DevTest Labs pode configurar tudo automaticamente após a solicitação. Depois que o teste for concluído, os DevTest Labs poderão desligar e desprovisionar a VM, o que economiza dinheiro quando ela não está em uso. A fim de controlar custos, a equipe de gerenciamento pode restringir quantos laboratórios podem ser criados, por quanto tempo eles são executados e assim por diante.

Use o **Azure DevTest Labs** quando for preciso automatizar e gerenciar a criação de laboratório de teste.

> O Azure Pipelines e o GitHub Actions pode ser usado para automatizar um processo de CI/CD.
>
> > Observação: CI/CD designa respectivamente Continuous Integration e Continuous Delivery traduzindo: Integração Contínua e Entrega Contínua. Ambas as siglas designam processos e técnicas modernas para tornar o processo de desenvolvimento, teste e entrega de ferramentas mais ágil e eficiente.
>
> O Azure Boards é uma ferramenta de gerenciamento de projeto ágil. Ele não seria usado para automatizar um processo de CI/CD.

> O Azure DevTest Labs é usado para gerenciar VMs para teste, incluindo a configuração, o provisionamento e o desprovisionamento automático.
>
> Ele seria o serviço ideal para gerenciar as VMs de que seus desenvolvedores e testadores precisam para garantir que seu novo aplicativo funcione em diversos sistemas operacionais.

> O Azure Pipelines é uma ferramenta de CI/CD para criar uma cadeia de ferramentas automatizada. Ele não tem recursos para atribuir tarefas nas quais desenvolvedores individuais devem trabalhar. No entanto, ele pode automatizar outras ferramentas para atribuir tarefas a usuários.
>
> Caso a empresa precise de um serviço que tenha recursos para atribuir a desenvolvedores individuais tarefas nas quais trabalhar, considere usar o **Azure Boards** ou o **GitHub**.
