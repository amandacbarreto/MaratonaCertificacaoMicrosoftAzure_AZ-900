# Decidir quando usar as Instâncias de Contêiner do Azure ou o Serviço de Kubernetes do Azure

Embora as máquinas virtuais sejam uma excelente maneira de reduzir os custos em comparação com os investimentos necessários para o hardware físico, elas ainda estão limitadas a um sistema operacional por máquina virtual. Se você quer executar várias instâncias de um aplicativo em um só computador host, os contêineres são uma ótima opção.

## O que são contêineres?

> ### **Contêineres são um ambiente de virtualização**.

Assim como a execução de várias máquinas virtuais em um só host físico, você pode executar vários contêineres em apenas um host físico ou virtual.

Diferentemente das máquinas virtuais, você não gerencia o sistema operacional para um contêiner.

As máquinas virtuais parecem ser uma instância de um sistema operacional ao qual você pode se conectar e que você pode gerenciar, **mas os contêineres são leves e projetados para serem criados, dimensionados e interrompidos dinamicamente**.

Embora seja possível criar e implantar máquinas virtuais à medida que a demanda do aplicativo aumenta, **os contêineres são projetados para permitir que você responda às alterações sob demanda**.

Com contêineres, você pode reiniciar rapidamente no caso de uma falha ou de uma interrupção de hardware. **Um dos mecanismos de contêiner mais populares é o Docker, que tem suporte do Azure.**

### Comparar máquinas virtuais e contêineres

> **Um contêiner agrupa um único aplicativo e suas dependências**, o que é chamado de "colocar o aplicativo em contêiner". Depois, ele o implementa como uma unidade em um host de contêiner.

O host de contêiner oferece um ambiente de tempo de execução padronizado que abstrai os requisitos de infraestrutura e de sistema operacional, permitindo que o aplicativo em contêiner seja executado lado a lado com outros aplicativos em contêineres.

<center><h3>
<em>VMs virtualizam o hardware</em> <strong>X</strong> <em>contêineres virtualizam o sistema operacional</em>
</h3></center>

A virtualização de contêineres no nível do sistema operacional é um dos motivos que torna a abordagem de contêiner mais eficiente do que uma máquina virtual completa. Ela permite que executar vários contêineres leves em único host sem sacrificar o isolamento que a máquina virtual oferece originalmente.

O Azure é compatível com diversas variações de contêiner, **sendo o Docker a mais popular**.

Ao contrário das VMs, é possível iniciar contêineres rapidamente. Você apenas aguarda o aplicativo ser iniciado, em vez de aguardar o sistema operacional e o aplicativo.

Além disso, os aplicativos em contêineres tendem a ter um tamanho menor e o processo de desenvolvimento é simplificado, já que seu ambiente de tempo de execução de desenvolvimento pode ser igual ao ambiente de produção.

Outra vantagem dos contêineres é que eles podem ser organizados com coordenação de clusters de contêiner. Você pode implantar e gerenciar vários aplicativos em contêineres facilmente, sem se preocupar sobre qual servidor hospedará cada contêiner.

**A decisão de usar uma VM ou um contêiner depende da flexibilidade necessária**. Se você quiser controlar completamente o ambiente, poderá escolher uma VM. Caso contrário, a portabilidade, as características de desempenho e os recursos de gerenciamento dos contêineres poderão ser uma escolha melhor.

### Gerenciar contêineres

Os contêineres são gerenciados por meio de um orquestrador de contêineres, que pode iniciar, interromper e dimensionar as instâncias do aplicativo conforme necessário. Há duas maneiras de gerenciar contêineres baseados no Docker e na Microsoft no Azure:

- Instâncias de Contêiner do Azure
- AKS (Serviço de Kubernetes do Azure).

#### Instâncias de Contêiner do Azure

As Instâncias de Contêiner do Azure oferecem a maneira mais rápida e simples de executar um contêiner no Azure, sem a necessidade de gerenciar máquinas virtuais nem adotar serviços adicionais. Trata-se de uma oferta de PaaS (plataforma como serviço) que permite que você carregue contêineres, que ela executará para você.

#### Serviço de Kubernetes do Azure

A tarefa de automatizar, gerenciar e interagir com um grande número de contêineres é conhecida como orquestração. O Serviço de Kubernetes do Azure é um serviço de orquestração completa para contêineres com arquiteturas distribuídas e grandes volumes de contêineres.

### O que é o Kubernetes?

> #### O kubernetes é uma das opções mais populares para gerenciar cargas de trabalho baseadas em contêiner.
> Ele combina a automação de gerenciamento de contêiner com uma API extensível para criar uma potência de gerenciamento de aplicativos nativos de nuvem.

Em seu núcleo, o Kubernetes gerencia o posicionamento de pods, que pode consistir em um ou mais contêineres, em um nó de cluster do Kubernetes. Além disso, se um desses pods falhar, o Kubernetes poderá criar uma nova instância dele. 

Se um nó de cluster for removido, o Kubernetes poderá mover qualquer carga de trabalho efetuada para um nó diferente no cluster.

Além disso, os pods do Kubernetes podem ser escalados para fornecer mais ou menos taxa de transfêrencia para atender às demandas de escala. E essas operações de escala podem ser disparadas de modo manual ou automático, usando o dimensionamento automático de pod horizontal do Kubernetes.

