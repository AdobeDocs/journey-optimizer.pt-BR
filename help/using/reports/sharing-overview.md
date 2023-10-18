---
solution: Journey Optimizer
product: journey optimizer
title: Visão geral do compartilhamento de etapas da jornada
description: Visão geral do compartilhamento de etapas da jornada
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 7%

---

# Criar relatórios de jornada {#design-jo-reports}

Além de [relatórios em tempo real](live-report.md) e incorporada [recursos de relatórios globais](global-report.md), [!DNL Journey Optimizer] O pode enviar automaticamente dados de desempenho do jornada para a Adobe Experience Platform, para que possa ser combinado com outros dados para fins de análise.

>[!NOTE]
>
>Esse recurso é ativado por padrão em todas as instâncias para eventos de etapas de jornada. Não é possível modificar ou atualizar os esquemas e conjuntos de dados que foram criados durante o provisionamento para eventos da etapa. Por padrão, esses esquemas e conjuntos de dados estão no modo somente leitura.

Por exemplo, você configurou uma jornada que envia vários emails. Esse recurso permite combinar [!DNL Journey Optimizer] dados com dados de evento downstream, como quantas conversões ocorreram, quanto engajamento aconteceu no site ou quantas transações ocorreram na loja. As informações da jornada podem ser combinadas com dados no Adobe Experience Platform, a partir de outras propriedades digitais ou de propriedades offline, para fornecer uma visualização mais abrangente do desempenho.

[!DNL Journey Optimizer] O cria automaticamente os esquemas e fluxos necessários em conjuntos de dados para a Adobe Experience Platform para cada etapa que um indivíduo realiza em uma jornada. Um evento de etapa corresponde a um indivíduo movendo-se de um nó para outro em uma jornada. Por exemplo, em uma jornada que tenha um evento, uma condição e uma ação, os eventos de três etapas são enviados para o Adobe Experience Platform.

A lista de campos XDM transmitidos é abrangente. Alguns contêm códigos gerados pelo sistema e outros têm nomes amigáveis legíveis. Os exemplos incluem o rótulo da atividade de jornada ou o status da etapa: quantas vezes uma ação atingiu o tempo limite ou terminou com erro.

>[!CAUTION]
>
>Os conjuntos de dados não podem ser ativados para o serviço de perfil em tempo real. Certifique-se de que o **[!UICONTROL Perfil]** a opção de alternância está desativada.

[!DNL Journey Optimizer] O envia dados conforme ocorrem, de forma streaming. Você pode consultar esses dados usando o Serviço de consulta. É possível conectar-se ao Customer Journey Analytics ou a outras ferramentas de BI para visualizar dados relacionados a essas etapas.

Os seguintes esquemas são criados:

* Esquema de evento de etapa de Jornada para [!DNL Journey Orchestration] - Evento de etapa de Jornada vinculado a Metadados de Jornada.
* Jornada esquema com campos de Jornada para [!DNL Journey Orchestration] - Jornada metadados para descrever Jornadas.

![](assets/sharing1.png)

![](assets/sharing2.png)

Os seguintes conjuntos de dados são transmitidos:

* Jornada eventos de etapa
* Jornadas

![](assets/sharing3.png)

As listas de campos XDM transmitidas para o Adobe Experience Platform estão detalhadas aqui:

* [Lista de campos de evento de etapa](../reports/sharing-field-list.md)
* [Campos de evento de etapa herdado](../reports/sharing-legacy-fields.md)

## Integração com o Customer Journey Analytics {#integration-cja}

[!DNL Journey Optimizer] Os eventos de etapa podem ser vinculados a outros conjuntos de dados no [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=pt-BR){target="_blank"}.

O fluxo de trabalho geral é:

* [!DNL Customer Journey Analytics] A assimila o conjunto de dados &quot;Evento de etapa de Jornada&quot;.
* A variável **profileID** no &quot;Esquema de evento de etapa de Jornada para Journey Orchestration&quot; associado, é definido como um campo de identidade. Entrada [!DNL Customer Journey Analytics], você pode vincular esse conjunto de dados a qualquer outro que tenha o mesmo valor que o identificador com base em pessoas.
* Para usar esse conjunto de dados no [!DNL Customer Journey Analytics], para análise de jornada entre canais, consulte [Documentação do Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html?lang=pt-BR){target="_blank"}.

