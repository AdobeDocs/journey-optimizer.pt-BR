---
solution: Journey Optimizer
product: journey optimizer
title: Controle de acesso baseado em atributos
description: O controle de acesso baseado em atributos (ABAC) permite definir autorizações para gerenciar o acesso aos dados de equipes ou grupos de usuários específicos.
feature: Access Management
topic: Administration
role: Admin,Leader
level: Intermediate
keywords: abac, atributo, autorizações, dados, acesso, confidencial, ativos
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 1%

---

# Controle de acesso baseado em atributos {#attribute-based-access}

O controle de acesso baseado em atributos (ABAC) permite definir autorizações para gerenciar o acesso aos dados de equipes ou grupos de usuários específicos. Seu objetivo é proteger ativos digitais sensíveis de usuários não autorizados, permitindo maior proteção de dados pessoais.

No Adobe Journey Optimizer, o ABAC permite proteger dados e conceder acesso específico a elementos de campo específicos, incluindo esquemas do Experience Data Model (XDM), atributos de perfil e públicos-alvo.

Para obter uma lista mais detalhada da terminologia usada com o ABAC, consulte [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html?lang=pt-BR).

Neste exemplo, queremos adicionar um rótulo à variável **Nacionalidade** campo de esquema para impedir que usuários não autorizados o utilizem. Para que isso funcione, é necessário executar as seguintes etapas:

1. Criar um novo  **[!UICONTROL Função]** e atribua-a com a variável correspondente  **[!UICONTROL Rótulo]** para que os usuários possam acessar e usar o campo de esquema.

1. Atribuir um  **[!UICONTROL Rótulo]** para o **Nacionalidade** campo de esquema no Adobe Experience Platform.

1. Use o  **[!UICONTROL Campo de esquema]** no Adobe Journey Optimizer.

Observe que **[!UICONTROL Funções]**, **[!UICONTROL Políticas]** e **[!UICONTROL Produtos]** O também pode ser acessado com a API de controle de acesso baseado em atributos. Para obter mais informações, consulte esta [documentação](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html).

## Criar uma função e atribuir rótulos {#assign-role}

>[!IMPORTANT]
>
>Antes de gerenciar permissões para uma função, primeiro será necessário criar uma política. Para obter mais informações, consulte [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html?lang=pt-BR).

**[!UICONTROL Funções]** são um conjunto de usuários que compartilham as mesmas permissões, rótulos e sandboxes na organização. Cada usuário pertencente a um **[!UICONTROL Função]** O tem direito aos aplicativos e serviços Adobe contidos no produto.
Você também pode criar o seu próprio **[!UICONTROL Funções]** se quiser ajustar o acesso dos usuários a determinadas funcionalidades ou objetos na interface.

Agora, queremos conceder aos usuários selecionados acesso ao **Nacionalidade** campo, com rótulo C2. Para isso, precisamos criar uma nova **[!UICONTROL Função]** com um conjunto específico de usuários e conceder a eles o rótulo C2, permitindo que usem o **Nacionalidade** detalhes em uma **[!UICONTROL Jornada]**.

1. No [!DNL Permissions] produto, selecione **[!UICONTROL Função]** no menu do painel esquerdo e clique em **[!UICONTROL Criar função]**. Observe que você também pode adicionar **[!UICONTROL Rótulo]** para funções integradas.

   ![](assets/role_1.png)

1. Adicionar um **[!UICONTROL Nome]** e **[!UICONTROL Descrição]** para o novo **[!UICONTROL Função]**, aqui: Função demográfica restrita.

1. No menu suspenso, selecione o **[!UICONTROL Sandbox]**.

   ![](assets/role_2.png)

1. No **[!UICONTROL Recursos]** clique em **[!UICONTROL Adobe Experience Platform]** para abrir os diferentes recursos. Aqui, selecionamos **[!UICONTROL Jornadas]**.

   ![](assets/role_3.png)

1. Na lista suspensa, selecione a variável **[!UICONTROL Permissões]** vinculado ao recurso selecionado, como **[!UICONTROL Exibir jornadas]** ou **[!UICONTROL Publicar jornadas]**.

   ![](assets/role_6.png)

1. Depois de salvar o arquivo recém-criado **[!UICONTROL Função]**, clique em **[!UICONTROL Propriedades]** para configurar ainda mais o acesso à sua função.

   ![](assets/role_7.png)

1. No **[!UICONTROL Usuários]** clique em **[!UICONTROL Adicionar usuários]**.

   ![](assets/role_8.png)

1. No **[!UICONTROL Rótulos]** selecione **[!UICONTROL Adicionar rótulo]**.

   ![](assets/role_9.png)

1. Selecione o **[!UICONTROL Rótulos]** que deseja adicionar à sua função e clique em **[!UICONTROL Salvar]**. Neste exemplo, concedemos o rótulo C2 para que os usuários tenham acesso ao campo do schema restrito anteriormente.

   ![](assets/role_4.png)

