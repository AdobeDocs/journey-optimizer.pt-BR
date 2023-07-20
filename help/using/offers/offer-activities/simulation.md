---
title: Criar simulações
description: Saiba como simular quais ofertas serão entregues para um determinado posicionamento para validar sua lógica de decisão
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: 4d196e6485b55fe63bd8da2c7cdfc454a26f80f3
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 12%

---

# Criar simulações {#create-simulations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_simulation"
>title="Simulação de decisões de ofertas"
>abstract="Uma simulação permite simular quais ofertas serão entregues a um perfil de teste para uma determinada inserção. Dessa forma, é possível testar e refinar várias versões de suas ofertas sem impacto nos destinatários direcionados."

## Sobre a simulação {#about-simulation}

Para validar a lógica de decisão, é possível simular quais ofertas serão entregues a um perfil de teste para uma determinada inserção.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Dessa forma, é possível testar e refinar várias versões de suas ofertas sem impacto nos destinatários direcionados.

>[!NOTE]
>
>Esse recurso simula uma única solicitação para o [!DNL Decisioning] API. Saiba mais sobre [Entregar ofertas usando a API de decisão](../api-reference/offer-delivery-api/decisioning-api.md).

Para acessar esse recurso, selecione a variável **[!UICONTROL Simulação]** na guia **[!UICONTROL Gerenciamento de decisão]** > **[!UICONTROL Ofertas]** menu.

![](../assets/offers_simulation-tab.png)

