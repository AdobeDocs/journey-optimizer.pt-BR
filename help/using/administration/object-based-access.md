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
source-git-commit: a2a5c081ee9a8ab04bf4c7b97097c0121ef8e4f8
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 14%

---

# Controle de acesso no nível do objeto {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Controle de acesso no nível do objeto"
>abstract="Se você aplicar qualquer rótulo ao qual não tenha acesso, seu acesso a esse objeto será revogado."

>[!IMPORTANT]
>
>O uso do controle de acesso no nível do objeto está atualmente restrito a clientes selecionados e será implantado em todos os ambientes em uma versão futura.

O controle de acesso em nível de objeto (OLAC) permite definir autorizações para gerenciar o acesso aos dados de uma seleção de objetos:

* Jornada
* Campaign
* Fragmento
* Página de destino
* Ofertas
* Coleção de ofertas
* Offer decisioning
* Modelo

Seu objetivo é proteger ativos digitais sensíveis de usuários não autorizados, permitindo maior proteção de dados pessoais.

No Adobe Journey Optimizer, o OLAC permite proteger dados e conceder acesso específico a objetos específicos.

## Criar rótulos {#create-assign-labels}

>[!IMPORTANT]
>
>Para criar rótulos, você deve fazer parte de uma função com o **[!UICONTROL Gerenciar rótulos de uso]** permissão.

**[!UICONTROL Os rótulos permitem categorizar conjuntos de dados e campos de acordo com as políticas de uso que se aplicam a esses dados.]** **[!UICONTROL Rótulos]** pode ser aplicado a qualquer momento, proporcionando flexibilidade na maneira como você escolhe administrar os dados.

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
