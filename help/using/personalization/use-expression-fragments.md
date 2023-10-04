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
source-git-commit: 4d74588b5df0afab7e56e540703891c48a94ab5f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Aproveitar fragmentos de expressão {#use-expression-fragments}

Ao usar o editor de expressão, você pode aproveitar todos os fragmentos de expressão que foram criados ou salvos na sandbox atual.

Saiba como criar e gerenciar fragmentos no [nesta seção](../content-management/fragments.md).

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

>[!NOTE]
>
>Se você criar um fragmento de expressão que contenha várias quebras de linha e usá-lo no [SMS](usi..ng/sms/create-sms.md#sms-content) ou [push](../push/design-push.md) conteúdo, as quebras de linha são preservadas. Assim, pré-visualize e teste seu [SMS](../sms/send-sms.md) ou [push](../push/send-push.md) antes de enviá-la.

## Interromper herança {#break-inheritance}

Ao adicionar uma ID de fragmento ao editor de expressão, as alterações feitas no fragmento de expressão original são sincronizadas.

No entanto, também é possível colar o conteúdo de um fragmento de expressão no editor. No menu contextual, selecione **[!UICONTROL Colar fragmento]** para inserir esse conteúdo.

![](assets/expression-fragment-paste.png)

Nesse caso, a herança do fragmento original é quebrada. O conteúdo do fragmento é copiado para o editor e as alterações não são mais sincronizadas.

Ele se torna um elemento independente que não está mais vinculado ao fragmento original; você pode editá-lo como qualquer outro elemento no seu código.

