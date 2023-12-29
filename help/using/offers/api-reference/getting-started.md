---
title: Introdução
description: Saiba como começar a usar a API da Biblioteca de ofertas para executar operações importantes usando o mecanismo de decisão.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 100%

---

# Manual do desenvolvedor da API de Gestão de decisões {#decision-management-api-developer-guide}

>[!CONTEXTUALHELP]
>id="od_api_support"
>title="Novas APIs de gestão de decisões"
>abstract="Já estão disponíveis novas APIs para criação e gerenciamento de objetos de gestão de decisões. As APIs herdadas serão compatíveis até 27/03/2024."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_api_support"
>title="Novas APIs de gestão de decisões"
>abstract="Já estão disponíveis novas APIs para criação e gerenciamento de objetos de gestão de decisões. As APIs herdadas serão compatíveis até 27/03/2024."

Este manual do desenvolvedor fornece etapas para ajudar a começar a usar a API [!DNL Offer Library]. O manual fornece chamadas de API de amostra para executar operações importantes usando o mecanismo de decisão.

➡️ [Saiba mais sobre os componentes da Gestão de decisões neste vídeo](#video)

## Pré-requisitos {#prerequisites}

Este manual necessita de uma compreensão funcional dos seguintes componentes da Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}: a estrutura padronizada pela qual a [!DNL Experience Platform] organiza os dados de experiência do cliente.
   * [Noções básicas da composição de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=pt-BR){target="_blank"}: saiba mais sobre os blocos de construção básicos de esquemas XDM.
* [Gestão de decisões](../../../using/offers/get-started/starting-offer-decisioning.md): explica os conceitos e componentes usados no Offer Decisioning em geral, particularmente a gestão de decisões. Ilustra as estratégias usadas para escolher a melhor opção a ser apresentada durante a experiência de um(a) cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=pt-BR){target="_blank"}: o PQL é uma linguagem avançada para gravar expressões em instâncias XDM. O PQL é usado para definir regras de decisão.

## Leitura de chamadas de API de amostra {#reading-sample-api-calls}

Este manual fornece exemplos de chamadas de API para demonstrar como formatar suas solicitações. Isso inclui caminhos, cabeçalhos necessários e conteúdos de solicitação formatados corretamente. Também fornece exemplos de JSON retornado nas respostas da API. Para obter informações sobre as convenções usadas na documentação para chamadas de API de exemplo, consulte a seção sobre [como ler chamadas de API de exemplo](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=pt-BR#how-do-i-format-an-api-request){target="_blank"} no manual de solução de problemas da [!DNL Experience Platform].

## Coletar valores para cabeçalhos necessários {#gather-values-for-required-headers}

Para fazer chamadas para APIs da [!DNL Adobe Experience Platform], primeiro conclua o [tutorial de autenticação](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=pt-BR){target="_blank"}. Concluir o tutorial de autenticação fornece os valores para cada um dos cabeçalhos necessários em todas as chamadas de API da [!DNL Experience Platform], conforme mostrado abaixo:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

Todas as solicitações que contêm um conteúdo (POST, PUT, PATCH) exigem um cabeçalho adicional:

* `Content-Type: application/json`

## Próximas etapas {#next-steps}

Este documento cobriu os conhecimento necessários para fazer chamadas para a API da [!DNL Offer Library]. Agora você pode prosseguir para as chamadas de amostra fornecidas neste manual do desenvolvedor e seguir suas instruções.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = "Mobile_Sheliak"`.
-->

## Vídeo explicativo {#video}

O vídeo a seguir é destinado a apoiar a compreensão dos componentes da Gestão de decisões.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

