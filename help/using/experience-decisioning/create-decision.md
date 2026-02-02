---
title: Introdução às políticas de decisões
description: Saiba como trabalhar com decisões e políticas para fornecer ofertas.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: c2388c84346ed9a0409270fd96f3a1458bf8ad88
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 29%

---

# Introdução às políticas de decisão {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="O que é uma decisão?"
>abstract="As políticas de decisão contêm toda a lógica de seleção, para que o mecanismo de decisão escolha o melhor conteúdo. As políticas de decisão são específicas de cada campanha. Sua finalidade é selecionar as melhores ofertas para cada perfil, enquanto a criação da campanha permite indicar como os itens de decisão selecionados devem ser apresentados, incluindo quais atributos dos itens devem ser incluídos na mensagem."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Sobre a decisão"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="Defina uma política de decisão"
>abstract="Uma política de decisão permite selecionar os melhores itens do mecanismo de decisão e entregá-los ao público-alvo correto."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Sobre a decisão"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="Política de decisão"
>abstract="Uma política de decisão permite selecionar os melhores itens do mecanismo de decisão e entregá-los a cada público-alvo."

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="Posicionamento"
>abstract="Um posicionamento determina onde os itens retornados do mecanismo de decisão aparecem em uma mensagem. Você pode acompanhar o desempenho em diferentes posicionamentos nos relatórios."

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="Selecionar atributos de decisão do catálogo"
>abstract="Os atributos de decisão são armazenados no esquema do catálogo. Selecione um atributo que deseja usar aqui no catálogo selecionado."

As políticas de decisão são containers para suas ofertas que aproveitam o mecanismo de decisão para retornar dinamicamente o melhor conteúdo a ser entregue para cada membro do público. O objetivo é selecionar as melhores ofertas para cada perfil, enquanto a criação de campanha/jornada permite indicar como os itens de decisão selecionados devem ser apresentados, incluindo quais atributos de item devem ser incluídos na mensagem.

>[!AVAILABILITY]
>
>Por enquanto, as políticas de decisão estão disponíveis para todos os clientes para o Canal de experiência baseado em código. Eles estão disponíveis para o canal de email como uma Disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

## Principais etapas {#key}

As principais etapas para aproveitar as políticas de decisão nas mensagens são as seguintes:

1. [Criar uma política de decisão](../experience-decisioning/create-decision-policy.md)

   Defina uma política de decisão em sua mensagem escolhendo o número de itens a serem retornados, configurando estratégias de seleção, opções de fallback e ordem de avaliação.

1. [Usar a política de decisão em seu conteúdo](../experience-decisioning/use-decision-policy.md)

   Personalize o conteúdo com a saída da política de decisão e os atributos dos itens de decisão que você deseja exibir na mensagem.

1. [Criar painéis de relatórios](cja-reporting.md)

   Crie painéis personalizados do Customer Journey Analytics para medir o desempenho e obter insights sobre como as políticas e ofertas de decisão estão sendo fornecidas e envolvidas.

## Medidas de proteção e limitações

* **Mirror pages de email** - Por enquanto, os itens de decisão não são renderizados em mirror pages de email.
* **Tipo de rastreamento e links** - Para rastrear links gerados pela decisão, defina-os no esquema como &quot;Assets de decisão&quot;. Os links baseados em atributos não são rastreáveis.
* **Aninhamento da política de decisão em emails** - Não é possível aninhar várias políticas de decisão em um componente de email principal que já tenha uma política de decisão associada.
* **jornadas/campanhas duplicadas com decisão** - Se você duplicar uma jornada ou campanha que inclui uma política de decisão, a versão duplicada fará referência ao email original ou à experiência baseada em código, causando erros. Sempre reconfigure a política de decisão após a duplicação.
* **Políticas de consentimento** - As atualizações das políticas de consentimento levam até 48 horas para entrarem em vigor. Se uma política de decisão fizer referência a um atributo vinculado a uma política de consentimento atualizada recentemente, as alterações não serão aplicadas imediatamente.

  Da mesma forma, se novos atributos de perfil sujeitos a uma política de consentimento forem adicionados a uma política de decisão, eles serão utilizáveis, mas a política de consentimento associada a eles não será aplicada até que o atraso tenha passado.

  As políticas de consentimento só estão disponíveis para organizações com o Adobe Healthcare Shield ou o complemento Privacy and Security Shield.

* **Classificação de IA** - Por enquanto, a classificação de IA não é compatível com o canal de email em jornadas com decisão.

## Próximas etapas {#next-steps}

Agora que você entende como as políticas de decisão funcionam e como elas ajudam a fornecer ofertas personalizadas, você está pronto para criar sua primeira política de decisão.

➡️ [Saiba como criar uma política de decisão](../experience-decisioning/create-decision-policy.md)

## Vídeo tutorial {#video}

Saiba como usar o Decisioning para personalizar emails para seu público-alvo.

>[!VIDEO](https://video.tv.adobe.com/v/3479215?captions=por_br&quality=12)
