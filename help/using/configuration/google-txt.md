---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar um registro TXT do Google a um subdomínio
description: Saiba como adicionar um registro TXT do Google a um subdomínio
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: subdomínio, google, txt, registro, gmail, capacidade de entrega
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 30%

---

# Adicionar um registro TXT do Google a um subdomínio {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Registros TXT do Google"
>abstract="Para garantir a entrega bem-sucedida de emails para endereços Gmail, você pode adicionar registros TXT de verificação de site do Google ao seu subdomínio para garantir que eles sejam verificados."

Os registros TXT são um tipo de registro DNS usado para fornecer informações de texto sobre um domínio, que pode ser lido por fontes externas.

Para garantir a entrega ideal e a entrega bem-sucedida de emails para endereços Gmail, o [!DNL Journey Optimizer] permite adicionar registros TXT especiais de verificação de site do Google ao seu subdomínio para garantir que eles sejam verificados.

>[!CAUTION]
>
> Esta operação só poderá ser executada depois que um subdomínio tiver o status **[!UICONTROL Êxito]**. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](about-subdomain-delegation.md#access-delegated-subdomains).

Para adicionar um registro TXT do Google ao subdomínio, siga estas etapas:

1. Abra o subdomínio no menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações de email]** > **[!UICONTROL Subdomínios]**.

1. Na seção **[!UICONTROL registro txt do Google]**, insira o código de verificação gerado pelo [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools--> e clique em **[!UICONTROL Salvar]**.

   ![](assets/subdomain-google-txt.png)

1. Depois de adicionado, o registro TXT deve ser verificado pelo Google. Para fazer isso, navegue até [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools--> e inicie a etapa de verificação.
