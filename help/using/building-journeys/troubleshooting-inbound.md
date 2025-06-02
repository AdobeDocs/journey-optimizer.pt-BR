---
solution: Journey Optimizer
product: journey optimizer
title: Guia de solução de problemas para ações de entrada no jornada
description: Saiba como depurar e resolver problemas relacionados a ações de entrada no jornada Adobe Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: ações de entrada, solução de problemas, jornada, depurar, autoajuda, verificação, erros
source-git-commit: 86b83f8b368a77ef96581c422f19f35d939e51f4
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 0%

---


# Solução de problemas de ações de entrada no jornada {#troubleshooting-inbound-actions}

Ações de entrada, como experiências no aplicativo, Web e baseadas em código, são componentes críticos do [!DNL Journey Optimizer], pois permitem o engajamento personalizado com os usuários durante a jornada. No entanto, pode ocorrer um comportamento inesperado, como ausência de conteúdo de entrada ou entrega contínua após um perfil sair da jornada.

Este guia fornece um processo passo a passo para depurar problemas relacionados a ações de entrada em uma jornada, a fim de ajudar você a identificá-los e resolvê-los de forma independente antes de entrar em contato com o suporte do.

<!--This guide addresses the two most common scenarios with inbound actions in a journey. They are as follows:

* A profile enters the inbound step, but the user does not receive the expected inbound content.
* A user continues to receive inbound content even after the profile exits the journey.

## Benefits {#benefits}

- Faster issue resolution through self-help.
- Reduced dependency on support teams.
- Improved understanding of inbound action functionality.
- Enhanced customer experience and confidence in using AJO.-->

## Pré-requisitos {#prerequisites}

Antes de começar a solução de problemas, verifique o seguinte:

