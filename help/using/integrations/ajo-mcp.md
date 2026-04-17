---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com clientes MCP (Beta)
description: Saiba como conectar o Adobe Journey Optimizer a clientes MCP usando o servidor MCP
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 1e42168a8eb2e5824a4054cced014b6ec57afd7f
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 1%

---

# Trabalhar com clientes MCP (Beta) {#ajo-mcp}

>[!CAUTION]
>
>**aviso sobre a documentação do Beta:** esta documentação abrange um recurso do Beta e não constitui a documentação final. O conteúdo descrito aqui está relacionado a uma versão do Beta e está sujeito a alterações até sua disponibilização geral. A Adobe não faz declarações sobre a integridade ou a precisão desta documentação.
>
>Ao usar o Adobe Journey Optimizer MCP Server (Beta) (&quot;Beta&quot;), você reconhece que o Beta é fornecido **&quot;no estado em que se encontra&quot; sem garantias de qualquer tipo**. A Adobe não tem nenhuma obrigação de manter, corrigir, atualizar, alterar, modificar ou oferecer suporte à Beta. É recomendável ter cuidado e não depender de forma alguma do funcionamento ou desempenho correto desse Beta e/ou dos materiais que o acompanham. O Beta é considerado Informações confidenciais da Adobe. Qualquer &quot;Feedback&quot; (informação sobre o Beta incluindo, mas não se limitando a, problemas ou defeitos encontrados durante o uso do Beta, sugestões, melhorias e recomendações) fornecido por Você ao Adobe é atribuído ao Adobe, incluindo todos os direitos, cargos e interesses no e no Feedback.

A integração do MCP [!DNL Adobe Journey Optimizer] permite consultar campanhas e ofertas usando prompts em linguagem simples, sem gravar chamadas de API ou navegar nas telas dos produtos. Esta página explica como a integração funciona, o que você pode fazer com ela e como começar.

>[!AVAILABILITY]
>
>O servidor MCP [!DNL Adobe Journey Optimizer] está disponível somente em **Claude Web** e **Claude Desktop**. O suporte para outros aplicativos compatíveis com MCP será adicionado em versões futuras.

## Qual é o protocolo de contexto do modelo? {#mcp-overview}

As equipes de marketing e de experiência do cliente dependem cada vez mais de aplicativos baseados em bate-papo e ferramentas de desenvolvedor — como Anthropic Claude, OpenAI ChatGPT, Cursor e Microsoft Copilot Studio — para simplificar seu trabalho diário. Esses aplicativos oferecem suporte ao **Protocolo de Contexto de Modelo (MCP)**, um padrão aberto que permite que os aplicativos exponham ferramentas de back-end a grandes modelos de idioma (LLMs) de maneira uniforme.

[!DNL Adobe Journey Optimizer] agora fornece um servidor MCP que exibe operações de campanha, fidelidade e sandbox diretamente dentro de qualquer aplicativo compatível com MCP. Com a integração do MCP [!DNL Adobe Journey Optimizer], diferentes personalidades podem colaborar pelos mesmos dados de orquestração — sem gravar consultas na API REST [!DNL Adobe Journey Optimizer] ou navegar por várias telas de interface do usuário. Os clientes podem descrever a intenção por conversação e permitir que o LLM chame as ferramentas de MCP apropriadas.

## Principais recursos {#mcp-capabilities}

O servidor MCP [!DNL Adobe Journey Optimizer] permite inspecionar, resumir e solucionar problemas de campanhas e ofertas diretamente do seu assistente de IA. Todas as operações são **somente leitura** — as superfícies do servidor MCP recuperam APIs como respostas em linguagem simples para que você possa:

