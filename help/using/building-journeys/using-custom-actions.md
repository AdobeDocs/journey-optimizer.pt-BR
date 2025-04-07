---
solution: Journey Optimizer
product: journey optimizer
title: Usar ações personalizadas
description: Saiba como usar ações personalizadas
feature: Journeys, Actions, Custom Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: action, custom, API, jornada, configuration, service
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 21%

---

# Usar ações personalizadas {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Ações personalizadas"
>abstract="As ações personalizadas permitem configurar a conexão de um sistema de terceiros para enviar mensagens ou chamadas de API. Uma ação pode ser configurada com qualquer serviço de qualquer provedor que possa ser chamado por meio de uma REST API com conteúdo formatado em JSON."

Use ações personalizadas para habilitar a conexão com um sistema de terceiros para enviar mensagens ou chamadas de API. Uma ação pode ser configurada com qualquer serviço de qualquer provedor que possa ser chamado por meio de uma REST API com conteúdo formatado em JSON.

Saiba mais sobre ações personalizadas em [esta seção](../action/action.md).

Saiba como criar e configurar uma ação personalizada em [esta página](../action/about-custom-action-configuration.md).

## Consentimento e governança de dados {#privacy}

No Journey Optimizer, você pode aplicar políticas de consentimento e governança de dados às ações personalizadas para impedir que campos específicos sejam exportados para sistemas de terceiros ou excluir clientes que não consentiram em receber comunicações por email, push ou SMS. Para obter mais informações, consulte as seguintes páginas:

* [Governança de dados](../action/action-privacy.md).
* [Consentimento](../action/consent.md).

## Configurar o URL

O painel de configuração da atividade **Ação personalizada** mostra os parâmetros de configuração de URL e os parâmetros de autenticação configurados para a ação personalizada. Não é possível definir a parte estática do URL na jornada, mas na configuração global da ação personalizada. [Saiba mais](../action/about-custom-action-configuration.md).

### Caminho dinâmico

Se a URL incluir um caminho dinâmico, especifique o caminho no campo **[!UICONTROL Caminho]**.

Para concatenar campos e cadeias de caracteres de texto sem formatação, use as funções String ou o sinal de adição (+) no editor de expressão avançado. Coloque cadeias de texto sem formatação entre aspas simples (&#39;) ou entre aspas duplas (&quot;). [Saiba mais](expression/expressionadvanced.md).

Esta tabela mostra um exemplo de configuração:

| Campo | Valor |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Caminho | `The _id + '/messages'` |

O URL concatenado tem este formato:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;ID>`/messages`

![](assets/journey-custom-action-url.png)

### Cabeçalhos e parâmetros de consulta {#headers}

A seção **[!UICONTROL Configuração de URL]** mostra os campos de cabeçalho dinâmico e parâmetro de consulta, mas não os campos constantes. Os campos de parâmetro de cabeçalho e consulta dinâmicos são definidos como variáveis na tela de configuração de ação. [Saiba mais](../action/about-custom-action-configuration.md#url-configuration)

Para especificar o valor dos campos de cabeçalho dinâmico e parâmetro de consulta, clique dentro do campo ou no ícone de lápis e selecione o campo desejado.

![](assets/journey-dynamicheaderfield.png)

## Parâmetros de ação

Na seção **[!UICONTROL Parâmetros de ação]**, você verá os parâmetros de mensagem definidos como _&quot;Variável&quot;_. Para esses parâmetros, você pode definir onde obter essas informações (por exemplo: eventos, fontes de dados), transmitir valores manualmente ou usar o editor de expressão avançado para casos de uso avançados. Casos de uso avançados podem ser manipulação de dados e outro uso de função. Consulte esta [página](expression/expressionadvanced.md).

