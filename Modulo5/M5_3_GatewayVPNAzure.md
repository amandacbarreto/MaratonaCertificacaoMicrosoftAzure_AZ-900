# Conceitos básicos do Gateway de VPN do Azure

VPNs usam um túnel criptografado dentro de outra rede. Normalmente, elas são implantadas para conectar duas ou mais redes privadas confiáveis entre si em uma rede não confiável (normalmente a Internet pública). O tráfego é criptografado ao viajar pela rede não confiável para evitar interceptação ou outros ataques.

## Gateways VPN

> **Um gateway de VPN é um tipo de gateway de rede virtual**.
> As instâncias do Gateway de VPN do Azure são implantadas em uma subrede dedicada da rede virtual e permitem a seguinte conectividade:

- Conecte datacenters locais a redes virtuais por meio de uma conexão site a site.
- Conecte dispositivos individuais a redes virtuais por meio de uma conexão ponto a site.
- Conecte redes virtuais a outras redes virtuais por meio de uma conexão rede a rede.

Você só poderá implantar um gateway de VPN em cada rede virtual, mas poderá usar um gateway para se conectar a vários locais, incluindo outras redes virtuais ou datacenters locais.

Ao implantar um gateway de VPN, você especifica o tipo de VPN: _baseada em política_ ou _baseada em rota_.

A principal diferença entre esses dois tipos de VPN é como o tráfego a ser criptografado é especificado.

No Azure, ambos os tipos de gateways de VPN usam uma chave pré-compartilhada como o único método de autenticação. Ambos os tipos também dependem do protocolo IKE na versão 1 ou na versão 2 e do protocolo IPsec. O IKE é usado para configurar uma associação de segurança (um contrato da criptografia) entre dois pontos de extremidade. Essa associação é passada para o conjunto do IPsec, que criptografa e descriptografa os pacotes de dados encapsulados no túnel VPN.

### VPNs baseadas em política

> Gateways de VPN baseados em política **especificam estaticamente o endereço IP dos pacotes que devem ser criptografados por meio de cada túnel**. Esse tipo de dispositivo **avalia cada pacote de dados em relação a esses conjuntos de endereços IP para escolher o túnel para o qual o pacote será enviado**.

- As VPNs baseadas em política devem ser usadas em cenários específicos que as exigem, por exemplo, para compatibilidade com os dispositivos VPN locais herdados.

### VPNs baseadas em rota

Caso seja muito complicado definir quais endereços IP estão por trás de cada túnel, será possível usar gateways baseados em rota.

> Com gateways baseados em rota, os túneis IPSec são modelados como uma interface de rede ou uma interface de túnel virtual. **O roteamento de IP (protocolos de roteamento dinâmico ou rotas estáticas) decide qual dessas interfaces de túnel usar ao enviar cada pacote**. VPNs baseadas em rota são o **método preferido para conectar dispositivos locais**. Elas são mais resilientes a alterações de topologia, como a criação de novas sub-redes.

Use um gateway de VPN baseado em rota se precisar de qualquer um dos seguintes tipos de conectividade:

- Conexões entre redes virtuais
- Conexões ponto a site
- Conexões multissite
- Coexistência com um gateway do Azure ExpressRoute

## Tamanhos do gateway de VPN

As funcionalidades do seu gateway de VPN são determinadas pelo SKU ou tamanho implantado.

> Um Gateway de VPN Básico deve ser usado apenas para cargas de trabalho de Desenvolvimento/Teste.

## Implantar gateways de VPN

Serão necessários os seguintes recursos do Azure antes que você possa implantar um gateway de VPN operacional:

- **Rede virtual**

  - Implante uma rede virtual com espaço de endereço suficiente para a sub-rede adicional que será necessária para o gateway de VPN. O espaço de endereço dessa rede virtual não pode se sobrepor à rede local à qual você se conectará. Só é possível implantar um único gateway de VPN em uma rede virtual.

- **GatewaySubnet**

  - Implante uma sub-rede chamada GatewaySubnet para o gateway de VPN. Use uma máscara de endereço de pelo menos /27 para garantir que você tenha endereços IP suficientes na sub-rede para crescimento futuro. Não é possível usar essa sub-rede para nenhum outro serviço.

