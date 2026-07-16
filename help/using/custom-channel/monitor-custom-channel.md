---
title: Gerenciar e monitorar canais personalizados
description: Saiba como gerenciar o ciclo de vida de canais personalizados e configurações de canal e monitorar o desempenho do delivery por meio de relatórios do Adobe Journey Optimizer.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 1%

---


# Monitorar canais personalizados {#monitor-custom-channel}

Depois que um canal personalizado é criado e ativado, você pode [gerenciar seu ciclo de vida](create-custom-channel.md#access-channel-builder) e monitorar o desempenho da entrega por meio da interface [!DNL Journey Optimizer].

## Aproveitar os relatórios de campanha e jornada {#reporting}

O [!DNL Journey Optimizer] fornece relatórios prontos para uso para canais personalizados.

As métricas a seguir estão disponíveis para canais personalizados em relatórios ao vivo (24 horas) e global (CJA).<!--TBC and add or replace with CJA link when available-->

| Métrica | Descrição |
|--------|-------------|
| **Tentativas de entrega** | Número total de mensagens enviadas para o ponto de extremidade externo. |
| **Entregas bem-sucedidas** | Mensagens para as quais o ponto de extremidade retornou uma resposta HTTP 2xx. |
| **Perfis direcionados** | Número de perfis únicos atingidos. |
| **Cliques** | Número de cliques em links rastreados na carga. Requer um subdomínio delegado para canais personalizados. |
| **Erros/Falhas** | Número de tentativas de entrega com falha, com detalhamento por motivo de erro. |

Saiba mais sobre [relatórios ao vivo](../reports/live-report.md) e [relatórios globais](../reports/report-gs-cja.md). Para obter detalhes sobre as funcionalidades de relatórios, consulte [esta documentação](../reports/report-cja-manage.md).

<!--
### Journey reports {#journey-reports}

To view delivery data for a custom channel action in a journey:

1. Open the journey from the **[!UICONTROL Journeys]** list.
1. Click **[!UICONTROL View report]** in the top-right area.
   * **[!UICONTROL Live report]** – Data for the last 24 hours.
   * **[!UICONTROL All time]** – Full lifetime data via Customer Journey Analytics (CJA).

### Campaign reports {#campaign-reports}

To view delivery data for a custom channel campaign:

1. Open the campaign from the **[!UICONTROL Campaigns]** list.
1. Click **[!UICONTROL Reports]** in the top-right area.

The campaign report includes execution count, successful deliveries, errors, and click data (if link tracking is enabled).
-->

## Monitorar desempenho da entrega {#monitoring}

Além dos relatórios de campanha e jornada, o [!DNL Journey Optimizer] fornece um painel de monitoramento de canal personalizado dedicado. Acesse-o em **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Construtor de Canais]** > **[!UICONTROL Monitoramento de canais personalizados]**.

![Painel de monitoramento de canal personalizado](assets/custom_channel_monitoring_dashboard.png){width="100%"}

Este painel permite monitorar a confiabilidade e o desempenho das chamadas de API que [!DNL Journey Optimizer] faz aos seus pontos de extremidade externos ao entregar mensagens de canal personalizadas. Use-o para detectar rapidamente problemas de integração, latência e limites de limitação.

O painel **[!UICONTROL Monitoramento de canais personalizados]** funciona como outros relatórios de todos os tempos em [!DNL Journey Optimizer]. Você pode selecionar um intervalo de tempo, filtrar por canal ou endpoint e detalhar para ver as campanhas e jornadas que dependem de cada canal personalizado. [Saiba mais](../reports/report-cja-manage.md)

### Métricas de canal personalizadas {#monitoring-kpis}

A seção **[!UICONTROL Métricas de canal personalizadas]** fornece uma exibição consolidada da integridade operacional e da confiabilidade das suas chamadas de canal personalizadas.

![Métricas de canal personalizadas](assets/custom_channel_metrics.png){width="100%"}

+++ Saiba mais sobre métricas de canal personalizadas

* **[!UICONTROL Chamadas com êxito]**: número total de chamadas HTTP que retornaram uma resposta válida sem erro.

* **[!UICONTROL 4xx/5xx errors]**: número de chamadas com falha devido a erros do lado do cliente (4xx) ou do lado do servidor (5xx), destacando problemas de configuração ou falhas de ponto de extremidade.

* **[!UICONTROL Chamadas de tempo limite]**: número de chamadas que falharam porque excederam o tempo máximo de resposta. Isso ajuda a exibir problemas de latência ou desempenho com pontos de extremidade externos.

* **[!UICONTROL Falhas de pré-chamada]**: Número de envios de canais personalizados que falharam antes da chamada HTTP ter sido feita ao ponto de extremidade externo. Essas falhas ocorrem na própria camada de infraestrutura do [!DNL Journey Optimizer], não no seu sistema externo. Existem três categorias:

  | Categoria | Descrição |
  |----------|-------------|
  | **Falhas de autenticação** (`AUTH_*`) | [!DNL Journey Optimizer] não pôde obter ou atualizar o token OAuth ou as credenciais necessárias para chamar o ponto de extremidade. Verifique se as credenciais de API vinculadas à configuração do canal são válidas e se não expiraram. |
  | **Solicitar erros de geração** (`REQUEST_GENERATION_ERROR`) | [!DNL Journey Optimizer] não pôde construir uma solicitação HTTP válida — por exemplo, porque um modelo de URL não pôde ser resolvido ou um campo de personalização obrigatório estava ausente. |
  | **Erros de análise de HTTP** (`HTTP_PARSE_ERROR`) | [!DNL Journey Optimizer] recebeu uma resposta do ponto de extremidade, mas não pôde analisá-la em uma estrutura utilizável. |

  >[!TIP]
  >
  >As falhas antes da chamada indicam um problema no lado do [!DNL Journey Optimizer] ou na configuração do canal, em vez de um problema com o ponto de extremidade externo. Comece a solução de problemas revisando as credenciais da API e os campos de carga necessários.

