# Resumo


Um SLA (Contrato de Nível de Serviço) é o contrato formal entre uma empresa de serviços e o cliente. No caso do Azure, esse contrato define os padrões de desempenho com os quais a Microsoft se compromete a fornecer para seus clientes.

Conforme os requisitos evoluem, é importante que a equipe entenda como o SLA de cada serviço escolhido afeta as garantias gerais de desempenho dos aplicativos.

Por exemplo, o site principal deve estar disponível o mais próximo possível de 100% do tempo. Para fazer isso, a empresa pode implantar instâncias adicionais da mesma máquina virtual em diferentes zonas de disponibilidade na mesma região do Azure. Isso ajuda a garantir que, se uma zona for afetada, as instâncias de máquina virtual na outra zona possam assumir a carga.

O aplicativo pode ter tolerâncias mais flexíveis. Desde que os funcionários do varejo não percam dados e possam rapidamente recuperar o acesso à rede, o aplicativo poderá ter um SLA menor. Aqui, a equipe pode optar por incluir menos redundância em seu design.

Ao definir seus requisitos de SLA, considere as suas necessidades comerciais e o tempo necessário para restaurar um componente após uma falha. Considere também como o uso de versões prévias dos recursos e serviços pode afetar seus sistemas em produção.

Para computar o SLA composto para um conjunto de serviços, você multiplica o SLA de cada serviço individual. Lembre-se de que o SLA composto existente é:

```
99,9%\vezes99,9%\vezes99,99%\vezes99,99%=99,78%
```

> O SLA para Azure Mapas em termos de tempo de atividade garantido é de 99,9%, conforme o [SLA para Azure Mapas](https://azure.microsoft.com/support/legal/sla/azure-maps?azure-portal=true)

> Para computar o SLA composto para um conjunto de serviços, você multiplica o SLA de cada serviço individual.

> Adicionar uma terceira máquina virtual reduz o SLA composto. Como a Tailwind Traders pode compensar essa redução?
> Resposta: Implantar instâncias extras das mesmas máquinas virtuais em diferentes zonas de disponibilidade na mesma região do Azure. Se uma zona de disponibilidade for afetada, a instância de máquina virtual na outra zona de disponibilidade não deverá ser afetada.

> Que abordagem a empresa pode adotar para adicionar a versão prévia do serviço de RA (realidade aumentada) à sua arquitetura?
>
> Resposta: A equipe de desenvolvimento pode criar uma versão de protótipo do aplicativo que inclui o serviço de RA que ela testa com os funcionários de varejo selecionados. Depois que o serviço de RA atingir a GA (disponibilidade geral), a equipe poderá distribuí-lo para a produção.
