---
solution: Journey Optimizer
product: journey optimizer
title: Uso de APIs do Journey Optimizer
description: O Journey Optimizer fornece APIs RESTful que permitem executar programaticamente as principais operações em seus aplicativos. Saiba como acessá-las e usá-las.
feature: Integrations, Data Ingestion
role: Developer
level: Intermediate
exl-id: 4c897c52-6eb2-4d6e-aaa9-9bd83608b2b6
source-git-commit: 7864012ad148c2e52bc38598016e7bd7fac9644e
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 7%

---

# Trabalhar com [!DNL Journey Optimizer] APIs {#apis-gs}

## Acesso rápido {#quick-access}

Navegue pela [referência de API concluída](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"} para acessar todas as APIs do Journey Optimizer e testá-las diretamente. Para começar, [configure a autenticação](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} para coletar as credenciais necessárias.

## Visão geral {#overview}

A API do Adobe Journey Optimizer permite fornecer experiências personalizadas, conectadas e oportunas ao cliente por meio de qualquer aplicativo, dispositivo ou canal e, por sua vez, gerenciar com eficiência a jornada completa do cliente. A jornada do cliente envolve todo o processo de interação do cliente com uma marca, desde o primeiro momento do contato até o cliente ir embora. Ela começa com a fase de percepção, onde o cliente aprende sobre a marca e começa a se envolver. O cliente interagirá ainda mais com a marca, visitará sites online e físicos, fará compras, enviará mensagens ou fará resenhas.

O Adobe Journey Optimizer é construído nativamente na Adobe Experience Platform e combina um perfil de cliente unificado em tempo real, uma estrutura aberta de priorização de API, um Offer Decisioning centralizado, além de inteligência artificial (IA) e aprendizado de máquina (ML) para personalização e otimização. Ao integrar-se à API do Journey Optimizer, as marcas podem determinar de forma inteligente a próxima melhor interação com escala, velocidade e flexibilidade em toda a jornada do cliente.

**Introdução às APIs do Journey Optimizer:**

* **[Procurar a referência completa da API](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}** - Acessar todas as APIs do Journey Optimizer e testá-las diretamente
* **[Configurar autenticação](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}** - Colete as credenciais necessárias para começar a usar as APIs
* **[APIs de Gestão de Decisões](../offers/api-reference/getting-started.md)** - Gerencie ofertas e decisões de forma programática
* **[APIs do Experience Decisioning](../experience-decisioning/api-reference/getting-started.md)** - Forneça itens de decisão personalizados usando experiências baseadas em código

## Autenticação {#authentication}

Antes de usar APIs do Journey Optimizer, você deve configurar a autenticação para acessar os endpoints da API.

Siga o [guia de autenticação](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} para coletar as credenciais de autenticação necessárias para todas as APIs do Journey Optimizer.

## Documentação da API {#api-documentation}

A documentação completa da API do Adobe Journey Optimizer inclui informações detalhadas sobre todos os endpoints disponíveis, formatos de solicitação/resposta e recursos de teste interativo.

Acesse a [documentação da API do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"} e procure o menu **Referências de API** para explorar todas as APIs disponíveis.

## APIs da Gestão de decisões {#decision-management-apis}

O Journey Optimizer fornece APIs dedicadas para a Gestão de decisões, permitindo gerenciar ofertas, decisões e posicionamentos de forma programática.

Consulte o [Guia do desenvolvedor da API de Gerenciamento de decisões](../offers/api-reference/getting-started.md) para começar a usar as APIs do Offer Decisioning.

## APIs do Experience Decisioning {#experience-decisioning-apis}

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

* [Referência da API do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}
* [Guia de autenticação](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}
* [Manual do desenvolvedor da API de Gestão de decisões](../offers/api-reference/getting-started.md)
* [Referência da API do Experience Decisioning](../experience-decisioning/api-reference/getting-started.md)

**integração com o Journey Optimizer**

* [Integrar o Adobe Analytics](../integrations/integration-ajo-analytics.md)
* [Integrar o Adobe Target](../integrations/integration-ajo-target.md)
* [Integrar o Adobe Campaign](../building-journeys/using-adobe-campaign-v7-v8.md)

**Recursos do desenvolvedor**

* [APIs do Adobe Experience Platform](https://developer.adobe.com/experience-platform-apis/){target="_blank"}
* [Console do desenvolvedor da Adobe](https://developer.adobe.com/console){target="_blank"}
* [Ações personalizadas em jornadas](../action/about-custom-action-configuration.md)
