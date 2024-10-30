---
solution: Journey Optimizer
product: journey optimizer
title: Criar condições
description: Saiba como criar condições
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor, condicional, regras
exl-id: 246a4a55-059e-462c-ac1e-43b90f4abda4
source-git-commit: 6f9bdb179f2bfff30494495b68a15aaac77d6b9e
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 9%

---

# Trabalhar com regras condicionais {#conditions}

As regras condicionais são conjuntos de regras que definem qual conteúdo deve ser exibido em suas mensagens, dependendo de vários critérios, como atributos de perfis, associação de público-alvo ou eventos contextuais.

As regras condicionais são criadas usando o editor de personalização e podem ser armazenadas se você quiser reutilizá-las no conteúdo. [Saiba como salvar uma regra condicional na biblioteca](#save)

>[!NOTE]
>
>As pessoas precisarão da permissão [Gerenciar itens de biblioteca](../administration/ootb-product-profiles.md) para salvar ou excluir regras condicionais. As condições salvas estão disponíveis para uso por todos os usuários em uma organização.

## Acessar o construtor de regras condicionais {#access}

As regras condicionais são criadas no menu **[!UICONTROL Condições]**, no editor de personalização, que pode ser acessado:

* No Designer de email, ao ativar o conteúdo dinâmico para um componente no corpo do email. [Saiba como adicionar conteúdo dinâmico a emails](dynamic-content.md#emails)

  ![](assets/conditions-access-email.png)

* Em qualquer campo onde você possa adicionar personalização usando o [editor de personalização](personalization-build-expressions.md).

  ![](assets/conditions-access-editor.png)

## Criar uma regra condicional {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="Criar condição"
>abstract="Combine atributos de perfil, eventos contextuais ou públicos para criar regras que definem qual conteúdo deve ser exibido nas mensagens."

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="Criar condição"
>abstract="Combine atributos de perfil, eventos contextuais ou públicos para criar regras que definem qual conteúdo deve ser exibido nas mensagens."

As etapas para criar uma regra condicional são as seguintes:

1. Acesse o menu **[!UICONTROL Condições]** do editor de personalização ou do Designer de email e clique em **[!UICONTROL Criar novo]**.

1. Crie a regra condicional de acordo com suas necessidades. Para fazer isso, arraste e solte e organize os atributos desejados do menu esquerdo na tela de desenho.

   As etapas para combinar atributos na tela são semelhantes à experiência de construção de segmentos. Para obter mais informações sobre como trabalhar com a tela do construtor de regras, consulte [esta documentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#rule-builder-canvas).

   ![](assets/conditions-create.png)

   Os atributos são organizados em três guias:

   * **[!UICONTROL Perfil]**:
      * **[!UICONTROL Públicos-alvo]** lista todos os atributos de público-alvo (ou seja, status, versão etc.) para o [serviço de Segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR),
      * **[!UICONTROL Perfis individuais XDM]** lista todos os atributos de perfil associados ao [esquema do Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR) definido no Adobe Experience Platform.
   * **[!UICONTROL Contextual]**: quando a mensagem é usada em uma jornada, os campos de jornada contextual ficam disponíveis por meio desta guia.
   * **[!UICONTROL Públicos-alvo]**: lista todos os públicos-alvo gerados pelas definições de segmento criadas no [serviço de Segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR).

1. Quando a regra condicional estiver pronta, você poderá adicioná-la à mensagem para criar conteúdo dinâmico. [Saiba como adicionar conteúdo dinâmico](dynamic-content.md)

   Você também pode salvar a regra para permitir mais reutilização. [Saiba como salvar uma condição](#save)

## Salvar uma regra condicional {#save}

Se houver regras de condição que serão reutilizadas com frequência, salve-as na biblioteca de condições. Todas as regras salvas são compartilhadas e podem ser acessadas e usadas por indivíduos em sua organização.

>[!NOTE]
>
>Regras condicionais que usam atributos contextuais do jornada não podem ser salvas na biblioteca.

1. Na tela de edição de condição, clique no botão **[!UICONTROL Salvar condição]**.

1. Dê um nome e uma descrição (opcional) à regra e clique em **[!UICONTROL Adicionar]**.

   ![](assets/conditions-name-description.png)

1. A regra condicional é salva na biblioteca. Agora você pode usá-lo para criar conteúdo dinâmico em suas mensagens. [Saiba como adicionar conteúdo dinâmico](dynamic-content.md)

## Editar e excluir regras condicionais salvas {#edit-delete}

É possível excluir uma regra condicional a qualquer momento usando o botão de reticências.

![](assets/conditions-open.png)

Regras condicionais salvas na biblioteca não podem ser modificadas. No entanto, você ainda pode usá-las para criar novas regras. Para fazer isso, abra a regra condicional, faça as alterações desejadas e salve-a na biblioteca. [Saiba como salvar uma condição na biblioteca](#save)
