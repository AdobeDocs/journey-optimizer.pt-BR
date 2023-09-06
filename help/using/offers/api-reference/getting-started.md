---
title: Introdução
description: Saiba como começar a usar a API da Biblioteca de ofertas para executar operações importantes usando o mecanismo de decisão.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 4f2bbef98b2e529c2f6a663a3cf7e1ad5493c41a
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 7%

---

# Guia do desenvolvedor da API de Gestão de decisões {#decision-management-api-developer-guide}

Este guia do desenvolvedor fornece etapas para ajudar você a começar a usar o [!DNL Offer Library] API. O guia fornece chamadas de API de amostra para executar operações importantes usando o mecanismo de decisão.

➡️ [Saiba mais sobre os componentes da Gestão de decisões neste vídeo](#video)

## Pré-requisitos {#prerequisites}

Este guia requer uma compreensão funcional dos seguintes componentes do Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}: o quadro normalizado pelo qual [!DNL Experience Platform] organiza os dados de experiência do cliente.
   * [Noções básicas da composição do esquema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=pt-BR){target="_blank"}: saiba mais sobre os blocos de construção básicos de esquemas XDM.
* [Gerenciamento de decisão](../../../using/offers/get-started/starting-offer-decisioning.md): explica os conceitos e componentes usados no Experience Decisioning em geral e na gestão de decisões em particular. Ilustra as estratégias usadas para escolher a melhor opção a ser apresentada durante a experiência de um cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}: o PQL é uma linguagem avançada para gravar expressões em instâncias XDM. O PQL é usado para definir regras de decisão.

## Leitura de chamadas de API de amostra {#reading-sample-api-calls}

Este guia fornece exemplos de chamadas de API para demonstrar como formatar suas solicitações. Isso inclui caminhos, cabeçalhos necessários e cargas de solicitação formatadas corretamente. O exemplo de JSON retornado nas respostas da API também é fornecido. Para obter informações sobre as convenções usadas na documentação para chamadas de API de exemplo, consulte a seção sobre [como ler chamadas de API de exemplo](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} no [!DNL Experience Platform] guia de solução de problemas.

## Coletar valores para cabeçalhos obrigatórios {#gather-values-for-required-headers}

Para fazer chamadas para [!DNL Adobe Experience Platform] APIs, primeiro conclua o [tutorial de autenticação](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=pt-BR){target="_blank"}. Concluir o tutorial de autenticação fornece os valores para cada um dos cabeçalhos necessários em todos os [!DNL Experience Platform] Chamadas de API, conforme mostrado abaixo:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

Todas as solicitações que contêm uma carga (POST, PUT, PATCH) exigem um cabeçalho adicional:

* `Content-Type: application/json`

## Próximas etapas {#next-steps}

Este documento cobriu os conhecimentos necessários para fazer chamadas para o [!DNL Offer Library] API. Agora você pode prosseguir para as chamadas de amostra fornecidas neste guia do desenvolvedor e seguir junto com as instruções.

## Vídeo explicativo {#video}

O vídeo a seguir é destinado a apoiar a compreensão dos componentes da Gestão de decisões.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

