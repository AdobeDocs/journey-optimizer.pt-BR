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
source-git-commit: fbcd5ae83c024d672d608d5f5aefc6a4252ec8c0
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 15%

---

# Controle de acesso no nível do objeto {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Rótulos de gerenciamento de acesso"
>abstract="Você pode limitar o acesso a esta campanha com base nos rótulos de acesso. Para adicionar uma limitação de acesso, navegue até o botão **Gerenciar acesso** na parte superior desta página. Selecione apenas os rótulos para os quais tem permissão."

O recurso OLAC (Object level access control) permite definir autorizações para gerenciar o acesso a dados a uma seleção de objetos:

* Jornada
* Campaign
* Modelo
* Fragmento
* Página de destino
* Oferta
* Coleção de ofertas estática
* Decisão de oferta
* Configuração de canais
* Plano de aquecimento de IP

Seu objetivo é proteger ativos digitais sensíveis de usuários não autorizados, permitindo maior proteção de dados pessoais.

## Pré-requisitos {#prereq-labels}

Para [criar rótulos](#create-labels), você deve fazer parte de uma função com a permissão **[!UICONTROL Gerenciar rótulos de uso]**.

Para poder [atribuir rótulos](#assign-labels), você deve fazer parte de uma função com uma permissão **Gerenciar**, ou seja, [!DNL Manage journeys], [!DNL Manage Campaigns] ou [!DNL Manage decisions]. Sem essa permissão, o botão **[!UICONTROL Gerenciar acesso]** fica esmaecido.

Saiba mais sobre permissões [nesta seção](../administration/permissions.md).

## Criar rótulos {#create-labels}

**[!UICONTROL Rótulos]** permitem categorizar conjuntos de dados e campos de acordo com as políticas de uso que se aplicam a esses dados. **[!UICONTROL Rótulos]** podem ser aplicados a qualquer momento, proporcionando flexibilidade na maneira como você escolhe controlar dados.

Use rótulos para fornecer acesso aos usuários, bem como impor a governança de dados e as políticas de consentimento. Esses rótulos de governança podem afetar o consumo downstream.

Você pode criar rótulos no produto [!DNL Permissions]. Para obter mais informações, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html){target="_blank"}.

Você também pode criar **[!UICONTROL Rótulos]** diretamente no Journey Optimizer. Para criar um rótulo, siga estas etapas:

1. De um objeto do Adobe Journey Optimizer, aqui uma **[!UICONTROL Campanha]** recém-criada, clique no botão **[!UICONTROL Gerenciar acesso]**.

   ![](assets/olac_1.png)

1. Na janela **[!UICONTROL Gerenciar acesso]**, clique em **[!UICONTROL Criar rótulo]**.

   ![](assets/olac_2.png)

1. Configure seu rótulo, você deve especificar:
   * **[!UICONTROL Nome]**
   * **[!UICONTROL Nome amigável]**
   * **[!UICONTROL Descrição]**

   ![](assets/olac_3.png)

1. Clique em **[!UICONTROL Criar]** para salvar seu **[!UICONTROL Rótulo]**.

Seu **[!UICONTROL Rótulo]** recém-criado está disponível na lista. Se necessário, você pode modificá-lo no produto [!DNL Permissions].

## Atribuir rótulos {#assign-labels}

Para atribuir rótulos de uso de dados personalizados ou principais aos objetos do Journey Optimizer:

1. De um objeto do Adobe Journey Optimizer, aqui uma **[!UICONTROL Campanha]** recém-criada, clique no botão **[!UICONTROL Gerenciar acesso]**.

   ![](assets/olac_1.png)

1. Na janela **[!UICONTROL Gerenciar acesso]**, selecione o(s) rótulo(s) personalizado(s) ou de uso dos dados principais para gerenciar o acesso a este objeto.

   Para obter mais informações sobre rótulos de uso de dados principais, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html){target="_blank"}.

   ![](assets/olac_4.png)

1. Clique em **[!UICONTROL Salvar]** para aplicar essa restrição de rótulo.

Para ter acesso a este objeto, os usuários precisarão ter o **[!UICONTROL Rótulo]** específico incluído em suas **[!UICONTROL Funções]**.
Por exemplo, um usuário com o rótulo C1 terá acesso somente a objetos com ou sem rótulo C1.

Para obter mais informações sobre como atribuir **[!UICONTROL Rótulo]** a uma **[!UICONTROL Função]**, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role){target="_blank"}.