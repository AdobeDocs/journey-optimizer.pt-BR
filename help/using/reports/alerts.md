---
solution: Journey Optimizer
product: journey optimizer
title: Acessar e assinar alertas do sistema
description: Saiba como acessar, assinar e gerenciar alertas do sistema no Adobe Journey Optimizer. Monitore o desempenho da jornada, erros de ação personalizada, problemas de perfil e capacidade de entrega de email com notificações de alerta proativas.
feature: Journeys, Alerts, Monitoring
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 6976f2b1b8b95f7dc9bffe65b7a7ddcc5dab5474
workflow-type: tm+mt
source-wordcount: '2693'
ht-degree: 1%

---

# Acessar e assinar alertas do sistema {#alerts}

## Visão geral

Os alertas são notificações automatizadas que ajudam a monitorar e solucionar problemas no Adobe Journey Optimizer. Eles fornecem percepção em tempo real de possíveis problemas em suas jornadas, campanhas e configurações de canal, permitindo que você tome medidas corretivas antes que as experiências do cliente sejam afetadas.

O Adobe Journey Optimizer fornece dois tipos de alertas:

* **Alertas de validação na tela**: ao criar jornadas e campanhas, use o botão **Alertas** na tela para identificar e resolver erros de configuração antes da publicação. Saiba como [solucionar problemas do jornada](../building-journeys/troubleshooting.md) e revisar suas campanhas: [Campanhas de ação](../campaigns/review-activate-campaign.md) | [Campanhas acionadas por API](../campaigns/review-activate-api-triggered-campaign.md) | [Campanhas orquestradas](../orchestrated/start-monitor-campaigns.md).

* **Alertas de monitoramento do sistema** (detalhados nesta página): receba notificações proativas quando os limites operacionais forem excedidos ou forem detectados problemas nas configurações de jornadas ativas e canais. Os alertas do sistema monitoram métricas como taxas de erro, descartes de perfis e problemas de capacidade de entrega de email.

**Principais benefícios dos alertas do sistema:**

* Detecção proativa de problemas antes do impacto no cliente
* Monitoramento automatizado do desempenho e da integridade da jornada
* Aviso antecipado para problemas de capacidade de entrega de email
* Tempo reduzido para identificar e resolver problemas operacionais

Os alertas do sistema estão disponíveis no menu **[!UICONTROL Alertas]** em **[!UICONTROL Administração]**. O Adobe Experience Platform fornece várias regras de alerta predefinidas que você pode habilitar, incluindo alertas específicos do [!DNL Adobe Journey Optimizer] para jornada e configurações de canal.

## Pré-requisitos

Antes de trabalhar com alertas:

