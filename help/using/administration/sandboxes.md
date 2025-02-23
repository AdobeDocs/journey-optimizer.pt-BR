---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de sandboxes
description: Saiba como gerenciar sandboxes
feature: Sandboxes
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: sandboxes, virtuais, ambientes, organização, plataforma
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 9f43387ff63c3d2c2849fad1ca6a98310b3915b3
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 56%

---

# Gerenciamento de sandboxes {#sandboxes}

## Usar sandboxes {#using-sandbox}

O [!DNL Journey Optimizer] permite particionar sua instância em ambientes virtuais separados chamados de sandboxes.
As sandboxes são atribuídas por meio de funções em Permissões. [Saiba como atribuir sandboxes](permissions.md#create-product-profile).

O [!DNL Journey Optimizer] reflete as sandboxes da Adobe Experience Platform que foram criadas para uma determinada organização. As sandboxes da Adobe Experience Platform podem ser criadas ou redefinidas pela instância da Adobe Experience Platform. [Saiba mais no guia de usuário de sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=pt-BR){target="_blank"}.

Você pode encontrar o controle do alternador de sandbox na parte superior direita da tela ao lado do nome da sua organização. Para alternar a sandbox, clique na sandbox atualmente ativa no alternador e selecione outra sandbox na lista suspensa.

![](assets/sandbox_5.png)

➡️ [Saiba mais sobre sandboxes neste vídeo](#video)

## Atribuir sandboxes {#assign-sandboxes}

>[!IMPORTANT]
>
> O gerenciamento de sandboxes só pode ser executado por um **[!UICONTROL Produto]** ou por um **[!UICONTROL Sistema]** administrador.

Você pode optar por atribuir diferentes sandboxes para **[!UICONTROL Funções]** predefinidas ou personalizadas.

Para atribuir sandboxes:

1. Em [!DNL Permissions], na guia **[!UICONTROL Funções]**, selecione uma **[!UICONTROL Função]**.

   ![](assets/sandbox_1.png)

1. Clique em **[!UICONTROL Edit]**.

1. No menu suspenso de recursos **[!UICONTROL Sandboxes]**, selecione a sandbox que será atribuída à sua função.

   ![](assets/sandbox_3.png)

1. Se necessário, clique no ícone X ao lado de remover o acesso das sandboxes à sua **[!UICONTROL Função]**.

   ![](assets/sandbox_4.png)

1. Clique em **[!UICONTROL Salvar]**.

## Acesso ao conteúdo {#content-access}

Para configurar a acessibilidade do conteúdo, é necessário atribuir uma pasta compartilhada de conteúdo a cada uma das sandboxes. Você pode criar e configurar sua pasta compartilhada na guia **[!UICONTROL Armazenamento]** exibida no [!DNL Admin Console] para administradores. Se você tiver acesso ao [!DNL Admin Console] como administrador do sistema, poderá criar pastas compartilhadas e adicionar delegados com nível de acesso diferente às suas pastas compartilhadas.

![](assets/do-not-localize/content_access.png)

Observe que para que o conteúdo seja sincronizado com a sandbox correta, é necessário seguir a mesma sintaxe da sandbox. Por exemplo, se a sandbox for chamada de desenvolvimento, a pasta compartilhada deverá ter o mesmo nome.

[Saiba como gerenciar pastas compartilhadas](https://helpx.adobe.com/br/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## Vídeo tutorial{#video}

Entenda o que são sandboxes e como distinguir sandboxes de desenvolvimento e produção. Saiba como criar, redefinir e excluir sandboxes.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)