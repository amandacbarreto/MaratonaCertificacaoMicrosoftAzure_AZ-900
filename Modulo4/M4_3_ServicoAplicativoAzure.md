# Decidir quando usar o Serviço de Aplicativo do Azure

> ### O Serviço de Aplicativo **permite que você crie e hospede aplicativos Web, trabalhos em segundo plano, back-ends de dispositivos móveis e APIs RESTful na linguagem de programação de sua escolha sem gerenciar a infraestrutura**. 
> Ele oferece dimensionamento automático e alta disponibilidade. O Serviço de Aplicativo é compatível com Windows e Linux e permite implantações automatizadas do GitHub, Azure DevOps ou qualquer repositório Git para dar suporte a um modelo de implantação contínua.

Esse ambiente de _PaaS (plataforma como serviço)_ permite que você se concentre no site e na lógica da API, enquanto o Azure manipula a infraestrutura para executar e dimensionar seus aplicativos Web.

## Custos do Serviço de Aplicativo do Azure

Você paga pelos recursos de Computação do Azure que o seu aplicativo usa ao processar solicitações com base no plano do Serviço de Aplicativo que você escolher. 

O plano do Serviço de Aplicativo determina a quantidade de hardware dedicada ao host (se hardware é dedicado ou compartilhado e a quantidade de memória reservada para ele). Há até mesmo uma camada gratuita que você pode usar para hospedar sites pequenos e de baixo tráfego.

## Tipos de serviços de aplicativos

Com o Serviço de Aplicativo, você pode hospedar os estilos mais comuns de serviço de aplicativos, como:

* Aplicativos Web
* Aplicativos de API
* WebJobs
* Aplicativos móveis

O Serviço de Aplicativo cuida da maioria das decisões de infraestrutura com as quais você lida ao hospedar aplicativos acessíveis pela Web:

* A implantação e o gerenciamento são integrados à plataforma.
* Pontos de extremidade podem ser protegidos.
* Sites podem ser dimensionados rapidamente para lidar com cargas de alto tráfego.
* O balanceamento de carga interno e o gerenciador de tráfego fornecem alta disponibilidade.

Todos esses estilos de aplicativos são hospedados na mesma infraestrutura e compartilham esses benefícios. Essa flexibilidade torna o Serviço de Aplicativo a escolha ideal para hospedar aplicativos voltados para a Web.

### Aplicativos Web

O Serviço de Aplicativo inclui suporte completo para a hospedagem de aplicativos Web usando ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP ou Python. Você pode escolher Windows ou Linux como sistema operacional do host.

### Aplicativos de API

Da mesma forma como se hospeda um site, você pode criar APIs Web baseadas em REST usando a linguagem e a estrutura que você quiser. Receba o suporte completo do Swagger e a capacidade de empacotar e publicar sua API no Azure Marketplace. Os aplicativos produzidos podem ser consumidos por qualquer cliente baseado em HTTP ou em HTTPS.

### WebJobs

Você pode usar o recurso do WebJobs para executar um script (.cmd, .bat, PowerShell ou Bash) ou um programa (.exe, Java, PHP, Python ou Node.js) no mesmo contexto de um aplicativo Web, aplicativo de API ou aplicativo móvel. Eles também podem ser agendados ou executados por um gatilho. O WebJobs geralmente é usado para executar tarefas em segundo plano como parte da lógica do aplicativo.

### Aplicativos móveis

Use o recurso Aplicativos Móveis do Serviço de Aplicativo para criar rapidamente um back-end para aplicativos iOS e Android. Com apenas alguns cliques no portal do Azure, você pode:

* Armazenar dados de aplicativo móvel em um Banco de Dados SQL baseado em nuvem.
* Autenticar os clientes em relação a provedores sociais comuns, como MSA, Google, Twitter e Facebook.
* Enviar notificações por push.
* Executar a lógica personalizada de back-end no C# ou Node.js.

No lado do aplicativo móvel, há suporte do SDK para aplicativos nativos para iOS, Android, Xamarin e React.


###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-compute-fundamentals/azure-app-services)

> ## [Próximo](./M4_4_ConteinerOuKubernetes.md)