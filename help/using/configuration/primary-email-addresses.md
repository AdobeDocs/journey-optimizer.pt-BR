---
solution: Journey Optimizer
product: journey optimizer
title: Alterar os endereços de execução
description: Saiba como determinar qual endereço de email usar no serviço de perfil.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: principal, execução, e-mail, destino, perfil, otimizador
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: fc12ee65fc773c70b88504a951e5f5c5b2b3b0e6
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 23%

---

# Alterar os endereços de execução {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definir qual endereço usar"
>abstract="Quando vários endereços de email ou números de telefone estão disponíveis no banco de dados (pessoal, profissional etc.), você pode escolher qual deles priorizar para envio."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="Definir qual endereço usar"
>abstract="Edite os campos usados para determinar o endereço de email ou número de telefone dos perfis para priorizar o envio."

Ao direcionar um perfil, vários endereços de email ou números de telefone podem estar disponíveis no banco de dados (endereço de email profissional, número de telefone pessoal etc.).

Nesse caso, [!DNL Journey Optimizer] usa **[!UICONTROL Campos de execução]** para determinar qual endereço de email ou número de telefone usar do serviço de perfil em prioridade.

Para verificar os campos que são usados por padrão no momento, acesse o menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configurações gerais]** > **[!UICONTROL Campos de execuções]**.

![](assets/primary-address-execution-fields.png)

>[!NOTE]
>
>Os campos de execução estão disponíveis para os canais de email e SMS.

Os valores atuais são usados para todos os deliveries no nível da sandbox. Você pode atualizar esses campos, se necessário.

Na maioria dos casos, você alterará um campo de execução globalmente e definirá um valor que deve ser usado para todas as mensagens de email ou SMS. <!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## Atualizar as configurações de Administração {#admin-settings}

Para alterar os campos de execução globalmente no nível da sandbox, siga as etapas abaixo.

1. Acesse o menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações gerais]** > **[!UICONTROL Campos de execuções]**.

1. Clique em **[!UICONTROL Editar]** para alterar os valores padrão.

   ![](assets/primary-address.png)

1. Clique no campo atual de sua escolha ou no ícone de edição para selecionar um novo campo.

   ![](assets/primary-address-edit.png)

1. A lista de campos XDM do tipo email disponíveis é exibida. Selecione o campo a ser usado.

   ![](assets/primary-address-select-field.png)

1. Clique em **[!UICONTROL Salvar]** para confirmar sua escolha.

O campo de execução é atualizado e agora será usado como o endereço principal.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## Substitua o campo de execução padrão nos parâmetros de jornada {#override-execution-address-journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_execution_address"
>title="Definir um valor personalizado"
>abstract="Em alguns casos específicos, é possível substituir o endereço de execução padrão. Use o ícone **Habilitar substituição de parâmetro** à direita do campo para definir um endereço principal personalizado."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/configuration/primary-email-addresses#journey-parameters" text="Sobre o endereço de execução"

Para casos de uso específicos, é possível substituir o conjunto de campos de execução globalmente e definir um valor diferente no nível da jornada.

Substituir esse valor pode ser útil, por exemplo, para:

* Teste um email. É possível adicionar seu próprio endereço de email: depois de publicar a jornada, o email será enviado para você.
* Enviar um email aos assinantes de uma lista. Saiba mais [neste caso de uso](../building-journeys/message-to-subscribers-uc.md).

Ao adicionar uma ação de **[!UICONTROL Email]** ou **[!UICONTROL SMS]** a uma [jornada](../email/create-email.md#create-email-journey-campaign), o endereço de email principal é exibido nos parâmetros avançados de jornada.

Substitua esse valor usando o ícone **[!UICONTROL Habilitar substituição de parâmetro]** à direita do campo.

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>A substituição de endereço de email deve ser usada somente para casos de uso específicos. Na maioria das vezes, não é necessário alterar o endereço de email, pois o valor definido como o endereço principal nos **[!UICONTROL Campos de execução]** é o que deve ser usado.

## Substituir o campo de execução padrão na configuração do canal {#override-execution-address-channel-config}

>[!CONTEXTUALHELP]
>id="ajo_email_config_execution_address"
>title="Substituir o endereço de execução padrão a ser usado"
>abstract="Quando vários endereços de email ou números de telefone estiverem disponíveis no banco de dados (pessoal, profissional etc.), você poderá escolher qual deles priorizar para envio. O endereço principal é definido no nível da sandbox, mas aqui você pode substituir a configuração padrão para essa configuração de canal específica."

Você pode alterar o endereço de execução padrão de uma [configuração de canal](channel-surfaces.md) de email ou SMS específica.

Para fazer isso, vá para a seção **[!UICONTROL Execution dimension]** e edite o campo em **[!UICONTROL Execution Address]**.

![](assets/sms-config-execution-address.png){width=85%}

Em seguida, selecione um item na lista de campos XDM do tipo email disponíveis.

![](assets/sms-config-execution-field.png)

O campo de execução é atualizado e, em seguida, usado como o endereço principal das campanhas ou jornadas que usam essa configuração de canal. Ele substitui a [configuração geral](#admin-settings) definida no nível da sandbox.

<!--[Learn more on the execution address in the email configuration ](../email/email-settings.md#execution-address)-->