<!--* **Understand journey logic** — Get a human-readable summary of any journey's branching, conditions, and actions.-->
* **Obtenha visibilidade instantânea da campanha** — Pergunte sobre os status da campanha e as configurações de canal em linguagem simples e obtenha respostas instantaneamente, sem menus de navegação ou receber relatórios manualmente.
* **Detectar problemas antecipadamente** — Superar campanhas interrompidas, rascunhos órfãos e problemas de configuração de canal no momento em que você pergunta, para que sua equipe possa agir com rapidez.
* **Colaborar com base em dados dinâmicos** — Profissionais de marketing, gerentes de campanha e partes interessadas podem consultar os mesmos dados dinâmicos [!DNL Adobe Journey Optimizer] por meio do assistente de IA, facilitando o alinhamento, a decisão e a movimentação.
* **Auditoria de seu portfólio de orquestração** — Revise o status completo das campanhas sem analisar o JSON ou pular entre telas de produtos.

## Ferramentas disponíveis {#mcp-tools}

As seguintes ferramentas são expostas pelo servidor MCP [!DNL Adobe Journey Optimizer]:

| Ferramenta | Descrição |
|---|---|
| **Listar Campanhas** | Navegue pelas campanhas de marketing do [!DNL Adobe Journey Optimizer]. Oferece suporte à filtragem por status (RASCUNHO, EM TEMPO REAL, PARADO, CONCLUÍDO). |
| **Obter Campanha** | Busque detalhes completos e a configuração de uma campanha específica por ID, incluindo o direcionamento de público, a programação, o canal e as configurações de conteúdo. |
| **Listar Configurações de Canal** | Visualize predefinições de superfície e configurações de marca para canais de email, SMS, push ou WhatsApp. |

>[!NOTE]
>
>Todas as ferramentas são somente leitura. As operações de gravação (criação, atualização ou exclusão de objetos) não são compatíveis com a versão atual do Beta.

## Casos de uso {#mcp-use-cases}

Os seguintes exemplos mostram como interagir com o servidor MCP [!DNL Adobe Journey Optimizer] usando linguagem natural:

| Meta | Exemplo de prompt |
|---|---|
| **Visão geral da campanha** | &quot;Mostrar todas as minhas campanhas do AJO&quot; / &quot;Quantas campanhas estão configuradas no AJO?&quot; |
| **Auditoria de status** | &quot;Quais campanhas estão ativas no momento?&quot; / &quot;Listar campanhas pausadas ou interrompidas.&quot; |
| **Detalhes da campanha** | &quot;Obtenha os detalhes completos da campanha [ID]&quot; / &quot;Mostre-me tudo configurado na campanha [ID].&quot; |
| **Público-alvo e direcionamento** | &quot;Qual público-alvo é direcionado na campanha [ID]?&quot; / &quot;Quais regras de qualificação são definidas na campanha [ID]?&quot; |
| **Agendamento e tempo** | &quot;Quando a campanha [ID] está agendada para execução?&quot; / &quot;A campanha [ID] é um envio ou recorrente único?&quot; |
| **Solução de problemas** | &quot;Por que a campanha [ID] pode não estar sendo enviada?&quot; / &quot;Revise a configuração da campanha [ID] para qualquer problema.&quot; |
| **Configuração de canais** | &quot;Quais predefinições de canal estão disponíveis na minha sandbox?&quot; / &quot;Mostre-me todas as minhas configurações de canal de email.&quot; |
| **Auditoria de canal** | &quot;Quais configurações de canal estão ausentes ou incompletas?&quot; / &quot;Quantas configurações de canal eu tenho em todos os canais?&quot; |

## Pré-requisitos {#mcp-prerequisites}

Antes de conectar o servidor MCP [!DNL Adobe Journey Optimizer] ao seu cliente MCP, verifique o seguinte:

* Você tem uma licença [!DNL Adobe Journey Optimizer] ativa.
* Você tem acesso a um aplicativo compatível com MCP (atualmente Claude Web ou Claude Desktop).
* Você tem as permissões necessárias em [!DNL Adobe Journey Optimizer] para exibir campanhas e ofertas.

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

## Limitações conhecidas (Beta) {#mcp-limitations}

As seguintes limitações se aplicam à versão atual do Beta do servidor MCP [!DNL Adobe Journey Optimizer]:

