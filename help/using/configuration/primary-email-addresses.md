---
title: 'Alterar os endereços de email principais '
description: Saiba como determinar qual endereço de email usar no serviço de perfil.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 6%

---

# Alterar os endereços de email principais {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definir qual endereço usar"
>abstract="Você pode escolher qual endereço de email priorizar para envio quando vários endereços estiverem disponíveis no banco de dados (pessoal, profissional etc.)."

Ao direcionar um perfil, vários endereços de email podem estar disponíveis no banco de dados (pessoal, endereço de email profissional etc.).

Com [!DNL Journey Optimizer], você pode determinar qual endereço de email usar no serviço de perfil e priorizar quando vários endereços estiverem disponíveis. Para fazer isso, siga as etapas abaixo.

1. Acesse o menu **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]**.

   ![](assets/primary-address-execution-fields.png)

1. O campo usado atualmente para determinar os endereços de email dos perfis é exibido nessa tela. Clique em **[!UICONTROL Edit]** para alterá-lo.

   ![](assets/primary-address.png)

1. Clique no campo atual ou no ícone de edição para selecionar um novo campo.

   ![](assets/primary-address-edit.png)

1. A lista de campos XDM do tipo de email disponíveis é exibida. Selecione o campo a ser usado.

   ![](assets/primary-address-field.png)

1. Clique em **[!UICONTROL Save]** para confirmar sua escolha.

   ![](assets/primary-address-save.png)

   O campo de execução é atualizado e agora será usado como o endereço principal.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
