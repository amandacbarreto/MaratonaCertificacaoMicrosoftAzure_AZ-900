# Visão geral dos serviços de computação do Azure

> ### A **computação do Azure** é um serviço de computação sob demanda para execução de aplicativos baseados em nuvem.
>
> Ela fornece recursos de computação, como discos, processadores, memória, rede e sistemas operacionais.
>
> Os recursos estão disponíveis sob demanda e normalmente podem ser disponibilizados em minutos ou até mesmo segundos. Você só paga pelos recursos utilizados e apenas pelo tempo que utilizar.

O Azure dá suporte a uma ampla gama de soluções de computação para desenvolvimento e teste, execução de aplicativos e extensão do datacenter. O serviço dá suporte a Linux, Windows Server, SQL Server, Oracle, IBM e SAP. O Azure também tem muitos serviços que podem executar VMs (máquinas virtuais). Cada serviço fornece opções diferentes dependendo de seus requisitos. Alguns dos serviços mais proeminentes são:

- Máquinas Virtuais do Azure
- Instâncias de Contêiner do Azure
- Serviço de aplicativo do Azure
- Azure Functions (ou computação sem servidor)

## Máquinas virtuais

> ### Máquinas virtuais são **emulações de software de computadores físicos**.
>
> Elas incluem um processador virtual, memória, armazenamento e recursos de rede.
>
> As VMs hospedam um sistema operacional, e você pode instalar e executar o software como se fosse um computador físico. .

Com as Máquinas Virtuais do Azure, você pode criar e usar VMs na nuvem. As Máquinas Virtuais fornecem _IaaS (infraestrutura como serviço)_ e podem ser usadas de maneiras diferentes.

Quando você precisa ter controle total sobre um sistema operacional e ambiente, as VMs são a opção ideal. Como em um computador físico, você pode personalizar todos os programas de software em execução na VM. Essa capacidade é útil quando você executa configurações personalizadas de software ou de hospedagem.

## Conjuntos de dimensionamento de máquinas virtuais

> ### Os conjuntos de dimensionamento de máquinas virtuais **são um recurso de computação do Azure que você pode usar para implantar e gerenciar um conjunto de VMs idênticas**.
>
> Com todas as VMs configuradas da mesma forma, os conjuntos de dimensionamento de máquinas virtuais têm a finalidade de dar suporte ao verdadeiro dimensionamento automático.
>
> Nenhum provisionamento prévio das VMs é necessário. Por esse motivo, é mais fácil criar serviços de grande escala direcionados a grandes cargas de trabalho de computação, Big Data e em contêineres.
>
> Conforme a demanda aumenta, mais instâncias de VM podem ser adicionadas. Conforme a demanda diminui, instâncias de VM podem ser removidas. O processo pode ser manual, automatizado ou uma combinação de ambos.

## Contêineres e Kubernetes

> ### As Instâncias de Contêiner e o Serviço de Kubernetes do Azure **são recursos de Computação do Azure que você pode usar para implantar e gerenciar contêineres**.

> ### Contêineres são **ambientes de aplicativos leves e virtualizados**.
>
> Eles foram projetados para serem criados rapidamente, escalados horizontalmente e interrompidos dinamicamente. Você pode executar várias instâncias de um aplicativo em contêineres em um computador host.

    Kubernetes é um produto Open Source utilizado para automatizar a implantação, o dimensionamento e o gerenciamento de aplicativos em contêiner.
    Ele agrupa contêineres que compõem uma aplicação em unidades lógicas para facilitar o gerenciamento e a descoberta de serviço.

## Serviço de Aplicativo

> ### Com o Serviço de Aplicativo do Azure, você pode **criar, implantar e dimensionar rapidamente aplicativos Web, móveis e de API de nível empresarial executados em qualquer plataforma**.
>
> Você pode atender a requisitos rigorosos de desempenho, escalabilidade, segurança e conformidade ao usar uma plataforma totalmente gerenciada para executar a manutenção de infraestrutura. O Serviço de Aplicativo é uma oferta de _PaaS (plataforma como serviço)_.

## Funções

> As funções são ideais quando você está preocupado apenas com o código que executa o serviço, e não com a plataforma ou a infraestrutura subjacente. Elas costumam ser usadas quando você precisa executar um trabalho em resposta a um evento (geralmente por meio de uma solicitação REST), um temporizador ou uma mensagem de outro serviço do Azure, e quando esse trabalho pode ser concluído dentro de segundos.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-compute-fundamentals/overview)

> ## [Próximo](./)
