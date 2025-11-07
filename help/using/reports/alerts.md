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
source-git-commit: 1349da209bc90dd8ebad0bd309f89039aa6ea3f2
workflow-type: tm+mt
source-wordcount: '2153'
ht-degree: 2%

---

# Acessar e assinar alertas do sistema {#alerts}

Ao criar jornadas e campanhas, use o botão **Alertas** para verificar e resolver erros antes de executá-los ou publicá-los.

* Saiba como solucionar problemas das jornadas nesta [página](../building-journeys/troubleshooting.md)

* Saiba como revisar e ativar suas campanhas: [Campanhas de ação](../campaigns/review-activate-campaign.md) | [Campanhas acionadas por API](../campaigns/review-activate-api-triggered-campaign.md) | [Campanhas orquestradas](../orchestrated/start-monitor-campaigns.md)


Além dessas, quando um determinado conjunto de condições é atingido, mensagens de alerta podem ser enviadas a todos os usuários em sua organização que se inscreveram neles. Esses alertas estão disponíveis no menu dedicado **[!UICONTROL Alertas]**. A Adobe Experience Platform fornece várias regras de alerta predefinidas que você pode ativar para sua organização. Além disso, você pode assinar alertas de sistema específicos do [!DNL Adobe Journey Optimizer], conforme detalhados nesta página.

>[!NOTE]
>
>Saiba mais sobre alertas no Adobe Experience Platform em [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=pt-BR){target="_blank"}.

No menu esquerdo, em **[!UICONTROL Administração]**, clique em **[!UICONTROL Alertas]**. Vários alertas pré-configurados para o Journey Optimizer estão disponíveis na guia **Procurar**.

![](assets/updated-alerts-list.png){width=50%}

