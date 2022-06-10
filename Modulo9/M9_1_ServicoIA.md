# Escolha o melhor serviço de IA para suas necessidades

A IA (inteligência artificial) é uma categoria de computação que adapta e melhora sua capacidade de tomada de decisão ao longo do tempo com base em sucessos e falhas. O Microsoft Azure oferece várias soluções de IA dentre as quais escolher dependendo do problema que você está tentando resolver.

## Identificar as opções de produto

A IA é uma classificação de computação ampla que permite a um sistema de software perceber seu ambiente e tomar medidas que maximizem sua chance de atingir as metas. Umas das metas da IA é criar um sistema de software capaz de adaptar-se ou de aprender algo por conta própria sem ser explicitamente programado para isso.

Há duas abordagens básicas à IA.

1. Empregar um sistema de aprendizado profundo modelado na rede neural da mente humana, permitindo que ele descubra, aprenda e cresça com a experiência.

2. Machine learning, uma técnica de ciência de dados que usa dados existentes para treinar um modelo, testá-lo e, em seguida, aplicar esse modelo a novos dados para prever comportamentos, resultados e tendências futuros.

As estimativas ou previsões de aprendizado de máquina podem tornar aplicativos e dispositivos mais inteligentes.

O machine learning também é usado para detectar fraudes de cartão de crédito, pois analisa cada nova transação usando o que foi aprendido com a análise de milhões de transações fraudulentas.

Praticamente todos os dispositivos ou sistemas de software que coletam dados textuais, visuais e de áudio podem alimentar um modelo de machine learning que torna esse dispositivo ou sistema de software mais inteligente sobre como ele funciona no futuro.

### Opções de produto do Azure

Em um alto nível, há três ofertas de produtos principais da Microsoft, cada uma delas projetada para um público-alvo e caso de uso específico.

**1. Azure Machine Learning**

> O Azure Machine Learning é uma **plataforma para fazer previsões**. Ele consiste em ferramentas e serviços que permitem que você se conecte a dados para treinar e testar modelos para encontrar um que preveja com mais precisão um resultado futuro. Depois de executar experimentos para testar o modelo, você pode implantar e usá-lo em tempo real por meio de um ponto de extremidade da API Web.

Com o Azure Machine Learning, você pode:

- Criar um processo que define como obter dados, como lidar com casos de dados ausentes ou inválidos, como dividir os dados em um conjunto de treinamento ou de teste e como entregar os dados ao processo de treinamento.
- Treinar e avaliar modelos de previsão usando ferramentas e linguagens de programação familiares aos cientistas de dados.
- Criar pipelines que definem onde e quando executar os experimentos com uso intensivo de computação necessários para pontuar os algoritmos com base nos dados de treinamento e teste.
- Implantar o algoritmo de melhor desempenho como uma API para um ponto de extremidade para que ele possa ser consumido em tempo real por outros aplicativos.

**Escolha o Azure Machine Learning quando os cientistas de dados precisarem de controle total sobre o design e o treinamento de um algoritmo usando os próprios dados**.

**2. Serviços Cognitivos do Azure**

> Os Serviços Cognitivos do Azure **fornecem modelos de machine learning pré-criados que permitem que os aplicativos vejam, ouçam, falem, entendam e até mesmo comecem a raciocinar**.

Use os Serviços Cognitivos do Azure para **resolver problemas gerais, como análise de texto quanto a sentimentos emocionais ou análise de imagens para reconhecer objetos ou rostos**. Você não precisa de machine learning especial nem de conhecimento de ciência de dados para usar esses serviços. Os desenvolvedores acessam os Serviços Cognitivos do Azure por meio de APIs e podem facilmente incluir esses recursos em apenas algumas linhas de código.

Embora o Azure Machine Learning exija que você traga seus próprios dados e treine os modelos com base neles, os Serviços Cognitivos do Azure, na maior parte, fornecem modelos pré-treinados para que você possa trazer seus dados dinâmicos para obter previsões.

Os Serviços Cognitivos do Azure podem ser divididos nas seguintes categorias:

- Serviços de Linguagem: permita que seus aplicativos processem linguagem natural com scripts pré-criados, avalie sentimentos e aprenda a reconhecer o que os usuários desejam.
- Serviços de Fala: converta fala em texto e texto em fala natural. Traduza de um idioma para outro e habilite o reconhecimento e a verificação do locutor.
- Serviços de Visão: adicione funcionalidades de reconhecimento e identificação ao analisar imagens, vídeos e outros conteúdos visuais.
- Serviços de Decisão: adicione recomendações personalizadas para cada usuário que melhorem automaticamente a cada vez que forem usadas, conteúdo moderado para monitorar e remover conteúdo ofensivo ou arriscado e detectar anormalidades nos dados de série temporal.

**3. Serviço de Bot do Azure**

