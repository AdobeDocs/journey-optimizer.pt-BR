---
solution: Journey Optimizer
product: journey optimizer
title: Integrar a serviços inteligentes
description: Saiba como aproveitar os Serviços inteligentes da Adobe e as previsões da IA do cliente na Journey Optimizer
feature: Journeys, Integrations
topic: Artificial Intelligence
role: User
level: Intermediate
keywords: artificial, IA, inteligente, jornada, serviço
exl-id: 20da09e1-0611-4d27-a589-30552011e06c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/rTKcWHwfwleQtD68fcdeqYK2AMQHVaknKtsNDFsOldI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 0%

---

# Integrar a serviços inteligentes {#ai-overview}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como integrar os Serviços inteligentes da Adobe e as previsões da IA do cliente à Journey Optimizer para usar pontuações de churn e conversão como atributos de perfil para decisões, ações e criação de segmentos.

>[!ENDSHADEBOX]

A integração com o **[!DNL Adobe Intelligent Services]** permite que você aproveite a inteligência artificial e o aprendizado de máquina para os casos de uso de experiência do cliente. Isso permite que os analistas de marketing definam previsões personalizadas para as necessidades de uma empresa usando configurações de nível empresarial sem exigir conhecimento especializado em ciência de dados.

O [!DNL Intelligent Services], criado em [!DNL Adobe Experience Platform], fornece IA como um serviço para as equipes de experiência do cliente. Ele ajuda a prever o comportamento do cliente, medir o impacto da campanha e melhorar o retorno sobre o investimento. Para obter mais detalhes, consulte a [[!DNL Adobe Experience Platform] documentação](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/home.html?lang=pt-BR){target="_blank"}.

A integração entre [!DNL Journey Optimizer] e [!DNL Intelligent Services] permite que você aproveite as previsões do cliente.

A IA do cliente, um componente de [!DNL Adobe Intelligent Services], prevê as prováveis ações do cliente. Consulte a [[!DNL Adobe Experience Platform] documentação](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/customer-ai/overview.html?lang=pt-BR){target="_blank"}.

A IA do cliente permite que as marcas criem pontuações de conversão ou churn baseadas em aprendizado de máquina. Essas pontuações estão disponíveis como atributos de perfil em [!DNL Adobe Experience Platform] perfis (Perfil do cliente em tempo real).

Como resultado, esses atributos podem ser usados como qualquer outro atributo de perfil no Journey Optimizer. Use-as em condições para decisões, ações ou criação de segmentos.

![Integração da IA do cliente mostrando pontuações e previsões de propensão](assets/customer-ai.png)

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

- **TL;DR:** esta página explica como o Journey Optimizer se integra aos Serviços inteligentes da Adobe — especificamente à IA do cliente — para aproveitar as pontuações de propensão baseadas em aprendizado de máquina como atributos de perfil no jornada.

**Intenções:**
- Entenda como os Serviços inteligentes da Adobe se integram ao Journey Optimizer
- Usar as pontuações de propensão da IA do cliente como atributos de perfil nas condições ou ações de jornada
- Permita previsões orientadas por IA para churn ou conversão sem exigir conhecimento especializado em ciência de dados
- Aplicar pontuações de aprendizado de máquina à criação de segmento no Journey Optimizer

**Glossário:**
- **Serviços inteligentes da Adobe**: um conjunto de serviços de IA/ML criado na Adobe Experience Platform que habilita previsões de experiência do cliente sem exigir especialização em ciência de dados *(específico do produto)*
- **IA do cliente**: um componente dos Serviços inteligentes da Adobe que gera pontuações de propensão de conversão ou churn baseadas em aprendizado de máquina para perfis de clientes *(específico de produto)*
- **Pontuação de propensão**: uma pontuação baseada em aprendizado de máquina que representa a probabilidade de um cliente executar uma ação específica (por exemplo, churn ou conversão), armazenada como um atributo de perfil *(específico do produto)*

**Medidas de Proteção:**
- Não é necessário conhecimento em ciência de dados, mas a configuração no nível de negócios deve ser concluída por analistas de marketing
- As pontuações da IA do cliente devem ser configuradas no Adobe Experience Platform antes de serem disponibilizadas como atributos de perfil no Journey Optimizer

**Terminologia:**
- Nome canônico: Serviços inteligentes da Adobe — Acrônimo: none — variantes: serviços inteligentes, serviços de IA
- Nome canônico: Customer AI — Acrônimo: none — variantes: pontuações do Customer AI, pontuações de propensão
- Sinônimos: &quot;pontuação de churn&quot; = &quot;propensão de churn&quot; ; &quot;pontuação de conversão&quot; = &quot;propensão de conversão&quot;
- Não confunda: &quot;Serviços inteligentes da Adobe&quot; ≠ &quot;Assistente de IA&quot; (Os serviços inteligentes são uma plataforma de ML preditiva; o Assistente de IA é uma interface conversacional)

**Perguntas frequentes:**
- **P: O que é a IA do cliente no contexto do Journey Optimizer?** — A IA do cliente é um componente dos Serviços inteligentes da Adobe que cria pontuações de conversão ou churn baseado em aprendizado de máquina, que ficam disponíveis como atributos de perfil utilizáveis em condições, ações e criação de segmentos da Journey Optimizer.
- **P: Preciso de habilidades em ciência de dados para usar os Serviços inteligentes da Adobe?** — Não, os analistas de marketing podem configurar previsões usando configurações no nível de negócios sem exigir conhecimento especializado em ciência de dados.
- **P: Onde as pontuações da IA do cliente são armazenadas?** — Eles são armazenados como atributos de perfil no Perfil do cliente em tempo real da Adobe Experience Platform, tornando-os acessíveis como qualquer outro atributo de perfil no Journey Optimizer.
- **P: Como posso usar as pontuações da IA do cliente em uma jornada?** — uma vez disponíveis como atributos de perfil, as pontuações podem ser usadas em condições para decisões, em configurações de ação ou para criar segmentos de público-alvo.

+++
