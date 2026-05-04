---
solution: Journey Optimizer
product: journey optimizer
title: Perguntas frequentes sobre integrações
description: Perguntas frequentes sobre integrações do Journey Optimizer para dados externos e conteúdo em mensagens.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: integração, Perguntas frequentes, dados externos, personalização
source-git-commit: 4cc3c959fe08c1d574a5d041bf7721441bc96f97
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 1%

---

# Perguntas frequentes sobre integrações {#vendor-integration-faq}

Abaixo estão perguntas frequentes sobre **Integrações** no Adobe Journey Optimizer.


## Introdução

+++ O que as integrações fazem no Journey Optimizer?

Ele conecta fontes de dados externas ao Journey Optimizer para que você possa extrair conteúdo e dados de sistemas de terceiros em suas campanhas e jornadas e personalizar mensagens usando esses dados.

➡️ [Saiba mais sobre a visão geral de Integrações](integrations.md)

+++

+++ Quem configura as Integrações e quem as usa no conteúdo?

Os administradores criam e ativam a configuração técnica (**[!UICONTROL Configurações]** > **[!UICONTROL Integrações]** > **[!UICONTROL Gerenciar]** > **[!UICONTROL Criar Integração]**). Os profissionais de marketing usam **[!UICONTROL Adicionar personalização]** em componentes de Texto ou HTML, abrir **[!UICONTROL Integrações]**, escolher uma integração ativa e mapear atributos.

➡️ [Saiba mais sobre fluxos de trabalho de administrador e de profissional de marketing](integrations.md)

+++

+++ Onde criar ou gerenciar integrações na interface do usuário como administrador?

Vá para a seção **[!UICONTROL Configurações]** no menu esquerdo, abra **[!UICONTROL Gerenciar]** no cartão **[!UICONTROL Integrações]** e selecione **[!UICONTROL Criar Integração]**.

