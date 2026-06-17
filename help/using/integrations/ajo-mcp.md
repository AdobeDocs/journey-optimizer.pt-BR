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
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 7ced44f92f816d83d9a9ad667b4322dcb5930741
workflow-type: tm+mt
source-wordcount: 1369
ht-degree: 1%

---

# Trabalhar com clientes MCP {#ajo-mcp}

>[!BEGINSHADEBOX]

**Nesta página:** obtenha uma visão geral passo a passo do servidor MCP [!DNL Adobe Journey Optimizer] — desde as noções básicas do Protocolo de Contexto de Modelo e clientes com suporte até as ferramentas disponíveis, exemplos de prompts, pré-requisitos de configuração, etapas de conexão e respostas a perguntas comuns.

>[!ENDSHADEBOX]

A integração do MCP [!DNL Adobe Journey Optimizer] permite consultar campanhas, jornadas e ofertas usando prompts em linguagem simples, sem gravar chamadas de API ou navegar nas telas dos produtos. Esta página explica como a integração funciona, o que você pode fazer com ela e como começar.

>[!AVAILABILITY]
>
>O servidor MCP [!DNL Adobe Journey Optimizer] está disponível atualmente no **Claude Web**, **Claude Desktop** e **Cursor**. O suporte para outros aplicativos compatíveis com MCP será adicionado em versões futuras.

## Beta, segurança e avisos legais {#mcp-notices}

**aviso sobre a documentação do Beta:** esta documentação abrange um recurso do Beta e não constitui a documentação final. O conteúdo descrito aqui está relacionado a uma versão do Beta e está sujeito a alterações até sua disponibilização geral. A Adobe não faz declarações sobre a integridade ou a precisão desta documentação.

Ao usar o Adobe Journey Optimizer MCP Server (Beta) (&quot;Beta&quot;), você reconhece que o Beta é fornecido **&quot;no estado em que se encontra&quot; sem garantias de qualquer tipo**. A Adobe não tem nenhuma obrigação de manter, corrigir, atualizar, alterar, modificar ou oferecer suporte à Beta. É recomendável ter cuidado e não depender de forma alguma do funcionamento ou desempenho correto desse Beta e/ou dos materiais que o acompanham. O Beta é considerado Informações confidenciais da Adobe. Qualquer &quot;Feedback&quot; (informação sobre o Beta incluindo, mas não se limitando a, problemas ou defeitos encontrados durante o uso do Beta, sugestões, melhorias e recomendações) fornecido por Você ao Adobe é atribuído ao Adobe, incluindo todos os direitos, cargos e interesses no e no Feedback.

>[!WARNING]
>
>O protocolo de contexto de modelo (MCP) é um padrão de código aberto emergente e pode apresentar riscos de segurança ou confiabilidade. As integrações do servidor Adobe MCP e a documentação relacionada são fornecidas &quot;no estado em que se encontram&quot;, sem garantias de nenhum tipo.
>
>Conectar clientes ou servidores MCP a produtos da Adobe é uma configuração selecionada pelo cliente. Os clientes são responsáveis por avaliar a segurança e a adequação de qualquer integração de MCP. O Adobe não é responsável por problemas resultantes de configuração incorreta, uso incorreto do MCP, vulnerabilidades em implementações de terceiros ou ações não intencionais executadas por meio de fluxos de trabalho habilitados para MCP.
>
>Para reduzir os riscos, a Adobe incentiva o teste de integrações em um ambiente de sandbox antes do uso produtivo e a análise e validação cuidadosas de todas as ações e respostas iniciadas pelo MCP antes de confirmar ou confiar nelas.

## Qual é o protocolo de contexto do modelo? {#mcp-overview}

As equipes de marketing e de experiência do cliente dependem cada vez mais de aplicativos baseados em bate-papo e ferramentas de desenvolvedor — como Anthropic Claude, OpenAI ChatGPT, Cursor e Microsoft Copilot Studio — para simplificar seu trabalho diário. Esses aplicativos oferecem suporte ao **Protocolo de Contexto de Modelo (MCP)**, um padrão aberto que permite que os aplicativos exponham ferramentas de back-end a grandes modelos de idioma (LLMs) de maneira uniforme.

[!DNL Adobe Journey Optimizer] agora fornece um servidor MCP que exibe operações de campanha e sandbox diretamente dentro de qualquer aplicativo compatível com MCP. Com a integração do MCP [!DNL Adobe Journey Optimizer], diferentes personalidades podem colaborar pelos mesmos dados de orquestração — sem gravar consultas na API REST [!DNL Adobe Journey Optimizer] ou navegar por várias telas de interface do usuário. Os clientes podem descrever a intenção por conversação e permitir que o LLM chame as ferramentas de MCP apropriadas.

## Principais recursos {#mcp-capabilities}

O servidor MCP [!DNL Adobe Journey Optimizer] permite inspecionar, resumir e solucionar problemas de campanhas, jornadas e ofertas diretamente do seu assistente de IA. Todas as operações são **somente leitura** — as superfícies do servidor MCP recuperam APIs como respostas em linguagem simples para que você possa:

