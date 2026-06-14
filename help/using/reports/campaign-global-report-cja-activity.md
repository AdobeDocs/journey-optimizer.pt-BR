---
solution: Journey Optimizer
product: journey optimizer
title: Relatório de atividades do Campaign Live
description: Saiba como usar os dados de atividade ao vivo no relatório Campanha
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
exl-id: 58034ec4-62dc-406c-99c4-d6b7aa107140
TQID: https://experienceleague.adobe.com/NBJkyh9TCAPxD0u3EpwaZth7-ePjEWdg2roQ7J2-RuY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 692
ht-degree: 1%

---

# Relatório de campanha de atividade ao vivo {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como ler o relatório Campanha de atividade ao vivo no Adobe Journey Optimizer para rastrear estatísticas de envio, eventos do ciclo de vida da atividade ao vivo, motivos de erro e motivos de exclusão.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Você pode acessar seu relatório de campanha de atividades ao vivo clicando no botão **[!UICONTROL Relatórios]** da campanha e selecionando **[!UICONTROL Exibir relatório de todas as horas]**. [Saiba mais](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Estatísticas de envio {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

A tabela **[!UICONTROL Estatísticas de envio]** fornece uma visão geral detalhada das métricas principais relacionadas à sua campanha de atividades online. Ele exibe informações essenciais, como o tamanho do público-alvo direcionado e o número de atividades ativas entregues com êxito, ajudando você a avaliar o alcance geral e o desempenho da atividade ativa.

+++ Saiba mais sobre como enviar métricas de estatísticas

* **[!UICONTROL Direcionado]**: número de perfis qualificados para o público-alvo antes da aplicação de exclusões, supressões ou remoções de consentimento.

* **[!UICONTROL Envios]**: número total de tentativas de envio de eventos de atividades ao vivo para perfis direcionados.

* **[!UICONTROL Entregue]**: número de eventos de atividade online entregues com êxito aos dispositivos, relativo ao número total de tentativas de envio.

* **[!UICONTROL Enviar erros]**: Número total de eventos de atividade online que não puderam ser enviados devido a erros (por exemplo, tokens inválidos ou problemas de conectividade).

* **[!UICONTROL Exclusões de envio]**: número de perfis excluídos do envio pelo Adobe Journey Optimizer (por exemplo, devido ao status de recusa ou às regras de qualificação).

+++

## Ciclo de vida da atividade ao vivo {#lifecycle}

A tabela **[!UICONTROL Ciclo de vida da atividade em tempo real]** oferece uma visão abrangente de como a atividade em tempo real progride. Ele oferece visibilidade sobre eventos importantes, como início, atualização ou término da atividade, ajudando você a entender melhor o engajamento do usuário e o ciclo de vida geral da campanha de atividades ao vivo.

Os relatórios diferem dependendo se você está usando campanhas transacionais ou de Marketing.

### Atividade Transacional em tempo real

![](assets/activity-lifecycle.png)

Para campanhas transacionais, o relatório Campanha de atividade ao vivo mostra todos os eventos do ciclo de vida, incluindo inícios remotos, inícios locais, atualizações e términos.

+++ Saiba mais sobre as medições de ciclo de vida de atividade em tempo real com campanhas transacionais

* **[!UICONTROL Inicializações remotas]**: número total de eventos de início de atividade online iniciados remotamente, normalmente acionados pelo servidor ou sistemas back-end.

* **[!UICONTROL Inicializações locais]**: número total de eventos de início de atividade online iniciados localmente no dispositivo de um usuário, geralmente resultantes da interação do usuário ou de acionadores do lado do cliente.

* **[!UICONTROL Atualizações]**: número total de atualizações de atividades online enviadas para dispositivos. As atualizações podem incluir alterações de status, novo conteúdo ou notificações de progresso.

* **[!UICONTROL Ends]**: número total de eventos de encerramento de atividades ao vivo enviados para dispositivos.

* **[!UICONTROL Contagem de totais]**: total geral de todos os eventos de ciclo de vida da atividade Live, incluindo inícios, atualizações e términos, fornecendo uma medida completa do volume de atividade Live.

+++

### Atividade de marketing em tempo real

![](assets/activity-lifecycle-broadcast.png)

As campanhas de marketing usam a atividade Live para casos de uso de transmissão, enviando atualizações para vários dispositivos simultaneamente.

Para a atividade do iOS Live em campanhas de marketing, o relatório mostra apenas **[!UICONTROL Remote Starts]** eventos e **[!UICONTROL Remote starts errors]** no início. Os eventos **[!UICONTROL Atualizações]** e **[!UICONTROL Fim]** não são rastreados porque os APNs distribuem atualizações para todos os dispositivos sem fornecer feedback. Para exibir eventos de **[!UICONTROL Atualizações]** e **[!UICONTROL Fim]**, use o [Console de Notificações por Push da Apple](https://developer.apple.com/notifications/push-notifications-console/).

+++ Saiba mais sobre as medições de ciclo de vida da atividade ao vivo com campanhas de marketing

* **[!UICONTROL Inicializações remotas]**: número total de eventos de início de atividade online iniciados remotamente, normalmente acionados pelo servidor ou sistemas back-end.

* **[!UICONTROL Erros de inicializações remotas]**: Número total de erros que ocorreram ao tentar iniciar a atividade Live remotamente (por exemplo, tokens inválidos ou problemas de conectividade).

+++

#### Recuperação de atualizações e contagens finais por meio da API {#retrieving-updates-end-api}

Como alternativa ao uso do console de Notificação por push do Apple, Atualizações e Contagens finais podem ser obtidas por meio de chamadas de API headless.

Ao executar chamadas de API de atualização ou fim para casos de uso de difusão, a resposta inclui uma seção `controlBreakdown` que fornece contadores indicando quantas chamadas de atualização e fim foram executadas para a execução da atividade ativa. Esse bloco está ausente para execuções herdadas sem dados do ciclo de vida. O status de execução também pode ser recuperado explicitamente usando o endpoint GET, quando necessário.

**ATUALIZAR / ENCERRAR Resposta (200 OK)**

```json
{
  "executionId": "HA-exec-abc",
  "campaignId": "campaign-abc-123",
  "campaignVersionId": "v1",
  "audienceId": "audience-segment-id",
  "status": "processing",
  "targetedProfileCount": 150000,
  "createdAt": "2026-02-27T10:00:00Z",
  "executionLifecycle": {
    "lastControlAt": "2026-02-27T10:45:00Z",
    "controlBreakdown": {
      "update": 5,
      "end": 1
    }
  }
}
```

**Status de Execução (GET)**

```
GET /im/executions/audience/{executionId}
```

## Motivos do erro {#error-reasons}

![](assets/error-reasons-activity.png)

A tabela **[!UICONTROL Motivos de erro]** permite identificar os erros específicos que ocorreram durante o processo de envio de sua atividade do Live, facilitando uma análise completa de todos os problemas encontrados.

## Motivos para exclusão {#excluded-reasons}

![](assets/excluded-activity.png)

A tabela **[!UICONTROL Motivos excluídos]** mostra visualmente os diversos fatores que levaram à exclusão de perfis de usuário do público-alvo direcionado, impedindo-o de receber sua atividade Ativa.
