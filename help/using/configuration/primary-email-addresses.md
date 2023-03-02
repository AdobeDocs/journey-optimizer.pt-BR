---
solution: Journey Optimizer
product: journey optimizer
title: Alterar os endereços de email principais
description: Saiba como determinar qual endereço de email usar no serviço de perfil.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: principal, execução, e-mail, destino, perfil, otimizador
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---

# Alterar os endereços principais {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definir qual endereço usar"
>abstract="Quando vários endereços de email ou números de telefone estiverem disponíveis no banco de dados (pessoal, profissional etc.), você poderá escolher qual deles priorizar para envio."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="Definir qual endereço usar"
>abstract="Edite os campos usados para determinar o endereço de email ou o número de telefone dos perfis que serão priorizados para envio."

Ao direcionar um perfil, vários endereços de email ou números de telefone podem estar disponíveis no banco de dados (endereço de email profissional, número de telefone pessoal etc.).

Com [!DNL Journey Optimizer], você pode determinar qual endereço de email ou número de telefone usar no serviço de perfil e priorizar quando vários endereços estiverem disponíveis. Para fazer isso, siga as etapas abaixo.

1. Acesse o  **[!UICONTROL Canais]** > **[!UICONTROL Geral]** > **[!UICONTROL Campos de execuções]** menu.

   ![](assets/primary-address-execution-fields.png)

1. Os campos atualmente usados por padrão para determinar o endereço de email e o número de telefone dos perfis são exibidos nesta tela. Clique em **[!UICONTROL Editar]** para alterá-los.

   ![](assets/primary-address.png)

1. Clique no campo atual de sua escolha ou no ícone de edição para selecionar um novo campo.

   ![](assets/primary-address-edit.png)

1. A lista de campos XDM do tipo email disponíveis é exibida. Selecione o campo a ser usado.

   ![](assets/primary-address-select-field.png)

1. Clique em **[!UICONTROL Salvar]** para confirmar sua escolha.

O campo de execução é atualizado e agora será usado como o endereço principal.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
