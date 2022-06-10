# Escolha o serviço de IoT do Azure mais adequado para o seu aplicativo

A IoT conecta o mundo físico ao mundo digital habilitando dispositivos com sensores e uma conexão com a Internet para se comunicar com sistemas baseados em nuvem por meio da Internet.

## Identificar as opções de produto

A IoT habilita os dispositivos para coletar e retransmitir informações a fim de obter uma análise dos dados. Os dispositivos inteligentes são equipados com sensores que coletam dados, como por exemplo:

- Sensores ambientais que capturam a temperatura e os níveis de umidade.
- Códigos de barras, códigos QR ou scanners de OCR (reconhecimento óptico de caracteres).
- Sensores de proximidade e localização geográfica.
- Sensores infravermelhos, de luz e cor.
- Sensores ultrassônicos e de som.
- Sensores de movimento e toque.
- Sensores de acelerômetro e inclinação.
- Sensores de fumaça, gás e álcool.
- Sensores de erro para detectar quando há um problema com o dispositivo.
- Sensores mecânicos que detectam anomalias ou deformações.
- Sensores de fluxo, nível e pressão para medir gases e líquidos.

> Ao usar os serviços IoT do Azure, os dispositivos equipados com esses tipos de sensores e que podem se conectar à Internet poderão enviar leituras do sensor a um ponto de extremidade específico no Azure por meio de uma mensagem. Os dados da mensagem serão coletados e agregados, além disso, eles poderão ser convertidos em relatórios e alertas. Como alternativa, todos os dispositivos poderão ser atualizados com o novo firmware para corrigir problemas ou adicionar novas funcionalidades, enviando atualizações de software dos serviços IoT do Azure para cada dispositivo.

## Hub IoT do Azure

> ### O Hub IoT do Azure é um **serviço gerenciado e hospedado na nuvem que atua como um hub central de mensagens para obter uma comunicação bidirecional entre o seu aplicativo de IoT e os dispositivos que ele gerencia**. É possível usar o Hub IoT do Azure para criar soluções de IoT com comunicações confiáveis e seguras entre milhões de dispositivos IoT e um back-end de solução hospedado na nuvem. É possível conectar virtualmente qualquer dispositivo ao seu hub IoT.

O serviço do Hub IoT é compatível com comunicações do dispositivo para a nuvem e da nuvem para o dispositivo. Ele também é compatível com vários padrões de envio de mensagens, como telemetria do dispositivo para nuvem, carregamento de arquivos de dispositivos e métodos de solicitação e resposta para controlar seus dispositivos da nuvem. Depois que o hub IoT recebe mensagens de um dispositivo, ele pode roteá-las para outros serviços do Azure.

De uma perspectiva de nuvem para dispositivo, o Hub IoT permite executar o comando e controle. Isso significa que você pode ter um controle remoto manual ou automatizado de dispositivos conectados para que seja possível instruir o dispositivo a fim de abrir válvulas, definir temperaturas de destino, reiniciar dispositivos travados e assim por diante.

## Azure IoT Central

> ### O Azure IoT Central **se baseia no Hub IoT adicionando um painel que permite que você conecte, monitore e gerencie os seus dispositivos IoT**. Com a IU (interface do usuário) visual é fácil se conectar rapidamente com novos dispositivos e observar quando eles começam a enviar telemetria ou mensagens de erro. É possível observar o desempenho geral de todos os dispositivos em agregação. Além disso, você pode configurar alertas que enviam notificações quando um dispositivo específico precisa de manutenção. Por fim, você pode efetuar push de atualizações de firmware para o dispositivo.

O IoT Central fornece modelos de início para cenários comuns em vários setores, como varejo, energia, serviços de saúde e administração pública. Com o IoT Central, é possível personalizar os modelos de início para os dados específicos que serão enviados de seus dispositivos, além dos relatórios que você deseja ver e os alertas que deseja enviar.

Você pode usar a interface do usuário para controlar os seus dispositivos remotamente. Esse recurso permite que você envie por push uma atualização de software ou modifique uma propriedade do dispositivo. É possível ajustar a temperatura desejada para uma ou todas as máquinas de venda automática refrigeradas diretamente do IoT Central.

Uma parte importante do IoT Central é **o uso de modelos de dispositivo**. Usando um modelo de dispositivo, você poderá conectar um dispositivo sem uma codificação no lado do serviço. O IoT Central usa os modelos para construir os painéis, alertas e assim por diante. Os desenvolvedores de dispositivos ainda precisarão criar o código a ser executado nos dispositivos. Além disso, esse código deverá corresponder à especificação do modelo de dispositivo.

## Azure Sphere

> ### O Azure Sphere **cria uma solução de IoT de ponta a ponta e altamente segura para os clientes**. Essa solução abrange tudo, do hardware e sistema operacional no dispositivo a um método seguro de envio de mensagens do dispositivo para o hub de mensagens. O Azure Sphere tem recursos internos de comunicação e segurança para dispositivos conectados à Internet.

O Azure Sphere é fornecido em três partes:

