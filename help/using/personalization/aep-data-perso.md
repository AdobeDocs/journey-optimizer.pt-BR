---
solution: Journey Optimizer
product: journey optimizer
title: Usar dados da Adobe Experience Platform para personalização
description: Saiba como usar os dados do Adobe Experience Platform para personalização.
badge: label="Disponibilidade limitada" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Developer
level: Intermediate
keywords: expressão, editor
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
TQID: https://experienceleague.adobe.com/DRnUwE5hO6ysGY9D9NeqgAHESjd8HHsCpiHDeqHLiJo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: f0577040-fadd-46a1-b0ae-9c7f828bb2da
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1335
ht-degree: 3%

---

# Usar dados da Adobe Experience Platform para personalização {#aep-data}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como usar a função auxiliar datasetLookup no editor de personalização para recuperar campos dos conjuntos de dados de registro do Adobe Experience Platform e personalizar seu conteúdo.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>No momento, esse recurso está disponível para todos os clientes como uma versão de disponibilidade limitada.
>
>Por enquanto, a função auxiliar &quot;datasetLookup&quot; pode ser usada em fragmentos de expressão para um conjunto limitado de clientes. Para obter acesso, entre em contato com um representante da Adobe.

O Journey Optimizer permite aproveitar os dados dos conjuntos de dados de registros do Adobe Experience Platform no editor de personalização para [personalizar seu conteúdo](../personalization/personalize.md). Antes de iniciar, os conjuntos de dados necessários para a personalização da pesquisa devem ser habilitados primeiro para a pesquisa. Informações detalhadas estão disponíveis nesta seção: [Usar dados do Adobe Experience Platform](../data/lookup-aep-data.md).

Depois que um conjunto de dados é habilitado para personalização de pesquisa, você pode usar seus dados para personalizar seu conteúdo no [!DNL Journey Optimizer].

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
     >O valor inserido para este campo pode ser uma ID de campo (`profile.packages.packageSKU`), um campo passado em um evento de jornada (`context.journey.events.event_ID.productSKU`) ou um valor estático (`sku007653`). Em qualquer caso, o sistema usará o valor e pesquisará no conjunto de dados para verificar se ele corresponde a uma chave.
     >
     >Se estiver usando um valor de sequência literal para a chave, mantenha o texto entre aspas. Por exemplo: `{{datasetLookup datasetId="datasetId" id="SKU1234" result="store" required=false}}`. Se estiver usando um valor de atributo como uma chave dinâmica, remova as aspas. Por exemplo: `{{datasetLookup datasetId="datasetId" id=category.product.SKU result="SKU" required=false}}`

   * **resultado** é um nome arbitrário que você precisa fornecer para fazer referência a todos os valores de campo que você vai recuperar do conjunto de dados. Esse valor será usado no código para chamar cada campo.

   * **required=false**: se o valor required for definido como TRUE, a mensagem só será entregue se uma chave correspondente for encontrada. Se definido como false, uma chave correspondente não será necessária e a mensagem ainda poderá ser entregue. Observe que, se definido como falso, é recomendável levar em conta os valores de fallback ou padrão no conteúdo da mensagem.

   +++Onde recuperar uma ID de conjunto de dados?

   As IDs dos conjuntos de dados podem ser recuperadas na interface do usuário do Adobe Experience Platform. Saiba como trabalhar com conjuntos de dados na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}.

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
   >
   >Não há limites rígidos no número de campos que podem ser obtidos usando a função auxiliar. No entanto, para obter o melhor desempenho, é recomendável manter o número de campos abaixo de 50 para evitar impacto na taxa de transferência.

   * **resultado** é o valor atribuído ao parâmetro **resultado** na função auxiliar **datasetLookup**. Neste exemplo, &quot;voo&quot;.
   * **fieldID** é a identificação do campo que você deseja recuperar. Esta ID é visível na interface do usuário [!DNL Adobe Experience Platform] ao navegar pelo esquema de registro relacionado ao seu conjunto de dados:

     +++Onde recuperar uma ID de campo?

     As IDs de campos podem ser recuperadas ao visualizar um conjunto de dados na interface do usuário do Adobe Experience Platform. Saiba como visualizar conjuntos de dados na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}.

     ![](assets/aep-data-field.png)

     +++

   Neste exemplo, queremos usar informações relacionadas ao horário e ao portão de embarque dos passageiros. Portanto, adicionamos estas duas linhas:

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. Agora que o código está pronto, você pode concluir o conteúdo como de costume e testá-lo usando o método de simulação: clique em **[!UICONTROL Simular conteúdo]** para testar as variações de conteúdo com dados de entrada de exemplo ou geração automática de IA, ou clique em **[!UICONTROL Simular conteúdo]** e selecione **[!UICONTROL Simular conteúdo (perfis do AEP)]** na lista suspensa para visualizar com perfis de teste. [Saiba como visualizar e testar o conteúdo](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)

