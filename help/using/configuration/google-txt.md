---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar um registro TXT do Google a um subdomínio
description: Saiba como adicionar um registro TXT do Google a um subdomínio
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: subdomínio, google, txt, registro, gmail, capacidade de entrega
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 24%

---

# Adicionar um registro TXT do Google a um subdomínio {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Registros TXT do Google"
>abstract="Para garantir a entrega bem-sucedida de emails para endereços Gmail, você pode adicionar registros TXT de verificação de site do Google ao seu subdomínio para garantir que eles sejam verificados."

Os registros TXT são um tipo de registro DNS usado para fornecer informações de texto sobre um domínio, que pode ser lido por fontes externas.

Para garantir a capacidade ideal de delivery e o sucesso do delivery de emails para endereços Gmail, [!DNL Journey Optimizer] O permite adicionar registros TXT especiais de verificação de site do Google ao subdomínio para verificar se ele foi verificado.

>[!CAUTION]
>
> Esta operação só poderá ser executada depois que um subdomínio tiver o **[!UICONTROL Sucesso]** status. Para obter mais informações sobre os status dos subdomínios, consulte [nesta seção](about-subdomain-delegation.md#access-delegated-subdomains).

Para adicionar um registro TXT do Google ao subdomínio, siga estas etapas:

1. Abra o subdomínio na **[!UICONTROL Canais]** / **[!UICONTROL Subdomínios]** menu.

1. No **[!UICONTROL registro txt do Google]** insira o código de verificação gerado de [Espaço de trabalho Google](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->e, em seguida, clique em **[!UICONTROL Salvar]**.

   ![](assets/subdomain-google-txt.png)

1. Depois de adicionado, o registro TXT deve ser verificado pelo Google. Para fazer isso, navegue até [Espaço de trabalho Google](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->, depois inicie a etapa de verificação.
