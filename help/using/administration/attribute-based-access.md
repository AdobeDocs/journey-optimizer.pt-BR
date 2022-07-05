---
title: Controle de acesso baseado em atributos
description: Saiba mais sobre o controle de acesso baseado em atributos
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 630b8ef5a140709161b24256083b2104be5b6121
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 2%

---

# Controle de acesso baseado em atributos {#attribute-based-access}

>[!IMPORTANT]
>
>O uso do controle de acesso baseado em atributos está disponível atualmente apenas para um conjunto de organizações (Disponibilidade limitada). Se quiser aproveitar esse recurso, entre em contato com o executivo da sua conta Adobe.

O ABAC (Attribute-based access control) permite definir autorizações para gerenciar o acesso a dados para equipes ou grupos de usuários específicos. Seu objetivo é proteger ativos digitais sensíveis de usuários não autorizados, permitindo uma maior proteção dos dados pessoais.

No Adobe Journey Optimizer, o ABAC permite proteger dados e conceder acesso específico a elementos de campo específicos, incluindo esquemas do Experience Data Model (XDM), atributos do perfil e segmentos.

<!--For a more detailed list of the terminology used with ABAC, refer to Adobe Experience Platform documentation.-->

Neste exemplo, queremos adicionar um rótulo à variável **Nacionalidade** campo de esquema para restringir a utilização de usuários não autorizados. Para que isso funcione, é necessário executar as seguintes etapas:

1. Atribua um  **[!UICONTROL Label]** para **Nacionalidade** no Adobe Experience Platform.

2. Crie um novo  **[!UICONTROL Role]** e atribua-a com o  **[!UICONTROL Label]** para que os usuários possam acessar e usar o campo schema .

3. Use o  **[!UICONTROL Schema field]** no Adobe Journey Optimizer.

## Atribuir rótulos a um objeto no Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>O uso incorreto de rótulos pode interromper o acesso a pessoas e acionar violações de política.

**[!UICONTROL Labels]** O pode ser usado para atribuir áreas de recursos específicos usando o controle de acesso baseado em atributos.
Neste exemplo, queremos restringir o acesso à variável **Nacionalidade** campo. Esse campo só será acessível para usuários com o **[!UICONTROL Label]** para  **[!UICONTROL Role]**.

Observe que você também pode adicionar  **[!UICONTROL Label]** para  **[!UICONTROL Schema]**,  **[!UICONTROL Datasets]** e  **[!UICONTROL Segments]**.

1. Crie seu **[!UICONTROL Schema]**. Para obter mais informações, consulte [esta documentação](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=pt-BR).

   ![](assets/label_1.png)

1. No **[!UICONTROL Schema]**, primeiro adicionamos o **[!UICONTROL Demographic details]** grupo de campos que contém a variável **Nacionalidade** campo.

   ![](assets/label_2.png)

1. No **[!UICONTROL Labels]** verifique o nome do campo restrito, aqui **Nacionalidade**. Em seguida, no menu do painel direito, selecione **[!UICONTROL Edit governance labels]**.

   ![](assets/label_3.png)

1. Selecione o **[!UICONTROL Label]**, nesse caso, C2 - Os dados não podem ser exportados para um terceiro. Para obter a lista detalhada de rótulos disponíveis, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels).

   ![](assets/label_4.png)

1. Se necessário, personalize ainda mais seu schema e, em seguida, habilite-o. Para obter as etapas detalhadas sobre como habilitar seu schema, consulte [página](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile).

O campo do esquema agora será visível somente e agora só pode ser usado por usuários que fazem parte de um conjunto de funções com o rótulo C2.
Ao aplicar uma **[!UICONTROL Label]** para **[!UICONTROL Field name]**, observe que o **[!UICONTROL Label]** será aplicado automaticamente ao **Nacionalidade** em cada schema criado.

![](assets/label_5.png)

## Criar uma função e atribuir rótulos {#assign-role}

**[!UICONTROL Roles]** são um conjunto de usuários que compartilham as mesmas permissões, rótulos e sandboxes em sua organização. Cada usuário pertencente a um **[!UICONTROL Role]** tem direito aos aplicativos e serviços do Adobe contidos no produto.
Você também pode criar seu próprio **[!UICONTROL Roles]** se quiser ajustar o acesso dos usuários a determinadas funcionalidades ou objetos na interface.

Agora, queremos conceder aos usuários selecionados acesso ao **Nacionalidade** , rotulada como C2. Para isso, precisamos criar um novo **[!UICONTROL Role]** com um conjunto específico de utilizadores e conceda-lhes o rótulo C2 que lhes permita utilizar o **Nacionalidade** detalhes em uma **[!UICONTROL Message]** ou **[!UICONTROL Journey]**.

