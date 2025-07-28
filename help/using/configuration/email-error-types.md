---
solution: Journey Optimizer
product: journey optimizer
title: Tipos de erro de email
description: Acesse a lista de todos os possíveis erros de email ao enviar deliveries com o Journey Optimizer.
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: tentativas, rejeição, soft, ignorado, hard, otimizador, erro
hide: true
hidefromtoc: true
source-git-commit: 1e36871c2c975c81d018fabb3cff51d11c98962e
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 11%

---


# Tipos de erro de email

Possíveis motivos de falha de delivery são múltiplos. A tabela abaixo detalha todos os erros que podem ocorrer ao enviar deliveries de email com [!DNL Journey Optimizer], juntamente com sua descrição e tipo de erro.

Esses erros podem ser encontrados no [Conjunto de Dados de Eventos de Feedback de Mensagens do AJO](../data/datasets-query-examples.md#message-feedback-event-dataset), que contém os logs de entrega de mensagens, incluindo informações sobre todas as entregas de mensagens de [!DNL Journey Optimizer] e registros de feedback dos ISPs de email sobre rejeições.

| Rótulo de erro | Tipo de erro | Valor técnico | Descrição |
| --- | --- | --- | --- |
| **Indeterminado** | Ignorado | 1 | Não é possível classificar a mensagem de rejeição SMTP recebida do ISP. |
| **Destinatário inválido** | Rejeição permanente | 10 | O endereço do destinatário não é válido. |
| **Destinatário recusado** | Rejeição permanente | 15 | O ISP do destinatário recusou a mensagem e o ISP pode bloquear o remetente se o destinatário não for suprimido. |
| **Rejeição leve** | Rejeição temporária | 20 | Ocorreu uma falha temporária na mensagem. Ele pode ter êxito em tentativas futuras. |
| **Falha de DNS** | Rejeição temporária | 21 | Falha temporária de DNS na entrega da mensagem. Ele pode ter êxito em tentativas futuras. |
| **Caixa de Correio Cheia** | Rejeição temporária | 22 | Ocorreu uma falha temporária de entrega na mensagem porque a caixa de correio do destinatário estava cheia. |
| **Muito Grande** | Ignorado | 23 | Ocorreu uma falha temporária de entrega na mensagem porque o tamanho da mensagem excedeu o limite do destinatário. |
| **Tempo limite** | Ignorado | 24 | A entrega da mensagem falhou porque a validade da mensagem expirou ou demorou muito para ser enviada para o ISP. |
| **Falha do administrador** | Administrador | 25 | Falha no delivery devido a alguma configuração de política na infraestrutura de envio de email. |
| **Rejeição genérica: SEM RCPT** | Ignorado | 30 | Não foi possível entregar a mensagem porque o destinatário não foi identificado. |
| **Rejeição genérica** | Ignorado | 40 | Ocorreu uma falha temporária de entrega na mensagem por motivos não especificados. |
| **Bloqueio de email** | Ignorado | 50 | O delivery apresentou falha temporária devido ao alto volume ou limites de taxa do ISP. |
| **Bloqueio de spam** | Ignorado | 51 | A entrega apresentou falha temporária porque o ISP considerou os domínios ou IPs do remetente uma fonte de spam conhecida. |
| **Conteúdo de spam** | Ignorado | 52 | O delivery sofreu uma falha temporária porque o ISP classificou o conteúdo do email como spam. |
| **Retransmissão negada** | Rejeição temporária | 54 | Não foi possível aceitar a mensagem porque o domínio de destino não está incluído na lista de permissões para retransmissão. |
| **Resposta automática** | Ignorado | 60 | Estas mensagens são descartadas por [!DNL Journey Optimizer] quando recebidas, a menos que o encaminhamento esteja habilitado. |
| **Falha transitória** | Ignorado | 70 | O delivery será repetido com uma taxa reduzida ou poderá ser adiado em caso de suspensão. |
| **Resposta-Desafio** | Rejeição temporária | 100 | A entrega pode falhar permanentemente, pois [!DNL Journey Optimizer] não oferece suporte a um mecanismo de autenticação de resposta a desafio. |
