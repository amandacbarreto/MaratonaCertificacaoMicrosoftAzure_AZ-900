# Decidir quando usar a Área de Trabalho Virtual do Azure

## O que é a Área de Trabalho Virtual do Azure?

> ### A Área de Trabalho Virtual do Azure é um **serviço de virtualização de área de trabalho e aplicativos que é executado na nuvem**. Ele permite que os usuários usem uma versão do Windows hospedada na nuvem em qualquer localização.

A Área de Trabalho Virtual do Azure funciona em dispositivos como Windows, Mac, iOS, Android e Linux. Ela funciona com aplicativos que você pode usar para acessar aplicativos e Áreas de Trabalho Remotas. Você também pode usar os navegadores mais modernos para acessar experiências hospedadas na Área de Trabalho Virtual do Azure.

## Por que você deve usar a Área de Trabalho Virtual do Azure?

### Fornecer a melhor experiência do usuário

Os usuários têm a liberdade de se conectar à Área de Trabalho Virtual do Azure com qualquer dispositivo pela Internet. Eles usam um cliente da Área de Trabalho Virtual do Azure para se conectar aos aplicativos e à área de trabalho do Windows publicados. Esse cliente pode ser um aplicativo nativo no dispositivo ou o cliente Web do HTML5 da Área de Trabalho Virtual do Azure.

Você pode garantir que suas VMs (máquinas virtuais) do host de sessão sejam executadas perto de aplicativos e serviços que se conectam ao seu datacenter ou à nuvem. Assim, os usuários permanecem produtivos e não encontram tempos de carregamento longos.

Você pode fornecer propriedade individual por meio de áreas de trabalho pessoais (persistentes). Por exemplo, talvez seja interessante fornecer Áreas de Trabalho Remotas pessoais para membros de uma equipe de engenharia. Eles podem adicionar ou remover programas sem afetar outros usuários nessa Área de Trabalho Remota.

### Aprimorar a segurança

A Área de Trabalho Virtual do Azure oferece gerenciamento de segurança centralizado para as áreas de trabalho dos usuários com o Azure AD (Azure Active Directory). Você pode habilitar a autenticação multifator para proteger as entradas do usuário. Você também pode proteger o acesso aos dados atribuindo RBACs (controles de acesso baseados em função) granulares aos usuários.

Com a Área de Trabalho Virtual do Azure, os dados e aplicativos ficam separados do hardware local. A Área de Trabalho Virtual do Azure os executa em um servidor remoto. O risco de dados confidenciais serem deixados em um dispositivo pessoal é reduzido.

As sessões de usuário são isoladas em ambientes de sessão única e de várias sessões.

A Área de Trabalho Virtual do Azure também aprimora a segurança usando a tecnologia de conexão reversa. Esse tipo de conexão é mais seguro do que o protocolo RDP. Não abrimos portas de entrada para as VMs do host de sessão.

## Quais são alguns dos principais recursos da Área de Trabalho Virtual do Azure?

### Gerenciamento simplificado

A Área de Trabalho Virtual do Azure é um serviço do Azure, de modo que será familiar para os administradores do Azure. Você usa o Azure AD e RBACs para gerenciar o acesso aos recursos. Com o Azure, você também obtém ferramentas para automatizar implantações de VM, gerenciar atualizações de VM e fornecer recuperação de desastre. Assim como acontece com outros serviços do Azure, a Área de Trabalho Virtual do Azure usa o Azure Monitor para monitoramento e alertas. Essa padronização permite que os administradores identifiquem problemas por meio de uma interface.

### Gerenciamento de desempenho

A Área de Trabalho Virtual do Azure oferece opções para balancear a carga dos usuários em seus pools de host de VM. Os pools de host são coleções de VMs com a mesma configuração atribuída a vários usuários. Para obter o melhor desempenho, você pode configurar o balanceamento de carga para ocorrer conforme os usuários entram (modo de amplitude). Com o modo de amplitude, os usuários são alocados sequencialmente no pool de host para sua carga de trabalho. Para economizar custos, você pode configurar suas VMs para o balanceamento de carga do modo de profundidade, em que os usuários são totalmente alocados em uma VM antes de passar para a próxima. A Área de Trabalho Virtual do Azure fornece ferramentas para provisionar automaticamente VMs adicionais quando a demanda de entrada excede um limite especificado.

### Implantação do Windows 10 multissessão

A Área de Trabalho Virtual do Azure permite que você use a multissessão do Windows 10 Enterprise, o único sistema operacional baseado em cliente Windows que habilita vários usuários simultâneos em uma VM. A Área de Trabalho Virtual do Azure também fornece uma experiência mais consistente com suporte a aplicativos mais amplo em comparação com sistemas operacionais baseados no Windows Server.

## Como você pode reduzir os custos com a Área de Trabalho Virtual do Azure?

### Traga sua própria licença

A Área de Trabalho Virtual do Azure estará disponível para você sem custos adicionais se você tiver uma licença do Microsoft 365 qualificada. Pague apenas pelos recursos do Azure usados pela Área de Trabalho Virtual do Azure.

- Traga sua licença do Windows ou Microsoft 365 qualificada para obter aplicativos e áreas de trabalho do Windows 10 Enterprise e Windows 7 Enterprise sem custo adicional.
- Se você for um cliente com licença de acesso para cliente aos Serviços de Área de Trabalho Remota da Microsoft, os aplicativos e as áreas de trabalho dos Serviços de Área de Trabalho Remota do Windows Server estarão disponíveis sem custo adicional.

### Economize em custos de computação

Compre Instâncias de Máquinas Virtuais Reservadas do Azure de um ou de três anos para economizar até 72 por cento em relação aos preços pagos conforme o uso. Você pode pagar por uma reserva de forma antecipada ou mensal. As reservas fornecem um desconto de cobrança e não afetam o estado de runtime dos recursos.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-compute-fundamentals/windows-virtual-desktop)

> ## [Próximo](./M4_7_Resumo.md)
