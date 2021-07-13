---
title: Delegar subdomínios
description: Saiba como delegar subdomínios
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Configurações do aplicativo
topic: Administração
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 27%

---


# Adicionar um registro TXT do Google a um subdomínio

Os registros TXT são um tipo de registro DNS usado para fornecer informações de texto sobre um domínio, que pode ser lido por fontes externas.

Para garantir um bom delivery de emails para endereços Gmail, o Gerenciamento de Jornadas do Cliente permite adicionar registros especiais TXT de verificação de site do Google aos subdomínios para garantir que eles sejam verificados.

>[!NOTE]
>
> Essa operação só pode ser executada depois que um subdomínio tiver o status **[!UICONTROL Success]** . Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](access-subdomains.md).

Para adicionar um registro TXT do Google ao seu subdomínio, siga estas etapas:

1. Abra o subdomínio no menu **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**.

1. Na seção do registro de texto do Google, digite o código de verificação gerado em [G Suite Admin tools](https://support.google.com/a/answer/183895) e clique em **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. Depois de adicionado, o registro TXT deve ser verificado pelo Google. Para fazer isso, navegue até as ferramentas do administrador do G Suite e inicie a etapa de verificação.
