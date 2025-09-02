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
source-git-commit: c39a71da901b888ff440a1488658b577ff72cc32
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 19%

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

## Substituir o campo de execução padrão {#override-default-execution-address}

>[!CONTEXTUALHELP]
>id="ajo_journey_execution_address"
>title="Definir um valor personalizado"
>abstract="Em alguns casos específicos, é possível substituir o endereço de execução padrão. Use o ícone **Habilitar substituição de parâmetro** à direita do campo para definir um endereço principal personalizado."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/configuration/primary-email-addresses#journey-parameters" text="Sobre o endereço de execução"

Para casos de uso específicos, é possível substituir o conjunto de campos de execução globalmente e definir um valor diferente no nível de configuração de email ou no nível de jornada.

Substituir esse valor pode ser útil, por exemplo, para:

* Teste um email. É possível adicionar seu próprio endereço de email: depois de publicar a jornada, o email será enviado para você.
* Enviar um email aos assinantes de uma lista. Saiba mais [neste caso de uso](../building-journeys/message-to-subscribers-uc.md).

### Na configuração do email

Você pode alterar o campo de execução padrão definido nas [configurações gerais](#admin-settings) ao definir uma configuração de canal de email. [Saiba mais](../email/email-settings.md#execution-address)

Quando um endereço de execução é definido na configuração de email, ele é usado como o endereço principal e substitui a configuração geral no nível da sandbox.

### Nos parâmetros de jornada {#journey-parameters}

Ao adicionar uma ação de **[!UICONTROL Email]** ou **[!UICONTROL SMS]** a uma [jornada](../email/create-email.md#create-email-journey-campaign), o endereço de email principal é exibido nos parâmetros avançados de jornada.

Em alguns contextos específicos, é possível substituir esse valor usando o ícone **[!UICONTROL Habilitar substituição de parâmetro]** à direita do campo.

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>A substituição de endereço de email deve ser usada somente para casos de uso específicos. Na maioria das vezes, não é necessário alterar o endereço de email, pois o valor definido como o endereço principal nos **[!UICONTROL Campos de execução]** é o que deve ser usado.