| Limitação | Descrição | Solução alternativa |
|---|---|---|
| **Nenhum envolvimento ou métrica de desempenho** | O servidor MCP não expõe dados de relatório. As ferramentas não retornam impressões, taxas de click-through, conversões ou estatísticas de delivery. | Use a interface do usuário de relatórios do AJO, o CJA MCP ou o Adobe Analytics MCP para métricas. O Serviço de consulta da AEP pode consultar dados brutos do evento usando a ID de execução da campanha. |
| **A paginação da lista de campanhas é limitada** | `List Campaigns` sempre retorna a primeira página de resultados (até 50 campanhas, classificadas alfabeticamente). Os valores de deslocamento e limite não são aplicados, tornando a enumeração completa impraticável para sandboxes grandes. | Use `Get Campaign` diretamente se a ID ou o nome da campanha for conhecido. Use a interface do usuário do AJO para navegar e filtrar a lista completa. |
| **Nenhuma filtragem do lado do servidor por data, canal ou agenda** | `List Campaigns` dá suporte apenas à filtragem por status. A filtragem por data de publicação, data de agendamento, canal ou tipo de campanha não está disponível no lado do servidor. | Use a lista de campanha da interface do usuário do AJO, que é compatível com filtragem de data e canal nativa. |
| **Recuperação de conteúdo de mensagem indisponível** | A ferramenta de conteúdo de mensagens retorna HTTP 502 para todos os tipos de canal (email, baseado em código e outros). O HTML de mensagem, as linhas de assunto, os tokens de personalização e o conteúdo da oferta não podem ser recuperados via MCP. | Exiba o conteúdo da mensagem e os tokens de personalização diretamente na interface do AJO em **Campanhas > [Campanha] > Conteúdo**. |

## Perguntas frequentes {#mcp-faq}

+++Quais clientes MCP são compatíveis?

O servidor MCP [!DNL Adobe Journey Optimizer] está disponível atualmente para o **Claude Web** e o **Claude Desktop**. O suporte para aplicativos adicionais compatíveis com MCP poderá ser adicionado em versões futuras.
+++

+++Quais objetos do [!DNL Adobe Journey Optimizer] posso acessar via MCP?

Você pode acessar campanhas, ofertas, dados de fidelidade e informações da sandbox. As operações são somente leitura (recuperar APIs); as operações de gravação não são compatíveis com a versão atual.
+++

+++Preciso de acesso de desenvolvedor para usar o servidor MCP [!DNL Adobe Journey Optimizer]?

Não. O servidor MCP foi projetado para personas técnicas e de marketing. Os profissionais de marketing podem interagir com ele usando prompts de linguagem natural em qualquer cliente MCP compatível, enquanto os desenvolvedores também podem usá-lo nas ferramentas de desenvolvedor que oferecem suporte ao MCP.
+++

+++Meus dados são enviados ao provedor do cliente MCP?

Ao enviar um prompt, o cliente MCP pode enviar o contexto relevante (incluindo os dados [!DNL Adobe Journey Optimizer] retornados pelo servidor MCP) ao seu modelo para processamento. Analise as políticas de privacidade e manuseio de dados do seu provedor de cliente MCP antes de se conectar aos dados de produção.
+++

+++Quais permissões são necessárias para o [!DNL Adobe Journey Optimizer]?

Você precisa de no mínimo **permissões de Visualização** para os objetos que deseja consultar — campanhas ou ofertas. Nenhuma permissão de gravação é necessária porque o servidor MCP executa somente operações de leitura. Entre em contato com o administrador do [!DNL Adobe Journey Optimizer] se não tiver certeza sobre o seu nível de acesso atual.
+++

+++Posso usar o servidor MCP em ambientes de sandbox?

Sim. O servidor MCP respeita a configuração da sandbox do [!DNL Adobe Journey Optimizer]. Você pode consultar dados específicos da sandbox especificando a sandbox no seu prompt ou conectando-se com credenciais com escopo para uma sandbox específica.
+++