1. No [!DNL Permissions] produto, selecione **[!UICONTROL Role]** no menu do painel esquerdo e clique em **[!UICONTROL Create role]**. Observe que você também pode adicionar **[!UICONTROL Label]** para funções integradas.

   ![](assets/role_1.png)

1. Adicione um **[!UICONTROL Name]** e **[!UICONTROL Description]** para o novo **[!UICONTROL Role]**, aqui: Função demográfica restrita.

1. No menu suspenso , selecione o **[!UICONTROL Sandbox]**.

   ![](assets/role_2.png)

1. No **[!UICONTROL Resources]** , clique em **[!UICONTROL Adobe Experience Platform]** para abrir os diferentes recursos. Aqui, selecionamos **[!UICONTROL Messages]**.

   ![](assets/role_3.png)

1. No menu suspenso , selecione o **[!UICONTROL Permissions]** vinculado ao recurso selecionado, como **[!UICONTROL View messages]** ou **[!UICONTROL Publish journeys]**.

   ![](assets/role_6.png)

1. Depois de salvar o recém-criado **[!UICONTROL Role]**, clique em **[!UICONTROL Properties]** para configurar ainda mais o acesso à sua função.

   ![](assets/role_7.png)

1. Na guia **[!UICONTROL Users]**, clique em **[!UICONTROL Add users]**.

   ![](assets/role_8.png)

1. Na guia **[!UICONTROL Labels]**, selecione **[!UICONTROL Add label]**.

   ![](assets/role_9.png)

1. Selecione o **[!UICONTROL Labels]** você deseja adicionar à sua função e clicar em **[!UICONTROL Save]**. Neste exemplo, concedemos o rótulo C2 para que os usuários tenham acesso ao campo do schema restrito anteriormente.

   ![](assets/role_4.png)

Os usuários da **Função demográfica limitada** agora têm acesso aos objetos rotulados do C2.

## Acessar objetos rotulados no Adobe Journey Optimizer {#attribute-access-ajo}

Depois de rotular nosso **Nacionalidade** nome do campo em um novo schema e nossa nova função, agora podemos ver o impacto dessa restrição no Adobe Journey Optimizer.
No nosso exemplo, um primeiro usuário X com acesso a objetos rotulados como C2 criará uma Jornada com uma condição direcionada à variável **[!UICONTROL Field name]**. Um segundo usuário Y sem acesso a objetos rotulados como C2 precisará publicar a Jornada.

1. No Adobe Journey Optimizer, primeiro é necessário configurar o **[!UICONTROL Data source]** com seu novo schema.

   ![](assets/journey_1.png)

1. Adicione um novo **[!UICONTROL Field group]** de seus **[!UICONTROL Schema]** para o **[!UICONTROL Data source]**. Você também pode criar um novo **[!UICONTROLDfonte de dados]** e associadas **[!UICONTROL Field groups]**.

   ![](assets/journey_2.png)

1. Depois de selecionar sua **[!UICONTROL Schema]**, clique em **[!UICONTROL Edit]** do **[!UICONTROL Fields]** categoria .

   ![](assets/journey_3.png)

1. Selecione o **[!UICONTROL Field name]** você deseja direcionar. Aqui, selecionamos a opção restrita **Nacionalidade** campo.

   ![](assets/journey_4.png)

1. Em seguida, crie uma Jornada que enviará uma mensagem para os usuários com uma nacionalidade específica. Adicione um **[!UICONTROL Event]** depois um **[!UICONTROL Condition]**.

   ![](assets/journey_5.png)

1. Selecione o **Nacionalidade** para começar a criar a expressão.

   ![](assets/journey_6.png)

1. Edite as **[!UICONTROL Condition]** para direcionar uma população específica com o **Nacionalidade** campo.

   ![](assets/journey_7.png)

1. Personalize sua jornada conforme necessário, aqui adicionamos um **[!UICONTROL Message]** ação.

   ![](assets/journey_8.png)

Se o Usuário Y sem acesso aos objetos C2 do rótulo precisar acessar essa jornada ou qualquer mensagem com esse campo restrito:

* O usuário Y não poderá usar o nome de campo restrito, pois ele não estará visível.

* O usuário Y não poderá editar a Expressão com o nome de campo restrito no modo Avançado. O seguinte erro será exibido `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.

* O usuário Y pode excluir a Expressão.

* O usuário Y não poderá testar a Jornada ou a mensagem.

* O usuário Y não poderá publicar a Jornada ou a mensagem.
