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

Para obter uma lista mais detalhada da terminologia usada com o ABAC, consulte a [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html?lang=pt-BR).

Neste exemplo, queremos adicionar um rótulo ao campo de esquema **Nacionalidade** para impedir que usuários não autorizados o utilizem. Para que isso funcione, é necessário executar as seguintes etapas:

1. Crie uma nova **[!UICONTROL Função]** e atribua-a com o **[!UICONTROL Rótulo]** correspondente para que os usuários possam acessar e usar o campo de esquema.

1. Atribua um **[!UICONTROL Rótulo]** ao campo de esquema **Nacionalidade** na Adobe Experience Platform.

1. Use o **[!UICONTROL Campo de esquema]** no Adobe Journey Optimizer.

Observe que **[!UICONTROL Funções]**, **[!UICONTROL Políticas]** e **[!UICONTROL Produtos]** também podem ser acessadas com a API de controle de acesso baseada em atributo. Para obter mais informações, consulte esta [documentação](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html).

## Criar uma função e atribuir rótulos {#assign-role}

>[!IMPORTANT]
>
>Antes de gerenciar permissões para uma função, primeiro será necessário criar uma política. Para obter mais informações, consulte a [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html?lang=pt-BR).

**[!UICONTROL Funções]** são um conjunto de usuários que compartilham as mesmas permissões, rótulos e sandboxes na sua organização. Cada usuário que pertence a uma **[!UICONTROL Função]** tem direito aos aplicativos e serviços do Adobe contidos no produto.
Você também pode criar suas próprias **[!UICONTROL Funções]** se quiser ajustar o acesso dos usuários a determinadas funcionalidades ou objetos na interface.

Agora, queremos conceder aos usuários selecionados acesso ao campo **Nacionalidade**, rotulado C2. Para fazer isso, precisamos criar uma nova **[!UICONTROL Função]** com um conjunto específico de usuários e conceder a eles o rótulo C2, permitindo que usem os detalhes de **Nacionalidade** em uma **[!UICONTROL Jornada]**.

1. No produto [!DNL Permissions], selecione **[!UICONTROL Função]** no menu do painel esquerdo e clique em **[!UICONTROL Criar função]**. Observe que você também pode adicionar **[!UICONTROL Rótulo]** às funções integradas.

   ![](assets/role_1.png)

1. Adicione um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** à sua nova **[!UICONTROL Função]**, aqui: Função demográfica restrita.

1. No menu suspenso, selecione sua **[!UICONTROL Sandbox]**.

   ![](assets/role_2.png)

1. No menu **[!UICONTROL Recursos]**, clique em **[!UICONTROL Adobe Experience Platform]** para abrir os diferentes recursos. Aqui, selecionamos **[!UICONTROL Jornadas]**.

   ![](assets/role_3.png)

1. Na lista suspensa, selecione as **[!UICONTROL Permissões]** vinculadas ao recurso selecionado, como **[!UICONTROL Exibir jornadas]** ou **[!UICONTROL Publish jornada]**.

   ![](assets/role_6.png)

1. Depois de salvar sua **[!UICONTROL Função]** recém-criada, clique em **[!UICONTROL Propriedades]** para configurar ainda mais o acesso à sua função.

   ![](assets/role_7.png)

1. Na guia **[!UICONTROL Usuários]**, clique em **[!UICONTROL Adicionar usuários]**.

   ![](assets/role_8.png)

1. Na guia **[!UICONTROL Rótulos]**, selecione **[!UICONTROL Adicionar rótulo]**.

   ![](assets/role_9.png)

1. Selecione os **[!UICONTROL Rótulos]** que você deseja adicionar à sua função e clique em **[!UICONTROL Salvar]**. Neste exemplo, concedemos o rótulo C2 para que os usuários tenham acesso ao campo do schema restrito anteriormente.

   ![](assets/role_4.png)

Os usuários na função **demográfica de função restrita** agora têm acesso aos objetos rotulados C2.

## Atribuir rótulos a um objeto no Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>O uso incorreto de rótulos pode interromper o acesso a pessoas e acionar violações de política.

**[!UICONTROL Rótulos]** podem ser usados para atribuir áreas de recursos específicas usando o controle de acesso baseado em atributos.
Neste exemplo, queremos restringir o acesso ao campo **Nacionalidade**. Este campo só poderá ser acessado por usuários com o **[!UICONTROL Rótulo]** correspondente à sua **[!UICONTROL Função]**.

