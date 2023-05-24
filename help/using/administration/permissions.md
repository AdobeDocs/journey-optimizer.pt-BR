---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar usuários e perfis de produtos
description: Saiba como gerenciar usuários e perfis de produtos
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: produto, perfis, sandbox
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 8%

---

# Gerenciar usuários e perfis de produtos {#manage-permissions}

>[!IMPORTANT]
>
> Cada um dos procedimentos a seguir especificados só pode ser executado por um **[!UICONTROL Produto]** ou **[!UICONTROL Sistema]** administrador. Para obter mais informações, consulte [Documentação do Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Perfis de produto]** são conjuntos de usuários que compartilham as mesmas permissões e sandboxes na organização.

A variável [!DNL Journey Optimizer] permite selecionar entre diferentes opções prontas para uso **[!UICONTROL Perfis de produto]** com diferentes níveis de permissões para atribuir aos usuários. Para obter mais informações sobre as **[!UICONTROL Perfis de produto]**, consulte este [página](ootb-product-profiles.md).

Cada usuário pertencente a um **[!UICONTROL Perfis de produto]** O tem direito aos aplicativos e serviços Adobe contidos no produto.

Você também pode criar o seu próprio **[!UICONTROL Perfis de produto]** se quiser ajustar o acesso dos usuários a determinadas funcionalidades ou objetos na interface.

## Atribuição de um perfil de produto {#assigning-product-profile}

Você pode optar por atribuir um pacote pronto para uso ou personalizado **[!UICONTROL Perfil do produto]** aos seus usuários.

A lista de cada perfil de produto pronto para uso com permissões atribuídas pode ser encontrada na [Perfis de produto incorporados](ootb-product-profiles.md) seção.

Para atribuir um **[!UICONTROL Perfil do produto]**:

1. No [!DNL Admin Console], do **[!UICONTROL Produtos]** , selecione a **[!UICONTROL Experience Cloud - Aplicativos alimentados por plataforma]** produto.

1. Selecione um **[!UICONTROL Perfil do produto]**.

   ![](assets/do-not-localize/access_control_2.png)

