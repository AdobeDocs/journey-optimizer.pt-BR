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
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 6%

---

# Gerenciar usuários e funções {#manage-permissions}

>[!IMPORTANT]
>
> Cada um dos procedimentos detalhados abaixo só podem ser executados por um **[!UICONTROL Produto]** ou um **[!UICONTROL Sistema]** administrador.

**[!UICONTROL Funções]** referem-se a uma coleção de usuários que compartilham as mesmas permissões e sandboxes. Essas funções permitem gerenciar facilmente o acesso e as permissões para diferentes grupos de usuários em sua organização.

Com o produto [!DNL Journey Optimizer], você pode escolher entre várias **[!UICONTROL Funções]** preexistentes, cada uma com níveis variados de permissões, para atribuir aos seus usuários. Para obter mais informações sobre as **[!UICONTROL Funções]** disponíveis, consulte esta [página](ootb-product-profiles.md).

Quando um usuário pertence a uma **[!UICONTROL Função]**, ele recebe acesso aos aplicativos e serviços da Adobe contidos no produto.

Se as funções pré-existentes não atenderem às necessidades específicas da sua organização, você também poderá criar **[!UICONTROL Funções]** personalizadas para ajustar o acesso a determinadas funcionalidades ou objetos na interface. Dessa forma, você pode garantir que cada usuário tenha acesso somente aos recursos e ferramentas necessários para executar suas tarefas com eficiência.

## Atribuir uma função {#assigning-role}

Você pode optar por atribuir uma **[!UICONTROL Função]** pronta para uso ou personalizada aos seus usuários.

A lista de todas as funções prontas para uso com permissões atribuídas pode ser encontrada na seção [Funções internas](ootb-product-profiles.md).

Para atribuir uma **[!UICONTROL Função]**:

1. Para atribuir uma função a um usuário no produto [!DNL Permissions], navegue até a guia **[!UICONTROL Funções]** e selecione a função desejada.

   ![](assets/do-not-localize/access_control_2.png)

1. Na guia **[!UICONTROL Usuários]**, clique em **[!UICONTROL Adicionar usuário]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Digite o nome de usuário ou endereço de email ou selecione o usuário na lista e clique em **[!UICONTROL Salvar]**.

   Se o usuário não tiver sido criado anteriormente no [!DNL Admin Console], consulte a [documentação Adicionar usuários](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/users.html?lang=pt-BR).

   ![](assets/do-not-localize/access_control_4.png)

O usuário deve receber um email de redirecionamento para sua instância.

Para obter mais informações sobre o gerenciamento de usuários, consulte a [Documentação de controle de acesso](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=pt-BR).

Ao acessar a instância, o usuário verá uma exibição específica, dependendo das permissões atribuídas na **[!UICONTROL Função]**. Se o usuário não tiver o acesso correto a um recurso, a seguinte mensagem será exibida:

`You don't have permission to access this feature. Permission needed: XX.`

## Editar uma função existente {#edit-product-profile}

Para **[!UICONTROL Funções]** predefinidas ou personalizadas, você pode decidir adicionar ou excluir permissões a qualquer momento.

Neste exemplo, queremos adicionar **[!UICONTROL Permissões]** relacionadas ao recurso **[!UICONTROL Jornada]** para usuários atribuídos à **[!UICONTROL Função]** do visualizador de Jornadas. Os usuários poderão publicar jornadas.

Observe que se você modificar uma **[!UICONTROL Função]** pronta para uso ou personalizada, isso afetará todos os usuários atribuídos a esta **[!UICONTROL Função]**.

1. Para atribuir uma função a um usuário no produto [!DNL Permissions], navegue até a guia **[!UICONTROL Funções]** e selecione a função desejada, aqui a **[!UICONTROL Função]** do visualizador de Jornadas.
   ![](assets/do-not-localize/access_control_5.png)

1. No painel **[!UICONTROL Função]**, clique em **[!UICONTROL Editar]**.

   ![](assets/do-not-localize/access_control_6.png)

1. O menu **[!UICONTROL Recursos]** exibe a lista de recursos que se aplicam ao produto **[!UICONTROL Experience Cloud - Aplicativos fornecidos pela Platform]**. Arraste e solte recursos para atribuir permissão.

   No menu suspenso de recursos do **[!UICONTROL Jornada]**, escolhemos aqui a jornada de Publicação **[!UICONTROL Permissão]**.

   ![](assets/do-not-localize/access_control_14.png)

1. Se necessário, em **[!UICONTROL Itens de permissão incluídos]**, clique no ícone X ao lado de remover permissões ou recursos da sua função.

1. Quando terminar, clique em **[!UICONTROL Salvar]**.

Se necessário, você também pode criar uma nova função com permissões específicas. Para obter mais informações, consulte [Criar uma nova função](#create-product-profile).

## Criar uma nova função {#create-product-profile}

O [!DNL Journey Optimizer] permite criar suas próprias **[!UICONTROL Funções]** e atribuir um conjunto de permissões e sandboxes aos usuários. Com **[!UICONTROL Funções]**, você pode autorizar ou negar acesso a determinadas funcionalidades ou objetos na interface.

Para obter mais informações sobre como criar e gerenciar sandboxes, consulte a [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=pt-BR){target="_blank"}.

Neste exemplo, criaremos uma função chamada **Jornada somente leitura**, na qual concederemos direitos somente leitura ao recurso de Jornada. Os usuários só poderão acessar e exibir jornadas e não poderão acessar outros recursos, como o **[!DNL &#x200B; Decision management]** no [!DNL Journey Optimizer].

Para criar nossa **Função somente leitura** **[!UICONTROL do Jornada]**:

1. Para atribuir uma função a um usuário no produto [!DNL Permissions], navegue até a guia **[!UICONTROL Funções]** e clique em **[!UICONTROL Criar função]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Adicione um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** para sua nova **[!UICONTROL Função]**. Em seguida, clique em **[!UICONTROL Confirmar]**.

   ![](assets/do-not-localize/access_control_10.png)

1. No menu suspenso de recursos **[!UICONTROL Sandbox]**, escolha quais sandboxes atribuir à sua **[!UICONTROL Função]**. [Saiba mais sobre sandboxes](sandboxes.md).

   ![](assets/do-not-localize/access_control_13.png)

1. Selecione entre os diferentes recursos, como **[!DNL Journeys]**, **[!DNL Segments]** ou **[!DNL Decision management]**, disponíveis em [!DNL Journey Optimizer], listados no menu à esquerda.

   Aqui selecionamos o recurso **[!UICONTROL Jornada]**.

   ![](assets/do-not-localize/access_control_11.png)

1. No menu suspenso **[!UICONTROL Jornada]**, selecione as permissões a serem atribuídas à sua **[!UICONTROL Função]**.

   Aqui selecionamos **[!DNL View journeys]**, **[!DNL View journeys report]** e **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Quando terminar, clique em **[!UICONTROL Salvar]**.

Sua **[!UICONTROL Função]** foi criada e configurada. Agora é necessário atribuí-lo aos usuários.

Para obter mais informações sobre criação e gerenciamento de funções, consulte a [documentação do Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html?lang=pt-BR).
