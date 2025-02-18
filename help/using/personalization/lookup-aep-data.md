---
solution: Journey Optimizer
product: journey optimizer
title: Usar dados da Adobe Experience Platform para personalização (Beta)
description: Saiba como usar os dados do Adobe Experience Platform para personalização.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: f41426bd41078b98a26c32ce259a848ab49d724c
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 2%

---

# Usar dados da Adobe Experience Platform para personalização{#aep-data}

>[!AVAILABILITY]
>
>No momento, esse recurso está disponível para todos os clientes como um beta público.
>
>Para usar esse recurso, primeiro você deve aceitar os termos beta para sua organização exibidos ao adicionar as novas funções auxiliares &quot;datasetLookup&quot; no editor de personalização.

O Journey Optimizer permite aproveitar os dados do Adobe Experience Platform no editor de personalização para [personalizar seu conteúdo](../personalization/personalize.md). Para fazer isso, os conjuntos de dados necessários para a personalização da pesquisa devem ser habilitados primeiro por meio de uma chamada de API, conforme descrito abaixo. Depois de concluído, você poderá usar os dados para personalizar o conteúdo no [!DNL Journey Optimizer].

## Restrições e diretrizes do Beta {#guidelines}

Antes de começar, reveja as seguintes restrições e diretrizes:

### Ativação de conjuntos de dados {#enablement}

* O **tamanho do conjunto de dados** é limitado a 5 GB para conjuntos de dados de produção e 1 GB para conjuntos de dados de sandbox dev
* **No máximo 50 conjuntos de dados podem ser habilitados** para pesquisa por organização a qualquer momento.
* **O número de registros** está restrito a 5 milhões em conjuntos de dados de produção e 1 milhão em conjuntos de dados de sandbox de desenvolvimento.
* **Rotulagem e Imposição de Uso de Dados** não é imposta no momento para conjuntos de dados habilitados para pesquisa.
* **Os conjuntos de dados habilitados para pesquisa e usados na personalização não estão protegidos contra exclusão**. Cabe a você acompanhar quais conjuntos de dados estão sendo usados para personalização para garantir que eles não sejam excluídos ou removidos.

### Personalization usando dados do [!DNL Adobe Experience Platform] {#perso}

* **Canais com suporte**: por enquanto, esse recurso só está disponível para uso em canais de email, SMS e correspondência direta.
* **Rotulagem e Imposição de Uso de Dados** não é imposta no momento para conjuntos de dados habilitados para pesquisa.
* **Fragmentos de expressão**: no momento, a personalização da pesquisa do conjunto de dados não pode ser colocada dentro dos fragmentos de expressão.

## Ativar um conjunto de dados para pesquisa de dados {#enable}

Para aproveitar os dados do conjunto de dados para personalização, é necessário usar uma chamada de API para recuperar o status e habilitar o serviço de pesquisa.

### Pré-requisitos {#prerequisites-enable}

* Siga as instruções detalhadas em [esta documentação](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) para configurar seu ambiente para enviar comandos de API.
* O projeto do desenvolvedor deve ter as APIs do Adobe Journey Optimizer e do Adobe Experience Platform adicionadas ao projeto.

  ![](assets/aep-data-api.png)

* Você deve ter permissão de gerenciamento de conjuntos de dados como parte de sua função.
* O esquema no qual o conjunto de dados se baseia deve conter uma **identidade primária** que possa atuar como a chave de pesquisa.

### Estrutura de chamada da API {#call}

```
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}"
```

Em que:

