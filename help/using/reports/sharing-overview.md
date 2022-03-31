---
title: Visão geral do compartilhamento de etapas da jornada
description: Visão geral do compartilhamento de etapas da jornada
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 22db9d3997e84d33ddb2febe7a07aaef4063a880
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 5%

---

# Criar relatórios de jornada {#design-jo-reports}

Além de [relatórios em tempo real](live-report.md) e incorporado [recursos de relatórios globais](global-report.md), [!DNL Journey Optimizer] O pode enviar automaticamente os dados de desempenho do jornada para o Adobe Experience Platform, para que possa ser combinado com outros dados para fins de análise.

>[!NOTE]
>
>Esse recurso é ativado por padrão em todas as instâncias para eventos de etapas do jornada. Não é possível modificar ou atualizar os esquemas e conjuntos de dados que foram criados durante o provisionamento para eventos de etapa. Por padrão, esses esquemas e conjuntos de dados estão no modo somente leitura.

Por exemplo, você configurou uma jornada que envia vários emails. Esse recurso permite combinar [!DNL Journey Optimizer] dados com dados de evento downstream como quantas conversões ocorreram, quanto envolvimento aconteceu no site ou quantas transações ocorreram na loja. As informações de jornada podem ser combinadas com dados no Adobe Experience Platform, de outras propriedades digitais ou de propriedades offline, para fornecer uma visão mais abrangente do desempenho.

[!DNL Journey Optimizer] O cria automaticamente os esquemas e fluxos necessários em conjuntos de dados para a Adobe Experience Platform para cada etapa que um indivíduo faz em uma jornada. Um evento de etapa corresponde a um indivíduo que se move de um nó para outro em uma jornada. Por exemplo, em uma jornada que tem um evento, uma condição e uma ação, três eventos de etapa são enviados para o Adobe Experience Platform.

A lista de campos XDM que são passados é abrangente. Alguns contêm códigos gerados pelo sistema e outros têm nomes amigáveis legíveis. Os exemplos incluem o rótulo da atividade de jornada ou o status da etapa: quantas vezes uma ação atingiu o tempo limite ou terminou com erro.

>[!CAUTION]
>
>Os conjuntos de dados não podem ser ativados para o serviço de perfil em tempo real. Certifique-se de que a variável **[!UICONTROL Profile]** está desligado.

[!DNL Journey Optimizer] envia dados conforme ocorre, de forma contínua. Você pode consultar esses dados usando o Serviço de query. Você pode se conectar ao Customer Journey Analytics ou a outras ferramentas de BI para exibir dados relacionados a essas etapas.

Os seguintes esquemas são criados:

* Esquema do Evento de etapa de Jornada para [!DNL Journey Orchestration] - Evento de etapa de Jornada vinculado a um Metadado de Jornada.
* Jornada esquema com Campos de Jornada para [!DNL Journey Orchestration] - Jornada metadados para descrever Jornadas.

![](assets/sharing1.png)

![](assets/sharing2.png)

Os seguintes conjuntos de dados são transmitidos:

* Jornada de eventos em etapas
* Jornadas

![](assets/sharing3.png)

As listas de campos XDM passados para o Adobe Experience Platform são detalhadas aqui:

* [Lista de campos de evento de etapa](../reports/sharing-field-list.md)
* [Campos de evento de etapa herdado](../reports/sharing-legacy-fields.md)

Para obter mais informações sobre os eventos das etapas relatados para o Adobe Experience Platform, assista a isso [vídeo tutorial](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/reporting-step-events-to-adobe-experience-platform.html){target=&quot;_blank&quot;}.

## Integração com o Customer Journey Analytics {#integration-cja}

[!DNL Journey Optimizer] os eventos da etapa podem ser vinculados a outros conjuntos de dados em [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=pt-BR){target=&quot;_blank&quot;}.

O fluxo de trabalho geral é:

* [!DNL Customer Journey Analytics] assimila o conjunto de dados &quot;Evento de etapa do Jornada&quot;.
* O **profileID** no &quot;Jornada Step Event schema for Journey Orchestration&quot; associado é definido como um campo Identity . Em [!DNL Customer Journey Analytics], é possível vincular esse conjunto de dados a qualquer outro conjunto de dados que tenha o mesmo valor do identificador baseado em pessoas.
* Para usar esse conjunto de dados em [!DNL Customer Journey Analytics]para análise de jornada entre canais, consulte [Documentação do Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target=&quot;_blank&quot;}.

