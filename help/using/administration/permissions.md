---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar usuários e funções
description: Saiba como gerenciar usuários e funções
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: produto, perfis, sandbox
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 8%

---

# Gerenciar usuários e funções {#manage-permissions}

>[!IMPORTANT]
>
> Cada um dos procedimentos a seguir especificados só pode ser executado por um **[!UICONTROL Produto]** ou **[!UICONTROL Sistema]** administrador. Para obter mais informações, consulte [Documentação do Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Funções]** consulte uma coleção de usuários que compartilham as mesmas permissões e sandboxes. Essas funções permitem gerenciar facilmente o acesso e as permissões para diferentes grupos de usuários em sua organização.

Com o [!DNL Journey Optimizer] produto, você tem a capacidade de escolher entre uma variedade de opções **[!UICONTROL Funções]**, cada um com níveis variáveis de permissões, para atribuir aos usuários. Para obter mais informações sobre as **[!UICONTROL Funções]**, consulte este [página](ootb-product-profiles.md).

Quando um usuário pertence a um **[!UICONTROL Função]**, eles terão acesso aos aplicativos e serviços do Adobe contidos no produto.

Se as funções pré-existentes não atenderem às necessidades específicas da sua organização, você também poderá criar funções personalizadas **[!UICONTROL Funções]** para ajustar o acesso a determinadas funcionalidades ou objetos na interface. Dessa forma, você pode garantir que cada usuário tenha acesso somente aos recursos e ferramentas necessários para executar suas tarefas com eficiência.

## Atribuir uma função {#assigning-role}

Você pode optar por atribuir um pacote pronto para uso ou personalizado **[!UICONTROL Função]** aos seus usuários.

A lista de todas as funções prontas para uso com permissões atribuídas pode ser encontrada no [Funções integradas](ootb-product-profiles.md) seção.

Para atribuir um **[!UICONTROL Função]**:

1. Para atribuir uma função a um usuário na [!DNL Permissions] produto, navegue até o **[!UICONTROL Funções]** e selecione a função desejada.

   ![](assets/do-not-localize/access_control_2.png)

1. No **[!UICONTROL Usuários]** clique em **[!UICONTROL Adicionar usuário]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Digite o nome de usuário ou endereço de email ou selecione o usuário na lista e clique em **[!UICONTROL Salvar]**.

   Se o usuário não tiver sido criado anteriormente na variável [!DNL Admin Console], consulte o [Adicionar documentação de usuários](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

O usuário deve receber um email de redirecionamento para sua instância.

Para obter mais informações sobre o gerenciamento de usuários, consulte [Documentação do Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Ao acessar a instância, o usuário verá uma visualização específica, dependendo das permissões atribuídas no **[!UICONTROL Função]**. Se o usuário não tiver o acesso correto a um recurso, a seguinte mensagem será exibida:

`You don't have permission to access this feature. Permission needed: XX.`

## Editar uma função existente {#edit-product-profile}

Para uso imediato ou personalizado **[!UICONTROL Funções]**, você pode decidir adicionar ou excluir permissões a qualquer momento.

Neste exemplo, queremos adicionar **[!UICONTROL Permissões]** relacionado com o **[!UICONTROL Jornadas]** recurso para usuários atribuídos ao visualizador de Jornadas **[!UICONTROL Função]**. Os usuários poderão publicar jornadas.

Observe que, se você modificar um pacote pronto para uso ou personalizado, **[!UICONTROL Função]**, afetará cada usuário atribuído a este **[!UICONTROL Função]**.

1. Para atribuir uma função a um usuário na [!DNL Permissions] produto, navegue até o **[!UICONTROL Funções]** e selecione a função desejada, aqui o visualizador de Jornadas **[!UICONTROL Função]**.
   ![](assets/do-not-localize/access_control_5.png)

1. Do seu **[!UICONTROL Função]** painel, clique em **[!UICONTROL Editar]**.

   ![](assets/do-not-localize/access_control_6.png)

1. A variável **[!UICONTROL Recursos]** exibe a lista de recursos que se aplicam à **[!UICONTROL Experience Cloud - Aplicativos alimentados por plataforma]** produto. Arraste e solte recursos para atribuir permissão.

   No **[!UICONTROL Jornadas]** recursos, escolhemos aqui a jornada Publicar **[!UICONTROL Permissão]**.

   ![](assets/do-not-localize/access_control_14.png)

1. Se necessário, em **[!UICONTROL Itens de permissão incluídos]**, clique no ícone X ao lado de remover permissões ou recursos da função.

1. Ao terminar, clique em **[!UICONTROL Salvar]**.

Se necessário, você também pode criar uma nova função com permissões específicas. Para obter mais informações, consulte [Criar uma nova função](#create-product-profile).

## Criar uma nova função {#create-product-profile}

[!DNL Journey Optimizer] permite criar o seu próprio **[!UICONTROL Funções]** e atribua um conjunto de permissões e sandboxes aos usuários. Com **[!UICONTROL Funções]**, você pode autorizar ou negar acesso a determinadas funcionalidades ou objetos na interface.

Para obter mais informações sobre como criar e gerenciar sandboxes, consulte a [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=pt-BR){target="_blank"}.

Neste exemplo, criaremos uma função chamada **Jornada somente leitura** onde concederemos direitos somente leitura ao recurso de Jornada. Os usuários só poderão acessar e visualizar jornadas e não poderão acessar outros recursos, como **[!DNL  Decision management]** in [!DNL Journey Optimizer].

Para criar o nosso **Jornada somente leitura** **[!UICONTROL Função]**:

1. Para atribuir uma função a um usuário na [!DNL Permissions] produto, navegue até o **[!UICONTROL Funções]** e clique em **[!UICONTROL Criar função]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Adicionar um **[!UICONTROL Nome]** e **[!UICONTROL Descrição]** para o seu novo **[!UICONTROL Função]**. Em seguida, clique em **[!UICONTROL Confirmar o]**.

   ![](assets/do-not-localize/access_control_10.png)

1. No **[!UICONTROL Sandbox]** escolha as sandboxes que serão atribuídas ao seu **[!UICONTROL Função]**. [Saiba mais sobre sandboxes](sandboxes.md).

   ![](assets/do-not-localize/access_control_13.png)

1. Selecione entre os diferentes recursos, como **[!DNL Journeys]**, **[!DNL Segments]** <!--CHECK--> ou **[!DNL Decision management]** disponível em [!DNL Journey Optimizer] listado no menu à esquerda.

   Aqui selecionamos o **[!UICONTROL Jornadas]** recurso.

   ![](assets/do-not-localize/access_control_11.png)

1. No **[!UICONTROL Jornadas]** selecione as permissões a serem atribuídas ao seu **[!UICONTROL Função]**.

   Aqui selecionamos **[!DNL View journeys]**, **[!DNL View journeys report]**  e **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Ao terminar, clique em **[!UICONTROL Salvar]**.

Seu **[!UICONTROL Função]** O agora é criado e configurado. Agora é necessário atribuí-lo aos usuários.

Para obter mais informações sobre criação e gerenciamento de funções, consulte [Documentação do Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html?lang=pt-BR).
