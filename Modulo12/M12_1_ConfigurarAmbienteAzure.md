# Escolha as melhores ferramentas para gerenciar e configurar seu ambiente do Azure

Usando as ferramentas de gerenciamento, os administradores, desenvolvedores e gerentes do Azure podem interagir com o ambiente de nuvem para executar tarefas como:

- Implantação de dezenas ou centenas de recursos de cada vez.
- Configuração programática de serviços individuais.
- Exibição de relatórios avançados sobre uso, integridade, custos e muito mais.

## Identificar as opções de produto

Há duas categorias amplas de ferramentas de gerenciamento:

- **ferramentas visuais**: fornecem acesso completo e de fácil visualização a todas as funcionalidades do Azure. No entanto, podem não ser tão úteis quando você tenta configurar uma grande implantação de recursos com interdependências e opções de configuração.
- **ferramentas baseadas em código**: geralmente é a melhor opção quando você tenta instalar e configurar rapidamente recursos do Azure. Embora possa levar algum tempo para entender os comandos e parâmetros certos primeiro, depois de terem sido inseridos, eles podem ser salvos em arquivos e usados repetidamente conforme a necessidade. Além disso, o código que executa a instalação e configuração pode ser armazenado, ter a versão controlada e ser mantido junto com o código-fonte do aplicativo em uma ferramenta de gerenciamento de código-fonte como o Git. Essa **abordagem para gerenciar recursos de hardware e de nuvem que os desenvolvedores usam quando escrevem código do aplicativo é conhecida como _infraestrutura como código_**.

Há duas abordagens de infraestrutura como código:

- **código imperativo**: detalha cada etapa individual que deve ser executada para alcançar um resultado desejado.
- **Declarativo**: detalha apenas um resultado desejado e permite que um interpretador decida como alcançar melhor esse resultado. Essa distinção é importante porque as ferramentas baseadas em código declarativo podem fornecer uma abordagem mais robusta para a implantação de dezenas ou centenas de recursos de maneira simultânea e confiável.

### Opções de produto

- **O portal do Azure**

Usando o portal do Azure, uma interface do usuário baseada na Web, você pode acessar praticamente todos os recursos do Azure.

O portal do Azure fornece uma interface gráfica do usuário amigável para exibir todos os serviços que você está usando, criar serviços, configurar seus serviços e exibir relatórios.

A portal do Azure é como a maioria dos usuários experimenta o Azure primeiro. Mas, à medida que o uso do Azure cresce, você provavelmente escolherá uma abordagem centrada em código mais fácil de repetir para gerenciar seus recursos do Azure.

- **O aplicativo móvel do Azure**

O aplicativo móvel do Azure fornece acesso do iOS e do Android aos recursos do Azure quando você está longe do seu computador. Com ele, você pode:

- - Monitorar a integridade e o status de seus recursos do Azure.
  - Verificar se há alertas, diagnosticar e corrigir problemas rapidamente e reiniciar um aplicativo Web ou VM (máquina virtual).
  - Executar comandos da CLI do Azure ou do Azure PowerShell para gerenciar seus recursos do Azure.

* **Azure PowerShell**

O Azure PowerShell é um **shell com o qual os desenvolvedores, DevOps e profissionais de TI podem executar comandos chamados cmdlets (pronuncia-se command-lets)**. Esses comandos chamam a API REST do Azure para executar toda tarefa de gerenciamento possível no Azure. Os cmdlets podem ser executados de forma independente ou combinados em um arquivo de script e executados juntos para orquestrar:

- - A configuração, desinstalação e manutenção de rotina de um único recurso ou de vários recursos conectados.
  - A implantação de uma infraestrutura inteira, que pode conter dezenas ou centenas de recursos, de um código imperativo.

A captura dos comandos em um script torna o processo repetível e automatizado.

O Azure PowerShell está disponível para Windows, Linux e Mac, e você pode acessá-lo em um navegador da Web por meio do Cloud Shell.

O Windows PowerShell ajudou as organizações de TI com foco no Windows a automatizar muitas de suas operações locais durante anos, e essas organizações criaram um grande catálogo de cmdlets e scripts personalizados, além de acumular experiência.

- **A CLI do Azure**

