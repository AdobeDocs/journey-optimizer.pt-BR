---
solution: Journey Optimizer
product: journey optimizer
title: Principal terminologia
description: Termos e conceitos essenciais no Adobe Journey Optimizer
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 965bb76529f500d6fa4d89fa1d56979afe9d5bb0
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 8%

---

# Terminologia principal {#key-terminology}

Este guia de referência define os termos essenciais que você encontrará ao usar o Adobe Journey Optimizer. A compreensão desses conceitos ajuda você a navegar na plataforma com confiança e a colaborar efetivamente com a sua equipe.

>[!TIP]
>
>Para obter explicações detalhadas sobre recursos e fluxos de trabalho, consulte as seções específicas de documentação vinculadas neste guia.

## Termos principais da plataforma {#core-terms}

| Termo | Definição |
|------|------------|
| **Adobe Journey Optimizer (AJO)** | Um aplicativo para criar e entregar mensagens personalizadas aos clientes por canais (email, SMS, notificações por push, Web). Ele permite projetar jornadas de clientes que respondem às ações do cliente em tempo real. |
| **Adobe Experience Platform (AEP)** | A base da Adobe Journey Optimizer que coleta e organiza todos os dados do cliente em um único local. Ele cria perfis unificados do cliente que o Journey Optimizer usa para personalização. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=pt-BR){target="_blank"} |
| **Perfil do cliente em tempo real** | Uma visualização unificada em tempo real de cada cliente que combina dados de vários canais, incluindo dados online, offline, de CRM e de terceiros. Cada perfil é atualizado dinamicamente à medida que os clientes interagem com sua marca. [Saiba mais](../audience/get-started-profiles.md) |
| **Sandbox** | Um espaço de trabalho separado para testes e experimentação sem afetar as comunicações ao vivo do cliente. A Adobe Journey Optimizer fornece várias sandboxes para ambientes de desenvolvimento, teste e produção. [Saiba mais](../administration/sandboxes.md) |

## Termos de Jornada e campanha {#journey-campaign-terms}

| Termo | Definição |
|------|------------|
| **Jornada** | Uma série de etapas conectadas que orientam os clientes pelas experiências com sua marca ao longo do tempo. Cada etapa ocorre com base nas ações do cliente ou nos acionadores de tempo, permitindo interações sequenciais e personalizadas. [Saiba mais](../building-journeys/journey.md) |
| **Campaign** | Uma única comunicação ou conjunto de comunicações enviado para um público-alvo específico. Diferentemente das jornadas que se desdobram com o tempo, as campanhas entregam mensagens de acordo com uma programação ou um acionador, imediatamente ou em um horário específico. [Saiba mais](../campaigns/get-started-with-campaigns.md) |
| **Evento** | Uma ação ou ocorrência que aciona ou avança uma jornada. Os eventos podem ser ações do cliente (fazer uma compra, abandonar um carrinho) ou eventos do sistema (data/hora, alteração de dados). [Saiba mais](../event/about-events.md) |
| **Canal** | O método usado para se comunicar com os clientes: email, SMS, notificações por push, mensagens no aplicativo, Web ou correspondência direta. Cada canal requer uma configuração específica. [Saiba mais](../configuration/get-started-configuration.md) |

## Termos de cliente e público-alvo {#customer-audience-terms}

| Termo | Definição |
|------|------------|
| **Público-alvo** | Um grupo de clientes que compartilham características ou comportamentos comuns, como &quot;clientes que compraram nos últimos 30 dias&quot; ou &quot;membros de programa de fidelidade&quot;. Os públicos-alvo são usados para direcionar segmentos específicos de clientes. [Saiba mais](../audience/about-audiences.md) |
| **Qualificação de público-alvo** | O processo automático que ocorre quando um cliente entra ou sai de um público-alvo. O Journey Optimizer pode acionar ações quando alguém entrar ou sair de um público-alvo, garantindo comunicações oportunas e relevantes. [Saiba mais](../building-journeys/audience-qualification-events.md) |
| **Público-alvo envolvente** | O número de perfis de clientes que você pode contatar ativamente por meio do Adobe Journey Optimizer com base no contrato de licença. Normalmente, refere-se aos perfis envolvidos nos últimos 12 meses. |
| **Perfil de Teste** | Perfis fictícios usados para testar e visualizar mensagens antes de enviá-las para clientes reais. Os perfis de teste ajudam a verificar a personalização, o conteúdo e a lógica da jornada. [Saiba mais](../audience/creating-test-profiles.md) |

## Termos de conteúdo e Personalization {#content-terms}

| Termo | Definição |
|------|------------|
| **Personalização** | O processo de personalizar o conteúdo para clientes individuais usando os dados de perfil, as preferências e os comportamentos. Por exemplo, inserir o nome de um cliente ou mostrar recomendações de produto com base no histórico de navegação. [Saiba mais](../personalization/personalize.md) |
| **Modelo de conteúdo** | Um design de mensagem reutilizável que pode ser usado em várias campanhas e jornadas para manter a consistência da marca e acelerar a criação de conteúdo. [Saiba mais](../content-management/content-templates.md) |
| **Fragmento** | Um bloco de conteúdo reutilizável (como cabeçalho, rodapé ou banner promocional) que pode ser usado em várias mensagens para garantir consistência e permitir atualizações centralizadas. [Saiba mais](../content-management/fragments.md) |
| **Página de aterrissagem** | Uma página da Web independente em que os clientes podem aceitar ou recusar comunicações, assinar serviços ou fornecer informações por meio de formulários online. [Saiba mais](../landing-pages/get-started-lp.md) |

## Termos de decisão e oferta {#decision-terms}

| Termo | Definição |
|------|------------|
| **Gestão de decisões** | Um recurso que seleciona automaticamente o melhor conteúdo ou oferta para cada cliente com base em dados de perfil em tempo real, contexto e regras de negócios. [Saiba mais](../offers/get-started/starting-offer-decisioning.md) |
| **Oferta** | Uma mensagem de marketing, desconto ou promoção que pode ser apresentada aos clientes. As ofertas incluem regras de qualificação que determinam quais clientes podem recebê-las. [Saiba mais](../offers/offer-library/creating-personalized-offers.md) |
| **Política de decisão** | Um conjunto de regras e estratégias que determinam qual oferta mostrar a qual cliente em que momento, com base em restrições como elegibilidade, prioridade e regras de limite. [Saiba mais](../experience-decisioning/create-decision.md) |

## Dados e termos de configuração {#data-config-terms}

| Termo | Definição |
|------|------------|
| **Esquema** | A estrutura que define como os dados são organizados no Adobe Experience Platform, incluindo nomes de campo, tipos de dados e relacionamentos. Os esquemas garantem a consistência dos dados em todos os sistemas. [Saiba mais](../data/get-started-schemas.md) |
| **Conjunto de dados** | Uma coleção de dados (geralmente uma tabela) que segue um schema específico. Os conjuntos de dados armazenam dados do cliente, eventos de interação e outras informações usadas para personalização. [Saiba mais](../data/get-started-datasets.md) |

>[!NOTE]
>
>Para ver um glossário abrangente de termos do Adobe Experience Platform, consulte o [glossário do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html?lang=pt-BR){target="_blank"}.

## Tópicos relacionados {#related-topics}

* [Entender como o Journey Optimizer funciona](understanding-ajo.md)
* [Introdução à interface do usuário](user-interface.md)
* [Escolha sua função e o caminho de aprendizagem](quick-start.md)