1. No **[!UICONTROL Usuários]** clique em **[!UICONTROL Adicionar usuário]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Digite o nome de usuário ou endereço de email e selecione o usuário.

   Se o usuário não tiver sido criado anteriormente na variável [!DNL Admin Console], consulte o [Adicionar documentação de usuários](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

1. Siga as mesmas etapas descritas acima para adicionar outros usuários ao seu **[!UICONTROL Perfil do produto]**. Em seguida, clique em **[!UICONTROL Salvar]**.

O usuário deve receber um email de redirecionamento para sua instância.

Para obter mais informações sobre o gerenciamento de usuários, consulte [Documentação do Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Ao acessar a instância, o usuário verá uma visualização específica, dependendo das permissões atribuídas no **[!UICONTROL Perfil do produto]**. Se o usuário não tiver o acesso correto a um recurso, a seguinte mensagem será exibida:

`You don't have permission to access this feature. Permission needed: XX.`

## Edição de um perfil de produto existente {#edit-product-profile}

Para uso imediato ou personalizado **[!UICONTROL Perfis de produto]**, você pode decidir adicionar ou excluir permissões a qualquer momento.

Neste exemplo, queremos adicionar **[!UICONTROL Permissões]** relacionado com o **[!UICONTROL Jornadas]** recurso para usuários atribuídos ao visualizador de Jornadas **[!UICONTROL Perfil do produto]**. Os usuários poderão publicar jornadas.

Observe que, se você modificar um pacote pronto para uso ou personalizado, **[!UICONTROL Perfil do produto]**, afetará cada usuário atribuído a este **[!UICONTROL Perfil do produto]**.

1. No [!DNL Admin Console], do **[!UICONTROL Produtos]** , selecione a **[!UICONTROL Experience Cloud - Aplicativos alimentados por plataforma]** produto.

1. Selecionar o visualizador de Jornadas **[!UICONTROL Perfil do produto]**.

1. Selecione a guia **[!UICONTROL Permissões.]**

   A variável **[!UICONTROL Permissões]** exibe a lista de recursos que se aplicam à variável **[!UICONTROL Experience Cloud - Aplicativos alimentados por plataforma]** produto.

   ![](assets/do-not-localize/access_control_5.png)

1. Selecione o **[!UICONTROL Jornadas]** capacidade.

   ![](assets/do-not-localize/access_control_6.png)

1. No **[!UICONTROL Itens de permissão disponíveis]** selecione as permissões a serem atribuídas ao seu **[!UICONTROL Perfil do produto]** clicando no ícone de adição (+).

   Aqui, adicionamos a variável **[!UICONTROL Publicar Jornadas]** permissão.

1. Se necessário, em **[!UICONTROL Itens de permissão incluídos]**, clique no ícone X ao lado de remover permissões do perfil do produto.

1. Ao terminar, clique em **[!UICONTROL Salvar]**.

Se necessário, também é possível criar um novo perfil de produto com permissões específicas. Para obter mais informações, consulte [Criação de um perfil de produto](#create-product-profile).

## Criação de um perfil de produto {#create-product-profile}

[!DNL Journey Optimizer] permite criar o seu próprio **[!UICONTROL Perfis de produto]** e atribua um conjunto de permissões e sandboxes aos usuários. Com **[!UICONTROL Perfis de produto]**, você pode autorizar ou negar acesso a determinadas funcionalidades ou objetos na interface.

Para obter mais informações sobre como criar e gerenciar sandboxes, consulte a [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=pt-BR){target="_blank"}.

Neste exemplo, criaremos um perfil de produto chamado **Jornada somente leitura** onde concederemos direitos somente leitura ao recurso de Jornada. Os usuários só poderão acessar e visualizar jornadas e não poderão acessar outros recursos, como **[!DNL  Decision management]** in [!DNL Journey Optimizer].

Para criar o nosso **Jornada somente leitura** **[!UICONTROL perfis de produto]**:

1. Acesse o [!DNL Admin Console].

1. No **[!UICONTROL Produtos]** , selecione a **[!UICONTROL Experience Cloud - Aplicativos alimentados por plataforma]** produto.

1. Clique em **[!UICONTROL Novo perfil]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Adicionar um **[!UICONTROL Nome do perfil do produto]**, **[!UICONTROL Nome de exibição]** e **[!UICONTROL Descrição]** para o seu novo **[!UICONTROL perfis de produto]**.

   ![](assets/do-not-localize/access_control_10.png)

1. No **[!UICONTROL Notificação]** escolha se os usuários serão notificados por email quando forem adicionados ou removidos deste perfil de produto.

1. Quando terminar, clique em **[!UICONTROL Salvar]** e selecione o recém-criado **[!UICONTROL perfis de produto]**.

1. Para adicionar permissões para que os usuários acessem diferentes recursos, selecione a **[!UICONTROL Permissões]** guia.

1. Selecione entre os diferentes recursos, como **[!DNL Journeys]**, **[!DNL Segments]** ou **[!DNL Decision management]** disponível em [!DNL Journey Optimizer] listado no menu à esquerda.

   Aqui selecionamos o **[!UICONTROL Jornadas]** capacidade.

   ![](assets/do-not-localize/access_control_11.png)

1. No **[!UICONTROL Itens de permissão disponíveis]** selecione as permissões a serem atribuídas ao seu **[!UICONTROL Perfil do produto]** clicando no ícone de adição (+).

   Aqui selecionamos **[!DNL View journeys]** e **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Selecione o **[!UICONTROL Acesso à sandbox]** capacidade de escolher quais sandboxes atribuir às suas **[!UICONTROL Perfil do produto]**.

   ![](assets/do-not-localize/access_control_13.png)

1. Em **[!UICONTROL Itens de permissões disponíveis]**, clique no ícone de adição (+) para atribuir sandboxes ao perfil. [Saiba mais sobre sandboxes](sandboxes.md).

1. Ao terminar, clique em **[!UICONTROL Salvar]**.

Seu **[!UICONTROL Perfil do produto]** O agora é criado e configurado. Agora é necessário atribuí-lo aos usuários.

Para obter mais informações sobre a criação e o gerenciamento de perfis de produtos, consulte [Documentação do Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
