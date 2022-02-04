---
title: Adicionar um registro TXT do Google a um subdomínio
description: Saiba como adicionar um registro TXT do Google a um subdomínio
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: dcdbf4a0cd6a93e56cbe97535515c1a6143db81b
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 26%

---

# Adicionar um registro TXT do Google a um subdomínio {#google-txt-record}

Os registros TXT são um tipo de registro DNS usado para fornecer informações de texto sobre um domínio, que pode ser lido por fontes externas.

Para garantir uma boa capacidade de delivery e o delivery bem-sucedido de emails para endereços Gmail, [!DNL Journey Optimizer] O permite adicionar registros TXT de verificação de site do Google especiais a seus subdomínios para garantir que eles sejam verificados.

>[!CAUTION]
>
> Essa operação só pode ser executada depois que um subdomínio tiver a variável **[!UICONTROL Success]** status. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](access-subdomains.md).

Para adicionar um registro TXT do Google ao seu subdomínio, siga estas etapas:

1. Abra o subdomínio do **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** menu.

1. No **[!UICONTROL Google txt record]** , digite o código de verificação gerado a partir de [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, depois clique em **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. Depois de adicionado, o registro TXT deve ser verificado pelo Google. Para fazer isso, navegue até [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->e inicie a etapa de verificação.
