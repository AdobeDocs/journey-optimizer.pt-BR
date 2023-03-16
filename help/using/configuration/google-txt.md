---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar um registro TXT do Google a um subdomínio
description: Saiba como adicionar um registro TXT do Google a um subdomínio
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: subdomínio, google, txt, registro, gmail, deliverability
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 23%

---

# Adicionar um registro TXT do Google a um subdomínio {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Registros TXT do Google"
>abstract="Para garantir a entrega bem-sucedida de emails para endereços Gmail, você pode adicionar registros TXT de verificação de site do Google ao seu subdomínio para garantir que eles sejam verificados."

Os registros TXT são um tipo de registro DNS usado para fornecer informações de texto sobre um domínio, que pode ser lido por fontes externas.

Para garantir o delivery ideal e o delivery bem-sucedido de emails para endereços Gmail, [!DNL Journey Optimizer] O permite adicionar registros especiais TXT de verificação do site do Google ao seu subdomínio para garantir que ele seja verificado.

>[!CAUTION]
>
> Essa operação só pode ser executada depois que um subdomínio tiver a variável **[!UICONTROL Sucesso]** status. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](about-subdomain-delegation.md#access-delegated-subdomains).

Para adicionar um registro TXT do Google ao seu subdomínio, siga estas etapas:

1. Abra o subdomínio do **[!UICONTROL Canais]** / **[!UICONTROL Subdomínios]** menu.

1. No **[!UICONTROL Registro de txt do Google]** , digite o código de verificação gerado a partir de [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->, depois clique em **[!UICONTROL Salvar]**.

   ![](assets/subdomain-google-txt.png)

1. Depois de adicionado, o registro TXT deve ser verificado pelo Google. Para fazer isso, navegue até [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->e inicie a etapa de verificação.