➡️ [Saiba mais sobre como criar uma integração](integrations.md#configure)

+++

+++ Quais são os casos de uso comuns para integrações?

Os exemplos incluem pontos de recompensa de sistemas de fidelidade, informações sobre preço do produto, recomendações de mecanismos de recomendação e atualizações de logística, como status de entrega.

➡️ [Saiba mais sobre dados de exemplo de sistemas de terceiros](integrations.md)

➡️ [Saiba mais sobre exemplos de integração de fornecedor](vendor-integration.md)

+++

## Configuração

+++ Como configurar uma integração em alto nível como administrador?

Você fornece um nome e uma descrição, uma URL de ponto de extremidade de API (opcionalmente com variáveis de caminho), valores de modelo de caminho, **[!UICONTROL GET]** ou **[!UICONTROL POST]**, cabeçalhos e parâmetros de consulta opcionais, um método de autenticação, configurações de política (como tempo limite e cache opcional ou tentativa), uma resposta JSON de exemplo para mapear campos, e executa **[!UICONTROL Enviar conexão de teste]** e **[!UICONTROL Ativar]** quando for válido.

➡️ [Saiba mais sobre a configuração de integração](integrations.md#configure)

+++

+++ Que tipos de autenticação são aceitos?

Estes tipos de autenticação estão disponíveis: **[!UICONTROL Sem autenticação]**, **[!UICONTROL Chave de API]**, **[!UICONTROL Autenticação Básica]** e **[!UICONTROL OAuth 2.0]** (com configuração de carga para OAuth onde aplicável).

➡️ [Saiba mais sobre tipos de autenticação](integrations.md#configure)

+++

+++ Para que a etapa de carga de resposta é usada?

Cole uma amostra de resposta JSON para que o sistema possa detectar tipos de dados e você possa escolher quais campos são expostos para personalização nas mensagens. É possível limitar quais campos estão disponíveis para profissionais de marketing durante a criação.

➡️ [Saiba mais sobre o mapeamento de carga de resposta](integrations.md#configure)

+++

+++ Como os profissionais de marketing adicionam uma integração a uma mensagem?

No conteúdo da campanha ou da jornada, use **[!UICONTROL Adicionar personalização]** em um componente de Texto ou HTML, vá para **[!UICONTROL Integrações]**, selecione uma integração e salve. Com o modo Pills no editor de personalização, você pode mapear valores para variáveis na configuração (como parâmetros de cabeçalho ou consulta ou variáveis de caminho no URL).

➡️ [Saiba mais sobre personalização com Integrações](integrations.md#personalization)

+++

## Recursos e casos de uso

+++ Posso usar integrações em jornadas e campanhas?

Sim. O recurso está disponível para jornadas e campanhas para **canais de saída** (por exemplo, email, SMS e push), dentro dos limites atuais do produto.

➡️ [Saiba mais sobre jornadas e campanhas](integrations.md#limitations)

+++

+++ Posso usar integrações em fragmentos reutilizáveis?

O recurso Integrações é compatível com Fragmentos.

➡️ [Saiba mais sobre fragmentos](aem-fragments-gs.md)

+++

## Limitações

+++ Quais canais oferecem suporte a integrações?

Há suporte para **canais de saída** (por exemplo, email, SMS e push).

➡️ [Saiba mais sobre os canais com suporte](integrations.md#limitations)

+++

+++ Quais formatos de resposta da API são compatíveis?

Para respostas de chamada de API, há suporte para **JSON** e **HTML** para mapeamento de campos. A saída de imagem binária bruta e os formatos que não são JSON não estão disponíveis para este fluxo de trabalho.

➡️ [Saiba mais sobre JSON e formatos de resposta](integrations.md#limitations)

+++

+++ A quais padrões de API posso me conectar?

**Recuperação** APIs que direcionam conteúdo específico são suportadas. Não há suporte para APIs de **Listagem** (lista ampla ou padrões de paginação) neste modelo de integração.

➡️ [Saiba mais sobre recuperação versus APIs de listagem](integrations.md#limitations)

+++

## Permissões e recursos relacionados

+++ Quais permissões são necessárias para configurar integrações?

Para começar a usar Integrações, os usuários precisam receber as permissões **[!UICONTROL Gerenciar configuração de integração do AJO]** e **[!UICONTROL Exibir configuração de integração do AJO]**.

➡️ [Saiba mais sobre permissões de integrações](integrations.md#overview)

+++

+++ As integrações substituem os conectores do Adobe Journey Optimizer nas Fontes do Experience Platform?

Não. **Integrações** são para campos de personalização no conteúdo da mensagem que você orienta das APIs. **Fontes** e outros recursos de assimilação de dados atendem a diferentes objetivos (por exemplo, assimilação de dados em lote e enriquecimento de perfil). Use cada recurso para o escopo desejado.

➡️ [Saiba mais sobre o que são as integrações](integrations.md)

➡️ [Saiba mais sobre Fontes do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=pt-BR){target="_blank"}

+++

## Solução de problemas

+++ Por que a conexão de teste falha ou permanece inválida?

Verifique o URL do endpoint, o método HTTP, os modelos de caminho, os cabeçalhos e parâmetros de consulta, a autenticação e o tempo limite da política. Usar **[!UICONTROL Enviar conexão de teste]** após ajustes. Para problemas de carga, verifique se a amostra reflete um JSON válido e se os campos selecionados correspondem ao que a API retorna.

➡️ [Saiba mais sobre conexão de teste e validação de carga](integrations.md#configure)

+++

+++ Por que os profissionais de marketing não veem minha integração no seletor?

As integrações devem ser **ativadas** após um teste bem-sucedido. Somente integrações ativas aparecem quando os profissionais de marketing abrem **[!UICONTROL Integrações]**. Se a integração ainda for de rascunho ou inativa, conclua a ativação primeiro.

➡️ [Saiba mais sobre conexão de teste e ativação](integrations.md#configure)

+++

## Fornecedores de terceiros

+++ Quais exemplos de fornecedores estão disponíveis e quem protege a API?

É possível integrar o a qualquer plataforma de terceiros que exponha um endpoint de API compatível. Padrões de fornecedor e exemplos de configuração **ilustrativos** podem ajudá-lo a modelar APIs compatíveis. A responsabilidade de proteger os endpoints é da plataforma de terceiros e da sua equipe.

➡️ [Saiba mais sobre os procedimentos de integração de fornecedores](vendor-integration.md)

+++