> O Serviço de Bot do Azure e o Bot Framework são **plataformas para a criação de agentes virtuais que compreendem e respondem a perguntas como um ser humano**. O Serviço de Bot do Azure é um pouco diferente do Azure Machine Learning e dos Serviços Cognitivos do Azure, pois tem um caso de uso específico. Ele cria um agente virtual capaz de se comunicar de maneira inteligente com humanos. Nos bastidores, o bot que você cria usa outros serviços do Azure, como os Serviços Cognitivos do Azure, para entender o que as suas contrapartes humanas estão solicitando.

Os bots podem ser usados para deslocar tarefas simples e repetitivas, como fazer uma reserva de jantar ou coletar informações de perfil, para sistemas automatizados que podem não exigir mais intervenção humana direta. Os usuários conversam com os bots usando texto, cartões interativos e fala. Uma interação de bot pode ser uma pergunta e resposta rápidas, ou pode ser uma conversa sofisticada que fornece acesso aos serviços de forma inteligente.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/ai-machine-learning-fundamentals/2-identify-product-options)

## Analisar os critérios de decisão

## Você está criando um agente virtual que interage com seres humanos por meio de linguagem natural?

Use o **Serviço de Bot do Azure** quando precisar criar um agente virtual para interagir com seres humanos usando linguagem natural.
O Serviço de Bot:

- integra fontes de conhecimento, processamento de linguagem natural e fatores forma para permitir a interação entre diferentes canais.
- geralmente dependem de outros serviços de IA para tarefas como reconhecimento de linguagem natural, ou até mesmo tradução, a fim de localizar respostas para o idioma preferencial de um cliente.

### Você precisa de um serviço capaz de entender o conteúdo e o significado de imagens, vídeos ou áudios, ou de traduzir texto para um idioma diferente?

Use os **Serviços Cognitivos do Azure** para tarefas de uso geral, como fazer conversão de fala em texto, integrar com a pesquisa ou identificar objetos em uma imagem.

Os Serviços Cognitivos do Azure são de uso geral, o que significa que muitos tipos de clientes podem se beneficiar do trabalho que a Microsoft já fez para treinar e testar esses modelos e oferecê-los de modo em escala.

### Você precisa prever o comportamento do usuário ou fornecer aos usuários recomendações personalizadas em seu aplicativo?

O serviço de **Personalizador dos Serviços Cognitivos do Azure** observa as ações dos usuários em um aplicativo.

Você pode usar o Personalizador para prever o comportamento deles e fornecer experiências relevantes, pois ele identifica padrões de uso. Novamente, você poderia capturar e armazenar o comportamento do usuário e criar sua própria solução personalizada do Azure Machine Learning para fazer isso, mas essa abordagem exigiria muito esforço e despesas.

### Seu aplicativo vai prever resultados futuros com base em dados históricos privados?

Escolha o **Azure Machine Learning** quando precisar analisar dados para prever resultados futuros.
Por exemplo, digamos que você precisa analisar anos de transações financeiras para descobrir novos padrões que poderiam ajudar a criar produtos e serviços para os clientes de sua empresa e oferecer esses novos serviços durante chamadas rotineiras do serviço de atendimento ao cliente. Quando estiver trabalhando com os dados proprietários, provavelmente você precisará criar um modelo de machine learning personalizado.

### Você precisa criar um modelo usando seus próprios dados ou precisa executar uma tarefa diferente daquelas listadas acima?

Use o **Azure Machine Learning** para obter a máxima flexibilidade.

Os cientistas de dados e os engenheiros de IA podem usar as ferramentas com as quais estão familiarizados e os dados que você fornece para desenvolver modelos de machine learning e aprendizado profundo ajustados para seus requisitos específicos.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/ai-machine-learning-fundamentals/3-analyze-decision-criteria)

## Usar Machine Learning para sistemas de suporte a decisões

1. A empresa está criando um agente virtual que interage com seres humanos por meio de linguagem natural? Se não, o Serviço de Bot do Azure não é um bom candidato para esse cenário.

2. A empresa precisa de um serviço que possa entender o conteúdo e o significado de imagens, vídeo, áudio ou conversão de texto em um idioma diferente? Se não, os Serviços Cognitivos relevantes não vão ajudar a empresa.

3. A empresa precisa prever o comportamento do usuário ou fornecer recomendações personalizadas aos usuários? Se sim, devemos continuar analisando.

   3.1. Se a empresa precisa criar um modelo complexo que incorpore dados de vendas históricas, tendências de dados de vendas, inventário e muito mais, é possível que o serviço de Personalizador do Serviço Cognitivo do Azure possa contribuir, mas ele não consegue lidar com toda a amplitude do projeto sozinho.

4. A empresa precisa prever resultados futuros com base em dados históricos privados? Se sim, o Azure Machine Learning é provavelmente a melhor opção.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/ai-machine-learning-fundamentals/4-use-machine-learning)

## Usar os Serviços Cognitivos para análise de dados

