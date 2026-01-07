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
hidefromtoc: true
source-git-commit: 5a1a356d6bf0dbd5290b2cf8257d87aa7db43b5b
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 5%

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
>Continue somente se entender totalmente os impactos nas jornadas e campanhas que fazem referência ao fragmento. [Saiba mais](#limitations)

1. Navegue até **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Fragmentos]**.

1. Selecione o fragmento publicado e clique em **[!UICONTROL Modificar]** para criar uma versão de rascunho.

   ![](assets/fragment-live-modify.png){width="70%" align="left"}

1. Clique em **[!UICONTROL Editar]** para abrir o editor de conteúdo do fragmento.

1. Alterne para o **[!UICONTROL Editor de código]** ou o **[!UICONTROL Modo avançado]** no editor de personalização.

1. Digite ou copie e cole manualmente o atributo contextual usando a sintaxe:

   ```
   {{context.attribute_name}}
   ```

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

