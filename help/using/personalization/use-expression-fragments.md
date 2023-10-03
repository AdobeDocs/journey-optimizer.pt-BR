---
solution: Journey Optimizer
product: journey optimizer
title: Usar fragmentos de expressão
description: Saiba como usar fragmentos de expressão no [!DNL Journey Optimizer] Editor de expressão.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor, biblioteca, personalização
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: dd463d36550b53faaffca90691550278498c862a
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Aproveitar fragmentos de expressão {#use-expression-fragments}

Ao usar o editor de expressão, você pode aproveitar todos os fragmentos de expressão que foram criados ou salvos na sandbox atual.

>[!NOTE]
>
>Saiba como criar e gerenciar fragmentos no [nesta seção](../content-management/fragments.md).

➡️ [Saiba como gerenciar, criar e usar fragmentos neste vídeo](../content-management/fragments.md#video-fragments)

## Usar um fragmento de expressão {#use-expression-fragment}

Para adicionar fragmentos de expressão ao seu conteúdo, siga as etapas abaixo.

1. Abra o [Editor de expressão](personalization-build-expressions.md) e selecione o **[!UICONTROL Fragmentos]** no painel esquerdo.

   ![](assets/expression-fragments-pane.png)

   A lista exibe todos os fragmentos de expressão criados ou salvos como fragmentos na sandbox atual. [Saiba mais](../content-management/fragments.md#create-expression-fragment)

   >[!NOTE]
   >
   >Os fragmentos são classificados por data de criação: os fragmentos de expressão adicionados recentemente são mostrados primeiro na lista.

1. Você também pode atualizar a lista.

   >[!NOTE]
   >
   >Se alguns fragmentos foram modificados ou adicionados enquanto você está editando o conteúdo, a lista será atualizada com as alterações mais recentes.

1. Clique no ícone + ao lado de um fragmento de expressão para inserir a ID do fragmento correspondente no editor.

   ![](assets/expression-fragment-add.png)

   Depois que a ID do fragmento for adicionada, se você abrir o fragmento de expressão correspondente e [editá-lo](../content-management/fragments.md#edit-fragments) na interface do, as alterações são sincronizadas. Eles são propagados automaticamente para todos **[!UICONTROL Rascunho]** jornadas/campanhas contendo essa ID de fragmento.

   >[!NOTE]
   >
   >As alterações não são propagadas para o conteúdo usado no **[!UICONTROL Ao vivo]** jornadas ou campanhas.

1. Clique em **[!UICONTROL Mais ações]** botão ao lado de um fragmento.

1. No menu contextual aberto, selecione **[!UICONTROL Exibir fragmento]** para obter mais informações sobre esse fragmento. A variável **[!UICONTROL ID do fragmento]** também é exibido e pode ser copiado daqui.

   ![](assets/expression-fragment-view.png)

1. É possível abrir o fragmento da expressão em outra janela para editar seu conteúdo e propriedades, usando o **[!UICONTROL Abrir fragmento]** no menu contextual ou na variável **[!UICONTROL Informações do fragmento]** painel. [Saiba como editar um fragmento](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. Em seguida, você pode personalizar e validar o conteúdo como de costume, usando todos os recursos de personalização e criação do [Editor de expressão](personalization-build-expressions.md).

## Interromper herança {#break-inheritance}

Ao adicionar uma ID de fragmento ao editor de expressão, as alterações feitas no fragmento de expressão original são sincronizadas.

No entanto, também é possível colar o conteúdo de um fragmento de expressão no editor. No menu contextual, selecione **[!UICONTROL Colar fragmento]** para inserir esse conteúdo.

![](assets/expression-fragment-paste.png)

Nesse caso, a herança do fragmento original é quebrada. O conteúdo do fragmento é copiado para o editor e as alterações não são mais sincronizadas.

Ele se torna um elemento independente que não está mais vinculado ao fragmento original; você pode editá-lo como qualquer outro elemento no seu código.

<!--
TO REPLACE WITH UPDATED VIDEO ON EXPRESSION FRAGMENTS
## How-to video{#video}

Learn how to use saved personalization library items in a message and how to create and manage personalization library items.

>[!VIDEO](https://video.tv.adobe.com/v/340941?quality=12)
-->

