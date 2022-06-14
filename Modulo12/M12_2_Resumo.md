# Resumo

Há duas categorias amplas de ferramentas de gerenciamento:

- **ferramentas visuais**: fornecem acesso completo e de fácil visualização a todas as funcionalidades do Azure. No entanto, podem não ser tão úteis quando você tenta configurar uma grande implantação de recursos com interdependências e opções de configuração.
- **ferramentas baseadas em código**: geralmente é a melhor opção quando você tenta instalar e configurar rapidamente recursos do Azure. O código que executa a instalação e configuração pode ser armazenado, ter a versão controlada e ser mantido junto com o código-fonte do aplicativo em uma ferramenta de gerenciamento de código-fonte como o Git. Essa **abordagem para gerenciar recursos de hardware e de nuvem que os desenvolvedores usam quando escrevem código do aplicativo é conhecida como _infraestrutura como código_**.

Há duas abordagens de infraestrutura como código:

- **código imperativo**: detalha cada etapa individual que deve ser executada para alcançar um resultado desejado.
- **Declarativo**: detalha apenas um resultado desejado e permite que um interpretador decida como alcançar melhor esse resultado. Essa distinção é importante porque as ferramentas baseadas em código declarativo podem fornecer uma abordagem mais robusta para a implantação de dezenas ou centenas de recursos de maneira simultânea e confiável.

## Opções de produto

### **O portal do Azure**

Usando o portal do Azure, uma interface do usuário baseada na Web, você pode acessar praticamente todos os recursos do Azure.

O portal do Azure fornece uma interface gráfica do usuário amigável para exibir todos os serviços que você está usando, criar serviços, configurar seus serviços e exibir relatórios.

A portal do Azure é como a maioria dos usuários experimenta o Azure primeiro. Mas, à medida que o uso do Azure cresce, você provavelmente escolherá uma abordagem centrada em código mais fácil de repetir para gerenciar seus recursos do Azure.

**Considerando que há a necessidade de mostrar os dados visualmente e criar relatórios personalizados durante a reunião, o portal do Azure é a melhor opção**.

### **O aplicativo móvel do Azure**

O aplicativo móvel do Azure fornece acesso do iOS e do Android aos recursos do Azure quando você está longe do seu computador. Com ele, você pode:

- - Monitorar a integridade e o status de seus recursos do Azure.
  - Verificar se há alertas, diagnosticar e corrigir problemas rapidamente e reiniciar um aplicativo Web ou VM (máquina virtual).
  - Executar comandos da CLI do Azure ou do Azure PowerShell para gerenciar seus recursos do Azure.

**Uma solução de telefone ou tablet poderia ajudar funcionários específicos a se manterem atentos à integridade do ambiente de nuvem quando estão fora do escritório**.

**A aplicativo móvel do Azure é provavelmente uma boa forma de se chegar a um acordo, pois permite que os funcionários estejam longe do trabalho e ainda realizem tarefas administrativas e de gerenciamento essenciais e pontuais**.

### **Azure PowerShell**

O Azure PowerShell é um **shell com o qual os desenvolvedores, DevOps e profissionais de TI podem executar comandos chamados cmdlets (pronuncia-se command-lets)**. Esses comandos chamam a API REST do Azure para executar toda tarefa de gerenciamento possível no Azure. Os cmdlets podem ser executados de forma independente ou combinados em um arquivo de script e executados juntos para orquestrar:

- - A configuração, desinstalação e manutenção de rotina de um único recurso ou de vários recursos conectados.
  - A implantação de uma infraestrutura inteira, que pode conter dezenas ou centenas de recursos, de um código imperativo.

A captura dos comandos em um script torna o processo repetível e automatizado.

O Azure PowerShell está disponível para Windows, Linux e Mac, e você pode acessá-lo em um navegador da Web por meio do Cloud Shell.

O Windows PowerShell ajudou as organizações de TI com foco no Windows a automatizar muitas de suas operações locais durante anos, e essas organizações criaram um grande catálogo de cmdlets e scripts personalizados, além de acumular experiência.

