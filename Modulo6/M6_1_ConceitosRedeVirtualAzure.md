# Conceitos básicos da conta de Armazenamento do Azure

> ### Armazenamento do Azure é um serviço que você pode usar para armazenar arquivos, mensagens, tabelas e outros tipos de informações. Clientes como sites, aplicativos móveis, aplicativos da área de trabalho e muitos outros tipos de soluções personalizadas podem ler dados do Armazenamento do Microsoft Azure e gravar dados nele. O Armazenamento do Azure também é usado por máquinas virtuais de infraestrutura como serviço e por serviços de nuvem de plataforma como serviço.

Uma conta de armazenamento fornece um namespace exclusivo para os dados do Armazenamento do Microsoft Azure, que podem ser acessados de qualquer lugar do mundo por HTTP ou HTTPS. Os dados nesta conta são seguros, altamente disponíveis, duráveis e maciçamente escalonáveis.

# Conceitos básicos do armazenamento em disco

> ### O Armazenamento em Disco **fornece discos para máquinas virtuais do Azure**. Aplicativos e outros serviços podem acessar e usar os discos conforme necessário, do mesmo modo que aconteceria em cenários locais. O Armazenamento em Disco permite que os dados sejam armazenados de forma persistente e acessados de um disco rígido virtual anexado.

Os discos são apresentados em vários tamanhos e níveis de desempenho diferentes, de SSDs (unidades de estado sólido) até HDs (unidades de disco rígido) giratórias tradicionais, com diferentes níveis de desempenho. É possível usar discos SSD e HDD padrão para cargas de trabalho menos críticas, discos SSD premium para aplicativos de produção críticos e discos ultra para cargas de trabalho com uso intensivo de dados, como SAP HANA, bancos de dados de nível superior e cargas de trabalho com muitas transações.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-storage-fundamentals/azure-disk-storage/)

# Conceitos básicos do Armazenamento de blobs do Azure

> ### O Armazenamento de Blobs do Azure é uma **solução de armazenamento de objetos para a nuvem**. Ele **pode armazenar grandes quantidades de dados, como texto ou dados binários**.
>
> O Armazenamento de Blobs do Azure não é estruturado, o que significa que **não há nenhuma restrição quanto aos tipos de dados que ele pode armazenar**. O Armazenamento de Blobs pode gerenciar milhares de carregamentos simultâneos, grandes quantidades de dados de vídeo, arquivos de log em constante crescimento e pode ser acessado de qualquer lugar com uma conexão com a Internet.

Os blobs não estão limitados a formatos de arquivo comuns. Um blob pode conter gigabytes de dados binários transmitidos de um instrumento científico, uma mensagem criptografada para outro aplicativo ou dados em um formato personalizado para um aplicativo que você está desenvolvendo. Uma vantagem do armazenamento de blobs sobre o armazenamento em disco é que os desenvolvedores não precisam pensar em discos nem gerenciá-los. Os dados são carregados como blobs, e o Azure cuida das necessidades do armazenamento físico.

O Armazenamento de Blobs é ideal para:

- Fornecimento de imagens ou de documentos diretamente a um navegador.
- Armazenamento de arquivos para acesso distribuído.
- Transmissão por streaming de áudio e vídeo.
- Armazenamento de dados de backup e restauração, recuperação de desastres e arquivamento.
- Armazenamento de dados para análise por um serviço local ou hospedado no Azure.
- Armazenamento de até 8 TB de dados para máquinas virtuais.

Os blobs podem ser armazenados em contêineres, o que ajuda a organizá-los de acordo com suas necessidades de negócios.

O diagrama a seguir ilustra como você pode usar contas, contêineres e blobs do Azure.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-storage-fundamentals/azure-blob-container-storage)

# Conceitos básicos dos Arquivos do Azure

