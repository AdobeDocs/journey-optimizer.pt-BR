---
solution: Journey Optimizer
product: journey optimizer
title: Usar dados do Adobe Experience Platform para personalização (beta)
description: Saiba como usar os dados do Adobe Experience Platform para personalização.
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor
hidefromtoc: true
hide: true
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: a03541b5f1d9c799c30bf1d38b6f187d94c21dff
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---

# Usar dados do Adobe Experience Platform para personalização (beta) {#aep-data}

>[!AVAILABILITY]
>
>No momento, esse recurso está disponível apenas como um beta privado.
>
>Por enquanto, ele só está disponível para o **canal de email** e para fins de teste na sandbox de não produção fornecida para o Adobe e para os conjuntos de dados solicitados para o beta.

O Journey Optimizer permite aproveitar os dados do Adobe Experience Platform no editor de personalização para [personalizar seu conteúdo](../personalization/personalize.md). As etapas são as seguintes:

1. Abra o editor de personalização, que está disponível em todos os contextos, onde é possível definir personalização, como mensagens. [Saiba como trabalhar com o editor de personalização](../personalization/personalization-build-expressions.md)

1. Navegue até a lista de funções auxiliares e adicione a função auxiliar **datasetLookup** ao painel de código.

   ![](assets/aep-data-helper.png)

1. Essa função fornece uma sintaxe predefinida para permitir que você chame campos a partir de conjuntos de dados da Adobe Experience Platform. A sintaxe é a seguinte:

   ```
   {{entity.datasetId="datasetId" id="key" result="store"}}
   ```

   * **entity.datasetId** é a ID do conjunto de dados com o qual você está trabalhando.
   * **id** é a identificação da coluna de origem que deve ser unida à identidade primária do conjunto de dados de pesquisa.

     >[!NOTE]
     >
     >O valor inserido para este campo pode ser uma ID de campo (*profile.couponValue*), um campo passado em um evento de jornada (*context.jornada.events.event_ID.couponValue*) ou um valor estático (*couponAbcd*). Em qualquer caso, o sistema usará o valor e pesquisará no conjunto de dados para verificar se ele corresponde a uma chave.

   * **resultado** é um nome arbitrário que você precisa fornecer para fazer referência a todos os valores de campo que você vai recuperar do conjunto de dados. Esse valor será usado no código para chamar cada campo.

   +++Onde recuperar uma ID de conjunto de dados?

   As IDs dos conjuntos de dados podem ser recuperadas na interface do usuário do Adobe Experience Platform. Saiba como trabalhar com conjuntos de dados na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}.

   ![](assets/aep-data-dataset.png)

+++

1. Adapte a sintaxe de acordo com suas necessidades. Neste exemplo, queremos recuperar dados relacionados aos voos dos passageiros. A sintaxe é a seguinte:

   ```
   {{entity.datasetId="1234567890abcdtId" id=profile.upcomingFlightId result="flight"}}
   ```

   * Estamos trabalhando no conjunto de dados cuja ID é &quot;1234567890abcdtId&quot;,
   * O campo que queremos usar para fazer uma associação com o conjunto de dados de pesquisa é *profile.comingFlightId*,
   * Queremos incluir todos os valores de campo sob a referência &quot;flight&quot;.

1. Depois que a sintaxe a ser chamada no conjunto de dados do Adobe Experience Platform for configurada, você poderá especificar quais campos deseja recuperar. A sintaxe é a seguinte:

   ```
   {{result.fieldId}}
   ```

   * **resultado** é o valor atribuído ao parâmetro **resultado** na função auxiliar **MultiEntity**. Neste exemplo, &quot;voo&quot;.
   * **fieldID** é a identificação do campo que você deseja recuperar. Essa ID é visível na interface do usuário do Adobe Experience Platform ao navegar no conjunto de dados. Expanda a seção abaixo para exibir um exemplo:

     +++Onde recuperar uma ID de campo?

     As IDs de campos podem ser recuperadas ao visualizar um conjunto de dados na interface do usuário do Adobe Experience Platform. Saiba como visualizar conjuntos de dados na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}.

     ![](assets/aep-data-field.png)

+++

   Neste exemplo, queremos usar informações relacionadas ao horário e ao portão de embarque dos passageiros. Portanto, adicionamos estas duas linhas:

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. Agora que o código está pronto, você pode concluir o conteúdo como de costume e testá-lo usando o botão **Simular conteúdo** para verificar a personalização. [Saiba como visualizar e testar o conteúdo](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