**O Azure PowerShell e a CLI do Azure são ferramentas de gerenciamento que lhe permitem obter rapidamente o endereço IP de uma VM (máquina virtual) implantada, reinicializar uma VM ou escalar um aplicativo**. Talvez seja interessante manter scripts personalizados das duas ferramentas sempre à mão em seu disco rígido local para determinadas operações que você executa várias vezes.

**Se você ou seus administradores de nuvem trazem experiência de administração do Windows, é provável que vocês prefiram o PowerShell.**

**Se a equipe já sabe que não quer depender do portal do Azure para essas ações pontuais**. Portanto, **o Azure PowerShell e a CLI do Azure são boas opções**

### **A CLI do Azure**

A interface de linha de comando CLI do Azure é um programa executável com o qual um desenvolvedor, DevOps profissional ou profissional de TI pode executar comandos no Bash. Os comandos chamam a API REST do Azure para executar toda tarefa de gerenciamento possível no Azure. Você pode executar os comandos de maneira independente ou combinados em um script e executados juntos na configuração, remoção e manutenção de rotina de um único recurso ou de um ambiente inteiro.

Em muitos aspectos, a CLI do Azure é quase idêntica ao Azure PowerShell no que você pode fazer com ela. Ambos são executados no Windows, Linux e Mac e podem ser acessados em um navegador da Web por meio do Cloud Shell. A principal diferença é a sintaxe usada. Se você já domina o PowerShell ou o Bash, pode usar a ferramenta que preferir.

**O Azure PowerShell e a CLI do Azure são ferramentas de gerenciamento que lhe permitem obter rapidamente o endereço IP de uma VM (máquina virtual) implantada, reinicializar uma VM ou escalar um aplicativo**. Talvez seja interessante manter scripts personalizados das duas ferramentas sempre à mão em seu disco rígido local para determinadas operações que você executa várias vezes.

**Se você ou seus administradores de nuvem trazem experiência de administração do Linux, é provável que vocês prefiram a CLI do Azure.**

**Se a equipe já sabe que não quer depender do portal do Azure para essas ações pontuais**. Portanto, **o Azure PowerShell e a CLI do Azure são boas opções**

### **Modelos de ARM**

Embora seja possível escrever um código imperativo no Azure PowerShell ou na CLI do Azure para configurar e remover um recurso do Azure ou orquestrar uma infraestrutura contendo centenas de recursos, há um modo mais adequado de implementar essa funcionalidade.

Ao usar os modelos do ARM (modelos do Azure Resource Manager), você pode descrever os recursos que deseja usar em um formato JSON declarativo. O benefício é que todo o modelo do ARM é verificado antes de algum código ser executado para fazer com que os recursos sejam criados e conectados corretamente. Em seguida, o modelo orquestra a criação desses recursos em paralelo. Ou seja, se você precisar de 50 instâncias do mesmo recurso, todas as 50 instâncias serão criadas ao mesmo tempo.

Ao contrário da CLI do Azure e do PowerShell, **os modelos do ARM (modelos do Azure Resource Manager) definem os requisitos de infraestrutura em seu aplicativo para implantações repetíveis**. Embora os modelos do ARM não se destinem a cenários pontuais, é possível usá-los para essa finalidade. No entanto, **para cenários únicos, você pode preferir ferramentas mais ágeis como PowerShell, scripts da CLI do Azure ou o portal do Azure**.

Os **modelos do ARM definem os requisitos de infraestrutura do aplicativo para uma implantação repetível que seja feita de maneira consistente**. Uma etapa de validação garante que todos os recursos possam ser criados na ordem correta com base nas dependências, em paralelo, e sejam idempotentes.

> A CLI do Azure permite que você use o Bash para executar tarefas pontuais no Azure.
>
> Um exemplo de uso seria para recuperar o endereço IP de uma VM específica usando o Bash.

> O portal do Azure é um ótimo local para novatos aprenderem sobre o Azure e configurar seus primeiros recursos.

> Os modelos do ARM são a melhor opção de infraestrutura como código para configurar de maneira rápida e confiável sua infraestrutura de nuvem inteira de maneira declarativa.