A interface de linha de comando CLI do Azure é um programa executável com o qual um desenvolvedor, DevOps profissional ou profissional de TI pode executar comandos no Bash. Os comandos chamam a API REST do Azure para executar toda tarefa de gerenciamento possível no Azure. Você pode executar os comandos de maneira independente ou combinados em um script e executados juntos na configuração, remoção e manutenção de rotina de um único recurso ou de um ambiente inteiro.

Em muitos aspectos, a CLI do Azure é quase idêntica ao Azure PowerShell no que você pode fazer com ela. Ambos são executados no Windows, Linux e Mac e podem ser acessados em um navegador da Web por meio do Cloud Shell. A principal diferença é a sintaxe usada. Se você já domina o PowerShell ou o Bash, pode usar a ferramenta que preferir.

- **Modelos de ARM**

Embora seja possível escrever um código imperativo no Azure PowerShell ou na CLI do Azure para configurar e remover um recurso do Azure ou orquestrar uma infraestrutura contendo centenas de recursos, há um modo mais adequado de implementar essa funcionalidade.

Ao usar os modelos do ARM (modelos do Azure Resource Manager), você pode descrever os recursos que deseja usar em um formato JSON declarativo. O benefício é que todo o modelo do ARM é verificado antes de algum código ser executado para fazer com que os recursos sejam criados e conectados corretamente. Em seguida, o modelo orquestra a criação desses recursos em paralelo. Ou seja, se você precisar de 50 instâncias do mesmo recurso, todas as 50 instâncias serão criadas ao mesmo tempo.

No fim das contas, o desenvolvedor, o DevOps profissional ou o profissional de TI precisa apenas definir o estado desejado e a configuração de cada recurso no modelo do ARM e o modelo fará o resto. Os modelos podem até mesmo executar scripts do PowerShell e Bash antes ou depois da configuração de um recurso.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/management-fundamentals/2-identify-product-options)

## Analisar os critérios de decisão

### Você precisa executar ações pontuais de gerenciamento, administração ou criação de relatórios?

**O Azure PowerShell e a CLI do Azure são ferramentas de gerenciamento que lhe permitem obter rapidamente o endereço IP de uma VM (máquina virtual) implantada, reinicializar uma VM ou escalar um aplicativo**. Talvez seja interessante manter scripts personalizados das duas ferramentas sempre à mão em seu disco rígido local para determinadas operações que você executa várias vezes.

Ao contrário da CLI do Azure e do PowerShell, **os modelos do ARM (modelos do Azure Resource Manager) definem os requisitos de infraestrutura em seu aplicativo para implantações repetíveis**. Embora os modelos do ARM não se destinem a cenários pontuais, é possível usá-los para essa finalidade. No entanto, **para cenários únicos, você pode preferir ferramentas mais ágeis como PowerShell, scripts da CLI do Azure ou o portal do Azure**.

Tenha em mente que os modelos do ARM podem incluir scripts do PowerShell e/ou da CLI do Azure, o que lhe dará a capacidade de utilizar scripts para tarefas que podem não ser possíveis com o próprio modelo do ARM. A capacidade de combinar as ferramentas de gerenciamento do Azure proporciona flexibilidade na escolha das ferramentas certas para sua necessidade específica.

O portal do Azure pode executar a maioria (se não todas) das ações administrativas e de gerenciamento. Se você está apenas aprendendo a usar o Azure e/ou precisa configurar e gerenciar recursos com pouca frequência (ou prefere uma interface visual para exibir relatórios), faz sentido tirar proveito da apresentação visual que o portal do Azure oferece.

No entanto, se você está em uma função administrativa ou de gerenciamento de nuvem, é menos eficiente confiar exclusivamente no exame visual e em cliques. Para localizar rapidamente as configurações e as informações com as quais você deseja trabalhar, a CLI do Azure ou o PowerShell fornecerá mais flexibilidade para tarefas repetíveis.

A última ferramenta de gerenciamento a apresentar é o aplicativo móvel do Azure, que você pode acessar por telefone ou tablet iOS ou Android. Como ele é completo, é provável que seja a melhor opção quando não houver um laptop prontamente disponível e você precisar exibir e fazer triagem de problemas imediatamente.~

### Você precisa de uma forma de configurar repetidamente um ou mais recursos e garantir que todas as dependências sejam criadas na ordem correta?

