# Resumo

Proteção completa é o tema recorrente. Pense na segurança como um interesse de várias camadas e de vários vetores. As ameaças vêm de locais que não esperamos e podem vir com uma força surpreendente.

- **O Firewall do Azure** é um serviço de segurança de rede gerenciado e baseado em nuvem que ajuda a proteger recursos nas redes virtuais do Azure.
- **Uma rede virtual do Azure** é semelhante a uma rede tradicional que você operaria em seu datacenter. Ela permite que máquinas virtuais e outros recursos de computação se comuniquem com segurança entre si, pela Internet e por redes locais.
- **Um NSG (grupo de segurança de rede)** permite que você filtre o tráfego de rede de e para recursos do Azure em uma rede virtual.
- **A Proteção contra DDoS do Azure** ajuda a proteger os recursos do Azure contra ataques de DDoS.

> A proteção contra DDoS ajuda a proteger os recursos do Azure contra ataques de DDoS. Um ataque de DDoS tenta sobrecarregar e esgotar os recursos de um aplicativo, tornando o aplicativo lento ou sem resposta a usuários legítimos.

> O Firewall do Azure permite limitar o tráfego de HTTP/S de saída a uma lista especificada de FQDNs (nomes de domínio totalmente qualificados), portanto essa seria a melhor maneira de uma empresa limitar todo o tráfego de saída de VMs para hosts conhecidos.
>
> É possível garantir que todos os aplicativos em execução se comuniquem apenas com portas e hosts confiáveis, porém o firewall da Azure é uma forma de configurar com mais facilidade o acesso à rede sem modificações de software.

> Para impletmentar com mais facilidade uma política de negar por padrão para que as VMs não possam se conectar entre si, é possível criar uma regra de grupo de segurança de rede que impeça o acesso de outra VM na mesma rede.
>
> Uma regra de grupo de segurança de rede permite filtrar o tráfego de e para os recursos por endereço IP de origem e de destino, porta e protocolo.
