# Recursos do Azure e Azure Resource Manager


* **Recurso**: um item gerenciável disponibilizado por meio do Azure. VMs (máquinas virtuais), contas de armazenamento, aplicativos Web, bancos de dados e redes virtuais são exemplos de recursos.
* **Grupo de recursos**: um contêiner que armazena os recursos relacionados de uma solução do Azure. O grupo de recursos inclui os recursos que você deseja gerenciar como um grupo. Você decide quais recursos pertencem a um grupo de recursos com base no que faz mais sentido para sua organização.

## Grupos de recursos do Azure

> ### Um grupo de recursos é um contêiner lógico para recursos implantados no Azure. 

Esses recursos são tudo o que você cria em uma assinatura do Azure, como VMs, instâncias do Gateway de Aplicativo do Azure e instâncias do Azure Cosmos DB. 

Todos os recursos precisam estar em um grupo, e um recurso pode ser um membro de apenas um grupo de recursos. Muitos recursos podem ser movidos entre grupos de recursos com alguns serviços que têm limitações ou requisitos específicos de movimentação. 

Os grupos de recursos não podem ser aninhados. Para que qualquer recurso possa ser provisionado, é necessário colocá-lo em um grupo de recursos.

### Agrupamento lógico

Os grupos de recursos existem para ajudar a gerenciar e organizar seus recursos do Azure. Ao colocar recursos de uso, tipo ou localização semelhante em um grupo de recursos, você pode proporcionar ordem e organização aos recursos criados no Azure. 

### Ciclo de vida

Se você excluir um grupo de recursos, todos os recursos contidos nele também serão excluídos. 

Organizar recursos por ciclo de vida pode ser útil em ambientes de não produção, em que você pode realizar um experimento e, depois, descartá-lo. Os grupos de recursos facilitam a remoção de um conjunto de recursos de uma só vez.

### Autorização

Grupos de recursos também são um escopo para a aplicação de permissões de RBAC (controle de acesso baseado em função). Ao aplicar permissões de RBAC a um grupo de recursos, você pode facilitar a administração e limitar o acesso, a fim de permitir apenas o que é necessário.

## Azure Resource Manager

> ### É o serviço de implantação e gerenciamento do Azure. Ele fornece uma camada de gerenciamento que lhe permite criar, atualizar e excluir recursos em sua conta do Azure. Você usa recursos de gerenciamento como controle de acesso, bloqueios e marcas para proteger e organizar seus recursos após a implantação.

Quando um usuário envia uma solicitação de ferramentas, APIs ou SDKs do Azure, o Resource Manager recebe a solicitação. Ele autentica e autoriza a solicitação. O Resource Manager envia a solicitação para o serviço do Azure, que executa a ação solicitada. Como todas as solicitações são manipuladas por meio da mesma API, você verá funcionalidades e resultados uniformes em todas as diferentes ferramentas.

Todos os recursos disponíveis no portal do Azure também estão disponíveis por meio do PowerShell, da CLI do Azure, das APIs REST e dos SDKs de cliente. A funcionalidade inicialmente lançada por meio de APIs será representada no portal em até 180 dias depois da versão inicial.

### Os benefícios de usar o Gerenciador de Recursos

Com o Resource Manager, você pode:

* Gerenciar sua infraestrutura por meio de modelos declarativos em vez de scripts. Um modelo do Resource Manager é um arquivo JSON que define o que você deseja implantar no Azure.
* Implantar, gerenciar e monitorar todos os recursos da sua solução como um grupo em vez de tratá-los individualmente.
* Reimplantar a solução durante o ciclo de vida de desenvolvimento e ter confiança de que os recursos serão implantados em um estado consistente.
* Definir as dependências entre os recursos para que eles sejam implantados na ordem correta.
* Aplicar o controle de acesso a todos os serviços porque o RBAC é integrado nativamente à plataforma de gerenciamento.
* Aplicar marcas aos recursos para organizar de modo lógico todos os recursos em sua assinatura.
* Esclarecer a cobrança da organização exibindo os custos de um grupo de recursos que compartilham a mesma marca.



###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-architecture-fundamentals/resources-resource-manager)

> ## [Próximo](./M3_4_AssinaturasGruposGerenciamento.md)