> ### Os Arquivos do Azure oferecem **compartilhamentos de arquivo totalmente gerenciados na nuvem que são acessíveis por meio dos protocolos SMB e Network File System** (versão prévia) padrão do setor.
>
> Os compartilhamentos de arquivos do Azure podem ser montados de maneira simultânea por implantações locais ou na nuvem do Windows, do Linux e do MacOS. Aplicativos executados em máquinas virtuais do Azure ou em serviços de nuvem podem montar um compartilhamento de armazenamento de arquivo para acessar dados de arquivos, assim como um aplicativo de área de trabalho montaria um compartilhamento SMB típico. Qualquer quantidade de máquinas virtuais ou funções do Azure podem montar e acessar o compartilhamento de armazenamento de arquivos simultaneamente. **Um cenário de uso típico seria compartilhar arquivos em qualquer lugar no mundo, bem como dados de diagnóstico ou compartilhamento de dados do aplicativo.**

Use Arquivos do Azure para as seguintes situações:

- Muitos aplicativos locais usam compartilhamentos de arquivos. Os Arquivos do Azure facilitam a migração desses aplicativos que compartilham dados para o Azure. Se você montar o compartilhamento de arquivo do Azure na mesma letra da unidade que o aplicativo local usa, a parte do aplicativo que acessa o compartilhamento de arquivo deverá funcionar com alterações mínimas, se houver.
- Armazene arquivos de configuração em um compartilhamento de arquivos e acesse-os de várias VMs. As ferramentas e utilitários usados por vários desenvolvedores em um grupo podem ser armazenados em um compartilhamento de arquivos, garantindo que todas as pessoas possam encontrá-los, e que usem a mesma versão.
- Grave dados em um compartilhamento de arquivos e processe ou analise os dados mais tarde. Por exemplo, talvez você queira fazer isso com logs de diagnóstico, métricas e despejos de memória.

**Os Arquivos do Azure garantem que os dados sejam criptografados em repouso, e o protocolo SMB garante que eles sejam criptografados em trânsito.**

Uma característica que distingue os Arquivos do Azure dos arquivos de um compartilhamento corporativo é que você pode acessá-los em qualquer lugar do mundo usando uma URL que aponte para eles. Você também pode usar tokens SAS (Assinatura de Acesso Compartilhado) para permitir o acesso a um ativo privado por um período específico.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-networking-fundamentals/azure-virtual-network-fundamentals/)

# Noções básicas sobre as camadas de acesso de blobs

O Armazenamento do Azure oferece diferentes camadas de acesso para seu armazenamento de blobs, ajudando você a armazenar dados de objeto da maneira mais econômica. As camadas de acesso disponíveis incluem:

- **Camada de acesso quente**: otimizada para armazenar dados que são acessados com frequência (por exemplo, imagens de seu site).
- **Camada de acesso frio**: otimizada para dados acessados com menos frequência e armazenados por pelo menos 30 dias (por exemplo, faturas de seus clientes).
- **Camada de acesso aos arquivos**: adequada para dados acessados raramente e armazenados por pelo menos 180 dias, com requisitos de latência flexíveis (por exemplo, backups de longo prazo).

As seguintes considerações se aplicam às diferentes camadas de acesso:

- Apenas as camadas de acesso quente e frio podem ser definidas no nível da conta. A camada de acesso aos arquivos não está disponível no nível da conta.
- Camadas de acesso frequente, esporádico e de arquivos podem ser definidas no nível do blob, durante ou após o upload.
- Os dados na camada de acesso frio podem tolerar uma disponibilidade ligeiramente inferior, mas ainda requerem alta durabilidade, latência de recuperação e características de taxa de transferência semelhantes a dados de acesso frequente. Para dados de acesso esporádico, um SLA (contrato de nível de serviço) de disponibilidade ligeiramente inferior e custos de acesso mais altos comparados com os dados de acesso frequente são compensações aceitáveis para custos de armazenamento mais baixos.
- O armazenamento de arquivos armazena dados offline e oferece os custos de armazenamento mais baixos, mas também os mais altos custos para reidratar e acessar dados.

###### Fonte: [Microsoft](https://docs.microsoft.com/pt-br/learn/modules/azure-storage-fundamentals/azure-storage-tiers/)

> ## [Próximo](./M6_2_Resumo.md)
