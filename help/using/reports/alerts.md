---
solution: Journey Optimizer
product: journey optimizer
title: Acessar e assinar alertas do sistema
description: Saiba como acessar e assinar alertas do sistema
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 13623d28ba7b852f7267b5f800f2c9a3afda4a62
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 0%

---

# Acessar e assinar alertas do sistema {#alerts}

Ao criar jornadas e campanhas, use o botão **Alertas** para verificar e resolver erros antes de executá-los ou publicá-los:

* Saiba como solucionar problemas das jornadas nesta [página](../building-journeys/troubleshooting.md).
* Saiba como revisar suas campanhas em [esta página](../campaigns/review-activate-campaign.md).

No menu dedicado **[!UICONTROL Alertas]**, você também pode assinar alertas do sistema [!DNL Adobe Journey Optimizer], conforme detalhado nesta página.

## Acessar alertas {#access-alerts}

Quando ocorrer uma falha, você poderá obter alertas do sistema na central de notificações da Journey Optimizer (alertas no aplicativo) e/ou receber um email. Para acessar esses alertas, siga as etapas abaixo.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

>[!NOTE]
>
>Saiba mais sobre alertas no Adobe Experience Platform em [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=pt-BR){target="_blank"}.

No menu esquerdo, em **[!UICONTROL Administração]**, clique em **[!UICONTROL Alertas]**. Vários alertas pré-configurados para o Journey Optimizer estão disponíveis.

Eles são listados a seguir e cada alerta é detalhado abaixo.

