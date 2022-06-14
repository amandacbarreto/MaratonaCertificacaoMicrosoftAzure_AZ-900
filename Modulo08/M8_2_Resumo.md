# Resumo

## Hub IoT do Azure

É um serviço gerenciado e hospedado na nuvem que atua como um hub central de mensagens para obter uma comunicação bidirecional entre o seu aplicativo de IoT e os dispositivos que ele gerencia. É possível usar o Hub IoT do Azure para criar soluções de IoT com comunicações confiáveis e seguras entre milhões de dispositivos IoT e um back-end de solução hospedado na nuvem. É possível conectar virtualmente qualquer dispositivo ao seu hub IoT.

### Quando usar o Hub IoT do Azure

1. Quando o não comprometimento do dispositivo não for fundamental, ou seja, quando a segurança não é uma consideração crítica no design do seu produto. Se precisasse, o ideal seria o Azure Sphere.

2. Quando não for preciso de um painel para os relatórios e o gerenciamento. Se precisasse, o ideal seria Azure IoT Central.

Em outras palavras, o Hub IoT é indicado quando se quer receber os dados dos diversos dispositivos, mas nao há uma grande necessidade de segurança das informações nem de uma visuzalização mais completa dos dados e necessidade de enviar comandos para esses dispositivos.

## Azure IoT Central

O Azure IoT Central se baseia no Hub IoT adicionando um painel que permite que você conecte, monitore e gerencie os seus dispositivos IoT. Com a IU (interface do usuário) visual é fácil se conectar rapidamente com novos dispositivos e observar quando eles começam a enviar telemetria ou mensagens de erro. 

Você pode usar a interface do usuário para controlar os seus dispositivos remotamente. Esse recurso permite que você envie por push uma atualização de software ou modifique uma propriedade do dispositivo. É possível ajustar a temperatura desejada para uma ou todas as máquinas de venda automática refrigeradas diretamente do IoT Central.

### Quando usar o IoT Central?

1. Quando obter um painel de relatórios e gerenciamento é um requisito, mas não há necessidade de uma grande segurança.

O modelo de início de Logística Conectada fornece um painel predefinido que atenderá a vários desses requisitos. Esse painel é pré-configurado para demonstrar a atividade de operações de logística críticas do dispositivo.

### Quando não usar o Azure IoT Central?

O Azure IoT Central fornece um painel que permite que as empresas gerenciem dispositivos IoT de maneira individual, bem como em agregação, além de exibir relatórios e configurar notificações de erro por meio de uma GUI.
Se a empresa já realiza a análise dos dados coletados em um outro software próprio e não precisarão da capacidade de atualizar configurações ou softwares de maneira remota, não é preciso usar o Azure IoT Central.


## Azure Sphere

O Azure Sphere cria uma solução de IoT de ponta a ponta e altamente segura para os clientes. Essa solução abrange tudo, do hardware e sistema operacional no dispositivo a um método seguro de envio de mensagens do dispositivo para o hub de mensagens. O Azure Sphere tem recursos internos de comunicação e segurança para dispositivos conectados à Internet.


### Quando usar o Azure Sphere

1. Quando a segurança do dispositivo é o requisito principal.

Nesse caso, se a empresa precisar de um painel de relatórios e gerenciamento será utilizada a Azure IoT Central como base e, ao usar a IoT central, a empresa também estaria usando o Hub IoT do Azure nos bastidores.

### Quando não usar o Azure Sphere?

O Azure Sphere fornece uma solução completa para cenários em que a segurança é crítica. Então, nos casos em que a segurança é preferencial, mas não fundamental, o Azure Sphere não será necessário.

> O Azure Sphere fornece o nível mais alto de segurança para garantir que o dispositivo não tenha sido adulterado.
>
> Um exemplo de uso seria a criação de um quiosque de votação. 

> O IoT Central cria rapidamente um portal de gerenciamento baseado na Web para habilitar o relatório e a comunicação com dispositivos IoT.

> Um hub IoT se comunica com dispositivos IoT enviando e recebendo mensagens.

