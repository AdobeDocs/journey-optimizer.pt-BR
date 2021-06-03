---
title: Gerenciamento de sandboxes
description: Saiba como gerenciar sandboxes
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
exl-id: null
source-git-commit: e4f69cd209665e7f13a0c21e92453cd5cdce45a1
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 27%

---

# Gerenciamento de sandboxes {#sandboxes}

![](../assets/do-not-localize/badge.png)

## Usar sandboxes {#using-sandbox}

O [!DNL Journey Optimizer] permite particionar sua instância em ambientes virtuais separados chamados de sandboxes.
As sandboxes são atribuídas por meio de perfis de produto no Admin Console. [Saiba como atribuir sandboxes](permissions.md#create-product-profile).

[!DNL Journey Optimizer] O reflete sandboxes da Adobe Experience Platform que foram criadas para uma determinada organização.
As sandboxes da Adobe Experience Platform podem ser criadas ou redefinidas pela instância da Adobe Experience Platform. [Saiba mais no guia](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html) de usuário de sandbox.

Você pode encontrar o controle do alternador de sandbox na parte superior esquerda da tela. Para alternar a sandbox, clique na sandbox atualmente ativa no alternador e selecione outra sandbox na lista suspensa.

## Atribuir sandboxes {#assign-sandboxes}

>[!IMPORTANT]
>
> O gerenciamento de sandboxes só pode ser realizado por um administrador **[!UICONTROL Product]** ou **[!UICONTROL System]**. Para obter mais informações, consulte a [documentação do Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

Você pode optar por atribuir sandboxes diferentes para predefinidas ou personalizadas **[!UICONTROL Product profiles]**.

Para atribuir sandboxes:

1. Na guia [!DNL Admin Console], na guia **[!UICONTROL Products]**, selecione o produto **[!UICONTROL Adobe Experience Platform Apps]**.

1. Selecione um **[!UICONTROL Product profile]**.

1. Selecione a guia **[!UICONTROL Permissions]**.

1. Selecione o recurso **[!UICONTROL Sandbox access]**.

1. Em **[!UICONTROL Available Permissions Items]**, clique no ícone de adição (+) para atribuir sandboxes ao perfil. [Saiba mais sobre sandboxes](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html).

1. Se necessário, em **[!UICONTROL Included Permission Items]**, clique no ícone X ao lado de remover sandboxes acesso a **[!UICONTROL Product profile]**.

1. Clique em **[!UICONTROL Save]**.

## Acesso ao conteúdo {#content-access}

Para configurar a acessibilidade do conteúdo, é necessário atribuir uma pasta compartilhada de conteúdo a cada uma das sandboxes. Você pode criar e configurar a pasta compartilhada na guia **[!UICONTROL Storage]** exibida no [!DNL Admin Console] para administradores. Se você tiver acesso ao [!DNL Admin Console] como administrador do sistema, poderá criar pastas compartilhadas e adicionar delegados com nível de acesso diferente às suas pastas compartilhadas.

![](../assets/do-not-localize/content_access.png)

Observe que para que o conteúdo seja sincronizado com a sandbox correta, é necessário seguir a mesma sintaxe da sandbox. Por exemplo, se a sandbox for chamada de desenvolvimento, a pasta compartilhada deverá ter o mesmo nome.

[Saiba como gerenciar pastas](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html) compartilhadas.
