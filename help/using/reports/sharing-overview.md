---
title: Visão geral do compartilhamento de etapas da jornada
description: Visão geral do compartilhamento de etapas da jornada
feature: Relatórios
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 7%

---

# Criar relatórios de jornada{#design-jo-reports}

Além dos [relatórios em tempo real](live-report.md) e dos [recursos de relatórios globais](global-report.md) integrados, [!DNL Journey Optimizer] podem enviar automaticamente os dados de desempenho do jornada para o Adobe Experience Platform, para que possam ser combinados com outros dados para fins de análise.

>[!NOTE]
>
>Esse recurso é ativado por padrão em todas as instâncias para eventos de etapas do jornada. Para eventos de etapa do perfil do jornada, a ativação é feita mediante solicitação. Os esquemas e conjuntos de dados criados durante o provisionamento para esse recurso não devem ser alterados.

Por exemplo, você configurou uma jornada que envia vários emails. Esse recurso permite combinar [!DNL Journey Optimizer] dados com dados de evento downstream, como quantas conversões ocorreram, quanto envolvimento aconteceu no site ou quantas transações ocorreram na loja. As informações de jornada podem ser combinadas com dados no Adobe Experience Platform, de outras propriedades digitais ou de propriedades offline, para fornecer uma visão mais abrangente do desempenho.

[!DNL Journey Optimizer] O cria automaticamente os esquemas e fluxos necessários em conjuntos de dados para a Adobe Experience Platform para cada etapa que um indivíduo faz em uma jornada. Um evento de etapa corresponde a um indivíduo que se move de um nó para outro em uma jornada. Por exemplo, em uma jornada que tem um evento, uma condição e uma ação, três eventos de etapa são enviados para o Adobe Experience Platform.

A lista de campos XDM que são passados é abrangente. Alguns contêm códigos gerados pelo sistema e outros têm nomes amigáveis legíveis. Os exemplos incluem o rótulo da atividade de jornada ou o status da etapa: quantas vezes uma ação atingiu o tempo limite ou terminou com erro.

>[!CAUTION]
>
>Os conjuntos de dados não podem ser ativados para o serviço de perfil em tempo real. Certifique-se de que a opção **[!UICONTROL Profile]** esteja desligada.

O Jornada envia dados conforme ocorre, de forma contínua. Você pode consultar esses dados usando o Serviço de query. Você pode se conectar ao Customer Journey Analytics ou a outras ferramentas de BI para exibir dados relacionados a essas etapas.

Os seguintes esquemas são criados:

* Schema de Evento de perfil de etapa de Jornada para [!DNL Journey Orchestration] - Eventos de experiência para as etapas executadas em uma Jornada junto com um Mapa de identidade a ser usado para mapear para um Participante de Jornada individual.
* Jornada esquema de evento de etapa para [!DNL Journey Orchestration] - Jornada evento de etapa vinculado a um Metadado de Jornada.
* Jornada esquema com Campos de Jornada para [!DNL Journey Orchestration] - Jornada metadados para descrever Jornadas.

![](../assets/sharing1.png)

![](../assets/sharing2.png)

Os seguintes conjuntos de dados são transmitidos:

* Esquema de Evento de Perfil de Etapa de Jornada para [!DNL Journey Orchestration]
* Jornada de eventos em etapas
* Jornadas

![](../assets/sharing3.png)

As listas de campos XDM passados para o Adobe Experience Platform são detalhadas aqui:

* [campos comuns de eventos journeySteps](../reports/sharing-common-fields.md)
* [campos de execução de ação de eventos journeyStep](../reports/sharing-execution-fields.md)
* [campos de busca de dados de eventos journeyStep](../reports/sharing-fetch-fields.md)
* [campos de identidade do evento journeyStep](../reports/sharing-identity-fields.md)
* [campos de jornada](../reports/sharing-journey-fields.md)

Para obter mais informações sobre eventos de etapa relatados para o Adobe Experience Platform, assista a este [vídeo tutorial](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/reporting-step-events-to-adobe-experience-platform.html){target=&quot;_blank&quot;}.
