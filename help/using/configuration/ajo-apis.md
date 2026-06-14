---
solution: Journey Optimizer
product: journey optimizer
title: Uso de APIs do Journey Optimizer
description: O Journey Optimizer fornece APIs RESTful que permitem executar programaticamente as principais operações em seus aplicativos. Saiba como acessá-las e usá-las.
feature: Integrations, Data Ingestion
role: Developer
level: Intermediate
exl-id: 4c897c52-6eb2-4d6e-aaa9-9bd83608b2b6
TQID: https://experienceleague.adobe.com/VkGKC5I4qSBcxCQQdjTJTYNNGvUoBRFUfUxs3nbIjtQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: []
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 611
ht-degree: 5%

---

# Trabalhar com [!DNL Journey Optimizer] APIs {#apis-gs}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como acessar, autenticar e usar as APIs RESTful do Adobe Journey Optimizer, incluindo as APIs da Gestão de decisões e da Decisão de experiências, para executar operações importantes de forma programática.

>[!ENDSHADEBOX]

## Acesso rápido {#quick-access}

Navegue pela [referência de API concluída](https://developer.adobe.com/journey-optimizer-apis){target="_blank"} para acessar todas as APIs do Journey Optimizer e testá-las diretamente. Para começar, [configure a autenticação](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"} para coletar as credenciais necessárias.

## Visão geral {#overview}

A API do Adobe Journey Optimizer permite fornecer experiências personalizadas, conectadas e oportunas ao cliente por meio de qualquer aplicativo, dispositivo ou canal e, por sua vez, gerenciar com eficiência a jornada completa do cliente. A jornada do cliente envolve todo o processo de interação do cliente com uma marca, desde o primeiro momento do contato até o cliente ir embora. Ela começa com a fase de percepção, onde o cliente aprende sobre a marca e começa a se envolver. O cliente interagirá ainda mais com a marca, visitará sites online e físicos, fará compras, enviará mensagens ou fará resenhas.

O Adobe Journey Optimizer é construído nativamente na Adobe Experience Platform e combina um perfil de cliente unificado em tempo real, uma estrutura aberta de priorização de API, um Offer Decisioning centralizado, além de inteligência artificial (IA) e aprendizado de máquina (ML) para personalização e otimização. Ao integrar-se à API do Journey Optimizer, as marcas podem determinar de forma inteligente a próxima melhor interação com escala, velocidade e flexibilidade em toda a jornada do cliente.

**Introdução às APIs do Journey Optimizer:**

* **[Procurar a referência completa da API](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}** - Acessar todas as APIs do Journey Optimizer e testá-las diretamente
* **[Configurar autenticação](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}** - Colete as credenciais necessárias para começar a usar as APIs
* **[APIs de Gestão de Decisões](../offers/api-reference/getting-started.md)** - Gerencie ofertas e decisões de forma programática
* **[APIs do Experience Decisioning](../experience-decisioning/api-reference/getting-started.md)** - Forneça itens de decisão personalizados usando experiências baseadas em código

## Autenticação {#authentication}

Antes de usar APIs do Journey Optimizer, você deve configurar a autenticação para acessar os endpoints da API.

Siga o [guia de autenticação](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"} para coletar as credenciais de autenticação necessárias para todas as APIs do Journey Optimizer.

## Documentação da API {#api-documentation}

A documentação completa da API do Adobe Journey Optimizer inclui informações detalhadas sobre todos os endpoints disponíveis, formatos de solicitação/resposta e recursos de teste interativo.

Acesse a [documentação da API do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis){target="_blank"} e procure o menu **Referências de API** para explorar todas as APIs disponíveis.

## Apis de gestão de decisão {#decision-management-apis}

O Journey Optimizer fornece APIs dedicadas para a Gestão de decisões, permitindo gerenciar ofertas, decisões e posicionamentos de forma programática.

Consulte o [Guia do desenvolvedor da API de Gerenciamento de decisões](../offers/api-reference/getting-started.md) para começar a usar as APIs do Offer Decisioning.

## Apis do Experience Decisioning {#experience-decisioning-apis}

A Journey Optimizer também oferece APIs do Experience Decisioning para fornecer itens de decisão personalizados por meio de experiências baseadas em código. O Experience Decisioning oferece uma abordagem simplificada de personalização com itens de decisão, regras de elegibilidade e estratégias de seleção.

**Operações de API disponíveis:**

* **Itens de decisão** - Criar, ler, atualizar e excluir itens de decisão
* **Estratégias de seleção** - Defina como selecionar e classificar itens de decisão
* **Regras de qualificação** - Definir condições para qualificação de item
* **Coleções de itens** - Organiza itens de decisão em coleções
* **Fórmulas de classificação** - Configurar lógica de classificação personalizada
* **Posicionamentos** - Defina onde os itens de decisão podem aparecer

Saiba mais na [Referência da API do Experience Decisioning](../experience-decisioning/api-reference/getting-started.md) e descubra como [fornecer ofertas usando experiências baseadas em código](../experience-decisioning/gs-experience-decisioning.md).

## Tópicos relacionados {#related-topics}

**Documentação e guias de API**

* [Referência da API do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}
* [Guia de autenticação](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}
* [Manual do desenvolvedor da API de Gestão de decisões](../offers/api-reference/getting-started.md)
* [Referência da API do Experience Decisioning](../experience-decisioning/api-reference/getting-started.md)

**integração com o Journey Optimizer**

* [Integrações com outras soluções](../integrations/ajo-integrations.md)
* [Integrar ao Adobe Analytics](../event/about-analytics.md)
* [Integrar o Adobe Campaign](../building-journeys/using-adobe-campaign-v7-v8.md)

**Recursos do desenvolvedor**

* [APIs do Adobe Experience Platform](https://developer.adobe.com/experience-platform-apis){target="_blank"}
* [Adobe Developer Console](https://developer.adobe.com/console){target="_blank"}
* [Ações personalizadas em jornadas](../action/about-custom-action-configuration.md)
