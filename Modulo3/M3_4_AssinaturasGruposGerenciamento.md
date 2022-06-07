# Assinaturas e Grupos de Gerenciamento do Azure

    Um recurso do Azure é um item gerenciável disponibilizado por meio do Azure. VMs (máquinas virtuais), contas de armazenamento, aplicativos Web, bancos de dados e redes virtuais são exemplos de recursos.


## Assinaturas do Azure

A utilização do Azure exige uma Assinatura do Azure. 
> Uma assinatura do Azure é uma unidade lógica de serviços do Azure que se vincula a uma conta do Azure, que é uma identidade no Azure AD (Azure Active Directory) ou em um diretório no qual o Azure AD confia.

> Uma assinatura fornece a você acesso autenticado e autorizado a serviços e produtos do Azure. Ela também permite que você provisione recursos. 

Uma conta pode ter uma ou várias assinaturas com diferentes modelos de cobrança e às quais você aplica diferentes políticas de gerenciamento de acesso. Você pode usar as assinaturas do Azure para definir limites em relação a produtos, serviços e recursos do Azure.

 Você pode usar dois tipos de limites de assinatura:

* **Limite de cobrança**: Esse tipo de assinatura determina como uma conta do Azure é cobrada pelo uso do Azure. Você pode criar várias assinaturas para atender a diferentes tipos de requisitos de cobrança. O Azure gera relatórios de cobrança e faturas separados para cada assinatura, para que você possa organizar e gerenciar os custos.
* **Limite de controle de acesso**: O Azure aplica políticas de gerenciamento de acesso no nível da assinatura, e você pode criar assinaturas separadas para refletir diferentes estruturas organizacionais. Um exemplo disso é que, em um negócio, você tem diferentes departamentos aos quais aplica políticas de assinatura do Azure distintas. Esse modelo de cobrança permite gerenciar e controlar o acesso aos recursos que os usuários provisionam com assinaturas específicas.

### Criar assinaturas adicionais do Azure

Talvez você queira criar assinaturas adicionais para fins de gerenciamento de recursos ou orçamento. Por exemplo, é possível criar assinaturas adicionais para separar:

* **Ambientes**: Ao gerenciar seus recursos, você pode optar por criar assinaturas adicionais a fim de configurar ambientes separados para desenvolvimento e teste, segurança ou para isolar dados por motivos de conformidade. Esse design é particularmente útil porque o controle de acesso ao recurso ocorre no nível da assinatura.
* **Estruturas organizacionais**: É possível criar assinaturas para refletir diferentes estruturas organizacionais. Você poderia, por exemplo, limitar a equipe a recursos de baixo custo, enquanto permite uma gama completa para o departamento de TI. Esse design permite gerenciar e controlar o acesso aos recursos que os usuários provisionam em cada assinatura.
* **Cobrança**: Talvez você também queira criar assinaturas adicionais para fins de cobrança. Como os custos são agregados primeiro no nível da assinatura, talvez você queira criar assinaturas para gerenciar e controlar os custos com base em suas necessidades. Por exemplo, talvez você queira criar uma assinatura para as cargas de trabalho de produção e outra para as cargas de trabalho de desenvolvimento e teste.

Talvez você também precise de assinaturas adicionais devido a:

* **Limites da assinatura**: As assinaturas estão associadas a algumas limitações rigorosas. Por exemplo, o número máximo de circuitos do Azure ExpressRoute por assinatura é 10. Esses limites devem ser considerados enquanto você cria assinaturas em sua conta. Se for preciso ultrapassar esses limites em cenários específicos, talvez seja necessário ter assinaturas adicionais.

### Personalizar a cobrança para atender às suas necessidades

Se você tiver várias assinaturas, poderá organizá-las em **seções de fatura**. Cada seção de fatura é um item de linha na fatura que mostra os encargos incorridos nesse mês. Por exemplo, você pode precisar de uma única fatura para sua organização, mas deseja organizar os encargos por departamento, equipe ou projeto.

Dependendo de suas necessidades, é possível configurar várias faturas dentro da mesma conta de cobrança. Para fazer isso, crie perfis de cobrança adicionais. Cada perfil de cobrança tem sua própria fatura mensal e formas de pagamento.

## Grupos de gerenciamento do Azure

Se a organização tiver muitas assinaturas, talvez você precise de uma forma de gerenciar o acesso, as políticas e a conformidade com eficiência para essas assinaturas. 

> Os grupos de gerenciamento do Azure fornecem um nível de escopo acima das assinaturas. Você organiza as assinaturas em contêineres chamados grupos de gerenciamento e aplica suas condições de governança a esses grupos. 
>
>Todas as assinaturas dentro de um grupo de gerenciamento herdam automaticamente as condições aplicadas ao grupo de gerenciamento. 
> 
> Os grupos de gerenciamento fornecem gerenciamento de nível empresarial em larga escala, independentemente do tipo de assinaturas que você possa ter. Todas as assinaturas dentro de um grupo de gerenciamento devem confiar no mesmo locatário do Azure AD.

Por exemplo, você pode aplicar políticas a um grupo de gerenciamento para limitar as regiões disponíveis para criação de VMs. Essa política seria aplicada a todos os grupos de gerenciamento, assinaturas e recursos nesse grupo de gerenciamento, permitindo que as VMs fossem criadas nessa região.

### Hierarquia de grupos de gerenciamento e assinaturas

É possível compilar uma estrutura flexível de grupos de gerenciamento e assinaturas para organizar seus recursos em uma hierarquia para políticas unificadas e gerenciamento de acesso. O diagrama a seguir mostra um exemplo de criação de uma hierarquia de governança usando grupos de gerenciamento.

Você pode criar uma hierarquia que aplica uma política. Por exemplo, você pode limitar os locais de VM à região Oeste dos EUA em um grupo chamado Produção. Essa política herdará todas as assinaturas do Contrato Enterprise que são descendentes desse grupo de gerenciamento e será aplicada a todas as VMs nessas assinaturas. Essa política de segurança não pode ser alterada pelo proprietário da assinatura nem do recurso, o que permite uma governança aprimorada.

Outro cenário em que você usaria grupos de gerenciamento é fornecer acesso de usuário a várias assinaturas. Ao mover várias assinaturas nesse grupo de gerenciamento, você poderá criar uma atribuição de RBAC (controle de acesso baseado em função) no grupo de gerenciamento, que herdará esse acesso a todas as assinaturas. Uma atribuição no grupo de gerenciamento pode permitir que os usuários tenham acesso a tudo o que precisam em vez de fazer script de atribuições de RBAC em várias assinaturas.

### Fatos importantes sobre os grupos de gerenciamento

* 10.000 grupos de gerenciamento podem ter suporte em um único diretório.
* Uma árvore do grupo de gerenciamento pode dar suporte a até seis níveis de profundidade. Esse limite não inclui o nível raiz nem o nível da assinatura.
* Cada grupo de gerenciamento e assinatura podem dar suporte a somente um pai.
* Cada grupo de gerenciamento pode ter vários elementos filhos.
* Todas as assinaturas e todos os grupos de gerenciamento estão em uma única hierarquia em cada diretório.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-architecture-fundamentals/management-groups-subscriptions)

> ## [Próximo](./M3_5_Resumo.md)