>[!NOTE]
>
>Como a simulação não gera nenhum evento de decisão, a variável [limite](../offer-library/creating-personalized-offers.md#capping) A contagem de não é afetada.

<!--
➡️ [Discover this feature in video](#video)
-->

## Selecionar perfis de teste {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_simulation_test_profile"
>title="Adicionar perfis de teste"
>abstract="Você pode adicionar um perfil de teste selecionando um namespace de identidade e um valor de identidade correspondente. Você deve ter perfis de teste já disponíveis para usá-los na simulação."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/profiles/creating-test-profiles.html?lang=pt-BR" text="Criar perfis de teste"

Primeiro, é necessário selecionar os perfis de teste que você usará para simulação.

>[!CAUTION]
>
>Você deve ter perfis de teste disponíveis para simular quais ofertas serão entregues a eles. Saiba como [criar perfis de teste](../../audience/creating-test-profiles.md).

1. Clique em **[!UICONTROL Gerenciar perfil]**.

   ![](../assets/offers_simulation-manage-profile.png)

1. Selecione o namespace de identidade que deseja usar para identificar perfis de teste. Neste exemplo, usaremos o **E-mail** namespace.

   >[!NOTE]
   >
   >Um namespace de identidade define o contexto de um identificador, como um endereço de email ou ID de CRM. Saiba mais sobre os namespaces de identidade da Adobe Experience Platform [nesta seção](../../audience/get-started-identity.md){target="_blank"}.

1. Insira o valor da identidade e clique em **[!UICONTROL Exibir]** para listar os perfis disponíveis.

   ![](../assets/offers_simulation-add-profile.png)

1. Adicione outros perfis se quiser testar dados de perfil diferentes e salve a seleção.

   ![](../assets/offers_simulation-save-profiles.png)

1. Depois de adicionado, todos os perfis são listados na lista suspensa em **[!UICONTROL Perfil de teste]**. Você pode alternar entre os perfis de teste salvos para exibir os resultados de cada perfil selecionado.

   ![](../assets/offers_simulation-saved-profiles.png)

   >[!NOTE]
   >
   >Os perfis selecionados permanecerão listados como perfis de teste na **[!UICONTROL Simulação]** de sessão para sessão até que sejam removidos usando **[!UICONTROL Gerenciar perfil]**.

1. Você pode clicar no link **[!UICONTROL Detalhes do perfil]** para exibir os dados de perfil selecionados.

<!--Learn more on [selecting test profiles](messages/preview.md#select-test-profiles)-->

## Adicionar escopos de decisão {#add-decision-scopes}

Agora selecione as decisões de oferta que deseja simular nos perfis de teste.

1. Selecionar **[!UICONTROL Adicionar escopo da decisão]**.

   ![](../assets/offers_simulation-add-decision.png)

1. Selecione uma disposição na lista.

   ![](../assets/offers_simulation-add-decision-scope.png)

1. As decisões disponíveis são exibidas.

   * Você pode usar o campo de pesquisa para refinar a seleção.
   * Você pode clicar no link **[!UICONTROL Abrir decisões de oferta]** para abrir a lista de todas as decisões que você criou. Saiba mais sobre [decisões](create-offer-activities.md).

   Selecione a decisão de sua escolha e clique em **[!UICONTROL Adicionar]**.

   ![](../assets/offers_simulation-add-decision-scope-add.png)

1. O escopo de decisão recém-definido é exibido no espaço de trabalho principal.

   Você pode ajustar o número de ofertas que deseja solicitar. Por exemplo, se você selecionar 2, as 2 melhores ofertas serão exibidas para esse escopo de decisão.

   ![](../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Você pode solicitar até 30 ofertas.

1. Repita as etapas acima para adicionar quantas decisões forem necessárias.

   ![](../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Mesmo que você defina vários escopos de decisão, somente uma solicitação de API será simulada.

## Definir configurações da simulação {#define-simulation-settings}

Para editar as configurações padrão para suas simulações, siga as etapas abaixo.

1. Clique em **[!UICONTROL Configurações]**.

   ![](../assets/offers_simulation-settings.png)

1. No **[!UICONTROL Desduplicação]** você pode optar por permitir ofertas duplicadas em decisões e/ou disposições. Isso significa que várias decisões/posicionamentos podem receber a mesma oferta.

   ![](../assets/offers_simulation-settings-deduplication.png)

   >[!NOTE]
   >
   >Por padrão, todos os sinalizadores de Desduplicação são ativados para simulação, o que significa que o mecanismo de decisão permite duplicatas e, portanto, pode fazer a mesma proposta em várias decisões/posicionamentos. Saiba mais sobre o [!DNL Decisioning] Propriedades da solicitação de API em [nesta seção](../api-reference/offer-delivery-api/decisioning-api.md).

1. No **[!UICONTROL Formato de resposta]** você pode optar por incluir metadados na visualização de código. Marque a opção correspondente e selecione os metadados de sua escolha. Eles serão exibidos nas cargas de solicitação e resposta ao selecionar **[!UICONTROL Exibir código]**. Saiba mais na [Exibir resultados da simulação](#simulation-results) seção.

   ![](../assets/offers_simulation-settings-response-format.png)

   >[!NOTE]
   >
   >Ao ativar a opção, todos os itens são selecionados por padrão.

1. Clique em **[!UICONTROL Salvar]**.

>[!NOTE]
>
>Atualmente, para dados de simulação, você só pode usar o **[!UICONTROL Hub]** API.

<!--
In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## Exibir resultados da simulação {#simulation-results}

Depois de adicionar um escopo de decisão e selecionar um perfil de teste, você pode visualizar os resultados.

1. Clique em **[!UICONTROL Exibir resultados]**.

   ![](../assets/offers_simulation-view-results.png)

1. As melhores ofertas disponíveis são exibidas de acordo com o perfil selecionado para cada decisão.

   Selecione uma oferta para exibir seus detalhes.

   ![](../assets/offers_simulation-offer-details.png)

1. Clique em **[!UICONTROL Exibir código]** para exibir as cargas de solicitação e resposta. [Saiba mais](#view-code)

1. Selecione outro perfil na lista para exibir os resultados das decisões de oferta para um perfil de teste diferente.

1. Você pode adicionar, remover ou atualizar os escopos de decisão quantas vezes forem necessárias.

>[!NOTE]
>
>Sempre que alterar perfis ou atualizar escopos de decisão, será necessário atualizar os resultados usando o **[!UICONTROL Exibir resultados]** botão.

## Exibir código {#view-code}

1. Use o **[!UICONTROL Exibir código]** botão para exibir as cargas de solicitação e resposta.

   ![](../assets/offers_simulation-view-code.png)

   A visualização de código mostra as informações do desenvolvedor para o usuário atual. Por padrão, a variável **[!UICONTROL Carga de resposta]** é exibido.

   ![](../assets/offers_simulation-request-payload.png)

1. Clique em **[!UICONTROL Carga de resposta]** ou **[!UICONTROL Carga da solicitação]** para navegar entre as duas guias.

   ![](../assets/offers_simulation-response-payload.png)

1. Para usar a carga da solicitação fora do [!DNL Journey Optimizer] - para fins de solução de problemas, por exemplo, copie-o usando o **[!UICONTROL Copiar para a área de transferência]** na parte superior da exibição de código.

   ![](../assets/offers_simulation-copy-payload.png)

   <!--You cannot copy the response payload. ACTUALLY YES YOU CAN > to confirm with PM/dev? -->

   >[!NOTE]
   >
   >Ao copiar as cargas da solicitação ou resposta para seu próprio código, substitua {USER_TOKEN} e {API_KEY} com valores válidos. Saiba como recuperar esses valores no [APIs do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target="_blank"} documentação.

