---
title: Criar simulações
description: Saiba como criar simulações
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: null
source-git-commit: bad206b6c9b48241dbbd7758a331d602fac466b4
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# Criar simulações

## Sobre a simulação

Para validar sua lógica de decisão, você pode simular quais ofertas serão entregues a um perfil de teste para uma determinada disposição.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Isso permite testar e refinar várias versões das ofertas sem afetar os recipients alvos.

>[!NOTE]
>
>Esse recurso simula uma única solicitação para o [!DNL Decisions] API. Saiba mais sobre [Fornecer ofertas usando a API de decisões](../api-reference/decisions-api/deliver-offers.md).

Para acessar esse recurso, selecione o **[!UICONTROL Simulation]** na guia do **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** menu.

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## Selecionar perfis de teste

Primeiro, é necessário selecionar os perfis de teste que serão usados para simulação.

1. Clique em **[!UICONTROL Manage profile]**.

   ![](../../assets/offers_simulation-manage-profile.png)

1. Selecione o namespace de identidade que deseja usar para identificar os perfis de teste. Neste exemplo, usaremos a variável **Email** namespace.

   >[!NOTE]
   >
   >Um namespace de identidade define o contexto de um identificador, como um endereço de email ou ID de CRM. Saiba mais sobre os namespaces de identidade da Adobe Experience Platform [nesta seção](../../get-started-identity.md){target=&quot;_blank&quot;}.

1. Insira o valor de identidade e clique em **[!UICONTROL View]** para listar os perfis disponíveis.

   ![](../../assets/offers_simulation-add-profile.png)

1. Adicione outros perfis se desejar testar dados de perfil diferentes e salve sua seleção.

   ![](../../assets/offers_simulation-save-profiles.png)

1. Depois de adicionados, todos os perfis são listados na lista suspensa em **[!UICONTROL Test profile]**. Você pode alternar entre os perfis de teste salvos para exibir os resultados de cada perfil selecionado.

   ![](../../assets/offers_simulation-saved-profiles.png)

1. Você pode clicar no botão **[!UICONTROL Profile details]** link para exibir os dados de perfil selecionados.

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## Adicionar escopos de decisão

Em seguida, selecione as decisões de oferta que deseja simular nos perfis de teste.

1. Selecione **[!UICONTROL Add decision scope]**.

   ![](../../assets/offers_simulation-add-decision.png)

1. Selecione uma disposição na lista.

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. As decisões disponíveis são exibidas.

   * Você pode usar o campo de pesquisa para refinar a seleção.
   * Você pode clicar no botão **[!UICONTROL Open offer decisions]** para abrir a lista de todas as decisões criadas. Saiba mais sobre [decisões](create-offer-activities.md).

   Selecione a decisão de sua escolha e clique em **[!UICONTROL Add]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. O escopo de decisão que você acabou de definir é exibido no espaço de trabalho principal.

   É possível ajustar o número de ofertas que deseja solicitar. Por exemplo, se você selecionar 2, as 2 melhores ofertas serão exibidas para esse escopo de decisão.

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Você pode solicitar até 30 ofertas.

1. Repita as etapas acima para adicionar quantas decisões forem necessárias.

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Mesmo que você defina vários escopos de decisão, apenas uma solicitação de API é simulada.
   >
   >Todos os sinalizadores de Eliminação de duplicação são ativados por padrão para simulação, o que significa que o mecanismo de decisão permite duplicatas e, portanto, pode fazer a mesma proposta em várias decisões. Saiba mais sobre o [!DNL Decisions] Propriedades da solicitação de API em [esta seção](../api-reference/decisions-api/deliver-offers.md).

## Exibir resultados da simulação

Depois de adicionar um escopo de decisão e selecionar um perfil de teste, você poderá visualizar os resultados.

1. Clique em **[!UICONTROL View results]**.

   ![](../../assets/offers_simulation-view-results.png)

1. As melhores ofertas disponíveis são exibidas de acordo com o perfil selecionado para cada decisão.

   Selecione uma oferta para exibir seus detalhes.

   ![](../../assets/offers_simulation-offer-details.png)

1. Selecione outro perfil na lista para exibir os resultados das decisões de oferta para um perfil de teste diferente.

1. Você pode adicionar, remover ou atualizar os escopos de decisão quantas vezes forem necessárias.

>[!NOTE]
>
>Sempre que alterar perfis ou atualizar escopos de decisão, será necessário atualizar os resultados usando o **[!UICONTROL View results]** botão.

<!--Questions

* Is it recommended to first select profiles or first add decision scopes?
* What does Request offer changes?
* Nothing displays when I click View results? Can't see any score...
* What's the typical example? i.e. how many decisions do you select, and how do you compare scores?
* What do you learn from simulation? i.e. if I selected 2 decisions and I compare the scores, which one is better or should I use for my customers?
* Is there a way to create relevant test profiles?
* Error on Profile details link.
* Is there a tutorial planned to be released?
* Why still a big red frame when no profile is found?

## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
-->