---
solution: Journey Optimizer
product: journey optimizer
title: Medidas de proteção e limitações para campanhas orquestradas
description: Saiba mais sobre as medidas de proteção e limitações das campanhas orquestradas
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/ViPJaOPo-AT-naQqq-PaPw-BI5YupYuYAEy56AUEp2A
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: cda41058be1eb26538f4b0ef8c7b6c3f1c01eccd
workflow-type: tm+mt
source-wordcount: 756
ht-degree: 2%

---

# Medidas de proteção e limitações {#guardrails}

>[!BEGINSHADEBOX]

**Nesta página:** Revise as medidas de proteção e limitações que se aplicam ao armazenamento de dados, assimilação, modelagem de dados, atividades e canais em campanhas orquestradas.

>[!ENDSHADEBOX]

Você encontrará abaixo as medidas de proteção e limitações ao usar campanhas orquestradas.

## Limitações do fluxo de dados

### Design e armazenamento de dados

* **Máximo de tabelas** - O armazenamento de dados relacional dá suporte a um máximo de 200 tabelas (esquemas).

* **Tamanho do esquema** - Para campanhas Orquestradas, o tamanho total de qualquer esquema individual não deve exceder 100 GB.

* **Volume de atualização diária** - As atualizações diárias de um esquema devem ser limitadas a menos de 20% de sua contagem total de registros para manter o desempenho e a estabilidade.

* **Modelo de dados relacional** - Os dados relacionais são o modelo principal com suporte para casos de uso de assimilação, modelagem de dados e segmentação.

* **Campo de identidade** - Os esquemas usados para direcionamento devem conter pelo menos um campo de identidade do tipo `String`, mapeado para um namespace de identidade definido.

* **Atributos por esquema** - O número médio de atributos por esquema não deve exceder 50 colunas para manter a capacidade de gerenciamento e o desempenho.

* **Habilitação de perfis** - Esquemas relacionais não podem ser habilitados para Perfis Adobe Experience Platform. Somente esquemas XDM padrão são suportados para Perfis do Adobe Experience Platform. Esquemas relacionais podem ser ativados para campanhas orquestradas ou campanhas Action. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Ingestão de dados {#data-ingestion}

* **Assimilação de perfil e relacional** - A assimilação de perfil + dados relacionais é necessária.

* **Alterar fontes de Captura de Dados** - Toda assimilação deve ocorrer por meio das fontes de Captura de Dados de Alteração:

   * **Fontes baseadas em arquivo** - O campo `_change_request_type` é obrigatório. Os valores com suporte são `u` (substituição) ou `d` (exclusão). Esses valores devem estar em minúsculas `u` e `d`, e não em maiúsculas `U` e `D`.

   * **Fontes baseadas em nuvem** - O log de tabela deve estar habilitado.

* **Somente registros concluídos** - Atualizações parciais de registros não são permitidas; cada linha deve ser fornecida como um registro completo.

* **Frequência de assimilação em lote** - A assimilação em lote para a Orquestração do Campaign é limitada a uma vez a cada 15 minutos.

* **Latência de assimilação** - A latência de assimilação no armazenamento relacional normalmente varia de 15 minutos a 2 horas, dependendo do seguinte:

   * Volume de dados

   * Simultaneidade do sistema

   * Tipo de operação (por exemplo, inserções são mais rápidas que atualizações)

* **Relação entre fluxo de dados e conjunto de dados** - A relação entre fluxo de dados e conjunto de dados é de 1 a 1. Somente uma fonte pode alimentar um conjunto de dados por vez. Para alternar a origem, exclua o fluxo de dados existente e crie um novo com a nova origem.

### Modelagem de dados

* **Descritor de versão** - Todos os esquemas, incluindo tabelas de fatos, devem incluir um descritor de versão para garantir o controle de versão e a rastreabilidade adequados.

* **Chave primária** - Cada tabela deve ter uma chave primária definida para oferecer suporte à integridade de dados e às operações downstream.

* **Nome de tabela permanente** - O `table_name` atribuído durante a criação do conjunto de dados é permanente e é usado em todos os recursos de segmentação e personalização.

* **Grupos de campos** - Não há suporte para grupos de campos na estrutura de modelagem de dados atual.

* **Chaves primárias compostas** - O suporte para chaves primárias compostas com fluxos de carregamento de arquivo não está disponível no momento.

## Limitações de atividades {#activities-limitations}

* **Limite de atividades do canal** - Uma campanha Orquestrada dá suporte a no máximo 10 atividades de canal (Email, SMS, Push ou Correspondência direta). Somente as atividades de canal contam para esse limite. As atividades de direcionamento e controle de fluxo não contam (por exemplo, Criar público, Aguardar, Dividir, Enriquecimento, Reconciliação, Bifurcar, Encerrar ou Teste).

  Se você exceder o limite ao salvar ou publicar, a operação falhará. Para ficar dentro do limite, reduza o número de atividades do canal ou divida a entrega de mensagens em várias campanhas orquestradas.

* **Limite de atividades da tela** - O número de atividades em uma tela de campanha orquestrada é limitado a 500. Esse limite se aplica a todos os tipos de atividade na tela. Ele é separado do limite de atividades do canal aplicado na publicação. Para manutenção e desempenho, mantenha os workflows abaixo de 100 atividades na prática.

* **Somente atributos escalares** - Somente atributos escalares têm suporte em definições de público-alvo; mapas e matrizes não são permitidos.

* **Dados relacionais para segmentação** - As atividades de segmentação dependem principalmente de dados relacionais. Embora os dados do perfil possam ser incluídos, o uso de grandes conjuntos de dados de perfil pode afetar o desempenho.

* **Limites de atributo de perfil** - Os limites são aplicados no número de atributos de perfil que podem ser usados em lotes e públicos de streaming para manter a eficiência do sistema.

* **Enumerations** - Enumerações são totalmente compatíveis.

* **Leitura de públicos não armazenados em cache** - Leitura de públicos não armazenados em cache; cada execução de campanha aciona uma avaliação completa do público a partir dos dados subjacentes.

* **Otimização do público-alvo** - A otimização é altamente recomendada ao trabalhar com definições de público-alvo grandes ou complexas para garantir o desempenho.

* **Os públicos salvos são estáticos** - As atividades salvas de públicos são estáticas; elas refletem os dados disponíveis no momento da execução da campanha.

* **Não anexar a um Público-alvo salvo** - Não há suporte para anexar a uma atividade de Público-alvo salvo. Quaisquer modificações exigem uma substituição completa do público-alvo.

## Limitações de canal

Somente os canais de SMS, Push, Email e Correspondência direta são compatíveis com campanhas orquestradas.
