---
solution: Journey Optimizer
product: journey optimizer
title: Usar ações personalizadas
description: Saiba como usar ações personalizadas
feature: Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: ação, personalizado, API, jornada, configuração, serviço
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 26%

---

# Usar ações personalizadas {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Ações personalizadas"
>abstract="As ações personalizadas permitem configurar a conexão de um sistema de terceiros para enviar mensagens ou chamadas de API. Uma ação pode ser configurada com qualquer serviço de qualquer provedor que possa ser chamado por meio de uma REST API com conteúdo formatado em JSON."

As ações personalizadas permitem configurar a conexão de um sistema de terceiros para enviar mensagens ou chamadas de API. Uma ação pode ser configurada com qualquer serviço de qualquer provedor que possa ser chamado por meio de uma REST API com conteúdo formatado em JSON.

## Consentimento e governança de dados {#privacy}

No Journey Optimizer, você pode aplicar políticas de controle e consentimento de dados às ações personalizadas para impedir que campos específicos sejam exportados para sistemas de terceiros ou excluir clientes que não consentiram em receber email, mensagens de push ou comunicações por SMS. Para obter mais informações, consulte as seguintes páginas:

* [Governança de dados](../action/action-privacy.md).
* [Consentimento](../action/consent.md).

## Configurar o URL

O painel de configuração do **Ação personalizada** mostra os parâmetros de configuração do URL e os parâmetros de autenticação configurados para a ação personalizada. Não é possível configurar a parte estática do URL na jornada, mas na configuração global da ação personalizada. [Saiba mais](../action/about-custom-action-configuration.md).

### Caminho dinâmico

Se o URL incluir um caminho dinâmico, especifique o caminho na variável **[!UICONTROL Caminho]** campo.

Para concatenar campos e strings de texto sem formatação, use as funções String ou o sinal de Mais (+) no editor de expressão avançado. Insira sequências de texto sem formatação em aspas simples (&#39;) ou aspas duplas (&quot;). [Saiba mais](expression/expressionadvanced.md).

Esta tabela mostra um exemplo de configuração:

| Campo | Valor |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Caminho | `The id of marketingCampaign + '/messages'` |

O URL concatenado tem este formulário:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](assets/journey-custom-action-url.png)

### Cabeçalhos e parâmetros de consulta {#headers}

O **[!UICONTROL Configuração de URL]** mostra o cabeçalho dinâmico e os campos de parâmetro de consulta, mas não os campos constantes. Os campos de cabeçalho dinâmico e parâmetro de consulta são definidos como variáveis na tela de configuração de ação. [Saiba mais](../action/about-custom-action-configuration.md#url-configuration)

Para especificar o valor dos campos dynamic header e query parameter , clique dentro do campo ou no ícone de lápis e selecione o campo desejado.

![](assets/journey-dynamicheaderfield.png)

## Parâmetros de ação

No **[!UICONTROL Parâmetros de ação]** , você verá os parâmetros da mensagem definidos como _&quot;Variável&quot;_. Para esses parâmetros, você pode definir onde obter essas informações (exemplo: eventos, fontes de dados), passe os valores manualmente ou use o editor de expressão avançado para casos de uso avançado. Casos de uso avançados podem ser manipulação de dados e outro uso da função. Consulte esta [página](expression/expressionadvanced.md).

**Tópicos relacionados**

[Configurar uma ação](../action/about-custom-action-configuration.md)
