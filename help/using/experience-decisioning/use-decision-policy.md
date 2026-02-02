---
title: Usar políticas de decisão em mensagens
description: Saiba como usar políticas de decisão em suas mensagens.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
version: Journey Orchestration
source-git-commit: 2dfc9c2db5af1b9b74f7405a68e85563f633a54f
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 3%

---

# Usar políticas de decisão em mensagens {#create-decision}

Depois de adicionar uma política de decisão ao conteúdo, você pode usar atributos de itens de decisão retornados para personalização. Para fazer isso, primeiro insira o código da política de decisão no seu conteúdo.

>[!CAUTION]
>
>As políticas de decisão estão disponíveis a todos os clientes para os canais **Experiência baseada em código**, **SMS** e **Notificação por push**.
>
>A Decisão do canal de email está disponível com disponibilidade limitada. Para solicitar acesso, entre em contato com o representante da Adobe. Saiba mais sobre [rótulos de disponibilidade](../rn/releases.md#availability-labels).

## Inserir o código de política de decisão {#insert}

>[!BEGINTABS]

>[!TAB Experiência baseada em código]

1. Edite sua experiência baseada em código e navegue até a **[!UICONTROL Política de decisão]**.

2. Selecione **[!UICONTROL Inserir política]** para adicionar o código de política de decisão.

   ![](assets/decision-code-based-add-decision.png)

>[!NOTE]
>
>Para experiências baseadas em código, se a política de decisão contiver itens de decisão, incluindo fragmentos, você poderá aproveitar esses fragmentos no código de política de decisão. [Saiba como aproveitar fragmentos](../experience-decisioning/fragments-decision-policies.md)

>[!TAB Email]

1. Abra o **Editor do Personalization** e navegue até **[!UICONTROL Políticas de decisão]**.

2. Selecione **[!UICONTROL Inserir sintaxe]** para adicionar o código da política de decisão.

   ![](assets/decision-policy-add.png)

   >[!NOTE]
   >
   >Se a opção de inserção não for exibida, talvez uma política de decisão já esteja configurada para o componente principal.

3. Se nenhum posicionamento tiver sido atribuído ainda ao componente, selecione um na lista e clique em **[!UICONTROL Atribuir]**.

   ![](assets/decision-policy-placement.png)

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
>O Experience Decisioning com notificações por push requer uma versão específica do Mobile SDK. Antes de implementar este recurso, verifique as [notas de versão](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"} para identificar a versão necessária e se você atualizou adequadamente. Você também pode exibir todas as versões do SDK disponíveis para sua plataforma [nesta seção](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}.

>[!ENDTABS]

O código de política de decisão é adicionado. Agora você pode usar atributos dos itens de decisão retornados para personalizar seu conteúdo.

>[!NOTE]
>
>Para canais de email e experiência baseados em código, repita essa sequência uma vez por item de decisão que deseja retornar. Por exemplo, se você optou por retornar 2 itens ao [criar a decisão](create-decision-policy.md), repita a sequência duas vezes. Para canais SMS e Push, somente um item de decisão pode ser retornado.

## Personalizar com atributos de item de decisão {#attributes}

Depois de ter adicionado o código de uma política de decisão em seu conteúdo, todos os atributos dos itens de decisão retornados ficam disponíveis para personalização. [Saiba como trabalhar com personalização](../personalization/personalize.md).

Os atributos são armazenados no [esquema de catálogo](catalogs.md) de &quot;Ofertas&quot;. Eles são exibidos nas seguintes pastas do editor de personalização:
* **Atributos personalizados**: `_\<imsOrg\>` pasta
* **Atributos padrão**: `_experience` pasta

Atributos de item de decisão e atributos contextuais não são suportados por padrão em fragmentos [!DNL Journey Optimizer]. No entanto, você pode usar variáveis globais, conforme descrito abaixo.

![](assets/decision-code-based-decision-attributes.png)

Para adicionar um atributo, clique no ícone **`+`** ao lado do atributo. Você pode adicionar quantos atributos forem necessários. Você também pode incluir outros atributos de personalização, como dados de perfil.

* Para canais **baseados em email** e **código**, coloque os atributos entre o loop `#each` usando colchetes `[ ]` e adicione uma vírgula antes de fechar a marca `/each`.

  +++Veja o exemplo

  ![](assets/decision-code-based-wrap-code.png)

  +++

* Para canais **SMS** e **Push**, insira atributos após o código de sintaxe da política de decisão. Essa sintaxe deve ser sempre mantida na linha 1.

  +++Veja o exemplo

  ![](assets/decision-added-sms.png)

  +++

  >[!NOTE]
  >Se você inserir um atributo de ativo de imagem no conteúdo de SMS ou Push (por exemplo, no título ou no corpo), o valor do atributo será exibido como um URL. A própria imagem não é renderizada nesses campos.

* Para habilitar o rastreamento de item de decisão, adicione o atributo `trackingToken`: `trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

## Visualizar e testar o conteúdo

Depois de criar o conteúdo, visualize-o e teste-o antes de ativar a jornada ou campanha. Os itens de decisão são renderizados com base nos perfis selecionados na interface de simulação. [Saiba como visualizar e testar o conteúdo](../content-management/preview-test.md).

## Próximas etapas {#final-steps}

Quando o conteúdo estiver pronto, revise e publique sua campanha ou jornada:

* [Publicar uma jornada](../building-journeys/publish-journey.md)
* [Revisar e ativar uma campanha](../campaigns/review-activate-campaign.md)

Para experiências baseadas em código, assim que o desenvolvedor fizer uma chamada de API ou SDK para buscar conteúdo para a superfície definida na configuração do canal, as alterações serão aplicadas à página da Web ou aplicativo.

>[!NOTE]
>
>No momento, você não pode simular conteúdo baseado em decisão para [campanhas ou jornadas baseadas em código](../code-based/create-code-based.md). Uma solução alternativa está disponível [aqui](../code-based/code-based-decisioning-implementations.md).

## Usar painéis de relatórios

Para ver o desempenho de suas decisões, você pode visualizar métricas de decisão prontas para uso no relatório de campanha ou jornada ou criar painéis personalizados do Customer Journey Analytics para medir o desempenho e obter insights sobre como as políticas e ofertas de decisão são fornecidas e envolvidas. [Saiba mais sobre os relatórios de decisão](cja-reporting.md).

![](../reports/assets/cja-decisioning-item-performance.png)
