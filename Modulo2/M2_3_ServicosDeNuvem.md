# Descrever diferentes serviços de nuvem

## O que são modelos de serviço de nuvem?

> Os modelos definem os diferentes níveis de responsabilidade compartilhada pelo provedor e pelo locatário de nuvem e podem ser *IaaS*, *PaaS* e *SaaS*.


| Modelo | Definição | Descrição |
| :--------:| :----: | :---- |
IaaS | Infraestrutura como Serviço | Esse modelo de serviço de nuvem é o mais próximo do gerenciamento de servidores físicos; um provedor de nuvem manterá o hardware atualizado, mas a manutenção do sistema operacional e a configuração da rede ficam a cargo do locatário da nuvem. Por exemplo, as máquinas virtuais do Azure são dispositivos de computação virtual totalmente operacionais em execução nos data centers da Microsoft. Uma vantagem desse modelo de serviço de nuvem é a implantação rápida de novos dispositivos de computação. A configuração de uma nova máquina virtual é consideravelmente mais rápida do que o processo de adquirir, instalar e configurar um servidor físico.
PaaS | Plataforma como serviço | Esse modelo de serviço de nuvem é um ambiente de hospedagem gerenciado. O provedor de nuvem gerencia as máquinas virtuais e os recursos de rede e o locatário de nuvem implanta seus aplicativos no ambiente de hospedagem gerenciado. Por exemplo, os Serviços de Aplicativos do Azure fornecem um ambiente de hospedagem gerenciado em que os desenvolvedores podem carregar os aplicativos Web sem precisar se preocupar com os requisitos de software e hardware físico.
SaaS | Software como serviço | Nesse modelo de serviço de nuvem, o provedor de nuvem gerencia todos os aspectos do ambiente de aplicativo, como as máquinas virtuais, os recursos de rede, o armazenamento de dados e os aplicativos. O locatário de nuvem só precisa fornecer seus dados para o aplicativo gerenciado pelo provedor de nuvem. Por exemplo, Microsoft Office 365 fornece uma versão totalmente funcional do Microsoft Office que é executada na nuvem. Você só precisa criar seu conteúdo e o Office 365 cuida de todo o resto.


### **IaaS**

> É a categoria mais flexível de serviços de nuvem. 
> **Objetivo**: oferecer total controle sobre o hardware que executa seu aplicativo. Com a IaaS, você aluga o hardware em vez de comprá-lo.

**Vantagens**

* **Não há CapEx**. Os usuários não têm custos antecipados.
* **Agilidade**. Os aplicativos podem ficar acessíveis rapidamente e desprovisionados sempre que necessário.
* **Gerenciamento**. O modelo de responsabilidade compartilhada se aplica; o usuário gerencia e mantém os serviços que provisionou e o provedor de nuvem gerencia e mantém a infraestrutura de nuvem.
* **Modelo baseado em consumo**. As organizações pagam apenas pelo que usam e operam em um modelo de OpEx (despesas operacionais).
* **Habilidades.** Não são necessárias habilidades técnicas refinadas para implantar, usar e obter os benefícios de uma nuvem pública. As organizações podem usar as habilidades e a competência do provedor de nuvem para garantir que as cargas de trabalho estejam seguras, protegidas e altamente disponíveis.
* **Benefícios de nuvem**. As organizações podem usar as habilidades e a competência do provedor de nuvem para garantir que as cargas de trabalho fiquem seguras, protegidas e altamente disponíveis.
* **Flexibilidade**. O IaaS é o serviço de nuvem mais flexível, pois você tem controle para configurar e gerenciar o hardware que executa seu aplicativo.

### **PaaS**

> Oferece os mesmos benefícios e considerações que a IaaS, mas há alguns benefícios adicionais a ter em mente.

**Vantagens**