Os **modelos do ARM definem os requisitos de infraestrutura do aplicativo para uma implantação repetível que seja feita de maneira consistente**. Uma etapa de validação garante que todos os recursos possam ser criados na ordem correta com base nas dependências, em paralelo, e sejam idempotentes.

Por outro lado, é totalmente possível usar o PowerShell ou a CLI do Azure para configurar todos os recursos para uma implantação. No entanto, não há nenhuma etapa de validação nessas ferramentas. Se um script encontrar um erro, os recursos de dependência não podem ser revertidos facilmente, as implantações acontecem em série e apenas algumas operações são idempotentes.

### Quando você está criando scripts, traz uma experiência de administração do Windows ou do Linux?

**Se você ou seus administradores de nuvem trazem experiência de administração do Windows, é provável que vocês prefiram o PowerShell.**

**Se você ou seus administradores de nuvem trazem experiência de administração do Linux, é provável que vocês prefiram a CLI do Azure.**

Na prática, qualquer ferramenta pode ser usada para executar a maioria das tarefas administrativas pontuais.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/management-fundamentals/3-analyze-decision-criteria)

## Usar o portal do Azure para compreender e gerenciar visualmente seu ambiente de nuvem

> **Cenário**:
>
> Para garantir que tanto a equipe técnica quanto a executiva estejam cientes dos gastos da empresa com a nuvem, o diretor de operações de nuvem começará a se reunir semanalmente com o diretor financeiro para conversar sobre os gastos com a nuvem. Os dois diretores podem querer se aprofundar nos detalhes durante a reunião para obter mais insights sobre como os recursos do Azure estão sendo usados. O ideal é que os dados sejam exibidos visualmente, mas eles também desejam executar relatórios personalizados em tempo real.

### Qual serviço escolher?

1. Neste cenário, a Tailwind Traders precisa executar ações pontuais de gerenciamento, administração ou criação de relatório?

Sim e, **considerando a necessidade de mostrar os dados visualmente e criar relatórios personalizados durante a reunião, o portal do Azure é a melhor opção**. Os participantes da reunião podem encontrar respostas rapidamente às suas perguntas usando uma infinidade de opções de relatório.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/management-fundamentals/4-use-azure-portal)

## Usar o Azure PowerShell para realizar tarefas administrativas pontuais

> **Cenário**:
>
> A Tailwind Traders emprega tecnólogos com muitas habilidades diferentes. Uma equipe de desenvolvedores e administradores cria e mantém uma coleção de aplicativos de intranet que são vitais para os negócios. Os **integrantes da equipe têm experiências comprovadas no desenvolvimento e na administração de rede do Windows**. A equipe moveu seus aplicativos para a nuvem e agora **precisa de uma maneira de realizar tarefas administrativas, de gerenciamento e de teste pontuais em seu ambiente de intranet**. A equipe percebeu rapidamente que o gerenciamento do Azure por meio do portal leva muito tempo e não é repetível.

### Qual serviço escolher?

1. Neste cenário, a equipe da Tailwind Traders precisa executar tarefas pontuais de gerenciamento, administração ou criação de relatório?

Sim. No entanto, **a equipe já sabe que não quer depender do portal do Azure para essas ações pontuais**. Portanto, **o Azure PowerShell e a CLI do Azure são boas opções**. Vamos analisar qual ferramenta a equipe deve usar daqui a pouco.

2. Neste cenário, a Tailwind Traders precisa de um meio reproduzível e confiável para implantar toda a infraestrutura?

Não, não neste cenário. Assim, os modelos do ARM (modelos do Azure Resource Manager) não são a escolha certa.

3. Quando a equipe da Tailwind Traders está criando scripts, ela traz experiência de administração do Windows ou do Linux?

**Essa equipe tem experiência de administração do Windows**. Provavelmente **seria mais confortável usar o Azure PowerShell**, pois essa ferramenta permite que ela use a sintaxe com a qual está mais confortável para executar tarefas administrativas pontuais.

O Azure PowerShell é a melhor opção para esse cenário.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/management-fundamentals/5-use-azure-powershell)

## Usar a CLI do Azure para realizar tarefas administrativas pontuais

