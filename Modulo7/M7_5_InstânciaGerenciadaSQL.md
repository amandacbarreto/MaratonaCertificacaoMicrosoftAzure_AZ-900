# Explorar a Instância Gerenciada de SQL do Azure

> ### A Instância Gerenciada de SQL do Azure é um **serviço de dados de nuvem escalonável que fornece a mais ampla compatibilidade do mecanismo de banco de dados do SQL Server com todos os benefícios de uma plataforma como serviço totalmente gerenciada**. Dependendo do cenário, a Instância Gerenciada de SQL do Azure pode oferecer mais opções para suas necessidades de banco de dados.

## Recursos

Assim como o Banco de Dados SQL do Azure, a Instância Gerenciada de SQL do Azure é um mecanismo de banco de dados PaaS (plataforma como serviço), o que significa que sua empresa poderá tirar proveito dos melhores recursos ao mover seus dados para a nuvem em um ambiente totalmente gerenciado. Por exemplo, a empresa não precisará mais comprar e gerenciar hardwares caros, e você não precisará manter a sobrecarga adicional de gerenciar a infraestrutura local. Sua empresa também se beneficiará dos recursos de provisionamento rápido e dimensionamento de serviços do Azure, bem como da aplicação de patch automatizada e das atualizações de versão. Além disso, você poderá ter a certeza de que seus dados sempre estarão lá quando você precisar deles, por meio de recursos internos de alta disponibilidade e de um SLA (contrato de nível de serviço) de 99,99% de tempo de atividade. Você também poderá proteger os dados com backups automatizados e um período de retenção de backup configurável.

O Banco de Dados SQL do Azure e a Instância Gerenciada de SQL do Azure oferecem muitos dos mesmos recursos. No entanto, _a Instância Gerenciada de SQL do Azure fornece várias opções que podem não estar disponíveis no Banco de Dados SQL do Azure_.

    Por exemplo, a Tailwind Traders atualmente usa vários servidores locais que executam o SQL Server e gostaria de migrar os bancos de dados existentes para um banco de dados SQL em execução na nuvem. No entanto, vários dos bancos de dados usam caracteres cirílico para ordenação. Nesse cenário, a Tailwind Traders deve migrar os bancos de dados para uma Instância Gerenciada de SQL do Azure, uma vez que o Banco de Dados SQL do Azure usa apenas a ordenação do servidor SQL_Latin1_General_CP1_CI_AS padrão.

## Migração

A Instância Gerenciada de SQL do Azure facilita a migração de dados locais no SQL Server para a nuvem usando o DMS (Serviço de Migração de Banco de Dados) do Azure ou backup e a restauração nativos. Depois de descobrir todos os recursos que sua empresa usa, você precisa avaliar quais instâncias do SQL Server locais pode migrar para a Instância Gerenciada de SQL do Azure para ver se há algum problema de bloqueio. Após resolver possíveis problemas, você pode migrar os dados e fazer a transferência do SQL Server local para a Instância Gerenciada de SQL do Azure alterando a cadeia de conexão em seus aplicativos.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-database-fundamentals/azure-sql-managed-instance)

> ## [Próximo](./M7_6_BigDataAnalise.md)