- **Endereço IP público**

  - Crie um endereço IP público dinâmico do SKU Básico se você estiver usando um gateway sem reconhecimento de zona. Esse endereço fornece um endereço IP roteável público como o destino do dispositivo VPN local. Embora esse endereço IP seja dinâmico, ele não será alterado a menos que você exclua e recrie o gateway de VPN.

- **Gateway de rede local**

  - Crie um gateway de rede local para definir a configuração da rede local, como onde o gateway de VPN se conectará e a que ele se conectará. Essa configuração inclui o endereço IPv4 público do dispositivo VPN local e as redes roteáveis locais. Essas informações são usadas pelo gateway de VPN para rotear, por meio do túnel IPsec, pacotes destinados a redes locais.

- **Gateway de rede virtual**

  - Crie o gateway de rede virtual para rotear tráfego entre a rede virtual e o datacenter local ou outras redes virtuais. O gateway de rede virtual pode ser um gateway de VPN ou ExpressRoute, mas esta unidade lida apenas com gateways de rede virtual de VPN. (Você aprenderá mais sobre o ExpressRoute em outra unidade posteriormente neste módulo.)

- **Conexão**
  - Crie um recurso de conexão para criar uma conexão lógica entre o gateway de VPN e o gateway de rede local.
    - A conexão é realizada com o endereço IPv4 do dispositivo VPN local conforme definido pelo gateway de rede local.
    - A conexão é realizada do gateway de rede virtual e seu endereço IP público associado.

## Recursos locais necessários

Para conectar seu datacenter a um gateway de VPN, serão necessários os seguintes recursos locais:

- Um dispositivo VPN que dá suporte a gateways de VPN baseada em política ou em rota
- Um endereço IPv4 (roteável pela Internet) voltado para o público

## Cenários de alta disponibilidade

Há várias maneiras de verificar se você tem uma configuração tolerante a falhas.

### Ativo/em espera

Por padrão, gateways de VPN são implantados como duas instâncias em uma configuração ativa/em espera, mesmo se você vê apenas um recurso de gateway de VPN no Azure. Quando a manutenção planejada ou a interrupção não planejada afeta a instância ativa, a instância de modo de espera assume automaticamente a responsabilidade pelas conexões sem nenhuma intervenção do usuário. Durante esse failover, as conexões são interrompidas, mas normalmente são restauradas em alguns segundos para manutenção planejada e dentro de 90 segundos em caso de interrupções não planejadas.

### Ativo/ativo

Com a introdução da compatibilidade com o protocolo de roteamento BGP, você também pode implantar os gateways de VPN em uma configuração ativo/ativo. Nessa configuração, você atribui um endereço IP público exclusivo a cada instância. Em seguida, cria túneis do dispositivo local para cada endereço IP. É possível estender a alta disponibilidade implantando um dispositivo VPN local adicional.

### Failover do ExpressRoute

Outra opção de alta disponibilidade é configurar um gateway de VPN como um caminho de failover seguro para conexões ExpressRoute. Os circuitos ExpressRoute têm resiliência integrada. Mas não são imunes a problemas físicos que afetam os cabos que fornecem conectividade nem a interrupções que afetam toda a localização do ExpressRoute. Em cenários de alta disponibilidade, nos quais há risco associado a uma interrupção de um circuito do ExpressRoute, você também pode provisionar um gateway de VPN que usa a Internet como um método alternativo de conectividade. Dessa forma, você pode garantir que sempre haja uma conexão com as redes virtuais.

### Gateways com redundância de zona

Nas regiões que dão suporte a zonas de disponibilidade, os gateways de VPN e os gateways de ExpressRoute podem ser implantados em uma configuração com redundância de zona. Essa configuração oferece resiliência, escalabilidade e maior disponibilidade para os gateways de rede virtual. A implantação de gateways em zonas de disponibilidade do Azure separa de forma física e lógica os gateways em uma região, enquanto protege a conectividade de rede local com o Azure contra falhas no nível da zona. Esses gateways exigem SKUs de gateway diferentes e usam os endereços IP públicos Standard em vez dos Básicos.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-networking-fundamentals/azure-vpn-gateway-fundamentals)

> ## [Próximo](./M5_4_ExpressRouteAzure.md)
