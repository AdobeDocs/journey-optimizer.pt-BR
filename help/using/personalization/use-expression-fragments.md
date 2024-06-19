---
solution: Journey Optimizer
product: journey optimizer
title: Usar fragmentos de expressão
description: Saiba como usar fragmentos de expressão no [!DNL Journey Optimizer] editor de personalização.
feature: Personalization, Fragments
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor, biblioteca, personalização
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: 893f7146b358da48153b1e6bc74b8f622028df76
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 0%

---

# Aproveitar fragmentos de expressão {#use-expression-fragments}

Ao usar o **editor de personalização**, você pode aproveitar todos os fragmentos de expressão que foram criados ou salvos na sandbox atual.

Um fragmento é um componente reutilizável que pode ser referenciado em [!DNL Journey Optimizer] campanhas e jornadas. Essa funcionalidade permite pré-construir vários blocos de conteúdo personalizado que podem ser usados por usuários de marketing para reunir conteúdo rapidamente em um processo de design aprimorado. [Saiba como criar e gerenciar fragmentos](../content-management/fragments.md).

➡️ [Saiba como gerenciar, criar e usar fragmentos neste vídeo](../content-management/fragments.md#video-fragments)

## Usar um fragmento de expressão {#use-expression-fragment}

Para adicionar fragmentos de expressão ao seu conteúdo, siga as etapas abaixo.

>[!NOTE]
>
>Você pode adicionar até 30 fragmentos em um determinado delivery. Os fragmentos só podem ser aninhados até um nível.

1. Abra o [editor de personalização](personalization-build-expressions.md) e selecione o **[!UICONTROL Fragmentos]** no painel esquerdo.

   A lista exibe todos os fragmentos de expressão criados ou salvos como fragmentos na sandbox atual. Eles são classificados por data de criação: os fragmentos de expressão adicionados recentemente são mostrados primeiro na lista. [Saiba mais](../content-management/fragments.md#create-expression-fragment)

   ![](assets/expression-fragments-pane.png)

   Você também pode atualizar esta lista.

   >[!NOTE]
   >
   >Se alguns fragmentos foram modificados ou adicionados enquanto você está editando o conteúdo, a lista será atualizada com as alterações mais recentes.

1. Clique no ícone + ao lado de um fragmento de expressão para inserir a ID do fragmento correspondente no editor.

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >É possível adicionar qualquer **Rascunho** ou **Ao vivo** fragmento ao seu conteúdo. No entanto, você não poderá ativar sua jornada ou campanha se um fragmento com o status Rascunho estiver sendo usado nele. Na publicação do jornada ou da campanha, os fragmentos de rascunho mostrarão um erro e você precisará aprová-los para poder publicar.
   >
   > Observe que os status dos fragmentos estão sendo implantados gradualmente durante vários dias após a versão de junho do Journey Optimizer. Embora alguns usuários tenham acesso imediato, outros podem enfrentar um atraso antes que ele se torne disponível em seus ambientes. Se esse aprimoramento ainda não estiver disponível em seu ambiente, observe que o fragmento não precisa ser **Ao vivo** para ser usado em suas jornadas e campanhas.

1. Depois que a ID do fragmento for adicionada, se você abrir o fragmento de expressão correspondente e [editá-lo](../content-management/fragments.md#edit-fragments) na interface do, as alterações são sincronizadas. Eles são propagados automaticamente para todas as jornadas/campanhas de rascunho ou ativas que contêm essa ID de fragmento.

1. Clique em **[!UICONTROL Mais ações]** botão ao lado de um fragmento. No menu contextual aberto, selecione **[!UICONTROL Exibir fragmento]** para obter mais informações sobre esse fragmento. A variável **[!UICONTROL ID do fragmento]** também é exibido e pode ser copiado daqui.

   ![](assets/expression-fragment-view.png)

1. É possível abrir o fragmento da expressão em outra janela para editar seu conteúdo e propriedades, usando o **[!UICONTROL Abrir fragmento]** no menu contextual ou na variável **[!UICONTROL Informações do fragmento]** painel. [Saiba como editar um fragmento](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. Em seguida, você pode personalizar e validar o conteúdo como de costume, usando todos os recursos de personalização e criação do [editor de personalização](personalization-build-expressions.md).

>[!NOTE]
>
>Se você criar um fragmento de expressão que contenha várias quebras de linha e usá-lo no [SMS](../sms/create-sms.md#sms-content) ou [push](../push/design-push.md) conteúdo, as quebras de linha são preservadas. Assim, certifique-se de testar seu [SMS](../sms/send-sms.md) ou [push](../push/send-push.md) antes de enviá-la.

## Interromper herança {#break-inheritance}

Ao adicionar uma ID de fragmento ao editor de personalização, as alterações feitas no fragmento de expressão original são sincronizadas.

No entanto, também é possível colar o conteúdo de um fragmento de expressão no editor. No menu contextual, selecione **[!UICONTROL Colar fragmento]** para inserir esse conteúdo.

![](assets/expression-fragment-paste.png)

Nesse caso, a herança do fragmento original é quebrada. O conteúdo do fragmento é copiado para o editor e as alterações não são mais sincronizadas.

Ele se torna um elemento independente que não está mais vinculado ao fragmento original; você pode editá-lo como qualquer outro elemento no seu código.