Observe que você também pode adicionar **[!UICONTROL Rótulo]** a **[!UICONTROL Esquema]**, **[!UICONTROL Conjuntos de dados]** e **[!UICONTROL Públicos-alvo]**.

1. Crie seu **[!UICONTROL Esquema]**. Para obter mais informações, consulte [esta documentação](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=pt-BR).

   ![](assets/label_1.png)

1. No **[!UICONTROL Esquema]** recém-criado, primeiro adicionamos o grupo de campos **[!UICONTROL Detalhes demográficos]** que contém o campo **Nacionalidade**.

   ![](assets/label_2.png)

1. Na guia **[!UICONTROL Rótulos]**, verifique o nome do campo restrito, aqui **Nacionalidade**. Em seguida, no menu do painel direito, selecione **[!UICONTROL Editar rótulos de governança]**.

   ![](assets/label_3.png)

1. Selecione o **[!UICONTROL Rótulo]** correspondente. Nesse caso, os dados C2 - não podem ser exportados para terceiros. Para obter a lista detalhada dos rótulos disponíveis, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels).

   ![](assets/label_4.png)

1. Personalize ainda mais seu esquema, se necessário, e ative-o. Para obter as etapas detalhadas sobre como habilitar seu esquema, consulte esta [página](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile).

O campo do esquema agora será visível apenas e só poderá ser usado por usuários que fazem parte de uma função definida com o rótulo C2.
Ao aplicar um **[!UICONTROL Rótulo]** ao seu **[!UICONTROL Nome do campo]**, observe que o **[!UICONTROL Rótulo]** será aplicado automaticamente ao campo **Nacionalidade** em cada esquema criado.

![](assets/label_5.png)

## Acessar objetos rotulados no Adobe Journey Optimizer {#attribute-access-ajo}

Depois de rotular o nome do campo **Nacionalidade** em um novo esquema e nossa nova função, podemos ver o impacto dessa restrição no Adobe Journey Optimizer.
Para o nosso exemplo, um primeiro usuário X com acesso a objetos rotulados C2 criará uma Jornada com uma condição direcionada ao **[!UICONTROL Nome do campo]** restrito. Um segundo usuário Y sem acesso a objetos rotulados C2 precisará publicar a Jornada.

1. No Adobe Journey Optimizer, primeiro é necessário configurar a **[!UICONTROL fonte de dados]** com seu novo esquema.

   ![](assets/journey_1.png)

1. Adicione um novo **[!UICONTROL Grupo de campos]** do **[!UICONTROL Esquema]** recém-criado à **[!UICONTROL Fonte de dados]** interna. Você também pode criar uma nova **[!UICONTROL fonte de dados]** externa e **[!UICONTROL Grupos de campos]** associados.

   ![](assets/journey_2.png)

1. Depois de selecionar o **[!UICONTROL Esquema]** criado anteriormente, clique em **[!UICONTROL Editar]** na categoria **[!UICONTROL Campos]**.

   ![](assets/journey_3.png)

1. Selecione o **[!UICONTROL Nome do campo]** que deseja direcionar. Aqui selecionamos o campo restrito **Nacionalidade**.

   ![](assets/journey_4.png)

1. Em seguida, crie uma Jornada que enviará um email para usuários com uma nacionalidade específica. Adicione um **[!UICONTROL Evento]** e depois uma **[!UICONTROL Condição]**.

   ![](assets/journey_5.png)

1. Selecione o campo restrito **Nacionalidade** para começar a criar sua expressão.

   ![](assets/journey_6.png)

1. Edite sua **[!UICONTROL Condição]** para segmentar uma população específica com o campo **Nacionalidade** restrito.

   ![](assets/journey_7.png)

1. Personalize sua jornada conforme necessário, aqui adicionamos uma ação **[!UICONTROL Email]**.

   ![](assets/journey_8.png)

Se o Usuário Y sem acesso para rotular objetos C2 precisar acessar esta jornada com este campo restrito:

* O usuário Y não poderá usar o nome de campo restrito, pois ele não estará visível.

* O usuário Y não poderá editar a Expressão com o nome de Campo restrito no modo Avançado. O seguinte erro aparecerá `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.

* O usuário Y pode excluir a expressão.

* O usuário Y não poderá testar a Jornada.

* O usuário Y não poderá publicar a Jornada.
