# Resumo

## **Azure Cosmos DB**

Serviço de multimodelo de banco de dados distribuído globalmente.

O Azure Cosmos DB fornece contratos de nível de serviço abrangentes para taxa de transferência, latência, disponibilidade e garantias de consistência.

O Azure Cosmos DB dá suporte a dados sem esquema, o que permite criar aplicativos "Always On" altamente responsivos para dar suporte a dados em constante mudança. Você pode usar esse recurso para armazenar dados que são atualizados e mantidos por usuários em todo o mundo.

O Azure Cosmos DB é flexível. No nível mais baixo, o Azure Cosmos DB armazena dados no formato ARS (atom-record-sequence). Os dados são então abstraídos e projetados como uma API, que você especifica ao criar o seu banco de dados. Suas opções incluem SQL, MongoDB, Cassandra, Tables e Gremlin. Esse nível de flexibilidade significa que, conforme você migra os bancos de dados da empresa para o Azure Cosmos DB, os desenvolvedores podem continuar usando as APIs com as quais se sentem mais confortáveis.

## **Banco de Dados SQL do Azure**

O Banco de Dados SQL do Azure é um banco de dados relacional baseado na última versão estável do mecanismo de banco de dados do Microsoft SQL Server. Ele pode ser usado para criar aplicativos orientados a dados e sites na linguagem de programação de sua escolha, sem a necessidade de gerenciar a infraestrutura.

## **Instância Gerenciada do Azure SQL**

A Instância Gerenciada de SQL do Azure é um serviço de dados de nuvem escalonável que fornece a mais ampla compatibilidade do mecanismo de banco de dados do SQL Server com todos os benefícios de uma plataforma como serviço totalmente gerenciada. Dependendo do cenário, a Instância Gerenciada de SQL do Azure pode oferecer mais opções para suas necessidades de banco de dados.

Assim como o Banco de Dados SQL do Azure, a Instância Gerenciada de SQL do Azure é um mecanismo de banco de dados PaaS (plataforma como serviço).

O Banco de Dados SQL do Azure e a Instância Gerenciada de SQL do Azure oferecem muitos dos mesmos recursos. No entanto, a Instância Gerenciada de SQL do Azure fornece várias opções que podem não estar disponíveis no Banco de Dados SQL do Azure.

## **Banco de Dados do Azure para MySQL**

O Banco de Dados do Azure para MySQL é um serviço de banco de dados relacional na nuvem que se baseia no mecanismo de banco de dados MySQL Community Edition, nas versões 5.6, 5.7 e 8.0. Com cada servidor do Banco de Dados do Azure para MySQL, você tira proveito dos recursos internos de segurança, tolerância a falhas e proteção de dados que, em outras situações, seria necessário comprar ou projetar, criar e gerenciar. Com o Banco de Dados do Azure para MySQL, você pode usar a restauração pontual para recuperar um servidor para um estado anterior, com alcance de até 35 dias.

## **Banco de Dados do Azure para PostgreSQL**

O Banco de Dados do Azure para PostgreSQL é um serviço de banco de dados relacional na nuvem. O software para servidores se baseia na versão da comunidade do mecanismo de banco de dados PostgreSQL de software livre.

O Banco de Dados do Azure para PostgreSQL está disponível em duas opções de implantação: Servidor Único e Hiperescala (Citus).

- **Servidor único**: oferece três tipos de preço (Básico, Uso Geral e Otimizado para Memória) e cada tipo oferece recursos diferentes para dar suporte a suas cargas de trabalho do banco de dados. Você pode criar seu primeiro aplicativo em um banco de dados pequeno por poucos dólares ao mês e depois ajustar a escala para atender às necessidades da solução. A escalabilidade dinâmica permite que o banco de dados responda de forma transparente a mudanças rápidas nos requisitos de recursos. Você paga apenas pelos recursos de que precisa, e somente quando precisa deles.

- **Hiperescala (Citus)**: escala horizontalmente as consultas em vários computadores usando a fragmentação. Seu mecanismo de consulta faz a correspondência entre consultas SQL recebidas nesses servidores para obter respostas mais rápidas em grandes conjuntos de dados. Ele serve para aplicativos que exigem maior escala e desempenho, que geralmente são as cargas de trabalho que estão se aproximando ou já excederam 100 GB de dados.

## **Big Data e análise**

- **Azure Synapse Analytics**: é um serviço de análise ilimitado que reúne data warehouse corporativo e análise de Big Data. Você pode consultar dados da maneira que preferir, usando recursos sem servidor ou provisionados em escala. Você tem uma experiência unificada para ingerir, preparar, gerenciar e fornecer dados para atender às necessidades imediatas de business intelligence e de aprendizado de máquina.

- **Azure HDInsight**: é um serviço de análise de software livre totalmente gerenciado para empresas. Trata-se de um serviço de nuvem que torna mais fácil, mais rápido e mais econômico o processamento de grandes quantidades de dados. Você pode executar estruturas de software livre populares e criar tipos de cluster como Apache Spark, Apache Hadoop, Apache Kafka, Apache HBase, Apache Storm e Serviços de Machine Learning. O HDInsight também dá suporte a uma ampla gama de cenários, como ETL (extração, transformação e carregamento), data warehousing, machine learning e IoT.

- **Azure Databricks**: ajuda a descobrir insights dos seus dados e a criar soluções de inteligência artificial. Você pode configurar seu ambiente do Apache Spark em minutos, dimensioná-lo automaticamente e colaborar em projetos compartilhados em um workspace interativo. O Azure Databricks dá suporte a Python, Scala, R, Java e SQL, bem como a bibliotecas e estruturas de ciência de dados, incluindo TensorFlow, PyTorch e scikit-lear

- **Análise Azure Data Lake**: serviço de trabalho de análise sob demanda que simplifica Big Data. Em vez de implantar, configurar e ajustar o hardware, você cria consultas para transformar os dados e extrair insights importantes. O serviço de análise pode manipular trabalhos de qualquer escala de maneira instantânea, simplesmente configurando o controle para a quantidade de potência necessária. Você pagará pelo trabalho somente quando ele estiver em execução, tornando-o mais econômico.

> O Azure Cosmos DB dá suporte às APIs de SQL, MongoDB, Cassandra, Tabelas e Gremlin.
>
> Então, se sua equipe de desenvolvimento está interessada em escrever aplicativos baseados em Graph que aproveitam a API do Gremlin, o Azure Cosmos DB seria a opção ideal.

> O Banco de Dados do Azure para MySQL é a escolha lógica para aplicativos existentes da pilha do LAMP.

> O Azure Synapse Analytics é a escolha lógica para analisar grandes volumes de dados.

> Banco de Dados SQL do Azure <- migração dos bancos de dados existentes do SQL Server
> Banco de Dados do Azure para MySQL <- migração dos bancos de dados existentes do MySQL
> Banco de Dados do Azure para PostgreSQL <- migração dos bancos de dados existentes do PostgreSQL para a nuvem.

> O Azure Cosmos DB funciona com uma variedade de APIs populares, incluindo o SQL, o MongoDB, o Cassandra, o Tables e o Gremlin. Você pode usá-los para migrar os seus dados para a nuvem e manter ou aprimorar as habilidades dos seus desenvolvedores.

> Os serviços de análise e de Big Data (grandes volumes de dados)são:
>
> - O Azure Synapse Analytics
> - O Azure HDInsight
> - O Azure Databricks
> - O Azure Data Lake Analytics
