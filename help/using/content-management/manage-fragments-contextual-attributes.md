---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar atributos contextuais aos fragmentos publicados
description: Saiba como adicionar atributos contextuais aos fragmentos publicados (disponibilidade limitada)
feature: Fragments
topic: Content Management
role: User
level: Intermediate, Experienced
hide: true
exl-id: a274656e-2570-4a9c-b72b-4e8e920b7462
TQID: https://experienceleague.adobe.com/yweu8QtcWU42ZI2z93vIf5-LUGP7pQ16bJUQnmDKNGY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 363
ht-degree: 8%

---

# Adicionar atributos contextuais aos fragmentos publicados {#adding-contextual-attributes}

>[!AVAILABILITY]
>
>Esse recurso só está disponível para clientes selecionados e envolve riscos significativos. Confirme com seu representante da Adobe se esse recurso está ativado para sua organização.

Por padrão, não há suporte para adicionar novos [atributos de personalização](../personalization/personalization-build-expressions.md) a um fragmento publicado. Depois que um fragmento é publicado, o conjunto de atributos de perfil ou contextuais é bloqueado para todas as campanhas e jornadas.

No entanto, para clientes selecionados, é possível adicionar **atributos contextuais** somente aos fragmentos publicados.

>[!WARNING]
>
>Ao adicionar atributos de personalização a um fragmento publicado, o processo de validação é menos rigoroso e podem não ser detectados erros. Isso pode causar quebras não intencionais em jornadas e campanhas usando esse fragmento em escala.

## Medidas de proteção e limitações {#limitations}

* Verifique se todas as jornadas e campanhas que atualmente usam o fragmento podem lidar com os novos atributos contextuais.
* Os atributos de perfil não podem ser adicionados aos fragmentos publicados. Somente atributos contextuais são suportados.
* Os atributos contextuais devem ser inseridos manualmente no editor de código, não podendo ser selecionados na interface do editor de personalização.
* Ao adicionar atributos personalizados a fragmentos ativos, as validações são atenuadas, o que significa que os erros podem não ser detectados e podem causar quebras não intencionais em escala.
* Depois de publicado, todos os erros afetarão imediatamente todas as comunicações usando esse fragmento.

## Adicionar atributos contextuais {#add-contextual-attributes}

Para adicionar atributos contextuais a um fragmento publicado, siga as etapas abaixo.

>[!IMPORTANT]
>
>Continue somente se você [entender totalmente os impactos](#limitations) nas jornadas e campanhas que fazem referência ao fragmento.

1. Navegue até **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Fragmentos]**.

1. Selecione o fragmento publicado e clique em **[!UICONTROL Modificar]** para criar uma versão de rascunho.

   ![](assets/fragment-live-modify.png){width="70%" align="left"}

1. Clique em **[!UICONTROL Editar]** para abrir o editor de conteúdo do fragmento.

1. Alterne para o **[!UICONTROL Editor de código]** ou o **[!UICONTROL Modo avançado]** no editor de personalização.

1. Digite ou copie e cole manualmente o atributo contextual usando a sintaxe `{{context.attribute_name}}`:

   Exemplo para um atributo `promotionCode`:

   ```
   {{context.promotionCode}}
   ```

   >[!CAUTION]
   >
   >Verifique novamente a precisão do caminho do atributo. Erros podem não ser detectados e podem interromper as comunicações do jornada ou da campanha em escala.

1. Salve as alterações.

1. Depois de confirmado, clique em **[!UICONTROL Publicar]** para ativar as alterações.

>[!NOTE]
>Para evitar interrupções não intencionais em jornadas e campanhas, você pode testar os caminhos de atributos contextuais em um ambiente de não produção.

## Tópicos relacionados {#related-topics}

* [Gerenciar fragmentos](manage-fragments.md)
* [Editar um fragmento](manage-fragments.md#edit-fragments)
* [Campanhas acionadas por API](../campaigns/api-triggered-campaigns.md)
* [Sintaxe de personalização](../personalization/personalization-syntax.md)
