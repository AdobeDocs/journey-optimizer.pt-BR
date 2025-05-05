---
solution: Journey Optimizer
product: journey optimizer
title: Alertas
description: Saiba como gerenciar alertas
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# Introdução a alertas {#alerts}

Ao criar jornadas e campanhas, use o botão **Alertas** para verificar e resolver erros antes de executá-los ou publicá-los. Saiba como solucionar problemas das jornadas nesta [página](../building-journeys/troubleshooting.md). Saiba como revisar suas campanhas em [esta página](../campaigns/review-activate-campaign.md).

Você também pode assinar alertas de sistema do Adobe Journey Optimizer, conforme detalhados nesta página.

## Acessar e assinar alertas {#alerting-capabilities}

Quando ocorrer uma falha, você poderá obter alertas do sistema na central de notificações da Journey Optimizer (alertas no aplicativo) e/ou receber um email.

No menu **Alertas**, você pode exibir os alertas disponíveis e se inscrever neles. Quando um determinado conjunto de condições em suas operações é atingido (como um problema em potencial quando o sistema ultrapassa um limite), as mensagens de alerta são entregues a todos os usuários em sua organização que se inscreveram neles.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Saiba mais sobre alertas no Adobe Experience Platform em [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=pt-BR){target="_blank"}.

No menu esquerdo, em **Administração**, clique em **Alertas**. Dois alertas pré-configurados para o Journey Optimizer estão disponíveis: o alerta [Falha na ação personalizada de Jornada](#alert-custom-actions) e o alerta [Falha no acionador de público-alvo de leitura](#alert-read-audiences). Esses alertas estão detalhados abaixo.

Você pode assinar cada alerta individualmente na interface selecionando a opção **Assinar** no painel **Alertas**. Use o mesmo método para cancelar a inscrição.

![](assets/alert-subscribe.png)

Você também pode assinar alertas por meio de [notificações de Eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=pt-BR){target="_blank"}. As regras de alerta são organizadas em diferentes pacotes de assinatura. As assinaturas de evento correspondentes aos alertas específicos do Journey Optimizer são detalhadas abaixo.

Se ocorrer um comportamento inesperado, uma notificação de alerta será enviada aos assinantes. Com base nas preferências do usuário, os alertas são enviados por email e/ou diretamente na central de notificações da Journey Optimizer, no canto superior direito da interface do usuário. Por padrão, somente o alerta no aplicativo está ativado. Para habilitar o alerta por email, consulte a [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=pt-BR#enable-email-alerts){target="_blank"}.

Quando um alerta é resolvido, os assinantes recebem uma notificação &quot;Resolvido&quot;.

>[!CAUTION]
>
>Os alertas específicos do Adobe Journey Optimizer se aplicam somente às jornadas **live**. Os alertas não são acionados para jornadas no modo de teste.

## Falha na ação personalizada de Jornada {#alert-custom-actions}

Esse alerta avisa se uma ação personalizada falhar. Consideramos que houve uma falha em que mais de 1% dos erros ocorreram em uma ação personalizada específica nos últimos 5 minutos. Isso é avaliado a cada 30 segundos.

![](assets/alerts-custom-action.png)

Os alertas de ações personalizadas são resolvidos quando, nos últimos 5 minutos:

* não ocorreu nenhum erro nessa ação personalizada (ou erros abaixo do limite de 1%),

* ou, nenhum perfil atingiu essa ação personalizada.

O nome de inscrição do evento de E/S correspondente ao alerta de ação personalizada é **Falha de Ação Personalizada de Jornada**.

## Falha ao ler o acionador de público-alvo {#alert-read-audiences}

Este alerta avisa se uma atividade **Ler público-alvo** não processou nenhum perfil 10 minutos após o horário agendado de execução. Essa falha pode ser causada por problemas técnicos ou porque o público-alvo está vazio. Se essa falha for causada por problemas técnicos, esteja ciente de que ainda podem ocorrer tentativas, dependendo do tipo de problema (por exemplo: se a criação do trabalho de exportação falhar, tentaremos novamente a cada 10mn para um máximo de 1h).

![](assets/alerts1.png)

Os alertas sobre atividades de **Ler público-alvo** se aplicam somente a jornadas recorrentes. As atividades de **Ler Público** em jornadas ativas com agendamento para execução de **Uma Vez** ou **Assim que possível** são ignoradas.

Os alertas em **Ler público-alvo** são resolvidos quando um perfil entra no nó **Ler público-alvo**.

O nome de inscrição do evento de E/S correspondente ao alerta **Falha no Acionador de Leitura de Público** é **Atrasos, Falhas e Erros de leitura de público-alvo de Jornada**.

## Solução de problemas {#alert-troubleshooting}

Para solucionar problemas de alertas do **Ler público-alvo**, verifique sua contagem de públicos na interface do Experience Platform.

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

Para solucionar problemas de alertas de **Ação personalizada**:

* Verifique sua ação personalizada usando o modo de teste em outra jornada:

  ![](assets/alert-troubleshooting-2.png)

* Verifique o relatório de jornadas para ver os motivos do erro na ação.

  ![](assets/alert-troubleshooting-3.png)

* Verifique stepEvents da jornada para obter mais informações sobre &quot;failureReason&quot;.

* Verifique a configuração de ação personalizada e valide se a autenticação ainda está OK. Execute uma verificação manual com o Postman, por exemplo.
