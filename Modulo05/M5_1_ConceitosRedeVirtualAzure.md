# Conceitos básicos da Rede Virtual do Azure
.

## O que é a rede virtual do Azure?

> ### **As redes virtuais do Azure** permitem que recursos do Azure, como VMs, aplicativos Web e bancos de dados, comuniquem-se uns com os outros, com usuários na Internet e com computadores cliente locais. Você pode pensar em uma rede do Azure como uma extensão de sua rede local com recursos que vinculam outros recursos do Azure.

As redes virtuais do Azure oferecem as seguintes funcionalidades de rede essenciais:

* Isolamento e segmentação
* Comunicação pela Internet
* Comunicação entre recursos do Azure
* Comunicação com os recursos locais
* Rotear tráfego de rede
* Filtrar tráfego de rede
* Conectar redes virtuais

### Isolamento e segmentação

> A rede virtual do Azure **permite criar várias redes virtuais isoladas**. 
Quando você configura uma rede virtual, define um espaço de endereço IP privado usando intervalos de endereços IP públicos ou privados. O intervalo de IP público existe somente na rede virtual e não é roteável pela Internet. Você pode dividir esse espaço de endereços IP em sub-redes e alocar parte do espaço de endereço definido para cada sub-rede nomeada.

Para a resolução de nomes, é possível usar o serviço de resolução de nomes interno do Azure. Você também pode configurar a rede virtual para usar um servidor DNS interno ou externo.

### Comunicações com a Internet

> **Uma VM no Azure pode se conectar à Internet por padrão**. É possível habilitar conexões de entrada da Internet atribuindo um IP à VM ou colocando a VM atrás de um balanceador de carga público.

Para o gerenciamento de VM, você pode se conectar por meio da CLI do Azure, do protocolo RDP ou do Secure Shell.

### Comunicação entre recursos do Azure

Convém habilitar recursos do Azure para que se comuniquem entre si com segurança. Você pode fazer isso de duas maneiras:

* **Redes virtuais**
    * As redes virtuais podem conectar não apenas VMs, mas outros recursos do Azure, como o Ambiente do Serviço de Aplicativo para Power Apps, o Serviço de Kubernetes do Azure e os conjuntos de dimensionamento de máquinas virtuais do Azure.
* **Pontos de extremidade de serviço**
    * Você pode usar pontos de extremidade de serviço para se conectar a outros tipos de recursos do Azure, como bancos de dados SQL do Azure e contas de armazenamento. Essa abordagem permite vincular vários recursos do Azure às redes virtuais para melhorar a segurança e fornecer o encaminhamento ideal entre recursos.

### Comunicação com os recursos locais

> As redes virtuais do Azure **permitem vincular recursos em seu ambiente local e na assinatura do Azure**. 

Na verdade, você pode criar uma rede que abranja os ambientes locais e de nuvem. Há três mecanismos para você obter essa conectividade:

* **Redes virtuais privadas ponto a site**
    * A abordagem típica de uma conexão de VPN (rede virtual privada) é de um computador fora da sua organização, de volta à sua rede corporativa. Nesse caso, o computador cliente inicia uma conexão VPN criptografada para conectar o computador à rede virtual do Azure.
* **Redes virtuais privadas site a site**
    * Uma VPN site a site vincula seu dispositivo VPN ou gateway de VPN local ao Gateway de VPN do Azure em uma rede virtual. Na verdade, os dispositivos no Azure podem aparecer como estando na rede local. A conexão é criptografada e funciona pela Internet.
* **Azure ExpressRoute**
    * No caso de ambientes em que você precisa de maior largura de banda e níveis de segurança ainda mais altos, o Azure ExpressRoute é a melhor abordagem. O ExpressRoute fornece uma conectividade privada dedicada para o Azure que não passa pela Internet. (Você aprenderá mais sobre o ExpressRoute em outra unidade posteriormente neste módulo.)

### Rotear tráfego de rede

Por padrão, o Azure faz o roteamento de tráfego entre sub-redes em redes virtuais conectadas, em redes locais e na Internet. Você também pode controlar o roteamento e substituir essas configurações da seguinte maneira:

* **Tabelas de rotas**
    * Uma tabela de rotas permite definir regras sobre como o tráfego deve ser direcionado. Você pode criar tabelas de rotas personalizadas que controlam como os pacotes são encaminhados entre as sub-redes.
* **Border Gateway Protocol**
    * O BGP (Border Gateway Protocol) funciona com Gateways de VPN do Azure, Servidor de Rota do Azure ou ExpressRoute para propagar as rotas BGP locais para redes virtuais do Azure.

### Filtrar tráfego de rede

As redes virtuais do Azure permitem filtrar o tráfego entre sub-redes usando as seguintes abordagens:

* **Grupos de segurança de rede** 
    * Um grupo de segurança de rede é um recurso do Azure que pode conter várias regras de segurança de entrada e saída. Você pode definir essas regras para permitir ou bloquear tráfego com base em fatores como endereço IP de origem e de destino, porta e protocolo.
* **Soluções de virtualização de rede**
    * Uma solução de virtualização de rede é uma VM especializada que pode ser comparada a um dispositivo de rede protegida. Uma solução de virtualização de rede realiza uma função de rede específica, como execução de um firewall ou otimização de WAN (rede de longa distância).

## Conectar redes virtuais

Você pode vincular redes virtuais usando o emparelhamento dessas redes. O emparelhamento permite que os recursos em cada rede virtual se comuniquem entre si. Essas redes virtuais podem estar em regiões separadas, o que permite criar uma rede global interconectada por meio do Azure.

As UDR (rotas definidas pelo usuário) são uma atualização significativa nas Redes Virtuais do Azure que permitem maior controle sobre o fluxo de tráfego de rede. Esse método permite que os administradores de rede controlem as tabelas de roteamento entre sub-redes dentro de uma VNet, bem como entre VNets.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-networking-fundamentals/azure-virtual-network-fundamentals/)


> ## [Próximo](./M5_2_ConfiguracoesRedeVirtualAzure.md)
