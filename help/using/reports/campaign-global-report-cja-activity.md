---
solution: Journey Optimizer
product: journey optimizer
title: Relatório de campanha
description: Saiba como usar os dados de atividade ao vivo no relatório Campanha
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 58034ec4-62dc-406c-99c4-d6b7aa107140
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 2%

---

# Relatório de campanha de atividade ao vivo {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

Você pode acessar seu relatório de campanha de atividades ao vivo clicando no botão **[!UICONTROL Relatórios]** da campanha e selecionando **[!UICONTROL Exibir relatório de todas as horas]**. [Saiba mais](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Estatísticas de envio {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

A tabela **[!UICONTROL Estatísticas de Envio]** fornece uma visão geral detalhada das métricas principais relacionadas às suas campanhas de atividade em tempo real. Ele exibe informações essenciais, como o tamanho do público-alvo e o número de notificações por push entregues com êxito, ajudando você a avaliar o alcance geral e o desempenho de suas notificações por push em tempo real.

+++ Saiba mais sobre como enviar métricas de estatísticas

* **[!UICONTROL Direcionado]**: número de perfis qualificados para o público-alvo antes da aplicação de exclusões, supressões ou remoções de consentimento.

* **[!UICONTROL Envios]**: número total de tentativas de envio de notificações por push a perfis direcionados.

* **[!UICONTROL Entregue]**: número de notificações por push entregues com êxito aos dispositivos, relativo ao número total de tentativas de envio.

* **[!UICONTROL Enviar erros]**: número total de notificações por push que não puderam ser enviadas devido a erros (por exemplo, tokens inválidos ou problemas de conectividade).

* **[!UICONTROL Exclusões de envio]**: número de perfis excluídos do envio pelo Adobe Journey Optimizer (por exemplo, devido ao status de recusa ou às regras de qualificação).

+++

## Ciclo de vida da atividade ao vivo {#lifecycle}

A tabela **[!UICONTROL Ciclo de vida da atividade Live]** oferece uma visão abrangente de como as suas atividades Live avançam ao longo do tempo. Ele oferece visibilidade sobre eventos importantes, como o início, a atualização ou o término das atividades, ajudando você a entender melhor o engajamento do usuário e o ciclo de vida geral das campanhas de atividades Ativas.

Os relatórios diferem dependendo se você está usando campanhas transacionais ou de Marketing.

### Atividades transacionais em tempo real

![](assets/activity-lifecycle.png)

Para campanhas transacionais, o relatório Campanha de atividades online mostra todos os eventos do ciclo de vida, incluindo inícios remotos, inícios locais, atualizações e términos.

+++ Saiba mais sobre as medições de ciclo de vida de atividade em tempo real com campanhas transacionais

* **[!UICONTROL Inicializações remotas]**: número total de eventos de inicialização de atividades online iniciados remotamente, normalmente acionados pelo servidor ou sistemas back-end.

* **[!UICONTROL Inicializações locais]**: número total de eventos de inicialização de atividades online iniciados localmente no dispositivo de um usuário, geralmente resultantes da interação do usuário ou de acionadores do lado do cliente.

* **[!UICONTROL Atualizações]**: número total de atualizações de atividades online enviadas para dispositivos. As atualizações podem incluir alterações de status, novo conteúdo ou notificações de progresso.

* **[!UICONTROL Ends]**: número total de eventos de encerramento de atividades online enviados para dispositivos.

* **[!UICONTROL Contagem de totais]**: total geral de todos os eventos de ciclo de vida da atividade Live, incluindo inícios, atualizações e términos, fornecendo uma medida completa do volume de atividade Live.

+++

### Atividades de marketing ao vivo

![](assets/activity-lifecycle-broadcast.png)

As campanhas de marketing usam atividades em tempo real para casos de uso de transmissão, enviando atualizações para vários dispositivos simultaneamente.

Para atividades do iOS Live em campanhas de marketing, o relatório mostra apenas **[!UICONTROL Remote Starts]** eventos e **[!UICONTROL Remote starts errors]** no início. Os eventos **[!UICONTROL Atualizações]** e **[!UICONTROL Fim]** não são rastreados porque os APNs distribuem atualizações para todos os dispositivos sem fornecer feedback. Para exibir eventos de **[!UICONTROL Atualizações]** e **[!UICONTROL Fim]**, use o [Console de Notificações por Push da Apple](https://developer.apple.com/notifications/push-notifications-console/).

+++ Saiba mais sobre as medições de ciclo de vida da atividade ao vivo com campanhas de marketing

* **[!UICONTROL Inicializações remotas]**: número total de eventos de inicialização de atividades online iniciados remotamente, normalmente acionados pelo servidor ou sistemas back-end.

* **[!UICONTROL Erros de inicializações remotas]**: Número total de erros que ocorreram ao tentar iniciar atividades online remotamente (por exemplo, tokens inválidos ou problemas de conectividade).

+++

## Motivos do erro {#error-reasons}

![](assets/error-reasons-activity.png)

A tabela **[!UICONTROL Motivos de erro]** permite identificar os erros específicos que ocorreram durante o processo de envio de suas atividades do Live, facilitando uma análise completa de todos os problemas encontrados.

## Motivos para exclusão {#excluded-reasons}

![](assets/excluded-activity.png)

A tabela **[!UICONTROL Motivos excluídos]** mostra visualmente os diversos fatores que levaram à exclusão de perfis de usuário do público-alvo direcionado, impedindo-o de receber sua atividade Ativa.