> **Cenário**:
>
> Como observamos na unidade anterior, a Tailwind Traders emprega tecnólogos com muitas habilidades diferentes. A equipe de DevOps tem experiência de administração do Linux. Eles precisam executar tarefas de administração relacionadas à integridade do ambiente de nuvem com frequência. A equipe percebeu rapidamente que o gerenciamento do Azure por meio do portal leva muito tempo e não é repetível.

### Qual serviço escolher?

Você pode eliminar rapidamente os modelos do ARM (modelos do Azure Resource Manager) e o portal do Azure como opções viáveis para este cenário. Então, vamos pular para o terceiro critério de decisão.

A escolha da opção correta nesse cenário deve ser determinada pela experiência da equipe. **Como essa equipe tem experiência de administração do Linux, provavelmente ficaria mais confortável usando a CLI do Azure**. A CLI do Azure permite que a equipe use o shell Bash e sua sintaxe para executar as tarefas de administração pontuais.

A CLI do Azure é a melhor opção para esse cenário.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/management-fundamentals/6-use-azure-cli)

## Usar o aplicativo móvel do Azure para gerenciar o Azure em qualquer lugar

> **Cenário**:
>
> A Tailwind Traders enfrenta picos no tráfego de comércio eletrônico que coincide com feriados nacionais e fins de semana. Nos primeiros anos da empresa, os gerentes de sistemas críticos tinham de se reunir no escritório do diretor de operações de nuvem durante esses períodos importantes. No entanto, agora que a Tailwind Traders tem operado com êxito os sistemas mais críticos, o diretor deseja flexibilizar esse requisito e permitir que os funcionários gastem essas datas com suas famílias. Há algum produto que possa dar suporte a esse cenário?

### Qual serviço escolher?

1. Primeiro, a Tailwind Traders precisa executar ações pontuais de gerenciamento, administração, criação de relatório? 

Sim. A verdadeira pergunta é: como? 

**Uma solução de telefone ou tablet poderia ajudar funcionários específicos a se manterem atentos à integridade do ambiente de nuvem quando estão fora do escritório**. 

**A aplicativo móvel do Azure é provavelmente uma boa forma de se chegar a um acordo, pois permite que os funcionários estejam longe do trabalho e ainda realizem tarefas administrativas e de gerenciamento essenciais e pontuais**.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/management-fundamentals/7-use-azure-mobile-app)

## Usar modelos do ARM para implantar uma infraestrutura de nuvem inteira

> **Cenário**:
>
> A Tailwind Traders deseja colocar suas implantações em nuvem em operação. A empresa precisa de uma maneira repetível e confiável de dimensionar suas operações durante períodos de vendas de pico. Como você vai escolher um processo para dimensionar seu ambiente de produção, precisará ter certeza de que o serviço escolhido:
> * Seja eficiente e tenha potencial para criar muitos recursos em paralelo.
> * Crie todas as dependências na ordem correta.
> * Possa ser usada sem a preocupação de que falhou no meio do provisionamento da infraestrutura necessária.

### Qual serviço escolher?

1. Neste cenário, a Tailwind Traders precisa executar ações pontuais de gerenciamento, administração ou criação de relatório? 

Desta vez, não estamos buscando suporte a tarefas de administração ou gerenciamento pontuais. **Estamos procurando uma tecnologia para automatizar a implantação de toda uma infraestrutura, conforme a necessidade**.

2. A Tailwind Traders precisa de uma maneira repetível e confiável de implantar sua infraestrutura inteira?

Sim, isso é exatamente o que a empresa precisa. Nossos critérios de decisão nos levam a escolher **modelos do ARM (modelos do Azure Resource Manager)** para esse cenário.

Você poderia usar o **Azure PowerShell ou a CLI do Azure**, mas essas tecnologias de script **têm limitações significativas quando se trata de implantação de infraestrutura.** Os modelos do ARM podem ajudar a superar essas limitações.

3. Você precisa criar um script usando código imperativo. 

No entanto, quando você usa modelos do ARM, define sua infraestrutura declarativamente usando código JSON. Em alguns casos, você ainda pode precisar de código imperativo para tarefas de configuração ou de limpeza. Nesses casos, você pode disparar a execução de scripts usando o Azure PowerShell ou a CLI do Azure para executar essas tarefas.

Neste cenário, os modelos do ARM são a opção correta.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/management-fundamentals/8-use-azure-resource-manager)

> ## [Próximo](./M12_2_Resumo.md)