* **Não há CapEx**. Os usuários não têm custos antecipados.
* **Agilidade**. A PaaS é mais ágil do que a IaaS, e os usuários não precisam configurar servidores para a execução de aplicativos.
* **Modelo baseado em consumo**. Os usuários pagam apenas pelo que usam e operam segundo um modelo OpEx.
* **Habilidades**. Não são necessárias habilidades técnicas refinadas para implantar, usar e obter os benefícios do PaaS.
* **Benefícios de nuvem**. Os usuários podem tirar proveito das habilidades e da competência do provedor de nuvem para garantir que as cargas de trabalho fiquem seguras, protegidas e altamente disponíveis. Além disso, os usuários podem ter acesso a mais ferramentas de desenvolvimento de ponta. Eles podem aplicar essas ferramentas em todo o ciclo de vida de um aplicativo.
* **Produtividade**. Os usuários podem se concentrar apenas no desenvolvimento de aplicativos, pois o provedor de nuvem cuida de todo o gerenciamento da plataforma. Trabalhar com equipes distribuídas como serviços é mais fácil porque a plataforma é acessada pela Internet. A plataforma pode ser disponibilizada globalmente com mais facilidade.

**Desvantagem**
* **Limitações da plataforma**. Pode haver algumas limitações para uma plataforma de nuvem que podem afetar a execução de um aplicativo. Quando estiver avaliando qual plataforma de PaaS é mais adequada para uma carga de trabalho, considere as limitações nessa área.

### **SaaS**

> É um software que é hospedado e gerenciado de maneira centralizada para você e seus usuários ou clientes. Geralmente, uma versão do aplicativo é usada para todos os clientes e é licenciada por meio de uma assinatura mensal ou anual.

O SaaS oferece os mesmos benefícios que a IaaS, mas, novamente, há alguns benefícios adicionais a ter em mente.

**Vantagens**


* **Não há CapEx**. Os usuários não têm custos antecipados.
* **Agilidade**. Os usuários podem fornecer acesso ao software mais recente à equipe de maneira rápida e fácil.
* **Modelo de preço pago conforme o uso**. Os usuários pagam pelo software que usam em um modelo de assinatura, normalmente mensal ou anual, independentemente de quanto eles usam o software.
* **Habilidades**. Não são necessárias habilidades técnicas refinadas para implantar, usar e obter os benefícios do SaaS.
* **Flexibilidade**. Os usuários podem acessar os mesmos dados de aplicativo de qualquer lugar.

**Desvantagem**
* **Limitações de software**. Pode haver algumas limitações para um aplicativo de software que podem afetar o trabalho dos usuários. Por estar usando um software no estado em que se encontra, você não tem controle direto dos recursos.

## Comparação de modelos de serviço de nuvem

| IaaS | PaaS | SaaS |
| :--------| :---- | :---- |
O serviço de nuvem mais flexível. | Focado no desenvolvimento de aplicativos. | Modelo de preço pago conforme o uso.
Você configura e gerencia o hardware para seu aplicativo. | O gerenciamento de plataforma é realizado pelo provedor de nuvem. | Os usuários pagam pelo software que utilizam em um modelo de assinatura.

## O que é a computação sem servidor?

> Assim como a PaaS, permite que os desenvolvedores criem aplicativos mais rapidamente, eliminando a necessidade de gerenciar a infraestrutura.
> Com aplicativos sem servidor, o provedor de serviços de nuvem provisiona, escala e gerencia automaticamente a infraestrutura necessária para executar o código. As arquiteturas sem servidor são altamente escalonáveis e orientadas a eventos, usando recursos apenas quando há uma função ou um gatilho específico.

O nome "sem servidor" é proveniente do fato de que as tarefas associadas ao provisionamento e ao gerenciamento de infraestrutura são invisíveis para o desenvolvedor, mas os servidores ainda estão executando o código. 

Essa abordagem permite que os desenvolvedores aumentem seu foco na lógica de negócios e ofereçam mais valor ao núcleo dos negócios. 






> ## [Próximo](./M2_4_Resumo.md)
