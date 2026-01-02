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
source-git-commit: e89bec74f597185065b274d22740324a09e9319e
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 22%

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
> Esta operação só poderá ser executada depois que um subdomínio tiver o status **[!UICONTROL Êxito]**. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](delegate-subdomain.md#access-delegated-subdomains).

Para adicionar um registro TXT do Google ao subdomínio, siga estas etapas:

1. Abra o subdomínio no menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações de email]** > **[!UICONTROL Subdomínios]**.

1. Na seção **[!UICONTROL registro txt do Google]**, insira o código de verificação gerado pelo [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools--> e clique em **[!UICONTROL Salvar]**.

   ![](assets/subdomain-google-txt.png)

1. Depois de adicionado, o registro TXT deve ser verificado pelo Google. Para fazer isso, navegue até [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools--> e inicie a etapa de verificação.

## Atualizar um registro TXT do Google {#update-google-txt-record}

Para atualizar um registro TXT do Google existente, siga estas etapas:

1. Abra o subdomínio no menu **[!UICONTROL Subdomínios]**.

1. Limpe o valor existente no campo **[!UICONTROL registro txt do Google]** e clique em **[!UICONTROL Salvar]**. Essa etapa substitui o valor do registro TXT do Google anterior por uma string vazia.

1. Agora, reabra o mesmo subdomínio e insira o novo código de verificação.

1. Clique em **[!UICONTROL Salvar]** novamente.

1. Verifique o registro atualizado por meio do [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}.
