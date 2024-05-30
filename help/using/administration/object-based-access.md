---
solution: Journey Optimizer
product: journey optimizer
title: Controle de acesso no nível do objeto
description: Saiba mais sobre o controle de acesso em nível de objeto que permite definir autorizações para gerenciar o acesso a dados a uma seleção de objetos
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: objeto, nível, acesso, controle, rótulos, olac, autorização
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 342b9210f79266cb11628dcdc411f90844a84e37
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 7%

---

# Controle de acesso no nível do objeto {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Controle de acesso no nível do objeto"
>abstract="Para manter o acesso a esse objeto, aplique somente os rótulos para os quais você tem permissão."

O controle de acesso em nível de objeto (OLAC) permite definir autorizações para gerenciar o acesso aos dados de uma seleção de objetos:

* Jornada
* Campaign
* Modelo
* Fragmento
* Página de destino
* Oferta
* Coleção de ofertas estática
* Decisão de oferta
* Superfície de canal
* Plano de aquecimento de IP

Seu objetivo é proteger ativos digitais sensíveis de usuários não autorizados, permitindo maior proteção de dados pessoais.

No Adobe Journey Optimizer, o OLAC permite proteger dados e conceder acesso específico a objetos específicos.

## Criar rótulos {#create-assign-labels}

>[!IMPORTANT]
>
>Para criar rótulos, você deve fazer parte de uma função com o **[!UICONTROL Gerenciar rótulos de uso]** permissão.

**[!UICONTROL Rótulos]** O permite categorizar conjuntos de dados e campos de acordo com as políticas de uso que se aplicam a esses dados. **[!UICONTROL Rótulos]** pode ser aplicado a qualquer momento, proporcionando flexibilidade na maneira como você escolhe administrar os dados.

É possível criar rótulos na [!DNL Permissions] produto. Para obter mais informações, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Rótulos]** O também pode ser criado diretamente no Journey Optimizer:

1. De um objeto do Adobe Journey Optimizer, aqui um **[!UICONTROL Campaign]**, clique no link **[!UICONTROL Gerenciar acesso]** botão.

   ![](assets/olac_1.png)

1. No **[!UICONTROL Gerenciar acesso]** clique em **[!UICONTROL Criar rótulo]**.

   ![](assets/olac_2.png)

1. Configure seu rótulo, você deve especificar:
   * **[!UICONTROL Nome]**
   * **[!UICONTROL Nome amigável]**
   * **[!UICONTROL Descrição]**

   ![](assets/olac_3.png)

1. Clique em **[!UICONTROL Criar]** para salvar seu **[!UICONTROL Rótulo]**.

Seu recém-criado **[!UICONTROL Rótulo]** O agora está disponível na lista. Se necessário, você pode modificá-lo nas [!DNL Permissions] produto.

## Atribuir rótulos {#assign-labels}

>[!IMPORTANT]
>
>Para atribuir rótulos, você deve fazer parte de uma função com uma permissão Gerenciar, ou seja, [!DNL Manage journeys], [!DNL Manage Campaigns] ou [!DNL Manage decisions]. Sem essa permissão, a variável **[!UICONTROL Gerenciar acesso]** estará esmaecido.

Para atribuir rótulos de uso de dados personalizados ou principais aos objetos do Journey Optimizer:

1. De um objeto do Adobe Journey Optimizer, aqui um **[!UICONTROL Campaign]**, clique no link **[!UICONTROL Gerenciar acesso]** botão.

   ![](assets/olac_1.png)

1. No **[!UICONTROL Gerenciar acesso]** selecione o(s) rótulo(s) personalizado(s) ou de uso dos dados principais para gerenciar o acesso a este objeto.

   Para obter mais informações sobre rótulos de uso de dados principais, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. Clique em **[!UICONTROL Salvar]** para aplicar essa restrição de rótulo.

Para ter acesso a esse objeto, os usuários precisarão ter as **[!UICONTROL Rótulo]** incluídos na sua **[!UICONTROL Funções]**.
Por exemplo, um usuário com o rótulo C1 terá acesso somente a objetos com ou sem rótulo C1.

Para obter mais informações sobre como atribuir **[!UICONTROL Rótulo]** para um **[!UICONTROL Função]**, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role).