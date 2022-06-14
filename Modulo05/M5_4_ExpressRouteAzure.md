# Assinaturas e Grupos de Gerenciamento do Azure

> O ExpressRoute permite que você estenda suas redes locais para a nuvem da Microsoft em uma conexão privada com a ajuda de um provedor de conectividade.
> Com o ExpressRoute, você pode estabelecer conexões com os serviços em nuvem da Microsoft, como o Microsoft Azure e o Microsoft 365.

A conectividade pode ocorrer de uma rede any-to-any (VPN de IP), uma rede Ethernet ponto a ponto ou uma conexão cruzada virtual por meio de um provedor de conectividade em uma colocação.
As conexões do ExpressRoute não passam pela Internet pública. Isso permite que as conexões de ExpressRoute ofereçam mais confiabilidade, mais velocidade, latências consistentes e muito mais segurança do que as conexões típicas pela Internet.

## Recursos e benefícios do ExpressRoute

Há vários benefícios de usar o ExpressRoute como o serviço de conexão entre o Azure e as redes locais.

- Conectividade de Camada 3 entre sua rede local e a Microsoft Cloud por meio de um provedor de conectividade. A conectividade pode ocorrer de uma rede “qualquer para qualquer” (IPVPN), de uma conexão Ethernet ponto a ponto ou por meio de uma conexão cruzada virtual via troca Ethernet.
- Conectividade com os serviços de nuvem da Microsoft em todas as regiões da região geopolítica.
- Conectividade global com os serviços da Microsoft em todas as regiões com o complemento premium do ExpressRoute.
- Roteamento dinâmico entre sua rede e a Microsoft por meio do BGP.
- Redundância interna em cada local de emparelhamento para proporcionar maior confiabilidade.
- SLAdo tempo de atividade da conexão.
- Suporte a QoS para Skype for Business.

## Modelos de conectividade do ExpressRoute

O ExpressRoute dá suporte aos seguintes modelos que podem ser usados para conectar sua rede local à nuvem da Microsoft:

* Colocação do CloudExchange
* Conexão Ethernet ponto a ponto
* Conexão qualquer para qualquer
* Direto de sites do ExpressRoute


## Considerações sobre segurança

Com o ExpressRoute, os seus dados não passam pela Internet pública e, portanto, não são expostos aos riscos potenciais associados às comunicações da Internet. O ExpressRoute é uma conexão particular de sua infraestrutura local com a infraestrutura do Azure. Mesmo que você tenha uma conexão do ExpressRoute, consultas DNS, verificações de listas de certificados revogados e solicitações da Rede de Distribuição de Conteúdo do Azure ainda serão enviadas pela Internet pública.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-networking-fundamentals/express-route-fundamentals)

> ## [Próximo](./M5_5_Resumo.md)
