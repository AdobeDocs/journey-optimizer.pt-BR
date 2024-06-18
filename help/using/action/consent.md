---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com políticas de consentimento
description: Saiba como trabalhar com as políticas de consentimento da Adobe Experience Platform
feature: Journeys, Actions, Custom Actions, Privacy, Consent Management
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: políticas, governança, plataforma, healthcare shield, consentimento
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 95%

---

# Trabalhar com políticas de consentimento {#consent-management}

Seus dados podem estar sujeitos a restrições de uso definidas por sua organização ou por regulamentos legais. Portanto, é importante garantir que suas operações de dados no Journey Optimizer estejam em conformidade com [políticas de uso de dados](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=pt-BR){target="_blank"}. Essas políticas são regras do Adobe Experience Platform que definem quais [ações de marketing](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=pt-BR#marketing-actions){target="_blank"} você tem permissão para executar nos dados.

Um tipo de política de uso de dados disponível é a **política de consentimento**. Elas permitem adotar e aplicar facilmente políticas de marketing para respeitar as preferências de consentimento dos clientes. [Saiba mais sobre a aplicação de políticas](https://experienceleague.adobe.com/docs/experience-platform/data-governance/enforcement/auto-enforcement.html?lang=pt-BR){target="_blank"}

>[!IMPORTANT]
>
>Atualmente, as políticas de consentimento estão disponíveis apenas para as organizações que compraram as ofertas complementares do Adobe **Healthcare Shield** ou do **Privacy and Security Shield** .

Por exemplo, é possível [criar políticas de consentimento](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=pt-BR#consent-policy){target="_blank"} na Experience Platform para excluir clientes que não consentiram em receber comunicações por email, push ou SMS.

* Para os canais de saída nativos (Email, Push, SMS, Correspondência direta), a lógica é a seguinte:

   * Por padrão, se um perfil não aceitou receber suas comunicações, ele será excluído das entregas subsequentes.

   * Se você tem o Adobe **Healthcare Shield** ou o **Privacy and Security Shield**, poderá criar uma política de consentimento personalizada que substitua a lógica padrão. Por exemplo, é possível definir uma política para apenas enviar mensagens de email às pessoas físicas que aceitaram recebê-las. Na ausência de uma política personalizada, a política padrão é aplicada.

  Para aplicar uma política personalizada, defina uma ação de marketing nessa política e associe-a a uma superfície de canal. [Saiba mais](#surface-marketing-actions)

No nível da jornada, é possível aplicar políticas de consentimento às suas ações personalizadas:

* Ao **configurar uma ação personalizada**, é possível definir um canal e uma ação de marketing. [Saiba mais](#consent-custom-action)
* Ao adicionar a **ação personalizada em uma jornada**, é possível definir uma ação de marketing adicional. [Saiba mais](#consent-journey)

## Utilizar políticas de consentimento por meio de superfícies de canal {#surface-marketing-actions}

No [!DNL Journey Optimizer], o consentimento é tratado pelo [Esquema de consentimento](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=pt-BR) da Experience Platform{target="_blank"}. Por padrão, o valor do campo de consentimento fica vazio e é tratado como consentimento para receber suas comunicações. Durante a integração, é possível modificar esse valor padrão para um dos valores possíveis listados [aqui](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=pt-BR#choice-values){target="_blank"}.

Para modificar o valor do campo de consentimento, crie uma política de consentimento personalizada e defina uma ação de marketing para ela, bem como as condições sob as quais essa ação é executada. [Saiba mais sobre ações de marketing](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=pt-BR#marketing-actions){target="_blank"}

Por exemplo, caso queira criar uma política de consentimento para direcionar apenas perfis que aceitaram receber comunicações por email, siga as etapas abaixo.

1. Verifique se sua organização adquiriu as ofertas complementares do Adobe **Healthcare Shield** ou **Privacy and Security Shield**. [Saiba mais](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html?lang=pt-BR){target="_blank"}

1. Na Adobe Experience Platform, crie uma política personalizada (no menu **[!UICONTROL Privacidade]** > **[!UICONTROL Políticas]**). [Saiba como](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=pt-BR#create-policy){target="_blank"}

   <!--![](assets/consent-policy-create.png)-->

1. Escolha o tipo de **[!UICONTROL Política de consentimento]** e configure uma condição da seguinte maneira. [Saiba como configurar políticas de consentimento](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=pt-BR#consent-policy){target="_blank"}

   1. Na seção **[!UICONTROL Se]**, selecione a ação de marketing padrão **[!UICONTROL Direcionamento de email]**.

      <!--![](assets/consent-policy-marketing-action.png)-->

      >[!NOTE]
      >
      >As principais ações de marketing fornecidas prontas para uso pelo Adobe estão listadas em [esta tabela](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=pt-BR#core-actions){target="_blank"}. As etapas para criar uma ação de marketing personalizada estão listadas em [nesta seção](https://experienceleague.adobe.com/docs/ Experience-platform/data-governance/policies/user-guide.html?lang=pt-BR#create-marketing-action){target="_blank"}.

   1. Selecione o que acontece quando a ação de marketing é aplicada. Neste exemplo, selecione **[!UICONTROL Consentimento de marketing por email]**.

   ![](assets/consent-policy-then.png)

1. Salve e [habilite](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=pt-BR#enable){target="_blank"} essa política.

1. No Journey Optimizer, crie uma superfície de email. [Saiba como](../configuration/channel-surfaces.md#create-channel-surface)

1. Nos detalhes da superfície de email, selecione a ação de marketing **[!UICONTROL Direcionamento de email]**.

   ![](assets/surface-marketing-action.png)

Todas as políticas de consentimento associadas a essa ação de marketing são automaticamente utilizadas, a fim de respeitar as preferências de clientes.

Portanto, nesse exemplo, qualquer [email](../email/create-email.md) que use essa superfície em uma campanha ou jornada só é enviado aos perfis que aceitaram o recebimento de emails. Perfis que não aceitaram receber comunicações por email são excluídos.

## Aproveitar as políticas de consentimento por meio de ações personalizadas {#journey-custom-actions}

### Observações importantes {#important-notes}

No Journey Optimizer, o consentimento também pode ser aproveitado em ações personalizadas. Se quiser usá-lo com os recursos de mensagem integrados, é necessário usar uma atividade de condição para filtrar os clientes na jornada.

Com o gerenciamento de consentimento, duas atividades de jornada são analisadas:

* Público-alvo de leitura: o público-alvo recuperado é considerado.
* Ação personalizada: o gerenciamento de consentimento leva em conta os atributos usados ([parâmetros de ação](../action/about-custom-action-configuration.md#define-the-message-parameters)) e as ações de marketing definidas (a ação de marketing necessária e a adicional).
* Os atributos que fazem parte de um grupo de campos usando o esquema de união predefinido não são compatíveis. Esses atributos ficarão ocultos na interface. É necessário criar outro grupo de campos usando um schema diferente.
* As políticas de consentimento só se aplicam quando uma ação de marketing (necessária ou adicional) é definida no nível da ação personalizada.

Todas as outras atividades usadas em uma jornada não são consideradas. Se iniciar a jornada com uma Qualificação de público-alvo, o público-alvo não será considerado.

Em uma jornada, se um perfil for excluído por causa de uma política de consentimento em uma ação personalizada, a mensagem não será enviada para ele, mas ele permanecerá na jornada. O perfil não irá para o caminho de erro e de tempo limite ao usar uma condição.

Antes de atualizar as políticas em uma ação personalizada inserida em uma jornada, verifique se a jornada não tem nenhum erro.

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

### Configuração da ação personalizada {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action"
>title="Definir uma ação de marketing necessária"
>abstract="A Ação de marketing necessária permite definir a ação de marketing relacionada à sua ação personalizada. Por exemplo, se você usar essa ação personalizada para enviar emails, será possível selecionar a opção Direcionamento de email. Quando usadas em uma jornada, todas as políticas de consentimento associadas a essa ação de marketing serão recuperadas e aproveitadas. Isso não pode ser modificado na tela."

Ao configurar uma ação personalizada, dois campos podem ser usados para o gerenciamento de consentimento.

O campo **Canal** permite selecionar o canal relacionado a esta ação personalizada: **Email**, **SMS** ou **Notificação por push**. Ele preencherá previamente o campo **Ação de marketing necessária** com a ação de marketing padrão do canal selecionado. Se você selecionar **outra**, nenhuma ação de marketing será definida por padrão. 

![](assets/consent1.png)

A **Ação de marketing necessária** permite definir a ação de marketing relacionada à sua ação personalizada. Por exemplo, se você usar essa ação personalizada para enviar emails, será possível selecionar a opção **Direcionamento de email**. Quando usadas em uma jornada, todas as políticas de consentimento associadas à ação de marketing em questão serão recuperadas e aproveitadas. Uma ação de marketing padrão estará selecionada, mas você pode clicar na seta para baixo para selecionar qualquer ação de marketing disponível na lista.

![](assets/consent2.png)

Para certos tipos de comunicações importantes (por exemplo, uma mensagem transacional enviada para redefinir a senha de um cliente), talvez você não queira aplicar uma política de consentimento. Então você pode selecionar **Nenhum** no campo **Ação de marketing necessária**.

As outras etapas para configurar uma ação personalizada estão detalhadas [nesta seção](../action/about-custom-action-configuration.md#consent-management).

### Construção da jornada {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_canvas"
>title="Ação de marketing necessária"
>abstract="Uma ação de marketing necessária é definida ao criar uma ação personalizada. Essa ação de marketing necessária não pode ser removida da ação nem ser modificada."

>[!CONTEXTUALHELP]
>id="ajo_consent_additional_marketing_action_canvas"
>title="Ação de marketing adicional"
>abstract="Adicione outra ação de marketing além da necessária. As políticas de consentimento relacionadas a ambas as ações de marketing serão aplicadas. "

>[!CONTEXTUALHELP]
>id="ajo_consent_refresh_policies_canvas"
>title="Visualize as políticas de consentimento que serão aplicadas no tempo de execução"
>abstract="As ações de marketing trazem políticas de consentimento que combinam os parâmetros de ação e valores de consentimento dos perfis individuais para filtrar os usuários. Obtenha a definição mais recente dessas políticas clicando no botão para atualizar."

Ao adicionar a ação personalizada em uma jornada, há várias opções que permitem gerenciar o consentimento. Clique em **Mostrar campos somente leitura** para exibir todos os parâmetros.

O **Canal** e a **Ação de marketing necessária**, definidos ao configurar a ação personalizada, são exibidos na parte superior da tela. Não é possível modificar esses campos.

![](assets/consent4.png)

Você pode configurar uma **Ação de marketing adicional** para definir o tipo de ação personalizada. Isso permite definir a finalidade da ação personalizada nesta jornada. Além da ação de marketing necessária, que geralmente é específica de um canal, é possível definir uma ação de marketing adicional, que será específica da ação personalizada da jornada em questão. Por exemplo: um comunicado de treino, um boletim informativo, um comunicado de fitness etc. A ação de marketing necessária junto com a ação de marketing adicional serão aplicadas.

![](assets/consent3.png)

Clique no botão **Atualizar políticas** na parte inferior da tela para atualizar e verificar a lista de políticas consideradas para esta ação personalizada. Isso é somente para fins informativos durante a criação de uma jornada. Em jornadas ativas, as políticas de consentimento são recuperadas e atualizadas automaticamente a cada 6 horas.

![](assets/consent5.png)

<!--
The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* action parameters defined in the custom action, see this [section](../action/about-custom-action-configuration.md#define-the-message-parameters) 
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-audience.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

As outras etapas para configurar uma ação personalizada em uma jornada são detalhadas [nesta seção](../building-journeys/using-custom-actions.md).