> **Cenário**
>
> A primeira geração do site de comércio eletrônico da Tailwind Traders estava disponível exclusivamente em inglês. No entanto, quando a equipe de Marketing patrocinou um estudo de dados demográficos nas unidades físicas da empresa, descobriu que, em média, apenas 80% dos clientes potenciais falam inglês. Em algumas vizinhanças, o número cai para 50%. A equipe de Marketing vê a adição de vários idiomas como uma oportunidade incrível de oferecer às pessoas que não falam inglês a mesma experiência de comércio eletrônico online que a oferecida aos falantes de inglês.

### Qual serviço escolher?

1. A empresa está criando um agente virtual que interage com seres humanos por meio de linguagem natural? Não, de modo que o Serviço de Bot do Azure não é um bom candidato para esse cenário. No entanto, se a empresa for implementar um agente de serviço de atendimento ao consumidor, pode ser útil considerar o uso da API de Tradução para fornecer tradução em tempo real para ajudar os clientes que não falam inglês.

2. A empresa precisa de um serviço que possa entender o conteúdo e o significado de imagens, vídeo, áudio ou conversão de texto em um idioma diferente? Sim, precisa. A tradução de conteúdo textual de um idioma para outro é uma tarefa de uso geral que pode ser simplificada usando o **serviço de Tradução dos Serviços Cognitivos do Azure**. O serviço é fácil de integrar a seus aplicativos, sites, ferramentas e soluções. Ele permite adicionar experiências de usuário em mais de 60 idiomas, e você pode usá-lo em qualquer plataforma de hardware com qualquer sistema operacional para tradução de idiomas de texto para texto.
   O recurso Serviços Cognitivos do Azure provavelmente é melhor opção para esse cenário, mas vamos continuar aplicando os critérios de decisão para garantir.

3. A Tailwind Traders precisa prever o comportamento do usuário ou fornecer recomendações personalizadas aos usuários? Não, de modo que o Personalizador dos Serviços Cognitivos do Azure não é um bom candidato para esse cenário.

4. O aplicativo da Tailwind Traders precisará prever resultados futuros com base em dados históricos privados? Não. Embora seja possível criar um modelo de Machine Learning para executar a tradução em vários idiomas, isso seria caro e demorado para a Tailwind Traders tentar criar modelos de tradução por conta própria. A equipe não tem a competência de aprendizado profundo nem os dados linguísticos necessários para treinar os modelos.

Então, nesse cenário, você pode selecionar **os Serviços Cognitivos** como a melhor opção.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/ai-machine-learning-fundamentals/5-use-cognitive-services)

## Usar o Serviço de Bot para experiências de chat interativas

> **Cenário**
>
> A equipe de serviço de atendimento ao consumidor vem pedindo há muito tempo um agente virtual para lidar com a grande maioria das perguntas que recebe. Não importa quanto destaque ele dê às respostas às perguntas frequentes no site, os compradores são impacientes e veem o contato em uma janela de chat como algo que lhes poupa tempo.
>
> A equipe quer que os compradores se sintam como se estivessem interagindo com um ser humano real. Quando fica claro que o agente virtual não pode fornecer uma resposta, a sessão de chat deve ser transferida para uma pessoa.

### Qual serviço escolher?

1. A empresa está criando um agente virtual que interage com seres humanos por meio de linguagem natural? Sim, está. O **Serviço de Bot do Azure** deve ser usado neste cenário para implementar uma experiência de chat de agente virtual. O Serviço de Bot poderia se beneficiar das informações na página de perguntas frequentes do site, juntamente com milhares de sessões de chat armazenadas entre compradores e representantes de atendimento ao cliente. Os supervisores do atendimento ao cliente podem testar e ajustar as respostas para continuarem a refinar a experiência do chat.

2. A empresa precisa de um serviço que possa entender o conteúdo e o significado de imagens, vídeo, áudio ou conversão de texto em um idioma diferente? Possivelmente, sim. Nesse cenário, os **Serviços Cognitivos do Azure podem ser usados em conjunto com o Serviço de Bot para criar a solução**. Além disso, qualquer solução de Bot do Azure provavelmente implementaria vários Serviços Cognitivos do Azure, como o LUIS (Reconhecimento Vocal) e, possivelmente, a Tradução para traduzir do idioma do comprador para o inglês e vice-versa.

3. A empresa precisa prever o comportamento do usuário ou fornecer recomendações personalizadas aos usuários? Não. O Personalizador dos Serviços Cognitivos do Azure não é um bom candidato para esse cenário.

4. O aplicativo da empresa precisará prever resultados futuros com base em dados históricos privados? Não. Embora a empresa tenha dados históricos para alimentar um modelo, o que possibilitaria usar o Azure Machine Learning para criar uma solução de chat, já existe uma opção adequada para a experiência de chat bot.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/ai-machine-learning-fundamentals/6-use-bot-services)

> ## [Próximo](./M9_2_Resumo.md)
