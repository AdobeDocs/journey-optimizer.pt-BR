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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 26%

---

# Adicionar um registro TXT do Google a um subdomínio

Os registros TXT são um tipo de registro DNS usado para fornecer informações de texto sobre um domínio, que pode ser lido por fontes externas.

Para garantir um bom delivery de emails para endereços Gmail, o Gerenciamento de Jornadas do Cliente permite adicionar registros especiais TXT de verificação de site do Google a seus subdomínios para garantir que eles sejam verificados.

>[!NOTE]
>
> Essa operação só pode ser executada depois que um subdomínio tiver a variável **[!UICONTROL Success]** status. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](access-subdomains.md).

Para adicionar um registro TXT do Google ao seu subdomínio, siga estas etapas:

1. Abra o subdomínio do **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** menu.

1. Na seção Google txt record , digite o código de verificação gerado em [Ferramentas administrativas do G Suite](https://support.google.com/a/answer/183895), depois clique em **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. Depois de adicionado, o registro TXT deve ser verificado pelo Google. Para fazer isso, navegue até as ferramentas do administrador do G Suite e inicie a etapa de verificação.
