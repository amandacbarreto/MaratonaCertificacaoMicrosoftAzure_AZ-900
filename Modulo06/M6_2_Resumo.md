# Resumo

## **Armazenamento em Disco do Azure**

Fornece discos para máquinas virtuais do Azure. Aplicativos e outros serviços podem acessar e usar os discos conforme necessário, do mesmo modo que aconteceria em cenários locais. O Armazenamento em Disco permite que os dados sejam armazenados de forma persistente e acessados de um disco rígido virtual anexado.

Os discos são apresentados em vários tamanhos e níveis de desempenho diferentes, de SSDs (unidades de estado sólido) até HDs (unidades de disco rígido) giratórias tradicionais, com diferentes níveis de desempenho.

## **Armazenamento do Blobs do Azure**

Armazenamento de objetos para a nuvem. Pode armazenar grandes quantidades de dados, como texto ou dados binários. Não é estruturado, o que significa que não há nenhuma restrição quanto aos tipos de dados que ele pode armazenar. O Armazenamento de Blobs pode gerenciar milhares de carregamentos simultâneos, grandes quantidades de dados de vídeo, arquivos de log em constante crescimento e pode ser acessado de qualquer lugar com uma conexão com a Internet.

Ideal para:

- Fornecimento de imagens ou de documentos diretamente a um navegador.
- Armazenamento de arquivos para acesso distribuído.
- Transmissão por streaming de áudio e vídeo.
- Armazenamento de dados de backup e restauração, recuperação de desastres e arquivamento.
- Armazenamento de dados para análise por um serviço local ou hospedado no Azure.
- Armazenamento de até 8 TB de dados para máquinas virtuais.

Você pode armazenar os blobs em contêineres.

## **Armazenamento de Arquivos do Azure**

Oferecem compartilhamentos de arquivo totalmente gerenciados na nuvem que são acessíveis por meio dos protocolos. Os compartilhamentos de arquivos do Azure podem ser montados de maneira simultânea por implantações locais ou na nuvem do Windows, do Linux e do MacOS.

Um cenário de uso típico seria compartilhar arquivos em qualquer lugar no mundo, bem como dados de diagnóstico ou compartilhamento de dados do aplicativo.

Use Arquivos do Azure para as seguintes situações:

- Muitos aplicativos locais usam compartilhamentos de arquivos. Os Arquivos do Azure facilitam a migração desses aplicativos que compartilham dados para o Azure.
- Armazene arquivos de configuração em um compartilhamento de arquivos e acesse-os de várias VMs. As ferramentas e utilitários usados por vários desenvolvedores em um grupo podem ser armazenados em um compartilhamento de arquivos, garantindo que todas as pessoas possam encontrá-los, e que usem a mesma versão.
- Grave dados em um compartilhamento de arquivos e processe ou analise os dados mais tarde. Por exemplo, talvez você queira fazer isso com logs de diagnóstico, métricas e despejos de memória.

## Camadas de acesso do Blob do Azure

O Azure fornece várias camadas de acesso para acomodar essas diferentes necessidades de acesso. Esse recurso pode ser usado para balancear os custos de armazenamento com suas necessidades de acesso.

As camadas de acesso disponíveis incluem:

- **Camada de acesso quente**: otimizada para armazenar dados que são acessados com frequência (por exemplo, imagens de seu site).
- **Camada de acesso frio**: otimizada para dados acessados com menos frequência e armazenados por pelo menos 30 dias (por exemplo, faturas de seus clientes).
- **Camada de acesso aos arquivos**: adequada para dados acessados raramente e armazenados por pelo menos 180 dias, com requisitos de latência flexíveis (por exemplo, backups de longo prazo).

> A primeira etapa para compartilhar um arquivo de imagem como um blob no Armazenamento do Azure é criar uma conta do Armazenamento do Azure para usar os recursos do Armazenamento do Azure.

> a melhor opção do Armazenamento do Azure para armazenar dados para backup e restaura é o _Armazenamento de Blobs do Azure_.

> O Armazenamento do Azure pode fornecer uma variedade de opções para armazenar seus dados.

> A primeira etapa ao usar o Armazenamento do Azure é criar uma conta de armazenamento.
> Depois que você faz isso, o Azure fornece várias opções para armazenar seus dados:
>
> - Armazenamento do Blobs do Azure
> - Armazenamento em Disco do Azure
> - Armazenamento de Arquivos do Azure

> Além disso, o Azure fornece várias camadas de acesso que você pode usar para equilibrar custos de armazenamento com suas necessidades de negócios.