- A primeira parte é o MCU (unidade do microcontrolador) do Azure Sphere, que é responsável por processar o sistema operacional e enviar sinais de sensores conectados.
- A segunda parte é um OS (sistema operacional) Linux personalizado que administra a comunicação com o serviço de segurança e pode executar o software do fornecedor.
- A terceira parte é o Serviço de Segurança do Azure Sphere, também conhecido como AS3.
  O trabalho dele é verificar se o dispositivo não foi comprometido de modo malicioso. Quando o dispositivo tenta se conectar ao Azure, primeiro ele precisa se autenticar, por dispositivo. Ele faz isso usando uma autenticação baseada em certificado. Caso ele seja autenticado com êxito, o AS3 faz uma verificação para garantir que o dispositivo não foi adulterado. Depois de ter estabelecido um canal seguro de comunicação, o AS3 envia por push um sistema operacional ou atualizações de software desenvolvidas pelo cliente para o dispositivo.

Depois que o sistema do Azure Sphere tiver validado a autenticidade do dispositivo e feito a autenticação dele, o dispositivo poderá interagir com outros serviços IoT do Azure enviando informações de telemetria e de erro.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/iot-fundamentals/2-identify-product-options)

## Analisar os critérios de decisão

### É essencial garantir que o dispositivo não seja comprometido?

Não em todos os casos. Os fabricantes e os clientes não querem que os respectivos dispositivos sejam comprometidos por ações mal-intencionadas e usados para fins maliciosos, mas, em alguns casos, a garantia da integridade é mais crítica do que em outros. Um exemplo seria um caixa eletrônico em comparação com uma máquina de lavar roupas.

> **Quando a segurança é uma consideração crítica no design do seu produto, a melhor opção de produto é o Azure Sphere, que fornece uma solução abrangente de ponta a ponta para dispositivos IoT.**

O **Azure Sphere garante um canal seguro de comunicação entre o dispositivo e o Azure controlando tudo, do hardware ao sistema operacional, além do processo de autenticação**. Isso garante que a integridade do dispositivo não seja comprometida. Depois que um canal seguro for estabelecido, o dispositivo poderá receber mensagens com segurança. Além disso, as mensagens ou atualizações de software poderão ser enviadas ao dispositivo de maneira remota.

### Preciso de um painel para relatórios e gerenciamento?

Sua próxima decisão deverá ser baseada no nível dos serviços que você exige de sua solução de IoT. Caso queira somente se **conectar aos dispositivos remotos para receber telemetria e, ocasionalmente, enviar atualizações por push e não há necessidade de obter funcionalidades de relatório, talvez você prefira implementar somente o Hub IoT do Azure**. Seus programadores ainda poderão criar um conjunto personalizado de ferramentas e relatórios de gerenciamento usando a API RESTful do Hub IoT.

No entanto, **caso queria uma interface do usuário personalizável e pré-criada com a qual será possível exibir e controlar seus dispositivos de maneira remota, talvez você prefira começar com o IoT Central**. Com essa solução, será possível controlar um dispositivo ou todos eles de uma vez. Além disso, você poderá configurar alertas para determinadas condições, como uma falha do dispositivo.

**O IoT Central integra-se com muitos produtos diferentes do Azure, incluindo o Hub IoT, para criar um painel com relatórios e recursos de gerenciamento**. O painel é baseado em modelos de início para cenários comuns de uso e do setor. Será possível usar o painel gerado pelo modelo de início como está ou personalizá-lo para atender às suas necessidades. Você poderá ter vários painéis e direcioná-los a uma variedade de usuários.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/iot-fundamentals/3-analyze-decision-criteria)

## Usar o Hub IoT

1. Quando o não comprometimento do dispositivo não for fundamental, ou seja, quando a segurança não é uma consideração crítica no design do seu produto. Se precisasse, o ideal seria o Azure Sphere.

2. Quando não for preciso de um painel para os relatórios e o gerenciamento. Se precisasse, o ideal seria Azure IoT Central.

Em outras palavras, o Hub IoT é indicado quando se quer receber os dados dos diversos dispositivos, mas nao há uma grande necessidade de segurança das informações nem de uma visuzalização mais completa dos dados e necessidade de enviar comandos para esses dispositivos.

### Quando não usar o Azure IoT Central?

O Azure IoT Central fornece um painel que permite que as empresas gerenciem dispositivos IoT de maneira individual, bem como em agregação, além de exibir relatórios e configurar notificações de erro por meio de uma GUI.
Se a empresa já realiza a análise dos dados coletados em um outro software próprio e não precisarão da capacidade de atualizar configurações ou softwares de maneira remota, não é preciso usar o Azure IoT Central.

### Quando não usar o Azure Sphere?

O Azure Sphere fornece uma solução completa para cenários em que a segurança é crítica. Então, nos casos em que a segurança é preferencial, mas não fundamental, o Azure Sphere não será necessário.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/iot-fundamentals/4-use-iot-hub)

## Usar o IoT Central

1. Quando obter um painel de relatórios e gerenciamento é um requisito, mas não há necessidade de uma grande segurança.

O modelo de início de Logística Conectada fornece um painel predefinido que atenderá a vários desses requisitos. Esse painel é pré-configurado para demonstrar a atividade de operações de logística críticas do dispositivo.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/iot-fundamentals/5-use-iot-central)

## Usar o Azure Sphere

1. Quando a segurança do dispositivo é o requisito principal.

Nesse caso, se a empresa precisar de um painel de relatórios e gerenciamento será utilizada a Azure IoT Central como base e, ao usar a IoT central, a empresa também estaria usando o Hub IoT do Azure nos bastidores.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/iot-fundamentals/6-use-azure-sphere)

> ## [Próximo](./M8_2_Resumo.md)