* **A URL** é `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* **ID do Conjunto de Dados** é o conjunto de dados para o qual você deseja habilitar.
* **A ação** está habilitada OU desabilitada.
* O **token de acesso** pode ser recuperado do console do desenvolvedor.
* A **chave de API** pode ser recuperada do console do desenvolvedor.
* **ID da Organização IMS** é sua organização da Adobe.
* **Nome da sandbox** é o nome da sandbox em que o conjunto de dados está (ou seja, prod, dev etc.).

>[!NOTE]
>
>Se você encontrar o erro abaixo ao tentar fazer uma chamada de API para habilitar conjuntos de dados, tente remover as APIs do Adobe Journey Optimizer do projeto do console do desenvolvedor e adicioná-las novamente.
>
>```
>
>"error_code": "403003", 
>"message": "Api Key is invalid"
>
>```

## Aproveitar um conjunto de dados para personalização {#leverage}

Depois que um conjunto de dados for habilitado para personalização de pesquisa usando uma chamada de API, você poderá usar seus dados para personalizar seu conteúdo no [!DNL Journey Optimizer].

1. Abra o editor de personalização, que está disponível em todos os contextos, onde é possível definir personalização, como mensagens. [Saiba como trabalhar com o editor de personalização](../personalization/personalization-build-expressions.md)

1. Navegue até a lista de funções auxiliares e adicione a função auxiliar **datasetLookup** ao painel de código.

   ![](assets/aep-data-helper.png)

1. Essa função fornece uma sintaxe predefinida para permitir que você chame campos a partir de conjuntos de dados da Adobe Experience Platform. A sintaxe é a seguinte:

   ```
   {{datasetLookup datasetId="datasetId" id="key" result="store" required=false}}
   ```

   * **datasetId** é a ID do conjunto de dados com o qual você está trabalhando.
   * **id** é a identificação da coluna de origem que deve ser unida à identidade primária do conjunto de dados de pesquisa.

     >[!NOTE]
     >
     >O valor inserido para este campo pode ser uma ID de campo (*profile.packages.packageSKU*), um campo passado em um evento de jornada (*context.jornada.events.event_ID.productSKU*) ou um valor estático (*sku007653*). Em qualquer caso, o sistema usará o valor e pesquisará no conjunto de dados para verificar se ele corresponde a uma chave.
     >
     >Se estiver usando um valor de sequência literal para a chave, mantenha o texto entre aspas. Por exemplo: `{{datasetLookup datasetId="datasetId" id="SKU1234" result="store" required=false}}`. Se estiver usando um valor de atributo como uma chave dinâmica, remova as aspas. Por exemplo: `{{datasetLookup datasetId="datasetId" id=category.product.SKU result="SKU" required=false}}`

   * **resultado** é um nome arbitrário que você precisa fornecer para fazer referência a todos os valores de campo que você vai recuperar do conjunto de dados. Esse valor será usado no código para chamar cada campo.

   * **required=false**: se o valor required for definido como TRUE, a mensagem só será entregue se uma chave correspondente for encontrada. Se definido como false, uma chave correspondente não será necessária e a mensagem ainda poderá ser entregue. Observe que, se definido como falso, é recomendável levar em conta os valores de fallback ou padrão no conteúdo da mensagem.

   +++Onde recuperar uma ID de conjunto de dados?

   As IDs dos conjuntos de dados podem ser recuperadas na interface do usuário do Adobe Experience Platform. Saiba como trabalhar com conjuntos de dados na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}.

   ![](assets/aep-data-dataset.png)

+++

1. Adapte a sintaxe de acordo com suas necessidades. Neste exemplo, queremos recuperar dados relacionados aos voos dos passageiros. A sintaxe é a seguinte:

   ```
   {{datasetLookup datasetId="1234567890abcdtId" id=profile.upcomingFlightId result="flight"}}
   ```

   * Estamos trabalhando no conjunto de dados cuja ID é &quot;1234567890abcdtId&quot;,
   * O campo que queremos usar para fazer uma associação com o conjunto de dados de pesquisa é *profile.comingFlightId*,
   * Queremos incluir todos os valores de campo sob a referência &quot;flight&quot;.

1. Depois que a sintaxe a ser chamada no conjunto de dados do Adobe Experience Platform for configurada, você poderá especificar quais campos deseja recuperar. A sintaxe é a seguinte:

   ```
   {{result.fieldId}}
   ```

   >[!NOTE]
   >
   >Ao referenciar um campo do conjunto de dados, verifique se você corresponde ao caminho de campo completo, conforme definido no esquema.

   * **resultado** é o valor atribuído ao parâmetro **resultado** na função auxiliar **MultiEntity**. Neste exemplo, &quot;voo&quot;.
   * **fieldID** é a identificação do campo que você deseja recuperar. Esta ID é visível na interface do usuário [!DNL Adobe Experience Platform] ao navegar pelo esquema de registro relacionado ao seu conjunto de dados:

     +++Onde recuperar uma ID de campo?

     As IDs de campos podem ser recuperadas ao visualizar um conjunto de dados na interface do usuário do Adobe Experience Platform. Saiba como visualizar conjuntos de dados na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}.

     ![](assets/aep-data-field.png)

+++

   Neste exemplo, queremos usar informações relacionadas ao horário e ao portão de embarque dos passageiros. Portanto, adicionamos estas duas linhas:

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. Agora que o código está pronto, você pode concluir o conteúdo como de costume e testá-lo usando o botão **Simular conteúdo** para verificar a personalização. [Saiba como visualizar e testar o conteúdo](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
