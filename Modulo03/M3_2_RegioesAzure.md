# Regiões do Azure, zonas de disponibilidade e pares de regiões

 > O Azure é composto por datacenters espalhados pelo mundo. 
 > 
 > Ao usar um serviço ou criar um recurso como uma VM (máquina virtual) ou um Banco de Dados SQL, você está usando equipamentos físicos em um ou mais desses locais. Esses data centers específicos não são expostos diretamente aos usuários. Em vez disso, o Azure os organiza em **regiões**.
 >Algumas dessas regiões oferecem **zonas de disponibilidade**, que são diferentes data centers do Azure dentro da região.


## Regiões do Azure

> Uma região é uma área geográfica do planeta que contém pelo menos um, mas possivelmente vários data centers próximos e conectados a uma rede de baixa latência. 
O Azure atribui e controla os recursos de modo inteligente dentro de cada região para garantir que as cargas de trabalho sejam balanceadas corretamente.

Quando você implanta um recurso no Azure, geralmente precisa escolher a região em que deseja que ele seja implantado.

> Alguns serviços ou recursos de VM estão disponíveis somente em determinadas regiões, como tamanhos específicos de VMs ou tipos de armazenamento. Também há alguns serviços globais do Azure que não exigem que você selecione uma região específica, como o Azure Active Directory, o Gerenciador de Tráfego do Azure e o DNS do Azure.



![Mapa mundi de todas as regiões disponíveis a partir de junho de 2020](https://docs.microsoft.com/pt-br/learn/azure-fundamentals/azure-architecture-fundamentals/media/regions-small-be724495.png)
###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-architecture-fundamentals/regions-availability-zones)


## Por que as regiões são importantes?

> ### As regiões dão flexibilidade para aproximar os aplicativos dos usuários, não importa onde estejam. As regiões globais proporcionam maior escalabilidade e redundância. Elas também preservam a residência de dados de seus serviços.

O Azure tem mais regiões globais do que qualquer outro provedor de nuvem.

## Regiões especiais do Azure

> ### As regiões são o que você usa para identificar a localização de seus recursos.

> O Azure tem regiões especializadas que talvez você queira usar ao criar seus aplicativos para fins de conformidade ou jurídicos. 

Alguns exemplos incluem:

* **US DoD Central, US Gov – Virgínia, US Gov Iowa, entre outros**: essas regiões são instâncias lógicas e físicas do Azure isoladas da rede, destinadas a parceiros e órgãos do governo dos EUA. Esses datacenters são operados por cidadãos selecionados dos EUA e incluem certificações de conformidade adicionais.
* **Leste da China, Norte da China, entre outros**: essas regiões estão disponíveis por meio de uma parceria exclusiva entre a Microsoft e a 21Vianet, segundo a qual a Microsoft não mantém diretamente os data centers.

 Há dois outros termos aos quais você também precisa estar atento: geografias e zonas de disponibilidade.

## Zonas de disponibilidade do Azure

É importante verificar se seus serviços e dados são redundantes para que você possa proteger suas informações em caso de falha. Ao hospedar sua infraestrutura, a configuração de sua redundância exigirá a criação de ambientes de hardware duplicados. O Azure pode ajudar a tornar seu aplicativo altamente disponível por meio das zonas de disponibilidade.

> ### O que é uma zona de disponibilidade?
>
>> são datacenters separados fisicamente dentro de uma região do Azure. 
>>
>> Cada zona de disponibilidade é composta de um ou mais datacenters equipados com energia, resfriamento e rede independentes. 
>> 
>> Uma zona de disponibilidade é configurada para ser um *limite de isolamento*. Se uma zona ficar inativa, as outras continuarão funcionando. 
>> 
>> Zonas de disponibilidade são conectadas por meio de redes de fibra óptica privadas de alta velocidade.

### Regiões com suporte

Nem todas as regiões têm suporte para zonas de disponibilidade. 

### Usar zonas de disponibilidade em seus aplicativos

Você pode usar as zonas de disponibilidade para executar aplicativos críticos e incorporar alta disponibilidade à arquitetura do aplicativo, colocalizando seus recursos de computação, armazenamento, rede e dados em uma zona e replicando em outras zonas. Tenha em mente que pode haver um custo para duplicar seus serviços e transferir dados entre zonas.

As zonas de disponibilidade são destinadas, principalmente, a VMs, discos gerenciados, balanceadores de carga e bancos de dados SQL. As seguintes categorias de serviços do Azure dão suporte a zonas de disponibilidade:

* **Serviços em zonas**: você fixa o recurso a uma zona específica (por exemplo, VMs, discos gerenciados, endereços IP).
* **Serviços com redundância de zona**: a plataforma replica automaticamente entre zonas (por exemplo, armazenamento com redundância de zona, Banco de Dados SQL).
* **Serviços não regionais**: os serviços estão sempre disponíveis em geografias do Azure e são resilientes a interrupções em toda a zona, bem como a interrupções em toda a região.

## Pares de regiões do Azure

As zonas de disponibilidade são criadas usando um ou mais data centers. Há um mínimo de três zonas em uma região. É possível que um desastre de maiores proporções cause uma interrupção grande o suficiente para afetar até mesmo dois datacenters. Por isso, o Azure também cria pares de regiões.

### O que é um par de regiões?

> Cada região do Azure é sempre emparelhada com outra região na mesma área geográfica (como EUA, Europa ou Ásia) a pelo menos 300 milhas (cerca de 480 km) de distância. Essa abordagem permite a replicação de recursos, como o armazenamento de VM, em uma geografia, o que ajuda a reduzir a probabilidade de interrupções devido a eventos como desastres naturais, conflitos civis, quedas de energia ou interrupções de rede física afetarem as duas regiões ao mesmo tempo. Se uma região em um par de regiões fosse afetada por um desastre natural, por exemplo, os serviços fariam failover automaticamente para a outra região desse par.

Exemplos de pares de regiões no Azure são Oeste dos EUA emparelhado com Leste dos EUA e Sudeste da Ásia emparelhado com Leste da Ásia.

Diagram showing relationship between geography, region pair, region, and datacenter.

Como o par de regiões está diretamente conectado e suficientemente afastado para ser isolado contra desastres regionais, você pode usá-lo para **fornecer redundância de dados e serviços confiáveis**. Alguns serviços oferecem armazenamento com redundância geográfica automática usando pares de regiões.

Vantagens adicionais dos pares de regiões:

* Se ocorrer uma interrupção ampla do Azure, uma região de cada par será priorizada para que pelo menos uma seja restaurada o quanto antes para os aplicativos hospedados nesse par de regiões.
* As atualizações planejadas do Azure são distribuídas para regiões emparelhadas uma por vez, de modo a minimizar o tempo de inatividade e o risco de interrupção dos aplicativos.
* Os dados continuam residindo na mesma geografia que seu par (com exceção do Sul do Brasil) para fins de jurisdição do imposto e aplicação da lei.

Ter um conjunto de datacenters distribuído em larga escala permite que o Azure forneça uma garantia de alta disponibilidade.


> ## [Próximo](./M3_3_RecursosAzure.md)






