---
title: Usar políticas de decisão em mensagens
description: Saiba como usar políticas de decisão em suas mensagens.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
version: Journey Orchestration
exl-id: 35fc3cf2-1b91-4f30-ad71-f9d7d2a0291c
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 3%

---

# Usar políticas de decisão em mensagens {#create-decision}

Depois de adicionar uma política de decisão ao conteúdo, você pode usar atributos de itens de decisão retornados para personalização. Para fazer isso, primeiro insira o código da política de decisão no seu conteúdo.

>[!CAUTION]
>
>As políticas de decisão estão disponíveis a todos os clientes para os canais **Experiência baseada em código**, **SMS**, **Notificação por push** e **Email**.

## Inserir o código de política de decisão {#insert}

>[!BEGINTABS]

>[!TAB Experiência baseada em código]

1. Edite sua experiência baseada em código e navegue até a **[!UICONTROL Política de decisão]**.

2. Selecione **[!UICONTROL Inserir política]** para adicionar o código de política de decisão.

   ![](assets/decision-code-based-add-decision.png)

>[!NOTE]
>
>Para experiências baseadas em código, se a política de decisão contiver itens de decisão, incluindo fragmentos, você poderá aproveitar esses fragmentos no código de política de decisão. [Saiba como aproveitar fragmentos](fragments-decision-policies.md)

>[!TAB Email]

1. Abra o **Editor do Personalization** e navegue até **[!UICONTROL Políticas de decisão]**.

2. Selecione **[!UICONTROL Inserir sintaxe]** para adicionar o código da política de decisão.

   ![](assets/decision-policy-add.png)

   >[!NOTE]
   >
   >Se a opção de inserção não for exibida, talvez uma política de decisão já esteja configurada para o componente principal.

3. Se nenhum posicionamento tiver sido atribuído ainda ao componente, selecione um na lista e clique em **[!UICONTROL Atribuir]**.

   ![](assets/decision-policy-placement.png)

   >[!NOTE]
   >
   >Se você usar várias políticas de decisão no mesmo email (por exemplo, uma para o cabeçalho e outra para o rodapé), a mesma oferta será desduplicada entre os posicionamentos: não é renderizada duas vezes. A segunda política de decisão não retornará nenhum conteúdo e exibirá um espaço em branco, a menos que você tenha configurado uma oferta de fallback, nesse caso, o fallback será exibido.

>[!TAB SMS]

1. Abra o **Editor do Personalization** e navegue até **[!UICONTROL Políticas de decisão]**.

2. Selecione **[!UICONTROL Inserir sintaxe]** para adicionar o código da política de decisão.

   ![](assets/decision-policy-add-sms-insert-syntax.png)

>[!TAB Push]

1. Abra o **Editor do Personalization** e navegue até **[!UICONTROL Políticas de decisão]**.

2. Selecione **[!UICONTROL Inserir sintaxe]** para adicionar o código da política de decisão.

   ![](assets/decision-policy-add-push-insert-syntax.png)

>[!IMPORTANT]
>
>O Experience Decisioning com notificações por push requer uma versão específica do Mobile SDK. Antes de implementar este recurso, verifique as [notas de versão](https://developer.adobe.com/client-sdks/home/release-notes){target="_blank"} para identificar a versão necessária e se você atualizou adequadamente. Você também pode exibir todas as versões do SDK disponíveis para sua plataforma [nesta seção](https://developer.adobe.com/client-sdks/home/current-sdk-versions){target="_blank"}.

>[!ENDTABS]

The decision policy code is added. You can now use attributes from the returned decision items to personalize your content.

>[!NOTE]
>
>For code-based experience and email channels, repeat this sequence once per decision item you want returned. For example, if you chose to return 2 items when [creating the decision](create-decision-policy.md), repeat the sequence twice. For SMS and Push channels, only one decision item can be returned.

## Personalize with decision item attributes {#attributes}

After you&#39;ve added the code for a decision policy in your content, all attributes from the returned decision items become available for personalization. [Learn how to work with personalization](../personalization/personalize.md).

Attributes are stored in the &quot;Offers&quot; [catalog schema](catalogs.md). They display in the following folders from the personalization editor:
* **Custom attributes**: `_\<imsOrg\>` folder
* **Standard attributes**: `_experience` folder

Decision item attributes and contextual attributes are not supported by default in [!DNL Journey Optimizer] fragments. However, you can use global variables instead, such as described below.

![](assets/decision-code-based-decision-attributes.png)

To add an attribute, click the **`+`** icon next to the attribute. You can add as many attributes as needed. You can also include other personalization attributes, such as profile data.

* For **Email** and **Code-based** channels, wrap the attributes within the `#each` loop using square brackets `[ ]`, and add a comma before the closing `/each` tag.

  +++See example

  ![](assets/decision-code-based-wrap-code.png)

  +++

* For **SMS** and **Push** channels, make sure you insert attributes after the syntax code for the decision policy. This syntax should always be kept at line 1.

  +++See example

  ![](assets/decision-added-sms.png)

  +++

  >[!NOTE]
  >If you insert an image asset attribute in SMS or Push content (for example, in the title or body), the attribute value displays as a URL. The image itself is not rendered in those fields.

* To enable decision item tracking, add the `trackingToken` attribute: `trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

## Visualizar e testar o conteúdo

Depois de criar o conteúdo, visualize-o e teste-o antes de ativar a jornada ou campanha. Os itens de decisão são renderizados com base nos perfis selecionados na interface de simulação. [Saiba como visualizar e testar o conteúdo](../content-management/preview-test.md).

## Próximas etapas {#final-steps}

Quando o conteúdo estiver pronto, revise e publique sua campanha ou jornada:

* [Publicar uma jornada](../building-journeys/publish-journey.md)
* [Revisar e ativar uma campanha](../campaigns/review-activate-campaign.md)

Para experiências baseadas em código, assim que o desenvolvedor fizer uma chamada de API ou SDK para buscar conteúdo para a superfície definida na configuração do canal, as alterações serão aplicadas à página da Web ou aplicativo.

## Usar painéis de relatórios

Para ver o desempenho de suas decisões, você pode visualizar métricas de decisão prontas para uso no relatório de campanha ou jornada ou criar painéis personalizados do Customer Journey Analytics para medir o desempenho e obter insights sobre como as políticas e ofertas de decisão são fornecidas e envolvidas. [Saiba mais sobre os relatórios de decisão](cja-reporting.md).

![](../reports/assets/cja-decisioning-item-performance.png)