Por fim, se um aplicativo precisa ser atualizado, o Kubernetes poderá escalonar a implantação da atualização para minimizar o tempo de inatividade. Além disso, se a atualização for problemática, o Kubernetes poderá ser revertido para uma versão anterior. 

Juntamente com o gerenciamento de pod o Kubernetes também pode gerenciar o armazenamento de contêiner e a rede. 

Os Volumes Persistentes do Kubernetes podem ser usados para apresentar o armazenamento de dados para um ou mais contêineres. Essa configuração permite aos contêinres ler e gravar dados de aplicativo e persistir esses dados entre muitas instâncias de pod. Dito isso, também é comum um aplicativo em execução no Kubernetes usar o armazenamento baseado em nuvem e o sistema de dados, como o Armazenamento do Azure ou o Azure Cosmos DB, para armazenamento e recuperação de dados.



### Usar contêineres em suas soluções

Contêineres geralmente são usados para criar soluções que utilizam uma arquitetura de microsserviço. Essa arquitetura é onde você divide as soluções em partes menores e independentes. Por exemplo, você pode dividir um site em um contêiner que hospeda o front-end, outro que hospeda o back-end e um terceiro para o armazenamento. Essa divisão permite separar as partes do aplicativo em seções lógicas que podem ser mantidas, dimensionadas ou atualizadas de forma independente.

Imagine que o back-end do site atingiu a capacidade, mas o front-end e o armazenamento não estão sob pressão. Você pode:

* Dimensionar o back-end separadamente para aprimorar o desempenho.
* Optar por usar outro serviço de armazenamento.
* Substituir o contêiner de armazenamento sem afetar o restante do aplicativo.

### O que é um microsserviço?

> #### Um microsserviço é apenas um **serviço Web que tem um escopo pequeno e bem definido e é acoplado de forma flexível a qualquer outro serviço Web**.

Geralmente, não se cria um único microsserviço.
A organização adota uma arquitetura de microsserviços que consiste em uma coleção deles. 
* Cada um é autosuficiente e implementa uma única funcionalidade comercial.
* Cada serviço é uma base de código separado, que pode ser gerenciado por uma equipe de desenvolvimento pequena.

Na verdade, os microsserviços não precisam compartilhar as mesmas pilhas de tecnologia, bibliotecas ou estruturas, o que permite que cada equipe escolha a ferramenta certa para o trabalho.

Isso significa que uma única equipe de desenvolvimento pode criar, testar e implantar um serviço. O resultado é inovação contínua e um ritmo mais rápido de liberação. Assim, as equipes podem se concentrar em um único serviço.

Além disso, com um escopo menor de cada serviço, a base de código fica mais fácil de ser entendida, facilitando a compreensão e o início do trabalho para novos membros da equipe. A adoção desse caminho permite que cada microsserviço seja implantado de forma independente dos outros na organização.

Uma equipe pode atualizar um serviço existente sem recompilar e reimplantar o aplicativo inteiro. Além disso, eles podem reverter ou efetuar roll foward facilmente em uma atualização quando algo dá errado. A melhor parte é que isso faz com que as correções de bugs e os lançamentos de recursos sejam mais gerenciáveis e menos arriscados.

A estratégia de implantação também significa que cada microsserviço pode ser dimensionado de forma independente. 

Um benefício dessa eficiência é que cada microsserviço é responsável por manter seus próprios dados ou seu estado externo  e sem depender de nenhuma camada de respositório comum (compartilhado).

Na verdade, alguns especialistas em microsserviços insistem que cada microsserviço deverá ter até mesmo seu próprio banco de dados separados. 

Novamente, a ideia é que cada microsserviço seja completamente autônomo, sem dependências cruzadas, de uma perspectiva de domínio de negócios. Esse tipo de liberdade oferece uma camada de isolamento de falhas. Se um serviço falhar, ele não travará o aplicativo inteiro. 

> **Os microsserviços podem se comunicar entre si por meio de APIs bem definidas**.

Os detalhes da implementação interna de cada serviço são encapsulados por trás de sua interface. 

> No entanto, normalmente a solução é reduzir essas interdependências e tentar introduzir uma camada de orquestração ou de gerenciamento no aplicativo de consumo de nível mais alto que coordene as chamadas a vários microsserviços de nível inferior e combine os resultados. 

Uma arquitetura de microsserviços resolve alguns problemas e é mais adequada quando há um aplicativo grande que precise de uma alta velocidade de liberação, há aplicativos complexos que precisam ser altamente escalonáveis, há aplicativos com domínios avançados ou muitos subdomínios ou quando a organização consiste em pequenas equipes de desenvolvimento.

Os microsserviços podem aproveitar as funcionalidades de gerenciamento e hospedagem de vários serviços diferentes do Azure. 

> Em suma, **os microsserviços são uma maneira de simplificar a arquitetura de um aplicativo, concentrando-se na criação de serviços Web menores, mais gerenciáveis, autônomos e implantados de forma independente, que abrangem um único domínio de negócios ou uma única funcionalidade**.


###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-compute-fundamentals/azure-container-services)

> ## [Próximo](./M4_5_AzureFunctions.md)
