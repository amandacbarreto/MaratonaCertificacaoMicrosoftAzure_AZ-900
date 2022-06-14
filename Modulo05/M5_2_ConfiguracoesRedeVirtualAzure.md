# Configurações de Rede Virtual do Azure

Você pode criar e configurar redes virtuais do Azure via portal do Azure, Azure PowerShell, CLI do Azure, Azure Cloud Shell ou um modelo do ARM.

## Criar uma rede virtual

### Configurações básicas

- **Assinatura**: só se aplica se você tem várias assinaturas para escolher.
- **Grupo de recursos**: como qualquer outro recurso do Azure, uma rede virtual precisa existir em um grupo de recursos.
- **Nome da rede**: o nome deve ser exclusivo em sua assinatura, mas não precisa ser globalmente exclusivo
- **Região**
- **Espaço de endereço**: espaço de endereço interno no formato CIDR (roteamento entre domínios). Esse espaço de endereço deve ser exclusivo dentro de sua assinatura e quaisquer redes às quais você deseje se conectar.

  - ###### Vamos supor que você escolha um espaço de endereço de 10.0.0.0/24 para sua primeira rede virtual. Os endereços definidos nesse espaço variam de 10.0.0.1 a 10.0.0.254. Em seguida, você criará uma segunda rede virtual e escolherá o espaço de endereço 10.0.0.0/8. Os endereços nesse espaço variam de 10.0.0.1 a 10.255.255.254. Alguns dos endereços se sobrepõem e não podem ser usados para as duas redes virtuais. Mas você pode usar 10.0.0.0/16, com endereços que variam de 10.0.0.1 a 10.0.255.254, e 10.1.0.0/16, com endereços que variam de 10.1.0.1 a 10.1.255.254. Você pode atribuir esses espaços de endereço às suas redes virtuais porque não há nenhuma sobreposição de endereços.
  - ##### **Observação: Você pode adicionar espaços de endereço depois de criar a rede virtual.**

- **Sub-rede**: em cada intervalo de endereços de rede virtual, você pode criar uma ou mais sub-redes que particionam o espaço de endereço da rede virtual. O roteamento entre sub-redes dependerá das rotas padrão de tráfego. Você também pode definir rotas personalizadas. Como alternativa, você pode definir uma sub-rede que abrange todos os intervalos de endereços das redes virtuais.

  - ##### **Observação:Os nomes de sub-rede devem começar com uma letra ou um número e terminar com uma letra, um número ou um sublinhado. Eles podem conter apenas letras, números, sublinhados, pontos ou hifens**.

- **Pontos de extremidade de serviço**: as opções incluem o Azure Cosmos DB, o Barramento de Serviço do Azure, o Azure Key Vault e assim por diante.

- **Gateway da NAT**: esse gateway é um serviço da NAT (Conversão de Endereços de Rede) totalmente gerenciado e altamente resiliente. Você pode configurar uma sub-rede para usar um endereço IP de saída estático ao acessar a Internet.

- **BastionHost**: você pode selecionar esse host para habilitar ou desabilitar o Azure Bastion em sua rede virtual. O serviço do Azure Bastion fornece conectividade de RDP/SSH contínua e segura às suas máquinas virtuais, diretamente no portal do Azure, via SSL.

- **Proteção contra DDoS Standard**: Você pode selecionar essa opção para habilitar ou desabilitar a proteção contra DDoS Padrão. A proteção contra DDoS do Standard é um serviço Premium. Para obter mais informações sobre a proteção contra DDoS do Standard, confira Visão geral da proteção contra DDoS do Standard do Azure.

- **Firewall**: Você pode habilitar ou desabilitar o Firewall do Azure. O Firewall do Azure é um serviço de segurança de rede baseado em nuvem gerenciado que protege seus recursos de Rede Virtual do Azure.

Depois de definir essas configurações, selecione Examinar + Criar eCriar quando a validação for aprovada.

### Configurações adicionais

Depois de criar uma rede virtual, você poderá definir outras configurações. Estão incluídos:

- **Grupo de segurança de rede**: Os grupos de segurança de rede têm regras de segurança que permitem filtrar o tipo de tráfego de rede que pode entrar e sair das sub-redes da rede virtual e dos adaptadores de rede. Crie o grupo de segurança de rede separadamente. Depois associe-a a cada sub-rede na rede virtual.
- **Tabela do rotas**: O Azure cria automaticamente uma tabela de rotas para cada sub-rede dentro de uma rede virtual do Azure e adiciona as rotas de sistema padrão à tabela. Você pode adicionar tabelas de rotas personalizadas para modificar o tráfego entre sub-redes e redes virtuais.
- **Delegação de sub-rede**: Você pode designar a sub-rede para uso por um serviço dedicado.

### Configurar redes virtuais

Depois de criar uma rede virtual, você poderá alterar configurações adicionais no painel Redes virtuais no portal do Azure. Como alternativa, você pode usar comandos do PowerShell ou comandos no Cloud Shell para fazer alterações.

Essas configurações incluem:

- **Espaços de endereço**: você pode adicionar mais espaços de endereço à definição inicial.
- **Dispositivos conectados**: veja uma lista de todos os host conectados na rede virtual.
- **Sub-redes**: você pode adicionar outras sub-redes.
- **Proteção contra DDos**: você pode habilitar ou desabilitar o plano de proteção contra DDos Padrão.
- **Firewall**: defina as configurações de firewall com o serviço de Firewall do Azure para a rede virtual.
- **Segurança**: fornece recomendação de segurança que você pode aplicar à sua rede virtual.
- **Gerenciador de Rede**: veja a configuração de administrador de segurança e conectividade à qual a rede virtual está associada.
- **Servidores DNS**: configure os servidores DNS internos ou externos que os recursos na rede virtual usarão.
- **Emparelhamentos**: vincule redes virtuais nas disposições de emparelhamento.
- **Pontos de extremidade de serviço**: habilita pontos de extremidade de serviço e os aplica a várias sub-redes.
- **Pontos de extremidade privados**: veja uma lista de pontos de extremidade privados habilitados em uma sub-rede.

Redes virtuais são mecanismos avançados e altamente configuráveis para conectar entidades no Azure. Você pode conectar recursos do Azure entre si ou aos recursos existentes no local. Você pode isolar, filtrar e rotear o tráfego de rede. O Azure permite que você aumente a segurança onde achar necessário.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-networking-fundamentals/azure-virtual-network-settings)

> ## [Próximo](./M5_3_GatewayVPNAzure.md)
