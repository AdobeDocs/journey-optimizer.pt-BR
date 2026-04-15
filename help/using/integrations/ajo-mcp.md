---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com clientes MCP
description: Saiba como conectar o Adobe Journey Optimizer a clientes MCP usando o servidor MCP
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 7ae497e7a0e4d1652413a5a6dbd5d617a3ec31fe
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 1%

---

# Trabalhar com clientes MCP {#ajo-mcp}

>[!AVAILABILITY]
>
>O servidor MCP [!DNL Adobe Journey Optimizer] está disponível somente em **Claude Web** e **Claude Desktop**. O suporte para outros aplicativos compatíveis com MCP será adicionado em versões futuras.

A integração do MCP [!DNL Adobe Journey Optimizer] permite consultar campanhas, jornadas e ofertas usando prompts em linguagem simples, sem gravar chamadas de API ou navegar nas telas dos produtos. Esta página explica como a integração funciona, o que você pode fazer com ela e como começar.

## O que é o protocolo de contexto de modelo? {#mcp-overview}

As equipes de marketing e de experiência do cliente dependem cada vez mais de aplicativos baseados em bate-papo e ferramentas de desenvolvedor — como Anthropic Claude, OpenAI ChatGPT, Cursor e Microsoft Copilot Studio — para simplificar seu trabalho diário. Esses aplicativos oferecem suporte ao **Protocolo de Contexto de Modelo (MCP)**, um padrão aberto que permite que os aplicativos exponham ferramentas de back-end a grandes modelos de idioma (LLMs) de maneira uniforme.

[!DNL Adobe Journey Optimizer] agora fornece um servidor MCP que exibe operações de campanha, jornada, fidelidade e sandbox diretamente dentro de qualquer aplicativo compatível com MCP. Com a integração do MCP [!DNL Adobe Journey Optimizer], diferentes personalidades podem colaborar pelos mesmos dados de orquestração — sem gravar consultas na API REST [!DNL Adobe Journey Optimizer] ou navegar por várias telas de interface do usuário. Os clientes podem descrever a intenção por conversação e permitir que o LLM chame as ferramentas de MCP apropriadas.

## Principais recursos {#mcp-capabilities}

O servidor MCP [!DNL Adobe Journey Optimizer] permite inspecionar, resumir e solucionar problemas de jornadas, campanhas e ofertas diretamente do seu assistente de IA. Todas as operações são **somente leitura** — as superfícies do servidor MCP recuperam APIs como respostas em linguagem simples para que você possa:

* **Entender a lógica da jornada** — Obtenha um resumo legível de qualquer ramificação, condições e ações da jornada.
* **Verificar preparação da campanha** — Identifique bloqueadores que impedem a publicação de uma campanha.
* **Lacunas de cobertura especial** — Veja quais canais são cobertos em suas jornadas e campanhas ativas e onde existem lacunas.
* **Auditoria de seu portfólio de orquestração** — Revise o status completo das campanhas e jornadas sem analisar o JSON ou pular para telas de produtos.

## Casos de uso {#mcp-use-cases}

Os seguintes exemplos mostram como interagir com o servidor MCP [!DNL Adobe Journey Optimizer] usando linguagem natural:

| Meta | Exemplo de prompt |
|---|---|
| **Resumir detalhes da campanha** | &quot;Obtenha a campanha cmp456 e resuma o público, a programação, o status e os pacotes.&quot; |
| **Auditoria de status e inventário** | &quot;O que temos e em que estado se encontra? Mostrar contagens ao vivo vs. de rascunho vs. concluídas/interrompidas/arquivadas para campanhas.&quot; |
| **Verificar preparação para publicação** | &quot;Por que a campanha cmp456 não está pronta para publicação? Mostre-me os bloqueadores.&quot; |
| **Comparar objetos** | &quot;Compare as campanhas abc123 e xyz789: o que mudou no status e na programação?&quot; |
| **Faça auditoria do seu portfólio** | &quot;Em todas as jornadas e campanhas ativas, quais canais são cobertos e onde estão as lacunas?&quot; |
| **Cobertura e combinação de canais** | &quot;Mostre o espaço ocupado pelo canal em jornadas, campanhas e disposições de ofertas — uso somente de email vs. multicanal, push/SMS/no aplicativo e incompatibilidades entre canais do jornada.&quot; |

## Pré-requisitos {#mcp-prerequisites}

Antes de conectar o servidor MCP [!DNL Adobe Journey Optimizer] ao seu cliente MCP, verifique o seguinte:

* Você tem uma licença [!DNL Adobe Journey Optimizer] ativa.
* Você tem acesso a um aplicativo compatível com MCP (atualmente Claude Web ou Claude Desktop).
* Você tem as permissões necessárias no [!DNL Adobe Journey Optimizer] para exibir campanhas, jornadas e ofertas.

## Conectar o servidor MCP [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Essa integração está no Beta. As etapas de configuração detalhadas serão publicadas quando atingirem a disponibilidade geral. Entre em contato com o representante da Adobe para solicitar acesso antecipado e receber instruções de configuração.

Durante a fase Beta, o representante da Adobe fornecerá:

* O URL do ponto de extremidade do servidor MCP específico para sua organização.
* Credenciais de autenticação para conectar seu assistente de IA ao [!DNL Adobe Journey Optimizer].
* Orientação sobre como configurar o servidor MCP no Claude Desktop ou no Claude Web.

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## Perguntas frequentes {#mcp-faq}

+++Quais clientes MCP são compatíveis?

O servidor MCP [!DNL Adobe Journey Optimizer] está disponível atualmente para o **Claude Web** e o **Claude Desktop**. O suporte para aplicativos adicionais compatíveis com MCP poderá ser adicionado em versões futuras.
+++

+++Quais objetos do [!DNL Adobe Journey Optimizer] posso acessar via MCP?

Você pode acessar campanhas, jornadas, ofertas, dados de fidelidade e informações da sandbox. As operações são somente leitura (recuperar APIs); as operações de gravação não são compatíveis com a versão atual.
+++

+++Preciso de acesso de desenvolvedor para usar o servidor MCP [!DNL Adobe Journey Optimizer]?

Não. O servidor MCP foi projetado para personas técnicas e de marketing. Os profissionais de marketing podem interagir com ele usando prompts de linguagem natural em qualquer cliente MCP compatível, enquanto os desenvolvedores também podem usá-lo nas ferramentas de desenvolvedor que oferecem suporte ao MCP.
+++

+++Meus dados são enviados ao provedor do cliente MCP?

Ao enviar um prompt, o cliente MCP pode enviar o contexto relevante (incluindo os dados [!DNL Adobe Journey Optimizer] retornados pelo servidor MCP) ao seu modelo para processamento. Analise as políticas de privacidade e manuseio de dados do seu provedor de cliente MCP antes de se conectar aos dados de produção.
+++

+++Quais permissões são necessárias para o [!DNL Adobe Journey Optimizer]?

Você precisa de no mínimo **permissões de Visualização** para os objetos que deseja consultar — campanhas, jornadas ou ofertas. Nenhuma permissão de gravação é necessária porque o servidor MCP executa somente operações de leitura. Entre em contato com o administrador do [!DNL Adobe Journey Optimizer] se não tiver certeza sobre o seu nível de acesso atual.
+++

+++Posso usar o servidor MCP em ambientes de sandbox?

Sim. O servidor MCP respeita a configuração da sandbox do [!DNL Adobe Journey Optimizer]. Você pode consultar dados específicos da sandbox especificando a sandbox no seu prompt ou conectando-se com credenciais com escopo para uma sandbox específica.
+++