Os usuários na **Demografia de função restrita** agora têm acesso aos objetos rotulados C2.

## Atribuir rótulos a um objeto no Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>O uso incorreto de rótulos pode interromper o acesso a pessoas e acionar violações de política.

**[!UICONTROL Rótulos]** pode ser usado para atribuir áreas de recursos específicos usando o controle de acesso baseado em atributo.
Neste exemplo, queremos restringir o acesso ao **Nacionalidade** campo. Este campo só poderá ser acessado por usuários com as **[!UICONTROL Rótulo]** aos seus  **[!UICONTROL Função]**.

Observe que você também pode adicionar  **[!UICONTROL Rótulo]** para  **[!UICONTROL Esquema]**,  **[!UICONTROL Conjuntos de dados]** e  **[!UICONTROL Públicos-alvo]**.

1. Crie seu **[!UICONTROL Esquema]**. Para obter mais informações, consulte [esta documentação](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=pt-BR).

   ![](assets/label_1.png)

1. No recém-criado **[!UICONTROL Esquema]**, primeiro adicionamos o **[!UICONTROL Detalhes demográficos]** grupo de campos que contém o **Nacionalidade** campo.

   ![](assets/label_2.png)

1. No **[!UICONTROL Rótulos]** , verifique o nome do campo restrito, aqui **Nacionalidade**. Em seguida, no menu do painel direito, selecione **[!UICONTROL Editar rótulos de governança]**.

   ![](assets/label_3.png)

1. Selecione o correspondente **[!UICONTROL Rótulo]**, nesse caso, o C2 - Data não pode ser exportado para um terceiro. Para obter a lista detalhada de rótulos disponíveis, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels).

   ![](assets/label_4.png)

1. Personalize ainda mais seu esquema, se necessário, e ative-o. Para obter as etapas detalhadas sobre como ativar o schema, consulte esta [página](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile).

O campo do esquema agora será visível apenas e só poderá ser usado por usuários que fazem parte de uma função definida com o rótulo C2.
Ao aplicar uma **[!UICONTROL Rótulo]** ao seu **[!UICONTROL Nome do campo]**, observe que a variável **[!UICONTROL Rótulo]** será automaticamente aplicada à variável **Nacionalidade** em cada esquema criado.

![](assets/label_5.png)

## Acessar objetos rotulados no Adobe Journey Optimizer {#attribute-access-ajo}

Depois de rotular o nosso **Nacionalidade** em um novo esquema e nossa nova função, agora podemos ver o impacto dessa restrição no Adobe Journey Optimizer.
Para o nosso exemplo, um primeiro usuário X com acesso a objetos rotulados C2 criará uma Jornada com uma condição direcionada à restrição **[!UICONTROL Nome do campo]**. Um segundo usuário Y sem acesso a objetos rotulados C2 precisará publicar a Jornada.

1. No Adobe Journey Optimizer, primeiro é necessário configurar o **[!UICONTROL Fonte de dados]** com o novo esquema.

   ![](assets/journey_1.png)

1. Adicionar um novo **[!UICONTROL Grupo de campos]** do seu recém-criado **[!UICONTROL Esquema]** ao incorporado **[!UICONTROL Fonte de dados]**. Você também pode criar uma nova conta externa **[!UICONTROL fonte de dados]** e associados **[!UICONTROL Grupos de campos]**.

   ![](assets/journey_2.png)

1. Depois de selecionar o criado anteriormente **[!UICONTROL Esquema]**, clique em **[!UICONTROL Editar]** do **[!UICONTROL Campos]** categoria.

   ![](assets/journey_3.png)

1. Selecione o **[!UICONTROL Nome do campo]** que deseja direcionar. Aqui selecionamos o restrito **Nacionalidade** campo.

   ![](assets/journey_4.png)

1. Em seguida, crie uma Jornada que enviará um email para usuários com uma nacionalidade específica. Adicionar um **[!UICONTROL Evento]** depois um **[!UICONTROL Condição]**.

   ![](assets/journey_5.png)

1. Selecione o restrito **Nacionalidade** para começar a criar a expressão.

   ![](assets/journey_6.png)

1. Editar seu **[!UICONTROL Condição]** para direcionar uma população específica com o tipo restrito **Nacionalidade** campo.

   ![](assets/journey_7.png)

1. Personalize sua jornada conforme necessário, aqui adicionamos um **[!UICONTROL E-mail]** ação.

   ![](assets/journey_8.png)

Se o Usuário Y sem acesso para rotular objetos C2 precisar acessar esta jornada com este campo restrito:

* O usuário Y não poderá usar o nome de campo restrito, pois ele não estará visível.

* O usuário Y não poderá editar a Expressão com o nome de Campo restrito no modo Avançado. O seguinte erro será exibido `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.

* O usuário Y pode excluir a expressão.

* O usuário Y não poderá testar a Jornada.

* O usuário Y não poderá publicar a Jornada.