* **Entender a lógica da jornada** — Obtenha um resumo legível de qualquer ramificação, condições e ações da jornada.
* **Obtenha visibilidade instantânea da campanha** — Pergunte sobre os status da campanha e as configurações de canal em linguagem simples e obtenha respostas instantaneamente, sem menus de navegação ou receber relatórios manualmente.
* **Detectar problemas antecipadamente** — Superar campanhas interrompidas, rascunhos órfãos e problemas de configuração de canal no momento em que você pergunta, para que sua equipe possa agir com rapidez.
* **Colaborar com base em dados dinâmicos** — Profissionais de marketing, gerentes de campanha e partes interessadas podem consultar os mesmos dados dinâmicos [!DNL Adobe Journey Optimizer] por meio do assistente de IA, facilitando o alinhamento, a decisão e a movimentação.
* **Auditoria de seu portfólio de orquestração** — Revise o status completo das campanhas sem analisar o JSON ou pular entre telas de produtos.

## Ferramentas disponíveis {#mcp-tools}

As seguintes ferramentas são expostas pelo servidor MCP [!DNL Adobe Journey Optimizer]:

**Ferramentas do Campaign**

| Ferramenta | Descrição |
|---|---|
| **Listar Campanhas** | Navegue pelas campanhas de marketing do [!DNL Adobe Journey Optimizer]. Oferece suporte à filtragem por status (RASCUNHO, EM TEMPO REAL, PARADO, CONCLUÍDO). |
| **Obter Campanha** | Busque detalhes completos e a configuração de uma campanha específica por ID, incluindo o direcionamento de público, a programação, o canal e as configurações de conteúdo. |
| **Listar Configurações de Canal** | Visualize predefinições de superfície e configurações de marca para canais de email, SMS, push ou WhatsApp. |

**ferramentas de Jornada**

| Ferramenta | Descrição |
|---|---|
| **Obter Todas as Jornadas** | Navegue por todas as jornadas em sua sandbox do [!DNL Adobe Journey Optimizer]. |
| **Obter Jornada** | Busque detalhes completos para uma jornada específica por ID, incluindo sua ramificação, condições e ações. |
| **Visualizar suas jornadas** | Renderize suas jornadas com ferramentas interativas para explorar visualmente sua estrutura e fluxo. |

>[!NOTE]
>
>Todas as ferramentas são somente leitura. As operações de gravação (criação, atualização ou exclusão de objetos) não são compatíveis com a versão atual do Beta.

## Casos de uso {#mcp-use-cases}

Os seguintes exemplos mostram como interagir com o servidor MCP [!DNL Adobe Journey Optimizer] usando linguagem natural:

| Meta | Exemplo de prompt |
|---|---|
| **Visão geral da campanha e da jornada** | Mostre todas as minhas campanhas/jornadas do Journey Optimizer / Quantas campanhas/jornadas estão configuradas no Journey Optimizer? |
| **Auditoria de status** | Quais campanhas/jornadas estão ativas no momento? / Liste quaisquer campanhas/jornadas pausadas ou interrompidas. |
| **Detalhes da campanha e da jornada** | Obtenha os detalhes completos da campanha [ID] / Mostre-me tudo configurado na campanha [ID]. / Obtenha os detalhes completos da jornada [ID] / Oriente-me sobre tudo o que foi configurado na jornada [ID]. |
| **Público-alvo e direcionamento** | Qual público-alvo é direcionado na campanha/jornada [ID]? / Quais regras de elegibilidade são definidas na campanha/jornada [ID]? |
| **Agendamento e tempo** | Quando a campanha [ID] está agendada para ser executada? / A campanha [ID] é um envio único ou recorrente? |
| **Solução de problemas** | Por que a campanha [ID] pode não estar sendo enviada? / Revise a configuração da campanha [ID] para quaisquer problemas. |
| **Configuração de canal** | Quais predefinições de canal estão disponíveis na minha sandbox? / Mostre-me todas as minhas configurações de canal de email. |
| **Auditoria de canal** | Quais configurações de canal estão ausentes ou incompletas? / Quantas configurações de canal eu tenho em todos os canais? |

## Pré-requisitos {#mcp-prerequisites}

Antes de conectar o servidor MCP [!DNL Adobe Journey Optimizer] ao seu cliente MCP, verifique o seguinte:

* Você tem uma licença [!DNL Adobe Journey Optimizer] ativa.
* Você tem acesso a um aplicativo compatível com MCP (atualmente Claude Web, Claude Desktop ou Cursor).
* Você tem as permissões necessárias no [!DNL Adobe Journey Optimizer] para exibir campanhas, jornadas e ofertas.

## Conectar o servidor MCP [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Essa integração está no Beta.

Você pode conectar o servidor MCP [!DNL Adobe Journey Optimizer] por meio de seu cliente MCP preferido, incluindo **Claude Web**, **Claude Desktop** e **Cursor**.

**Conectar via cliente MCP**

Ao configurar o servidor MCP no cliente MCP, use o seguinte URL de ponto final do servidor:

`https://ajo-mcp.adobe.io/mcp`

**Conectar via Claude Web ou Claude Desktop**

Para configurar o servidor MCP no Claude Web ou no Claude Desktop, vá para **Connectors** e selecione **Adobe Journey Optimizer**.

## Perguntas frequentes {#mcp-faq}

+++Quais clientes MCP são compatíveis?

O servidor MCP [!DNL Adobe Journey Optimizer] está disponível atualmente para **Claude Web**, **Claude Desktop** e **Cursor**. O suporte para aplicativos adicionais compatíveis com MCP poderá ser adicionado em versões futuras.
+++

+++Quais objetos do [!DNL Adobe Journey Optimizer] posso acessar via MCP?

Você pode acessar campanhas, jornadas, ofertas e informações da sandbox. As operações são somente leitura (recuperar APIs); as operações de gravação não são compatíveis com a versão atual.
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

