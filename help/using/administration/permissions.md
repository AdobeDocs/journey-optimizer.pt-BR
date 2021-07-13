---
title: Gerenciar usuários e perfis de produtos
description: Saiba como gerenciar permissões
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Grupos de controle
topic: Administração
role: Admin
level: Intermediate
source-git-commit: 7e879a56a5ed416cc12c2acc3131e17f9dd1e757
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 15%

---

# Gerenciar usuários e perfis de produtos {#manage-permissions}

>[!IMPORTANT]
>
> Cada um dos procedimentos detalhados abaixo só pode ser executado por um administrador **[!UICONTROL Product]** ou **[!UICONTROL System]**. Para obter mais informações, consulte a [documentação do Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Product profiles]** são conjuntos de usuários que compartilham as mesmas permissões e sandboxes em sua organização.

O produto [!DNL Journey Optimizer] permite selecionar entre diferentes níveis prontos para uso **[!UICONTROL Product profiles]** com diferentes níveis de permissões para atribuir aos usuários. Para obter mais informações sobre o **[!UICONTROL Product profiles]** disponível, consulte esta [página](ootb-product-profiles.md).

Cada usuário pertencente a um **[!UICONTROL Product profiles]** tem direito com os aplicativos e serviços do Adobe contidos no produto.

Você também pode criar seu próprio **[!UICONTROL Product profiles]** se quiser ajustar o acesso dos usuários a determinadas funcionalidades ou objetos na interface.

## Atribuição de um perfil de produto {#assigning-product-profile}

Você pode optar por atribuir um **[!UICONTROL Product profile]** personalizado ou predefinido aos usuários.

A lista de cada perfil de produto pronto para uso com permissões atribuídas pode ser encontrada na seção [Perfis de produto incorporados](ootb-product-profiles.md).

Para atribuir um **[!UICONTROL Product profile]**:

1. Na guia [!DNL Admin Console], na guia **[!UICONTROL Products]**, selecione o produto **[!UICONTROL Experience Cloud - Platform powered applications]**.

1. Selecione um **[!UICONTROL Product profile]**.

   ![](../assets/do-not-localize/access_control_2.png)

1. Na guia **[!UICONTROL Users]**, clique em **[!UICONTROL Add user]**.

   ![](../assets/do-not-localize/access_control_3.png)

1. Digite o nome do usuário ou endereço de email e selecione o usuário.

   Se o usuário não tiver sido criado anteriormente no [!DNL Admin Console], consulte a [Documentação Adicionar usuários](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](../assets/do-not-localize/access_control_4.png)

1. Siga as mesmas etapas descritas acima para adicionar outros usuários a **[!UICONTROL Product profile]**. Em seguida, clique em **[!UICONTROL Save]**.

O usuário deve receber um email de redirecionamento para sua instância.