* Alertas específicos de jornadas:

   * o alerta [Acionador de Leitura de Público-alvo sem Êxito](#alert-read-audiences)
   * o alerta [Taxa de Erro de Ação Personalizada Excedida](#alert-custom-action-error-rate) (substitui o alerta anterior Falha de Ação Personalizada de Jornada)
   * o alerta [Taxa de Descarte de Perfil Excedida](#alert-discard-rate)
   * o alerta [Taxa de Erro de Perfil Excedida](#alert-profile-error-rate)
   * o alerta [Jornada publicada](#alert-journey-published)
   * o alerta [Jornada concluída](#alert-journey-finished)
   * o alerta [Limite de ação personalizada](#alert-custom-action-capping) foi acionado

* Alertas específicos para configuração de canal:

   * o alerta [&#x200B; do registro DNS de domínio do AJO &#x200B;](#alert-dns-record-missing)está ausente
   * alerta de [falha na configuração do canal do AJO](#alert-channel-config-failure)
     <!--* the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## Assinatura de alertas {#subscribe-alerts}

Se ocorrer um comportamento inesperado e/ou se um determinado conjunto de condições em suas operações for atingido (como um problema em potencial quando o sistema viola um limite), as notificações de alerta serão entregues a todos os usuários em sua organização que se subscreveram a elas.

É possível assinar cada alerta individualmente na interface do usuário, seja globalmente, pelo menu **[!UICONTROL Alertas]** (consulte [Assinatura global](#global-subscription)), ou unitária para uma jornada específica (consulte [Assinatura unitária](#unitary-subscription)).

Com base nas preferências do assinante, os alertas são enviados por email e/ou diretamente no centro de notificações da Journey Optimizer, no canto superior direito da interface do usuário (notificações no aplicativo). Selecione como você deseja receber esses alertas nas [!DNL Adobe Experience Cloud] **[!UICONTROL Preferências]**. [Saiba mais](../start/user-interface.md#in-product-alerts)

Quando um alerta é resolvido, os assinantes recebem uma notificação &quot;Resolvido&quot;. Os alertas são resolvidos após 1 hora para proteger contra a alternância de valores.


### Assinatura global {#global-subscription}

Para assinar/cancelar a assinatura de um alerta para todas as jornadas e campanhas, siga estas etapas:

1. Navegue até o painel **[!UICONTROL Alertas]** no menu esquerdo e selecione a opção **[!UICONTROL Assinar]** para o alerta no qual deseja se inscrever.

   ![Assinando um alerta](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >A assinatura se aplica somente a uma sandbox específica. Você deve assinar alertas para cada sandbox individualmente.

1. Use o mesmo método para **[!UICONTROL Cancelar inscrição]**.

Você também pode assinar por meio de [notificações de Eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}. As regras de alerta são organizadas em diferentes pacotes de assinatura. As assinaturas de evento correspondentes aos alertas específicos do Journey Optimizer estão detalhadas [abaixo](#journey-alerts).

### Assinatura unitária {#unitary-subscription}

Para assinar/cancelar a assinatura de um alerta para uma jornada específica, siga estas etapas:

1. Navegue até o inventário de jornadas e selecione a opção **[!UICONTROL Assinar alertas]** para uma jornada específica.

   ![Assinando um alerta para uma jornada específica](assets/subscribe-journey-alert.png){width=75%}

1. Escolha os alertas. Os seguintes alertas estão disponíveis: [Taxa de Descarte de Perfil Excedida](#alert-discard-rate), [Taxa de Erro de Ação Personalizada Excedida](#alert-custom-action-error-rate), [Taxa de Erro de Perfil Excedida](#alert-profile-error-rate), [Jornada Publicada](#alert-journey-published), [Jornada Concluída](#alert-journey-finished) e [Limite de Ação Personalizada Disparado](#alert-custom-action-capping).

1. Para cancelar a inscrição em um alerta, desmarque-o na mesma tela.

1. Clique em **[!UICONTROL Salvar]** para confirmar.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.-->

## Jornada alertas {#journey-alerts}


Todas as notificações de jornada disponíveis na interface do usuário estão listadas abaixo.

>[!CAUTION]
>
>Os alertas específicos do Adobe Journey Optimizer se aplicam somente às jornadas **live**. Os alertas não são acionados para jornadas no modo de teste.

### Falha ao ler o acionador de público-alvo {#alert-read-audiences}

Este alerta avisa se uma atividade **Ler público-alvo** não processou nenhum perfil 10 minutos após o horário agendado de execução. Essa falha pode ser causada por problemas técnicos ou porque o público-alvo está vazio. Se essa falha for causada por problemas técnicos, esteja ciente de que ainda podem ocorrer tentativas, dependendo do tipo de problema (por exemplo: se a criação do trabalho de exportação falhar, tentaremos novamente a cada 10mn para um máximo de 1h).

Os alertas sobre atividades de **Ler público-alvo** se aplicam somente a jornadas recorrentes. As atividades de **Ler Público** em jornadas ativas com agendamento para execução de **Uma Vez** ou **Assim que possível** são ignoradas.

Os alertas em **Ler público-alvo** são resolvidos quando um perfil entra no nó **Ler público-alvo** ou após 1 hora.

O nome de inscrição do evento de E/S correspondente ao alerta **Falha no Acionador de Leitura de Público** é **Atrasos, Falhas e Erros de leitura de público-alvo de Jornada**.

Para solucionar problemas de alertas do **Ler público-alvo**, verifique sua contagem de públicos na interface do Experience Platform.

### Taxa de descarte do perfil excedida {#alert-discard-rate}

Esse alerta avisará se a proporção de descartes de perfil em relação aos perfis inseridos nos últimos 5 minutos exceder o limite. O limite padrão está definido como 20%, mas você pode [definir um limite personalizado](#custom-threshold).

Clique no nome do alerta para verificar os detalhes e a configuração do alerta.

![](assets/profile-discard-alert.png)

Há vários motivos pelos quais um perfil pode ser descartado, o que informará o método de solução de problemas. Alguns motivos comuns estão listados abaixo:

* Perfil descartado na entrada porque já está vivo nessa jornada unitária. Para resolver isso, verifique se o perfil tem tempo suficiente para sair da jornada antes que o próximo evento chegue para esse perfil.
* A identidade não está definida para o perfil ou o namespace usado pela jornada de público-alvo de leitura não está sendo utilizado nesse perfil. Para resolver isso, verifique se o namespace na jornada corresponde ao namespace de identidade usado pelos perfis.
* Taxa de transferência de evento excedida. Para resolver isso, certifique-se de que os eventos que entram no sistema não excedam esses limites.


### Taxa de erros de ação personalizada excedida {#alert-custom-action-error-rate}

Este alerta avisa se a proporção de erros de ação personalizada para chamadas HTTP bem-sucedidas nos últimos 5 minutos excedeu o limite. O limite padrão está definido como 20%, mas você pode [definir um limite personalizado](#custom-threshold).

>[!NOTE]
>
>Este alerta substitui o alerta **Falha da ação personalizada de Jornada** anterior.

Clique no nome do alerta para verificar os detalhes e a configuração do alerta.

Podem ocorrer erros de ações personalizadas por vários motivos. Para solucionar esses erros, você pode:

* Verifique sua ação personalizada usando o [modo de teste](../building-journeys/testing-the-journey.md) em outra jornada.
* Verifique seu [relatório de jornadas](../reports/journey-live-report.md) para ver os motivos do erro na ação.
* Verifique stepEvents da jornada para obter mais informações sobre &quot;failureReason&quot;.
* Verifique se a ação personalizada está configurada corretamente e valide se a autenticação ainda é válida. Execute uma verificação manual com o Postman, por exemplo.
* Verifique se o endpoint pode ser acessado e se a ação personalizada pode acessá-lo por meio do verificador de conectividade da ação personalizada.
* Verifique as credenciais de autenticação, verifique a conectividade com a Internet etc.

### Taxa de erros do perfil excedida {#alert-profile-error-rate}

Esse alerta avisará se a proporção de perfis com erro em relação aos perfis inseridos nos últimos 5 minutos exceder o limite. O limite padrão está definido como 20%, mas você pode [definir um limite personalizado](#custom-threshold).

Clique no nome do alerta para verificar os detalhes e a configuração do alerta.

Para solucionar problemas de erro de perfil, consulte os dados na etapa de eventos para entender onde e por que o perfil falhou na jornada.

### Jornada publicada {#alert-journey-published}

Esse alerta notifica quando uma jornada foi publicada por um profissional na tela de jornada.

Este é um alerta informativo que ajuda você a rastrear os eventos de ciclo de vida da jornada em sua organização. Não há critérios de resolução, pois esta é uma notificação única.

### Jornada concluída {#alert-journey-finished}

Este alerta notifica quando uma jornada é concluída. A definição de &quot;concluído&quot; varia dependendo do tipo de jornada:

| Tipo de jornada | Recorrente? | Tem data de término? | Definição de &quot;concluído&quot; |
|--------------|------------|---------------|--------------------------|
| Público-alvo de leitura | Não | n/d | 91 dias após o início da execução |
| Público-alvo de leitura | Sim | Não | 91 dias após o início da execução |
| Público-alvo de leitura | Sim | Sim | Quando a data final é alcançada |
| Jornada acionada por evento | n/d | Sim | Quando a data final é alcançada |
| Jornada acionada por evento | n/d | Não | Quando fechado na interface do usuário ou por meio da API |

Este é um alerta informativo que ajuda a monitorar a conclusão da jornada. Não há critérios de resolução, pois esta é uma notificação única.

### Limite de ação personalizada acionado {#alert-custom-action-capping}

Esse alerta avisa quando o limite é acionado em uma ação personalizada. O limite é usado para limitar o número de chamadas enviadas para um ponto de extremidade externo para evitar a sobrecarga do ponto de extremidade.

Clique no nome do alerta para verificar os detalhes e a configuração do alerta.

Quando o limite é acionado, significa que o número máximo de chamadas de API foi atingido dentro do período definido e outras chamadas estão sendo limitadas ou colocadas em fila. Saiba mais sobre como limitar ações personalizadas nesta [página](../action/about-custom-action-configuration.md#custom-action-enhancements-best-practices).

Esse alerta é resolvido quando o limite não está mais ativo ou quando nenhum perfil atinge a ação personalizada durante o período de avaliação.

Para solucionar problemas de limite:

* Revise a configuração de limitação em sua ação personalizada para garantir que os limites sejam apropriados para seu caso de uso.
* Verifique se o volume de chamadas de API é maior do que o esperado e considere ajustar o design da jornada ou as configurações de limite.
* Monitore o endpoint externo para garantir que ele consiga lidar com a carga esperada.

## Alertas de configuração {#configuration-alerts}

Os alertas de monitoramento de configuração de canal disponíveis na interface do usuário estão listados abaixo.

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

## Gerenciar alertas {#manage-alerts}

### Editar um alerta

Você pode verificar os detalhes de um alerta clicando na linha correspondente. Os canais de nome, status e notificação são exibidos no painel esquerdo.
Para alertas de Jornada, use o botão **[!UICONTROL Mais ações]** para editá-los. Você pode então definir um [limite personalizado](#custom-threshold) para esses alertas.

![](assets/alert-more-actions.png){width=60%}

### Definir um limite personalizado {#custom-threshold}

Você pode definir limites para os [alertas de Jornada](#journey-alerts). O limite de alertas acima do padrão é de 20%.

Para alterar o limite:

1. Navegar até a tela **Alertas**
1. Clique no botão **[!UICONTROL Mais ações]** do alerta para atualizar
1. Insira o novo limite e confirme. O novo limite se aplica a **todas** jornadas


![](assets/alert-threshold.png){width=60%}

>[!CAUTION]
>
>Os níveis de limite são globais em todas as jornadas e não podem ser modificados individualmente por jornada.

### Desativar um alerta

Por padrão, todos os alertas são ativados. Para desabilitar um alerta, selecione a opção **[!UICONTROL Desabilitar alerta]**: todos os assinantes deste alerta não receberão mais as notificações relacionadas.


### Status de alerta

Os possíveis status de alerta estão listados abaixo:

* **[!UICONTROL Habilitado]** - O alerta está habilitado e está monitorando a condição do acionador no momento.
* **[!UICONTROL Desabilitado]** - O alerta está desabilitado e não está monitorando a condição do acionador no momento. Você não receberá notificações para este alerta.
* **[!UICONTROL Acionado]** - A condição de acionador do alerta está sendo atendida no momento.


### Exibir e atualizar assinantes {#manage-subscribers}

Selecione **[!UICONTROL Gerenciar assinantes de alertas]** para ver a lista de usuários que assinaram o alerta.

![](assets/alert-subscribers.png){width=80%}

Para adicionar mais assinantes, insira seus emails separados por vírgula e selecione **[!UICONTROL Atualizar]**.

Para remover os assinantes, exclua seus endereços de email dos assinantes atuais e selecione **[!UICONTROL Atualizar]**.

## Recursos adicionais {#additional-resources-alerts}

* Saiba como solucionar problemas das jornadas nesta [página](../building-journeys/troubleshooting.md).
* Saiba como revisar suas campanhas em [esta página](../campaigns/review-activate-campaign.md).