* **Permissões**: você precisa de permissões específicas para exibir e gerenciar alertas. Consulte [permissões necessárias no Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=pt-BR#permissions){target="_blank"}.

* **Reconhecimento de sandbox**: as assinaturas de alerta são específicas da sandbox. Quando você assina alertas, eles se aplicam somente à sandbox atual. Quando uma sandbox é redefinida, todas as assinaturas de alerta também são redefinidas.

* **Preferências de notificação**: configure como você recebe alertas (email e/ou no aplicativo) nas [Preferências da Adobe Experience Cloud](../start/user-interface.md#in-product-uc).

>[!NOTE]
>
>Os alertas específicos do Journey Optimizer se aplicam somente às jornadas do **live**. Os alertas não são acionados para jornadas no modo de teste. Para obter mais informações sobre a estrutura de alertas, consulte a [documentação de alertas do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=pt-BR){target="_blank"}.

## Alertas disponíveis no Journey Optimizer {#available-alerts}

O Journey Optimizer fornece regras de alerta pré-configuradas que monitoram aspectos específicos das suas jornadas e configurações de canal. Não é necessário criar esses alertas: eles estão disponíveis prontos para uso e podem ser ativados por meio de assinatura.

**Para acessar a lista de alertas:**

Navegue até **[!UICONTROL Administração]** > **[!UICONTROL Alertas]** no menu esquerdo. A guia **Procurar** exibe todos os alertas pré-configurados disponíveis para o Journey Optimizer.

![](assets/updated-alerts-list.png){width=50%}

### Categorias de alerta

A Journey Optimizer fornece duas categorias de alertas do sistema:

>[!BEGINTABS]

>[!TAB Jornada alertas]

Monitorar a execução e o desempenho da jornada:

* [Acionador de Leitura de Público-Alvo Malsucedido](#alert-read-audiences) - Avisa quando uma atividade de Leitura de Público falha ao processar perfis
* [Taxa de Erro de Ação Personalizada Excedida](#alert-custom-action-error-rate) - Detecta altas taxas de erro em chamadas de API de ação personalizada (substitui o alerta anterior de Falha de Ação Personalizada de Jornada)
* [Taxa de Descarte de Perfil Excedida](#alert-discard-rate) - Identifica quando os perfis estão sendo descartados em uma taxa anormal
* [Taxa de Erro de Perfil Excedida](#alert-profile-error-rate) - Sinaliza quando perfis encontram erros durante a execução da jornada
* [Jornada Publicada](#alert-journey-published) - Notificação informativa quando uma jornada é publicada
* [Jornada concluída](#alert-journey-finished) - Notificação informativa quando uma jornada é concluída
* [Limite de Ação Personalizada Acionado](#alert-custom-action-capping) - Notifica quando os limites de chamada da API são atingidos

>[!TAB Alertas de configuração de canal]

Detectar problemas com a configuração da capacidade de entrega de emails:

* [Registro DNS de Domínio do AJO ausente](#alert-dns-record-missing) - Identifica registros DNS ausentes ou configurados incorretamente
* [Falha na configuração do canal do AJO](#alert-channel-config-failure) - Detecta problemas de configuração de email (registros SPF, DKIM, MX)
  <!--* the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

>[!ENDTABS]

>[!NOTE]
>
>Para obter alertas de outros serviços da Adobe Experience Platform (assimilação de dados, resolução de identidade, segmentação e muito mais), consulte a [documentação de regras de alerta padrão](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/rules.html?lang=pt-BR){target="_blank"}.

## Assinatura de alertas {#subscribe-alerts}

As assinaturas de alerta determinam quais usuários recebem notificações quando condições específicas são atendidas (como limites de taxa de erro excedidos ou problemas de configuração detectados). Somente os usuários inscritos recebem notificações de alerta para os alertas selecionados.

### Métodos de subscrição

Você pode assinar alertas de duas maneiras:

* **[Assinatura global](#global-subscription)**: aplica-se a todas as jornadas e campanhas na sandbox atual. Use esse método quando quiser monitorar todas as atividades de jornada na organização.
* **[Assinatura específica de Jornada](#unitary-subscription)**: aplica-se somente a jornadas individuais. Use esse método quando quiser monitorar jornadas específicas de alta prioridade sem receber alertas para todas as jornadas.

### Como funcionam as notificações de alerta

**Ciclo de vida do alerta:**

1. **Acionamento**: o alerta dispara quando sua condição específica é atendida (por exemplo, a taxa de erros excede 20%)
2. **Notificação**: todos os usuários inscritos recebem notificações por meio de seus canais configurados
3. **Monitoramento**: o alerta continua a monitorar a condição em intervalos regulares
4. **Solução**: quando a condição é resolvida, os assinantes recebem uma notificação &quot;Resolvido&quot;

**Entrega de notificação:**

* **Canais de entrega**: os alertas são enviados por email e/ou notificações no aplicativo na central de notificações da Journey Optimizer (ícone de sino no canto superior direito). Configure seus canais de entrega preferidos em suas [Preferências da Adobe Experience Cloud](../start/user-interface.md#in-product-uc).

* **Tipos de alerta**: o Journey Optimizer fornece alertas únicos (eventos informativos como &quot;jornada publicada&quot;) e alertas repetitivos (limites de monitoramento). Os alertas repetitivos continuam a ser avaliados e notificados até que a condição seja resolvida.

* **Resolução automática**: para evitar a fadiga da notificação de valores flutuantes, os alertas são resolvidos automaticamente após 1 hora, mesmo se a condição persistir. Isso impede notificações contínuas quando as métricas passam o mouse sobre valores limite.

**Método de assinatura alternativo:**

Para integrações avançadas, você pode assinar por meio de Eventos de I/O para enviar alertas a sistemas externos. Consulte a [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=pt-BR){target="_blank"}.


### Assinatura global {#global-subscription}

Assinaturas globais permitem que você receba alertas para todas as jornadas e campanhas na sandbox atual.

**Para assinar um alerta:**

1. Navegue até **[!UICONTROL Administração]** > **[!UICONTROL Alertas]** no menu esquerdo.

1. Na guia **[!UICONTROL Procurar]**, localize o alerta que você deseja monitorar.

1. Clique em **[!UICONTROL Assinar]** para obter o alerta desejado.

   ![Assinando um alerta](assets/alert-subscribe.png){width=80%}

**Para cancelar a inscrição:**

Clique em **[!UICONTROL Cancelar inscrição]** ao lado do alerta.

>[!IMPORTANT]
>
>As assinaturas de alerta são específicas da sandbox. Você deve assinar alertas separadamente em cada sandbox em que deseja receber notificações.

**Método de assinatura alternativo:**

Você também pode assinar por meio de [Notificações de Eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=pt-BR){target="_blank"}, o que permite a integração com sistemas externos. Os nomes de inscrição em eventos para alertas do Journey Optimizer estão listados em cada [descrição de alerta abaixo](#journey-alerts).

### Assinatura específica do Jornada {#unitary-subscription}

As assinaturas específicas de jornada permitem monitorar jornadas individuais de alta prioridade sem receber alertas para todas as jornadas da organização.

**Para assinar alertas para uma jornada específica:**

1. Vá para o inventário do jornada.

1. Clique no menu **&#x200B;**&#x200B;(mais ações) da jornada que você deseja monitorar.

1. Selecione **[!UICONTROL Assinar alertas]**.

   ![Assinando um alerta para uma jornada específica](assets/subscribe-journey-alert.png){width=75%}

1. Selecione o(s) alerta(s) que deseja ativar nas opções disponíveis:
   * [Taxa de descarte do perfil excedida](#alert-discard-rate)
   * [Taxa de erros de ação personalizada excedida](#alert-custom-action-error-rate)
   * [Taxa de erros do perfil excedida](#alert-profile-error-rate)
   * [Jornada publicada](#alert-journey-published)
   * [Jornada concluída](#alert-journey-finished)
   * [Limite de ação personalizada acionado](#alert-custom-action-capping)

1. Clique em **[!UICONTROL Salvar]** para confirmar suas assinaturas.

**Para cancelar a inscrição:**

Abra a mesma caixa de diálogo, desmarque o(s) alerta(s) e clique em **[!UICONTROL Salvar]**.

>[!NOTE]
>
>O alerta [Acionador de Leitura de Público-alvo sem Êxito](#alert-read-audiences) está disponível somente por assinatura global, não por assinatura de jornada.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=pt-BR#enable-email-alerts){target="_blank"}.-->

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

Este alerta notifica quando uma jornada é concluída. A definição de &quot;concluído&quot; varia dependendo do tipo de jornada. [Saiba mais sobre a conclusão das jornadas](../building-journeys/end-journey.md#journey-finished-definition).

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

## Tópicos relacionados {#additional-resources-alerts}

**Gerenciamento de Jornadas e campanhas:**

* [Solução de problemas do jornada](../building-journeys/troubleshooting.md) - Identificar e resolver problemas e erros comuns de jornada
* [Testar e publicar jornadas](../building-journeys/publishing-the-journey.md) - Valide a configuração do jornada antes de publicar
* [Revisar e ativar campanhas de ação](../campaigns/review-activate-campaign.md) - Validação pré-publicação para campanhas agendadas e únicas
* [Revisar e ativar campanhas acionadas por API](../campaigns/review-activate-api-triggered-campaign.md) - Validação para campanhas acionadas por API
* [Monitorar campanhas orquestradas](../orchestrated/start-monitor-campaigns.md) - Rastrear e gerenciar a execução de campanhas orquestradas

**Estrutura de alertas:**

* [Visão Geral dos Alertas do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=pt-BR){target="_blank"} - Noções básicas sobre a estrutura de alertas
* [Gerenciar alertas na interface](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=pt-BR){target="_blank"} - Exibir, assinar e gerenciar alertas
* [Assinar alertas por meio de Eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=pt-BR){target="_blank"} - Opções de integração avançadas
* [Regras padrão de alerta](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/rules.html?lang=pt-BR){target="_blank"} - Lista completa de alertas da Plataforma disponíveis