Para obter mais informações sobre o gerenciamento de usuários, consulte a [documentação do Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Ao acessar a instância, o usuário verá uma exibição específica dependendo das permissões atribuídas no **[!UICONTROL Product profile]**. Se o usuário não tiver o acesso correto a um recurso, a tela a seguir será exibida.

![](../assets/do-not-localize/access_control_1.png)

## Edição de um perfil de produto existente {#edit-product-profile}

Para soluções prontas para uso ou personalizadas **[!UICONTROL Product profiles]**, é possível adicionar ou excluir permissões a qualquer momento.

Neste exemplo, queremos adicionar **[!UICONTROL Permissions]** relacionado ao recurso **[!UICONTROL Message]** para usuários atribuídos ao visualizador de Jornada **[!UICONTROL Product profile]**. Os usuários poderão publicar mensagens.

Observe que, se modificar um **[!UICONTROL Product profile]** pronto para uso ou personalizado, isso afetará todos os usuários atribuídos a esse **[!UICONTROL Product profile]**.

1. Na guia [!DNL Admin Console], na guia **[!UICONTROL Products]**, selecione o produto **[!UICONTROL Experience Cloud - Platform powered applications]**.

1. Selecione o visualizador de Jornada **[!UICONTROL Product profile]**.

1. Selecione a guia **[!UICONTROL Permissions]**.

   A guia **[!UICONTROL Permissions]** exibe a lista de recursos que se aplicam ao produto **[!UICONTROL Experience Cloud - Platform powered applications]**.

   ![](../assets/do-not-localize/access_control_5.png)

1. Selecione o recurso **[!UICONTROL Messages]**.

   ![](../assets/do-not-localize/access_control_6.png)

1. Na lista **[!UICONTROL Available Permission Items]**, selecione as permissões a serem atribuídas a **[!UICONTROL Product profile]** clicando no ícone de adição (+).

   Aqui, adicionamos a permissão **[!UICONTROL Publish messages]** .

   ![](../assets/do-not-localize/access_control_7.png)

1. Se necessário, no **[!UICONTROL Included Permission Items]**, clique no ícone X ao lado de remover permissões do perfil do produto.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   ![](../assets/do-not-localize/access_control_8.png)

Se necessário, também é possível criar um novo perfil de produto com permissões específicas. Para obter mais informações, consulte [Criação de um perfil de produto](#create-product-profile).

## Criação de um perfil de produto {#create-product-profile}

[!DNL Journey Optimizer] O permite criar o seu próprio  **[!UICONTROL Product profiles]** e atribuir um conjunto de permissões e sandboxes aos usuários. Com **[!UICONTROL Product profiles]**, você pode autorizar ou negar acesso a determinadas funcionalidades ou objetos na interface.

Para obter mais informações sobre como criar e gerenciar sandboxes, consulte a [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=pt-BR){target=&quot;_blank&quot;}.

Neste exemplo, criaremos um perfil de produto chamado **Jornada somente leitura**, onde concederemos direitos somente leitura ao recurso Jornada. Os usuários só poderão acessar e visualizar jornadas e não poderão acessar outros recursos, como **[!UICONTROL Decision management]** ou **[!UICONTROL Messages]** em [!DNL Journey Optimizer].

Para criar o **Jornada somente leitura** **[!UICONTROL product profiles]**:

1. Acesse o [!DNL Admin Console].

1. Na guia **[!UICONTROL Products]** , selecione o produto **[!UICONTROL Experience Cloud - Platform powered applications]**.

1. Clique em **[!UICONTROL New Profile]**.

   ![](../assets/do-not-localize/access_control_9.png)

1. Adicione um **[!UICONTROL Product Profile Name]**, **[!UICONTROL Display Name]** e **[!UICONTROL Description]** para seu novo **[!UICONTROL product profiles]**.

   ![](../assets/do-not-localize/access_control_10.png)

1. Na categoria **[!UICONTROL Notifications]**, escolha se os usuários serão notificados por email quando forem adicionados ou removidos do perfil de produto.

1. Quando terminar, clique em **[!UICONTROL Save]** e selecione o **[!UICONTROL product profiles]** recém-criado.

1. Para adicionar permissões para que usuários acessem diferentes recursos, selecione a guia **[!UICONTROL Permissions]** .

1. Selecione entre os diferentes recursos, como **[!UICONTROL Messages]**, **[!UICONTROL Segments]** ou **[!UICONTROL Decision management]** disponíveis em [!DNL Journey Optimizer] listados no menu à esquerda.

   Aqui selecionamos o recurso **[!UICONTROL Journeys]**.

   ![](../assets/do-not-localize/access_control_11.png)

1. Na lista **[!UICONTROL Available Permission Items]**, selecione as permissões a serem atribuídas a **[!UICONTROL Product profile]** clicando no ícone de adição (+).

   Aqui selecionamos **[!UICONTROL View journeys]** e **[!UICONTROL View journeys event, data sources, actions]**.

   ![](../assets/do-not-localize/access_control_12.png)

1. Selecione o recurso **[!UICONTROL Sandbox access]** para escolher as sandboxes que serão atribuídas a **[!UICONTROL Product profile]**.

   ![](../assets/do-not-localize/access_control_13.png)

1. Em **[!UICONTROL Available Permissions Items]**, clique no ícone de adição (+) para atribuir sandboxes ao perfil. [Saiba mais sobre sandboxes](sandboxes.md).

1. Quando terminar, clique em **[!UICONTROL Save]**.

Seu **[!UICONTROL Product profile]** foi criado e configurado. Agora é necessário atribuí-lo aos usuários.

Para obter mais informações sobre a criação e o gerenciamento de perfis de produtos, consulte a [documentação do Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
