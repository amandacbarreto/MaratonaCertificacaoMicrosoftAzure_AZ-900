# Decidir quando usar Máquinas Virtuais do Azure

Com as Máquinas Virtuais do Azure, você pode criar e usar VMs na nuvem.

> As VMs fornecem **IaaS (infraestrutura como serviço)** na forma de um servidor virtualizado e podem ser usadas de várias maneiras.

Como em um computador físico, você pode personalizar todos os programas de software em execução na VM.

> As VMs são uma opção ideal quando você precisa de:
>
> - Controle total sobre o SO (sistema operacional).
> - Capacidade para executar um software personalizado.
> - Usar configurações personalizadas de hospedagem.

Uma VM do Azure oferece a flexibilidade da virtualização sem a necessidade de comprar e manter o hardware físico que a executa. Você ainda precisa configurar, atualizar e manter o software executado na VM.

Você pode criar e provisionar uma VM em minutos quando seleciona uma imagem de VM pré-configurada. A seleção de uma imagem é uma das decisões mais importantes a tomar ao criar uma VM. Uma imagem é um modelo usado para criar uma VM. Esses modelos já incluem um sistema operacional e, muitas vezes, outros programas de software, como ferramentas de desenvolvimento ou ambientes de hospedagem na Web.

### Exemplos de quando usar VMs:

- **Durante o teste e o desenvolvimento**. As VMs fornecem uma maneira rápida e fácil de criar diferentes configurações de sistema operacional e de aplicativo. A equipe de teste e desenvolvimento pode excluir facilmente as VMs quando não precisarem mais delas.
- **Ao executar aplicativos na nuvem**. A capacidade de executar determinados aplicativos na nuvem pública, em vez de criar uma infraestrutura tradicional para executá-los, pode trazer benefícios econômicos substanciais. Por exemplo, um aplicativo pode precisar lidar com flutuações na demanda. Desligar VMs quando elas não são necessárias ou iniciá-las rapidamente para atender a um aumento repentino na demanda significa que você paga apenas pelos recursos que usa.
- **Ao estender seu datacenter para a nuvem**. Uma organização pode estender os recursos de sua própria rede local criando uma rede virtual no Azure e adicionando VMs a ela. Aplicativos como o SharePoint podem, então, ser executados em uma VM do Azure em vez de localmente. É mais fácil ou menos caro implantar dessa forma do que em um ambiente local.
- **Durante a recuperação de desastre**. Assim como acontece com a execução de determinados tipos de aplicativos na nuvem e com a extensão de uma rede local para a nuvem, você pode conseguir economias significativas usando uma abordagem baseada em IaaS para a recuperação de desastre. Se um datacenter primário falhar, você poderá criar VMs em execução no Azure para executar seus aplicativos críticos e desligá-los quando o datacenter primário ficar operacional novamente.

## Migrar para a nuvem com VMs

As VMs também são uma excelente opção quando você migra de um servidor físico para a nuvem (também conhecido como lift-and-shift). Você pode criar uma imagem do servidor físico e hospedá-la em uma VM com poucas ou nenhuma alteração. Assim como um servidor físico local, você deve manter a VM. Atualize o sistema operacional instalado e o software em que ele é executado.

## Dimensionar VMs no Azure

Você pode executar VMs únicas para teste, desenvolvimento ou para tarefas secundárias. Ou pode agrupar VMs para fornecer alta disponibilidade, escalabilidade e redundância. Independentemente dos seus requisitos de tempo de atividade, o Azure conta com diversos recursos para atendê-los. Esses recursos incluem:

- conjuntos de escala de máquina virtual
- Lote do Azure

### O que são os conjuntos de dimensionamento de máquinas virtuais?

Os Conjuntos de Dimensionamento de Máquinas Virtuais **permitem criar e gerenciar um grupo de VMs idênticas e com balanceamento de carga**.

Imagine que você esteja executando um site que permite aos cientistas carregarem imagens de astronomia que precisam ser processadas. Se você duplicasse a VM, normalmente precisaria configurar um serviço adicional para rotear solicitações entre várias instâncias do site. Os conjuntos de dimensionamento de máquinas virtuais podem fazer esse trabalho para você.

Os conjuntos de dimensionamento **permitem que você gerencie, configure e atualize centralmente um grande número de VMs em minutos para fornecer aplicativos de alta disponibilidade**. O número de instâncias de VM pode aumentar ou diminuir automaticamente em resposta à demanda ou a um agendamento definido. Com conjuntos de dimensionamento de máquinas virtuais, você pode criar serviços em grande escala para áreas como computação, big data e cargas de trabalho de contêiner.

### O que é o Lote do Azure?

O Lote do Azure **faz trabalhos em lotes paralelos e de HPC (computação de alto desempenho) de grande escala com a capacidade de dimensionar dezenas, centenas ou milhares de VMs**.

Quando você estiver pronto para executar um trabalho, o lote fará o seguinte:

- Iniciar um pool de VMs de computação para você.
- Instalar aplicativos e dados de preparo.
- Executar trabalhos com todas as tarefas que você tiver.
- Identificar falhas.
- Colocar o trabalho em filas.
- Reduzir verticalmente o pool conforme o trabalho for concluído.

Pode haver situações em que você precise de potência de computação bruta ou de potência de computação no nível de supercomputador. O Azure fornece esses recursos.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-compute-fundamentals/azure-virtual-machines)

> ## [Próximo](./M4_3_ServicoAplicativoAzure.md)