1. Configure uma sessão **Assurance**. Saiba mais na [documentação do Adobe Experience Platform Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

1. Navegue até a jornada que contém a ação de entrada para recuperar o nome da jornada e a ID da versão.

   >[!NOTE]
   >
   >A ID da versão do jornada pode ser encontrada na URL após *jornada/* (por exemplo: *86232fb1-2932-4036-8198-55dfec606fd7*).

   ![](assets/troubleshoot-inbound-retrieve-journey-id.png)

1. Clique na ação de entrada para exibir seus detalhes. Recupere o rótulo e a ID da ação de entrada.

   ![](assets/troubleshoot-inbound-retrieve-action-id.png)

1. Obtenha o namespace e a ID do perfil para identificar o perfil que está encontrando problemas. Com base na sua configuração, o namespace pode ser ECID, email ou ID do cliente, por exemplo. Saiba como pesquisar um perfil na [documentação do Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide#browse-identity){target="_blank"}.

## Cenário 1: o usuário não recebeu o conteúdo de entrada {#scenario-1}

Nesse cenário, um perfil inseriu a ação de entrada na jornada, mas mesmo depois de 30 minutos, o conteúdo de entrada correspondente não é exibido no dispositivo/cliente na etapa de acionamento da configuração.


### Pré-verificações {#pre-checks}

1. **O conjunto de dados de Entrada do Jornada está habilitado para assimilação de perfil**

   A ação de entrada usa o conjunto de dados **Entrada de Jornada** para as atualizações de perfil durante a execução. Verifique se o conjunto de dados está ativado para Perfis na sandbox atual. [Saiba mais sobre conjuntos de dados](../data/get-started-datasets.md)

2. **identidade &#39;joai&#39; definida nas identidades da plataforma**

   A ação de entrada usa o namespace **&#39;joai&#39;** no perfil `segmentMembership` para ativar o perfil para a etapa de entrada. Verifique se ele foi definido nas Identidades da plataforma para a sandbox. Saiba mais sobre o [Experience Platform Identity Service](https://experienceleague.adobe.com/en/docs/experience-platform/identity/home){target="_blank"}

### Etapas de depuração {#debugging-steps}

O gráfico abaixo mostra a sequência de etapas de depuração que você pode seguir:

![](assets/troubleshoot-inbound-scenario-1-steps.png){width="70%" align="center"}

### Etapa 1: verifique se o dispositivo/cliente está recebendo o conteúdo do Edge Network {#step-1}

Comece verificando se o dispositivo/cliente está obtendo o conteúdo esperado.

>[!BEGINTABS]

>[!TAB Canal no aplicativo]

1. Vá para a sessão [Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"} e selecione a seção **[!UICONTROL Mensagens no Aplicativo]** no painel esquerdo.

1. Na guia **[!UICONTROL Mensagens no Dispositivo]**, clique na lista suspensa **[!UICONTROL Mensagens]** e verifique se há uma mensagem com o nome de jornada seguido de &quot;- Mensagem no aplicativo&quot;. Se presente, significa que a mensagem no aplicativo está presente no dispositivo/cliente e o problema pode estar relacionado ao acionador no aplicativo.

1. Se a mensagem não for encontrada, a mensagem no aplicativo não foi recebida pelo dispositivo/cliente. Vá para a [próxima etapa](#step-2) para depuração adicional.

>[!TAB Canal da Web]

Visite a página e inspecione a guia de rede, ou verifique a carga de resposta do Edge na seção **[!UICONTROL Edge Delivery]** da sessão [Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

>[!TAB Canal de experiência baseado em código]

Execute uma solicitação de curl usando a [API do Adobe](https://developer.adobe.com/data-collection-apis/docs/api/) e verifique a carga de resposta do Edge na seção **[!UICONTROL Edge Delivery]** da sessão [Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

>[!ENDTABS]

#### Etapa 2: verifique se o Edge Network está retornando o conteúdo {#step-2}

Essa etapa é para garantir que o Edge Network retorne o conteúdo de entrada esperado para ser renderizado no dispositivo/cliente.

Quando um perfil entra em uma ação de entrada em uma jornada, ele é automaticamente qualificado em um segmento de público-alvo especial (no namespace **joai**) correspondente à ação de jornada de entrada.

Quando um cliente faz uma solicitação à Edge Network para um determinado perfil e superfície, o perfil se qualifica para receber conteúdo para as ações de jornada de entrada que direcionam essa superfície somente se o perfil for atualmente membro do segmento **joai** correspondente.

Para depurar o comportamento do Edge Network, siga as etapas abaixo.

1. Abra a exibição **[!UICONTROL Edge Delivery]** na sessão do Assurance. Esta visualização fornece informações sobre a execução da ação de entrada no servidor do Edge Network. Saiba mais na [documentação da Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.

   <!--![](assets/troubleshoot-inbound-scenario-1-edge-delivery.png)-->

1. Verifique se a atividade de Edge correspondente à ação de entrada está listada nas seções **[!UICONTROL Atividades qualificadas]** ou **[!UICONTROL Atividades não qualificadas]**:

   * Se estiver na seção **Atividades qualificadas**, o perfil se qualificará para a ação de jornada de entrada, e o conteúdo deverá ser retornado.
   * Se estiver na seção **Atividades não qualificadas**, o perfil não se qualificou para a ação de jornada de entrada. Consulte os motivos de exclusão para obter mais detalhes.
   * Se em **nenhuma seção**, houve um problema com a publicação da ação de jornada de entrada na Edge Network ou o URI de superfície solicitado não correspondeu às definições de configuração de canal da ação de entrada.

   >[!NOTE]
   >
   >Para encontrar sua atividade do Edge na sessão **Assurance**, procure a atividade em que **[!UICONTROL audienceNamespace]** é **joai** e o **[!UICONTROL audienceSegmentId]** é `<JourneyVersionID>_<JourneyAction ID>` (por exemplo: *86232fb1-2932-4036-8198-55dfec606fd7_708f718d-8503-4427-ad8d-8e28979b554c*).

1. Se sua atividade estiver na seção **[!UICONTROL Atividades Não Qualificadas]** e o motivo da exclusão for *&#39;O segmento não está ativo&#39;*, significa que o servidor de entrega do Edge Network não acha que o perfil faz parte do segmento de público-alvo **joai** relevante.

   Você pode verificar novamente se o segmento **joai** está presente na exibição do perfil do servidor de entrega do Edge Network, abrindo o elemento **segmentsMap** da seção Perfil e procurando a presença da ID de segmento **joai**.

1. Se o servidor de entrega do Edge Network não exibir o perfil como estando no segmento **joai** relevante, vá para a próxima etapa.<!--use the Platform Profile viewer UI to check if the expected **joai** segment is in a realized state in the Edge profile. Learn more in the [Experience Platform Profile UI documentation](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide){target="_blank"}-->

#### Etapa 3: verificar se a associação de público-alvo joai se propagou para a Edge Network {#step-3}

Esta etapa é para verificar se o perfil do Edge foi atualizado corretamente quando o perfil entrou na ação de jornada de entrada e o perfil foi qualificado no segmento **joai** correspondente.

Quando um perfil é qualificado em um segmento **joai**, ele é atualizado primeiro no Hub e, em seguida, a associação do segmento é projetada para o Perfil do Edge para uso pelo servidor de entrega do Edge Network.

>[!NOTE]
>
>A propagação do Hub para o Edge pode levar de 15 a 30 minutos a partir do momento em que o perfil é atualizado no Hub.

Para verificar a presença do segmento **joai** no atributo `segmentMembership` do perfil do Edge, siga as etapas abaixo.

1. Navegue até o menu **[!UICONTROL Cliente]** > **[!UICONTROL Perfis]** no painel de navegação esquerdo [!DNL Journey Optimizer] e navegue até o perfil usando o namespace e a ID. Saiba mais sobre [Perfis de clientes em tempo real](../audience/get-started-profiles.md)

1. Selecione a guia **[!UICONTROL Atributos]** e escolha a exibição **[!UICONTROL Edge]**.
   <!--cannot see Hub/Edge wiews for the profile-->

1. Clique em **[!UICONTROL Exibir JSON]** para abrir a exibição JSON do perfil.

   ![](assets/troubleshoot-inbound-profile-view-json.png)

1. Vá para o atributo **[!UICONTROL segmentMembership]** e verifique se a ID do segmento `<JourneyVersionID>_<ActionID>` está presente no namespace **joai** e se está no status **[!UICONTROL performed]** <!--or existing?-->.

   ![](assets/troubleshoot-inbound-profile-json-realized.png)

   * Se estiver presente, significa que o segmento **joai** correspondente à ação de jornada de entrada foi propagado corretamente para o perfil do Edge.

   * Se não for exibido na visualização do perfil do servidor de entrega do Edge Network, pode haver um problema com a forma como o servidor de entrega está carregando o perfil do Edge.

1. Se a ID de segmento **joai** não estiver presente ou se estiver no estado **[!UICONTROL encerrado]**, significa que ela (ainda) não foi propagada para o Edge.

   Aguarde de 15 a 30 minutos para que os valores de `segmentMembership` sejam propagados do Hub para a Edge. Se ainda não estiver presente, vá para a próxima etapa.

<!--The next step is to check whether the audience segment is present in the profile on the Hub.-->

#### Etapa 4: verifique se a associação de público-alvo de joai está presente no perfil no Hub {#step-4}

Esta etapa é para verificar se o perfil de Hub foi atualizado corretamente quando o perfil entrou na ação de jornada de entrada e o perfil foi qualificado no segmento **joai** correspondente.

>[!NOTE]
>
>A assimilação da associação de segmento **joai** no perfil de Hub pode levar de 15 a 30 minutos a partir do momento em que o perfil entrou na ação de jornada de entrada.

Para verificar a presença do segmento **joai** no atributo `segmentMembership` do perfil de Hub, siga as etapas abaixo.

1. Navegue até o menu **[!UICONTROL Cliente]** > **[!UICONTROL Perfis]** no painel de navegação esquerdo [!DNL Journey Optimizer] e navegue até o perfil usando o namespace e a ID. Saiba mais sobre [Perfis de clientes em tempo real](../audience/get-started-profiles.md)

1. Selecione a guia **[!UICONTROL Atributos]** e escolha a exibição **[!UICONTROL Hub]**. <!--cannot see Hub/Edge wiews for the profile-->

1. Clique em **[!UICONTROL Exibir JSON]** para abrir a exibição JSON do perfil.

1. Vá para o atributo **[!UICONTROL segmentMembership]** e verifique se a ID do segmento `<JourneyVersionID>_<ActionID>` está presente no namespace **joai** e se está no status **[!UICONTROL performed]** <!--or existing?-->.

   * Se estiver presente, significa que o segmento **joai** correspondente à ação de jornada de entrada foi assimilado corretamente no perfil de Hub.

   * Se não for encontrado no perfil do Edge após pelo menos 30 minutos, talvez haja um problema com o sistema de projeção do Edge.

1. Se a ID de segmento **joai** não estiver presente ou se estiver no estado **[!UICONTROL encerrado]**, significa que o perfil não foi (ainda) qualificado corretamente no segmento de público-alvo **joai** especial ao entrar na ação de jornada de entrada correspondente.

   Aguarde de 15 a 30 minutos para que os valores `segmentMembership` sejam assimilados no perfil no Hub. Se ainda não estiver presente, vá para a próxima etapa.

#### Etapa 5: se o cliente/dispositivo ainda não estiver obtendo o conteúdo esperado {#step-5}

Se você tiver passado por todas as etapas acima e não estiver vendo o comportamento esperado após esperar de 30 a 60 minutos pela propagação da associação do segmento para a Edge Network, entre em contato com o Atendimento ao cliente da Adobe ou com seu representante da Adobe.

Inclua o máximo de detalhes possível das etapas de depuração, como:

* a etapa em que você vê o comportamento inesperado;
* a ID da versão do jornada;
* a ID da ação de jornada;
* o rastreamento completo do Assurance;
* a visualização JSON do perfil do Edge;
* a visualização JSON do perfil do Hub;
* etc.

## Cenário 2: o usuário ainda está recebendo o conteúdo de entrada mesmo depois que o perfil sair da jornada {#scenario-2}

Este cenário é o inverso do [Cenário 1](#scenario-1). Quando um perfil sai de uma jornada, ele não deve mais se qualificar para os segmentos de público-alvo **joai** correspondentes às ações de entrada na jornada.

Siga as mesmas etapas de depuração do [Cenário 1](#debugging-steps) para verificar se o perfil do Hub, o perfil do Edge e o servidor de entrega do Edge Network refletem corretamente o status de associação do segmento relevante **joai** e se o cliente não está mais recebendo o conteúdo de entrada.

<!--
## Additional Notes {#additional-notes}

- **Propagation Time:** Segment membership updates can take up to 15-30 minutes to propagate from the Hub to the Edge Network.
- **Support:** If issues persist after following the steps, open a support ticket with details such as:
  - Journey Version ID and Journey Action ID.
  - Assurance trace.
  - JSON views of Edge and Hub profiles.
  - Debugging observations.

## Reference Section {#reference-section}

- [Assurance Setup Guide](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/using-assurance)
- [Adobe Experience Platform Documentation](https://experienceleague.adobe.com/docs/experience-platform/home.html)
- [Streaming Ingestion APIs Troubleshooting](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html)

## Warnings and Notes {#warnings-and-notes}

> **Warning:** Ensure the `joai` namespace is correctly configured in Platform Identities. Misconfiguration can lead to qualification issues for inbound actions.

> **Note:** Segment membership updates may take up to 30 minutes to propagate. Plan debugging sessions accordingly.

## Cross-References {#cross-references}

- [Testing the Journey](../building-journeys/testing-the-journey.md)
- [Using the Journey Designer](../building-journeys/using-the-journey-designer.md#paths)
- [Troubleshooting Custom Actions](../action/troubleshoot-custom-action.md)
-->