## Referência rápida {#quick-reference}

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

>[!BEGINTABS]

>[!TAB Visão geral]

**TL;DR**

Esta página ensina como usar a função auxiliar `datasetLookup` no editor de personalização do Journey Optimizer para recuperar campos de conjuntos de dados de registro do Adobe Experience Platform e incorporá-los à personalização de mensagens.

**Intenções**

* Ativar um conjunto de dados de registro do AEP para personalização de pesquisa
* Adicionar a função auxiliar `datasetLookup` a uma expressão de personalização
* Configure a função com uma ID de conjunto de dados, chave de junção, alias de resultado e sinalizador obrigatório
* Referência de campos de conjunto de dados recuperados em expressões de personalização usando o alias do resultado
* Testar conteúdo personalizado usando o fluxo de conteúdo Simular

>[!TAB Glossário]

* **datasetLookup**: uma função auxiliar no editor de personalização que recupera valores de campo de um conjunto de dados de registro do AEP ingressando em uma chave especificada. *(específico do produto)*
* **Conjunto de dados de registro**: um tipo de conjunto de dados do Adobe Experience Platform que contém dados de nível de registro que podem ser habilitados para personalização de pesquisa. *(específico do produto)*
* **Personalização da pesquisa**: o processo de buscar campos de um conjunto de dados de registro do AEP no momento do envio para personalizar o conteúdo da mensagem. *(específico do produto)*
* **parâmetro de resultado**: um alias arbitrário atribuído na chamada `datasetLookup`; usado para fazer referência a todos os valores de campo recuperados em expressões subsequentes (por exemplo, `{{result.fieldId}}`).
* **parâmetro obrigatório**: um sinalizador booleano em `datasetLookup` que controla se a entrega de mensagens requer que uma chave correspondente seja encontrada no conjunto de dados.

>[!TAB Terminologia]

* **Nome canônico:** datasetLookup — variantes: pesquisa de conjunto de dados, auxiliar de pesquisa de conjunto de dados, função auxiliar de pesquisa de conjunto de dados
* **Sinônimos:** &quot;datasetLookup&quot; = &quot;função auxiliar de pesquisa do conjunto de dados&quot;
* **Não confunda:** &quot;datasetId&quot; (identificador do conjunto de dados do AEP) ≠ &quot;id&quot; (a coluna de origem usada para unir com a identidade principal do conjunto de dados) ≠ &quot;result&quot; (o alias para referenciar valores de campos recuperados)

>[!TAB Medidas de proteção e limitações]

* O recurso está em Disponibilidade limitada — ainda não está disponível para todos os clientes.
* A função auxiliar `datasetLookup` nos fragmentos de expressão está disponível somente para um conjunto limitado de clientes; entre em contato com o representante da Adobe para obter acesso.
* Os conjuntos de dados devem ser habilitados explicitamente para personalização de pesquisa antes de serem usados com `datasetLookup`.
* Mantenha o número de campos recuperados por chamada `datasetLookup` abaixo de 50 para evitar impacto na taxa de transferência (limite recomendado — nenhum limite rígido é declarado na página).

>[!TAB Perguntas frequentes]

**P: Qual é a função auxiliar `datasetLookup`?**

É uma função auxiliar no editor de personalização que recupera valores de campo de conjuntos de dados de registro do Adobe Experience Platform, permitindo que você incorpore esses dados na personalização da mensagem.

**P: O que acontece se `required=false` e nenhuma chave correspondente for encontrada no conjunto de dados?**

A mensagem ainda poderá ser entregue. É recomendável considerar valores de fallback ou padrão no conteúdo da mensagem ao usar `required=false`.

**P: O que acontece se `required=true` e nenhuma chave correspondente for encontrada?**

A mensagem só será entregue se uma chave correspondente for encontrada no conjunto de dados.

**P: Onde encontro a ID do conjunto de dados e as IDs de campo necessárias para a sintaxe?**

As IDs dos conjuntos de dados podem ser recuperadas na interface do usuário do Adobe Experience Platform em Conjuntos de dados. As IDs de campo ficam visíveis ao visualizar um conjunto de dados e navegar pelo esquema de registro na interface do usuário do AEP.

**P: Como testar o conteúdo que usa o `datasetLookup`?**

Use o botão **Simular conteúdo** para testar com dados de entrada de exemplo ou geração automática de IA, ou selecione **Simular conteúdo (perfis do AEP)** na lista suspensa para visualizar com perfis de teste.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 89d99e47 -->
