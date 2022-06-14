# Resumo

A governança de nuvem exige uma boa coleta de requisitos e análise.

O Cloud Adoption Framework para Azure pode ajudar você a definir e implementar sua estratégia de governança.

Há vários serviços e recursos no Azure que dão suporte a esses esforços:

- **O RBAC do Azure** (controle de acesso baseado em função do Azure) permite que você crie funções que definem permissões de acesso.
- **Os bloqueios de recursos** impedem que os recursos sejam excluídos ou alterados acidentalmente.
- **As marcas de recursos** fornecem informações extras ou metadados sobre os recursos.
- **O Azure Policy** é um serviço do Azure que permite criar, atribuir e gerenciar políticas que controlam ou auditam os recursos.
- **O Azure Blueprints** permite que você defina um conjunto repetível de ferramentas de governança e de recursos padrão do Azure necessário para a sua organização.

Com esses pontos em mente, você está pronto para realizar a próxima etapa para a criação de uma boa estratégia de governança de nuvem.

> O RBAC do Azure permite que você crie funções que definem as permissões de acesso. Você pode criar uma função que limita o acesso somente às máquinas virtuais e uma segunda função que fornece aos administradores acesso a tudo.
>
> Uma empresa pode permitir que alguns usuários controlem as máquinas virtuais em cada ambiente, mas impedir que eles modifiquem a rede e outros recursos no mesmo grupo de recursos ou na mesma assinatura do Azure através da criação de uma atribuição de função por meio do RBAC do Azure (controle de acesso baseado em função do Azure).
>
> Dividir o ambiente em grupos de recursos separados não é uma solução ideal para esse cenário, pois os grupos de recursos devem conter recursos relacionados. Embora você possa dividir o ambiente em grupos de recursos separados, essa abordagem provavelmente será mais complexa do que necessária.

> A melhor maneira para uma garantir que a equipe implante apenas tamanhos econômicos de SKU de máquina virtual é criar uma política no Azure Policy que especifique os tamanhos de SKU permitidos.
>
> Depois que você habilita essa política, ela é aplicada quando as máquinas virtuais são criadas ou as existentes são redimensionadas. O Azure Policy também avalia as máquinas virtuais atuais do ambiente.
>
> O RBAC do Azure permite que você crie funções que definem as permissões de acesso, mas não permite que você defina tamanhos de SKU de máquina virtual permitidos.

> A melhor maneira para a empresa identificar a qual departamento de cobrança cada recurso do Azure pertence é aplicar uma marca a cada recurso que inclua o departamento de cobrança associado.
>
> As marcas fornecem informações extras ou metadados sobre os recursos. A equipe pode criar uma marca chamada BillingDept, cujo valor é o nome do departamento de cobrança. Você poderá usar o Azure Policy para garantir que as marcas apropriadas sejam atribuídas quando os recursos forem provisionados.
