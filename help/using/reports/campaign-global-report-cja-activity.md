---
solution: Journey Optimizer
product: journey optimizer
title: Relatório de campanha
description: Saiba como usar os dados de atividade ao vivo no relatório Campanha
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 7945ab9369498f23685aa2f727542c7367c2d830
workflow-type: tm+mt
source-wordcount: '407'
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

![](assets/activity-lifecycle.png)

A tabela **[!UICONTROL Ciclo de vida da atividade Live]** oferece uma visão abrangente de como as suas atividades Live avançam ao longo do tempo. Ele oferece visibilidade sobre eventos importantes, como o início, a atualização ou o término das atividades, ajudando você a entender melhor o engajamento do usuário e o ciclo de vida geral das campanhas de atividades Ativas.

+++ Saiba mais sobre as métricas de ciclo de vida de atividade online

* **[!UICONTROL Inicializações remotas]**: número de atividades Ativas iniciadas remotamente, normalmente acionadas pelo servidor ou sistema de back-end.

* **[!UICONTROL Inicializações locais]**: número de atividades Ativas iniciadas localmente no dispositivo de um usuário, geralmente resultantes da interação do usuário ou de acionadores do lado do cliente.

**[!UICONTROL Atualizações]**: número total de atualizações de atividades online enviadas para dispositivos. As atualizações podem incluir alterações de status, novo conteúdo ou notificações de progresso.

**[!UICONTROL Ends]**: número de atividades Live que foram encerradas, automaticamente após a conclusão ou manualmente por meio de um gatilho ou tempo limite definido.

**[!UICONTROL Contagem de totais]**: total geral de todos os eventos de ciclo de vida da atividade Live, incluindo inícios, atualizações e términos, fornecendo uma medida completa do volume de atividade Live.

+++

## Motivos do erro {#error-reasons}

![](assets/error-reasons-activity.png)

A tabela **[!UICONTROL Motivos de erro]** permite identificar os erros específicos que ocorreram durante o processo de envio de suas atividades do Live, facilitando uma análise completa de todos os problemas encontrados.

## Motivos para exclusão {#excluded-reasons}

![](assets/excluded-activity.png)

A tabela **[!UICONTROL Motivos excluídos]** mostra visualmente os diversos fatores que levaram à exclusão de perfis de usuário do público-alvo direcionado, impedindo-o de receber sua atividade Ativa.