* Alertas específicos de jornadas:

   * o alerta [Falha da Ação Personalizada de Jornada](#alert-custom-actions)
   * o alerta [Acionador de Leitura de Público-alvo sem Êxito](#alert-read-audiences)

* Alertas específicos para configuração de canal:

   * o alerta [ do registro DNS de domínio do AJO ](#alert-dns-record-missing)está ausente
  <!--* the [AJO channel configuration failure](#alert-channel-config-failure) alert
   * the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## Assinatura de alertas {#subscribe-alerts}

1. Você pode assinar cada alerta individualmente na interface de usuário selecionando a opção **[!UICONTROL Assinar]**.

   ![](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >A assinatura se aplica somente a uma sandbox específica. Você deve assinar alertas para cada sandbox individualmente.

1. Use o mesmo método para **[!UICONTROL Cancelar inscrição]**.

1. Você também pode assinar alertas por meio de [notificações de Eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=pt-BR){target="_blank"}. As regras de alerta são organizadas em diferentes pacotes de assinatura. As assinaturas de evento correspondentes aos alertas específicos do Journey Optimizer estão detalhadas [abaixo](#journey-alerts).

1. Se ocorrer um comportamento inesperado e/ou se um determinado conjunto de condições em suas operações for atingido (como um problema em potencial quando o sistema viola um limite), as notificações de alerta serão entregues a todos os usuários em sua organização que se subscreveram a elas.

Com base nas preferências do assinante, os alertas são enviados por email e/ou diretamente no centro de notificações da Journey Optimizer, no canto superior direito da interface do usuário (notificações no aplicativo). Selecione como você deseja receber esses alertas nas [!DNL Adobe Experience Cloud] **[!UICONTROL Preferências]**. [Saiba mais](../start/user-interface.md#in-product-alerts)

>[!NOTE]
>
>Por padrão, somente o alerta no aplicativo está ativado.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=pt-BR#enable-email-alerts){target="_blank"}.-->

Quando um alerta é resolvido, os assinantes recebem uma notificação &quot;Resolvido&quot;.

## Gerenciar alertas {#manage-alerts}

Para gerenciar alertas, selecione um item e use o botão **[!UICONTROL Mais ações]**.

![](assets/alert-more-actions.png){width=80%}

Por padrão, todos os alertas são ativados. Para desabilitar um alerta, selecione a opção **[!UICONTROL Desabilitar alerta]** no menu **[!UICONTROL Mais ações]**. Todos os assinantes deste alerta não receberão mais as notificações relacionadas.

Selecione **[!UICONTROL Gerenciar assinantes de alertas]** para ver a lista de usuários que assinaram o alerta. Use o campo em branco para adicionar mais assinantes.

![](assets/alert-subscribers.png){width=80%}

Os possíveis status de alerta estão listados abaixo:

* **[!UICONTROL Habilitado]** - O alerta está habilitado e está monitorando a condição do acionador no momento.
* **[!UICONTROL Desabilitado]** - O alerta está desabilitado e não está monitorando a condição do acionador no momento. Você não receberá notificações para este alerta.
* **[!UICONTROL Acionado]** - A condição de acionador do alerta está sendo atendida no momento.

## Jornada alertas {#journey-alerts}

>[!CAUTION]
>
>Os alertas específicos do Adobe Journey Optimizer se aplicam somente às jornadas **live**. Os alertas não são acionados para jornadas no modo de teste.

### Falha na ação personalizada de Jornada {#alert-custom-actions}

Esse alerta avisa se uma ação personalizada falhar. Consideramos que houve uma falha em que mais de 1% dos erros ocorreram em uma ação personalizada específica nos últimos 5 minutos. Isso é avaliado a cada 30 segundos.

![](assets/alerts-custom-action.png)

Os alertas de ações personalizadas são resolvidos quando, nos últimos 5 minutos:

* não ocorreu nenhum erro nessa ação personalizada (ou erros abaixo do limite de 1%),

* ou, nenhum perfil atingiu essa ação personalizada.

O nome de inscrição do evento de E/S correspondente ao alerta de ação personalizada é **Falha de Ação Personalizada de Jornada**.

Para solucionar problemas de alertas de **Ação personalizada**:

* Verifique sua ação personalizada usando o modo de teste em outra jornada:

  ![](assets/alert-troubleshooting-2.png)

* Verifique o relatório de jornadas para ver os motivos do erro na ação.

  ![](assets/alert-troubleshooting-3.png)

* Verifique stepEvents da jornada para obter mais informações sobre &quot;failureReason&quot;.

* Verifique a configuração de ação personalizada e valide se a autenticação ainda está OK. Execute uma verificação manual com o Postman, por exemplo.

### Falha ao ler o acionador de público-alvo {#alert-read-audiences}

Este alerta avisa se uma atividade **Ler público-alvo** não processou nenhum perfil 10 minutos após o horário agendado de execução. Essa falha pode ser causada por problemas técnicos ou porque o público-alvo está vazio. Se essa falha for causada por problemas técnicos, esteja ciente de que ainda podem ocorrer tentativas, dependendo do tipo de problema (por exemplo: se a criação do trabalho de exportação falhar, tentaremos novamente a cada 10mn para um máximo de 1h).

![](assets/alerts1.png)

Os alertas sobre atividades de **Ler público-alvo** se aplicam somente a jornadas recorrentes. As atividades de **Ler Público** em jornadas ativas com agendamento para execução de **Uma Vez** ou **Assim que possível** são ignoradas.

Os alertas em **Ler público-alvo** são resolvidos quando um perfil entra no nó **Ler público-alvo**.

O nome de inscrição do evento de E/S correspondente ao alerta **Falha no Acionador de Leitura de Público** é **Atrasos, Falhas e Erros de leitura de público-alvo de Jornada**.

Para solucionar problemas de alertas do **Ler público-alvo**, verifique sua contagem de públicos na interface do Experience Platform.

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

## Alertas de configuração {#configuration-alerts}

### Registro DNS de domínio do AJO ausente {#alert-dns-record-missing}

Esse alerta notifica quando registros DNS críticos (NS ou CNAME) necessários para a configuração apropriada da capacidade de entrega estão ausentes ou configurados incorretamente. Sem esses registros, a capacidade de entrega de e-mails pode estar comprometida.

>[!NOTE]
>
>* Os registros NS são essenciais para a delegação completa de subdomínio para o Adobe. [Saiba mais](../configuration/about-subdomain-delegation.md#full-subdomain-delegation)
>
>* Os registros CNAME são compatíveis com a configuração de subdomínio CNAME. [Saiba mais](../configuration/about-subdomain-delegation.md#cname-subdomain-setup)

O alerta de **Registro DNS de Domínio do AJO ausente** é disparado quando o sistema detecta que os registros NS ou CNAME necessários estão ausentes ou não correspondem aos padrões de configuração.

1. Clique no alerta a ser direcionado ao [subdomínio](../configuration/delegate-subdomain.md) afetado na interface [!DNL Journey Optimizer].

   <!--For guidance on editing delegated subdomains, see [this section](../configuration/delegate-subdomain.md).-->

1. Corrija a configuração de DNS definindo os registros corretamente e [envie a delegação de subdomínio](../configuration/delegate-subdomain.md#submit-subdomain) novamente.

   >[!NOTE]
   >
   >Antes de continuar, verifique se todos os registros foram criados corretamente na solução de hospedagem de domínio.

1. Se você não tiver certeza dos valores corretos, poderá criar um novo subdomínio em [!DNL Journey Optimizer] com o mesmo nome do subdomínio afetado. [Saiba como configurar um novo subdomínio](../configuration/delegate-subdomain.md#set-up-subdomain)

Se as alterações não resolverem o problema, o mesmo alerta será acionado novamente no dia seguinte.

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?-->

### Falha na configuração do canal do AJO {#alert-channel-config-failure}

>[!IMPORTANT]
>
>Este alerta se aplica somente às configurações de canal de **email** que usam o tipo de delegação [subdomínio personalizado](../configuration/delegate-custom-subdomain.md). <!--Other channel types (such as SMS, push, or in-app) are not covered by this alert.-->

Esse alerta é disparado caso a auditoria do sistema detecte problemas de configuração do canal de email. Esses problemas podem incluir configurações de canal mal definidas, configuração DNS inválida, problemas da lista de supressão, inconsistência de IP ou quaisquer outros erros que possam afetar a entrega de email.

Se você receber esse alerta, as etapas de resolução estão listadas abaixo:

1. Clique no alerta a ser direcionado para a [configuração do canal de email](../email/get-started-email-config.md) afetada na interface [!DNL Journey Optimizer].

   Para obter orientação sobre como editar configurações de canal, consulte [esta seção](../configuration/channel-surfaces.md#edit-channel-surface).

1. Revise os detalhes da configuração e as mensagens de erro fornecidas. Os motivos comuns de falha incluem:

   * Falha na validação do SPF
   * Falha na validação do DKIM
   * Falha na validação do registro MX
   * Registros DNS inválidos

   >[!NOTE]
   >
   >Os possíveis motivos de falha na configuração estão listados em [esta seção](../configuration/channel-surfaces.md).

1. Resolva o problema:

   * Atualize a configuração do canal conforme necessário.
   * Talvez seja necessário corrigir problemas específicos de DNS mencionados no alerta.

   >[!NOTE]
   >
   >Como um único domínio pode ser associado a várias configurações de canal, a resolução de problemas de DNS para uma configuração de canal pode corrigir automaticamente problemas relacionados em várias configurações.

Se a alteração não resolver o problema, o mesmo alerta será acionado novamente no dia seguinte.

Ao resolver problemas de configuração de email, lembre-se das práticas recomendadas listadas abaixo:

* Agir imediatamente - Solucionar falhas de configuração assim que forem detectadas, para evitar interrupções no delivery de email.
* Verificar todas as configurações - se o alerta indicar várias configurações de email afetadas, revise e corrija cada uma delas.

<!--### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->





