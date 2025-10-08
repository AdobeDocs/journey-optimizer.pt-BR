---
solution: Journey Optimizer
product: journey optimizer
title: Medidas de proteção e limitações para campanhas orquestradas
description: Saiba mais sobre as medidas de proteção e limitações das campanhas orquestradas
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
source-git-commit: a9b790bc833b5819862bf2f3284968d81f595f28
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 2%

---


# Proteções e limitações {#guardrails}

Você encontrará abaixo as medidas de proteção e limitações ao usar campanhas orquestradas.

## Limitações do fluxo de dados

### Design e armazenamento de dados

* O armazenamento de dados relacional oferece suporte a **no máximo 200 tabelas** (esquemas).

* Para campanhas orquestradas, o tamanho total de qualquer esquema individual **não deve exceder 100 GB**.

* As atualizações diárias de um esquema devem ser **limitadas a menos de 20%** de sua contagem total de registros para manter o desempenho e a estabilidade.

* Os dados relacionais são o modelo principal compatível com casos de uso de assimilação, modelagem de dados e segmentação.

* Os esquemas usados para direcionamento devem conter pelo menos **um campo de identidade do tipo`String`**, mapeado para um namespace de identidade definido.

* O número médio de atributos por esquema **não deve exceder 50 colunas** para manter a capacidade de gerenciamento e o desempenho.

* Esquemas baseados em modelo não podem ser habilitados para **Perfis** do Adobe Experience Platform. Somente esquemas XDM padrão são suportados para **Perfis** do Adobe Experience Platform. Os esquemas baseados em modelo podem ser ativados para Campanhas orquestradas ou Campanhas de ação. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Assimilação de dados

* É necessária a assimilação de perfil + dados relacionais.

* Toda assimilação deve ocorrer via **fontes do Change Data Capture**:

   * Para **baseado em arquivo**: o campo `_change_request_type` é obrigatório. Os valores com suporte são `U` (substituição) ou `D` (exclusão).

   * Para **baseado em nuvem**: o log de tabela deve estar habilitado.

* **Não são permitidas atualizações parciais de registros**. Cada linha deve ser fornecida como um registro completo.

* A assimilação em lote para a Orquestração de campanha é limitada a **uma vez a cada 15 minutos**.

* A latência de assimilação, no armazenamento relacional, normalmente varia de **15 minutos a 2 horas**, dependendo de:

   * Volume de dados

   * Simultaneidade do sistema

   * Tipo de operação, por exemplo, inserções são mais rápidas que atualizações

* **A relação entre o fluxo de dados e o conjunto de dados é de 1 a 1**. Isso significa que apenas uma fonte pode alimentar um conjunto de dados em um determinado momento. Para alternar a origem, o fluxo de dados existente deve ser excluído e um novo fluxo de dados deve ser criado com a nova origem.

### Modelagem de dados

* Todos os esquemas, incluindo tabelas de fatos, devem incluir **um descritor de versão** para garantir o controle de versão e a rastreabilidade adequados.

* Cada tabela deve ter uma **chave primária** definida para oferecer suporte à integridade de dados e às operações downstream.

* O `table_name` atribuído durante a criação do conjunto de dados é permanente e usado em todos os recursos de segmentação e personalização.

* **Não há suporte para** grupos de campos na estrutura de modelagem de dados atual.

* O suporte para chaves primárias compostas com fluxos de upload de arquivo não está disponível no momento.

## Limitações de atividades

* Somente **atributos escalares têm suporte** nas definições de público-alvo; **não são permitidos mapas e matrizes**.

* **As atividades de segmentação dependem principalmente de dados relacionais**. Embora os dados do perfil possam ser incluídos, o uso de grandes conjuntos de dados de perfil pode afetar o desempenho.

* **Os limites são aplicados ao número de atributos de perfil** que podem ser usados em lotes e públicos de streaming para manter a eficiência do sistema.

* **Enumerações** são totalmente compatíveis.

* **Os públicos-alvo de leitura não são armazenados em cache**, cada execução de campanha aciona uma avaliação completa do público-alvo a partir dos dados subjacentes.

* **A otimização é altamente recomendada** ao trabalhar com definições de público-alvo grandes ou complexas para garantir o desempenho.

* **As atividades dos públicos salvos são estáticas**, refletem os dados disponíveis no momento da execução da campanha.

* **Não há suporte para anexar a uma atividade de Público-alvo salvo**. Quaisquer modificações exigem uma substituição completa do público-alvo.

## Limitações de canal

Somente os canais SMS, Push e Email são compatíveis com campanhas orquestradas.
