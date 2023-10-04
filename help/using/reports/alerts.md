---
solution: Journey Optimizer
product: journey optimizer
title: Alertas
description: Saiba como gerenciar alertas
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 01bc2351b08fc7226c5e5633820f476c8621e404
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 1%

---

# Introdução a alertas {#alerts}

## Recursos de alerta {#alerting-capabilities}

Você pode acessar alertas do sistema por meio da interface ou receber um email quando ocorrer uma falha. No **Alertas** , é possível exibir os alertas disponíveis e assiná-los. Quando um determinado conjunto de condições em suas operações é atingido (como um problema em potencial quando o sistema ultrapassa um limite), as mensagens de alerta são entregues a todos os usuários em sua organização que se inscreveram neles.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Saiba mais sobre alertas no Adobe Experience Platform em [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=pt-BR){target="_blank"}.

No menu esquerdo, em **Administração**, clique em **Alertas**. Dois alertas pré-configurados para o Journey Optimizer estão disponíveis: o [Falha na ação personalizada de Jornada](#alert-custom-actions) alerta e o [Acionador de segmento de leitura malsucedido](#alert-read-audiences) alerta. Esses alertas estão detalhados abaixo.

É possível assinar cada alerta individualmente na interface do usuário do selecionando o **Assinar** opção no **Alertas** painel. Use o mesmo método para cancelar a inscrição.

![](assets/alert-subscribe.png)

Também é possível assinar alertas por meio do [Notificações de Eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}No entanto, as regras de alerta são organizadas em diferentes pacotes de assinatura.

Se ocorrer um comportamento inesperado, uma notificação de alerta será enviada aos assinantes. Com base nas preferências do usuário, os alertas são enviados por email ou diretamente no centro de notificações da Journey Optimizer, no canto superior direito da interface do usuário.

Quando um alerta é resolvido, os assinantes recebem uma notificação &quot;Resolvido&quot;.

>[!WARNING]
>
>Os alertas específicos do Adobe Journey Optimizer se aplicam somente ao **live** jornadas. Os alertas não são acionados para jornadas no modo de teste.

## Falha na ação personalizada de Jornada {#alert-custom-actions}

Esse alerta avisa se uma ação personalizada falhar. Consideramos que houve uma falha em que mais de 1% dos erros ocorreram em uma ação personalizada específica nos últimos 5 minutos. Isso é avaliado a cada 30 segundos.

![](assets/alerts-custom-action.png)

Os alertas de ações personalizadas são resolvidos quando, nos últimos 5 minutos:

* não ocorreu nenhum erro nessa ação personalizada (ou erros abaixo do limite de 1%),

* Ou, nenhum perfil atingiu essa ação personalizada.

O nome de inscrição do evento de E/S correspondente ao alerta de ação personalizada é **Falha na ação personalizada de Jornada**.

## Acionador de segmento de leitura malsucedido {#alert-read-audiences}

Esse alerta avisará se uma **Segmento de leitura** A atividade não processou nenhum perfil 10 minutos após o horário agendado de execução. Essa falha pode ser causada por problemas técnicos ou porque o público-alvo está vazio.

![](assets/alerts1.png)

Alertas ativados **Segmento de leitura** as atividades se aplicam somente a jornadas recorrentes. **Segmento de leitura** atividades em jornadas ativas com agendamento para execução **Uma vez** ou **Assim que possível** são ignorados.

Alertas ativados **Segmento de leitura** são resolvidos quando um perfil entra na variável **Segmento de leitura** nó.

O nome de inscrição do evento de E/S correspondente ao **Segmento de leitura** o alerta é **Atrasos, falhas e erros no segmento de leitura do Jornada**.
