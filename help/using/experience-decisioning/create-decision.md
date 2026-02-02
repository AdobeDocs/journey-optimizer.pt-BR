---
title: Introdução às políticas de decisões
description: Saiba como trabalhar com decisões e políticas para fornecer ofertas.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: 6cfea1a34cb004d4028f190be92d8365f90de6b2
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 27%

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

➡️ [Conheça este recurso no vídeo](#video)

## Medidas de proteção e limitações

* **Canais com suporte** - As políticas de decisão estão disponíveis para estes canais: experiência baseada em código, email e notificações por push.
* **Requisito do SDK para notificações por push** - A Experience Decisioning com notificações por push requer uma versão específica do Mobile SDK. Antes de implementar este recurso, verifique as [notas de versão](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"} para identificar a versão necessária e se você atualizou adequadamente. Você também pode exibir todas as versões do SDK disponíveis para sua plataforma [nesta seção](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}.
* **Mirror pages de email** - Por enquanto, os itens de decisão não são renderizados em mirror pages de email.
* **Tipo de rastreamento e links** - Para rastrear links gerados pela decisão, defina-os no esquema como &quot;Assets de decisão&quot;. Os links baseados em atributos não são rastreáveis.
* **Aninhamento da política de decisão em emails** - Não é possível aninhar várias políticas de decisão em um componente de email principal que já tenha uma política de decisão associada.
* **jornadas/campanhas duplicadas com decisão** - Se você duplicar uma jornada ou campanha que inclui uma política de decisão, a versão duplicada fará referência ao email original ou à experiência baseada em código, causando erros. Sempre reconfigure a política de decisão após a duplicação.
* **Políticas de consentimento** - As atualizações das políticas de consentimento levam até 48 horas para entrarem em vigor. Se uma política de decisão fizer referência a um atributo vinculado a uma política de consentimento atualizada recentemente, as alterações não serão aplicadas imediatamente.

  Da mesma forma, se novos atributos de perfil sujeitos a uma política de consentimento forem adicionados a uma política de decisão, eles serão utilizáveis, mas a política de consentimento associada a eles não será aplicada até que o atraso tenha passado.

  As políticas de consentimento só estão disponíveis para organizações com o Adobe Healthcare Shield ou o complemento Privacy and Security Shield.

* **Classificação de IA** - Por enquanto, a classificação de IA não é compatível com o canal de email em jornadas com decisão.

* **Modelos de conteúdo** - Qualquer política de decisão configurada no conteúdo não será salva no modelo. Se você aplicar o modelo a outra ação, precisará reconfigurar a política.

## Principais etapas {#key}

As principais etapas para aproveitar as políticas de decisão nas mensagens são as seguintes:

1. **Criar uma política de decisão**

   Adicione uma política de decisão em sua mensagem e configure o número de itens a serem retornados, a estratégia de seleção e as opções de fallback.

   ➡️ [Saiba como criar uma política de decisão](../experience-decisioning/create-decision-policy.md)

1. **Usar a política de decisão em seu conteúdo**

   Personalize o conteúdo com a saída da política de decisão inserindo os atributos dos itens de decisão que deseja exibir na mensagem

   ➡️ [Saiba como usar políticas de decisão em mensagens](../experience-decisioning/create-decision-policy.md)

## Vídeos tutoriais {#video}

Saiba como usar o Decisioning para personalizar emails para seu público-alvo.

>[!VIDEO](https://video.tv.adobe.com/v/3479215?captions=por_br&quality=12)

Saiba como usar o Decisioning para personalizar notificações por push para seu público-alvo.

>[!VIDEO](https://video.tv.adobe.com/v/3479215?captions=por_br&quality=12)
