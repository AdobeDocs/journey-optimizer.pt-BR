---
title: Usar ações personalizadas
description: Saiba como usar ações personalizadas
feature: Actions
topic: Content Management
role: User
level: Intermediate
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: a5ea934615385e6dc0edd482ce14f3faf546d750
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 19%

---

# Usar ações personalizadas {#use-custom-actions}

As ações personalizadas permitem configurar a conexão de um sistema de terceiros para enviar mensagens ou chamadas de API. Uma ação pode ser configurada com qualquer serviço de qualquer provedor que possa ser chamado por meio de uma REST API com uma carga útil formatada em JSON.

## Configurar o URL

O painel de configuração do **Ação personalizada** mostra os parâmetros de configuração do URL e os parâmetros de autenticação configurados para a ação personalizada. Não é possível configurar a parte estática do URL na jornada, mas na configuração global da ação personalizada. [Saiba mais](../action/about-custom-action-configuration.md).

### Caminho dinâmico

Se o URL incluir um caminho dinâmico, especifique o caminho na variável **[!UICONTROL Path]** campo.

Para concatenar campos e strings de texto sem formatação, use as funções String ou o sinal de Mais (+) no editor de expressão avançado. Insira sequências de texto sem formatação em aspas simples (&#39;) ou aspas duplas (&quot;). [Saiba mais](expression/expressionadvanced.md).

Esta tabela mostra um exemplo de configuração:

| Campo | Valor |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Path | `The id of marketingCampaign + '/messages'` |

O URL concatenado tem este formulário:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](../assets/journey-custom-action-url.png)

### Cabeçalhos

O **[!UICONTROL URL Configuration]** mostra os campos de cabeçalho dinâmicos, mas não os campos de cabeçalho constantes. Os campos de cabeçalho dinâmicos são campos de cabeçalho HTTP cujo valor é configurado como uma variável. [Saiba mais](../action/about-custom-action-configuration.md).

Se necessário, especifique o valor dos campos de cabeçalho dinâmico:

1. Selecione a ação personalizada na jornada.
1. No painel de configuração, clique no ícone de lápis ao lado do campo de cabeçalho no **[!UICONTROL URL Configuration]** seção.

   ![](../assets/journey-dynamicheaderfield.png)

1. Selecione um campo e clique em **[!UICONTROL OK]**.

## Parâmetros de ação

No **[!UICONTROL Action parameters]** , você verá os parâmetros da mensagem definidos como _&quot;Variável&quot;_. Para esses parâmetros, você pode definir onde obter essas informações (exemplo: eventos, fontes de dados), passe os valores manualmente ou use o editor de expressão avançado para casos de uso avançado. Casos de uso avançados podem ser manipulação de dados e outro uso da função. Consulte [Documentação do Journey Orchestration Adobe](expression/expressionadvanced.md).

**Tópicos relacionados**

[Configurar uma ação](../action/about-custom-action-configuration.md)
