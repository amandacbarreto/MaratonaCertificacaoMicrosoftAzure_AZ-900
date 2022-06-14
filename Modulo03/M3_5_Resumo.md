# Resumo

> **Grupos de gerenciamento** podem ser usadas para gerenciar a governança entre várias assinaturas do Azure.
>
> > Os grupos de gerenciamento facilitam a ordenação hierárquica de recursos do Azure em coleções em um nível de escopo acima das assinaturas. Condições de governança distintas podem ser aplicadas a cada grupo de gerenciamento, juntamente com o Azure Policy e os controles de acesso baseado em função do Azure, para gerenciar assinaturas do Azure com eficiência. Os recursos e as assinaturas atribuídos a um grupo de gerenciamento herdam automaticamente as condições aplicadas ao grupo de gerenciamento.

> **Assinatura do Azure** é uma unidade lógica dos serviços do Azure vinculadas a uma conta do Azure.
>
> > Uma assinatura do Azure é um objeto que representa um contêiner em que você pode inserir recursos. As assinaturas estão vinculadas aos locatários, portanto, cada locatário pode ter várias assinaturas, mas não o contrário.

> Os grupos de recursos _**não** são uma unidade lógica dos serviços do Azure vinculadas a uma conta do Azure_. Eles mantêm recursos como máquinas virtuais e armazenamento. Eles funcionam dentro das contas do Azure.

> Quanto aos grupos de recursos:
>
> - **os recursos podem estar em apenas um grupo de recursos**.
> - **O controle de acesso baseado em função pode ser aplicado ao grupo de recursos**.
> - Os grupos de recursos **NÃO** podem ser aninhados.

> Uma assinatura do Azure é uma unidade lógica de serviços do Azure.
>
> > Uma assinatura é um conjunto de serviços do Azure agrupados para acompanhamento e cobrança. O controle de acesso a recursos ocorre no nível da assinatura. As organizações usam as assinaturas do Azure para gerenciar e controlar os recursos do Azure delas.