* **[!UICONTROL Latência média]**: tempo médio de resposta de ponta a ponta (em milissegundos) para todas as chamadas HTTP, incluindo chamadas bem-sucedidas, erros e tempos limite.

<!--
* **[!UICONTROL Capped calls]**: Number of calls that were blocked due to capping limits, ensuring downstream systems are not overloaded.

* **[!UICONTROL Average RPS]**: Number of requests per second processed by the custom channel over the selected time range.

* **[!UICONTROL Average successful latency]**: Average end-to-end response time (in milliseconds) for successful calls only, excluding failed requests and timeouts.

* **[!UICONTROL Average queue time]**: Average time (in milliseconds) calls spent waiting in the execution queue before being sent. This only applies to throttled endpoints, where [!DNL Journey Optimizer] queues calls when the throughput limit is reached.
-->

+++

### Resultados dos canais personalizados ao longo do tempo {#outcomes-overtime}

![Resultados do canal personalizado ao longo do tempo](assets/custom_channel_metrics.png){width="100%"}

O gráfico **[!UICONTROL Resultados dos canais personalizados ao longo do tempo]** mostra a tendência do KPI de chamadas HTTP ao longo do período selecionado. A granularidade da série temporal depende do intervalo de tempo selecionado:

* Para um relatório de 7 dias, cada ponto de dados mostra os KPIs para um dia.
* Para um intervalo de tempo de 1 dia, o gráfico mostra os KPIs por hora.
* Para um intervalo de tempo de 1 hora, o gráfico mostra os KPIs por minuto.

### Latência ao longo do tempo {#latency-overtime}

![Latência de canal personalizada ao longo do tempo](assets/custom_channel_latency.png){width="100%"}

O gráfico **[!UICONTROL Latência ao longo do tempo]** visualiza a tendência das métricas de latência ao longo do período selecionado. Essa visualização de série temporal permite rastrear padrões de desempenho, identificar períodos de latência de pico e monitorar o impacto de otimizações ou alterações do sistema ao longo do tempo.

### Detalhamento do resultado do canal personalizado {#outcome-breakdown}

![Detalhamento personalizado do resultado do canal](assets/custom_channel_latency.png){width="100%"}

A tabela **[!UICONTROL Detalhamento personalizado dos resultados do canal]** fornece um detalhamento hierárquico das métricas de chamada HTTP — desde as métricas gerais por ponto de extremidade no nível superior até as métricas por canal personalizado usando esse ponto de extremidade, passando pelas campanhas e jornadas que dependem delas no nível inferior.

### Detalhamento de latência {#latency-breakdown}

A tabela **[!UICONTROL Detalhamento de latência]** fornece um detalhamento das métricas de latência em seus canais personalizados. Essa visualização ajuda a identificar quais endpoints ou canais específicos estão tendo problemas de desempenho, permitindo que você identifique e resolva gargalos de latência de maneira eficaz.

### Insight Builder {#insight-builder}

Use o **[!UICONTROL Insight Builder]** para criar visualizações e painéis personalizados com base nas métricas de canal personalizadas. Essa ferramenta permite combinar vários KPIs, aplicar filtros e criar exibições personalizadas que se alinhem às suas necessidades de monitoramento e relatórios. [Saiba mais](../reports/report-cja-manage.md#insight-builder)

## Solução de problemas {#troubleshooting}

Se você encontrar problemas com seu canal personalizado, a tabela a seguir lista sintomas comuns, possíveis causas e resoluções recomendadas.

| Sintoma | Causa possível | Resolução |
|---------|----------------|------------|
| **HTTP 401 / 403 erros** | Falha de autenticação — credenciais expiradas ou incorretas. | Atualize as credenciais em **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Credenciais de API]**. |
| **HTTP 429 erros** | O ponto de extremidade externo está limitando as solicitações de [!DNL Journey Optimizer]. | Revise os limites de taxa do seu ponto de extremidade. Reduza a configuração de limitação na configuração de política do Channel Builder. |
| **HTTP 5xx errors** | O sistema externo está inativo ou retorna erros do servidor. | Verifique o painel de integridade do sistema externo. Configure caminhos de erro na atividade de ação de jornada para lidar com falhas transitórias normalmente. |
| **Tokens de personalização não resolvidos** | A expressão faz referência a um atributo que não está presente no perfil. | Verifique se o caminho do atributo XDM está correto. Adicionar um valor padrão de fallback: `{{profile.person.name.firstName \| default("Valued Customer")}}`. |
| **Erro de validação de campo obrigatório** | Um campo de conteúdo obrigatório não tem valor no momento da criação. | Verifique se todos os campos obrigatórios estão preenchidos no editor de conteúdo. Como alternativa, remova a restrição necessária no Construtor de canais se o campo for realmente opcional. |

<!--
## Related resources {#related}

* [Get started with custom channels](get-started-custom-channel.md)
* [Configure a custom channel](custom-channel-configuration.md)
* [Global report overview](../reports/report-gs-cja.md)
* [Journey live report](../reports/live-report.md
-->