---
title: Controle de acesso no nível do objeto
description: Saiba mais sobre o controle de acesso no nível do objeto
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 61293a2ad45d30d24e1b38d8a5df81534dc19b40
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 3%

---

# Controle de acesso no nível do objeto {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Controle de acesso no nível do objeto"
>abstract="Se você aplicar qualquer rótulo ao qual não tenha acesso, seu acesso a esse objeto será revogado."

>[!IMPORTANT]
>
>O uso do controle de acesso do nível de objeto está atualmente restrito a clientes selecionados e será implantado em todos os ambientes em uma versão futura.

O OLAC (Object Level Access Control, controle de acesso a nível de objeto) permite definir autorizações para gerenciar o acesso a dados de uma seleção de objetos:

* Jornada
* Campaign
* Landing page
* Ofertas
* Coleção de ofertas
* Offer decisioning

Seu objetivo é proteger ativos digitais sensíveis de usuários não autorizados, permitindo uma maior proteção dos dados pessoais.

No Adobe Journey Optimizer, o OLAC permite proteger dados e conceder acesso específico a objetos específicos.

## Criar rótulos {#create-assign-labels}

>[!IMPORTANT]
>
>Para criar rótulos, você deve fazer parte de uma função com o **[!UICONTROL Gerenciar rótulos de uso]** permissão.

**[!UICONTROL Rótulos]** permitem categorizar os conjuntos de dados e campos de acordo com as políticas de uso que se aplicam a esses dados. **[!UICONTROL Rótulos]** pode ser aplicada a qualquer momento, fornecendo flexibilidade na maneira como você escolhe administrar os dados.

Você pode criar rótulos na variável [!DNL Permissions] produto. Para obter mais informações, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Rótulos]** também pode ser criado diretamente no Journey Optimizer:

1. Em um objeto do Adobe Journey Optimizer, aqui um objeto recém-criado **[!UICONTROL Campanha]**, clique no botão **[!UICONTROL Gerenciar acesso]** botão.

   ![](assets/olac_1.png)

1. No **[!UICONTROL Gerenciar acesso]** , clique em **[!UICONTROL Criar rótulo]**.

   ![](assets/olac_2.png)

1. Configure seu rótulo, você deve especificar:
   * **[!UICONTROL Nome]**
   * **[!UICONTROL Nome amigável]**
   * **[!UICONTROL Descrição]**

   ![](assets/olac_3.png)

1. Clique em **[!UICONTROL Criar]** para salvar **[!UICONTROL Rótulo]**.

Seu recém-criado **[!UICONTROL Rótulo]** agora está disponível na lista. Se necessário, você pode modificá-lo na função [!DNL Permissions] produto.

## Atribuir rótulos {#assign-labels}

>[!IMPORTANT]
>
>Para atribuir rótulos, você deve fazer parte de uma função com uma permissão Gerenciar , ou seja, [!DNL Manage journeys], [!DNL Manage Campaigns] ou [!DNL Manage decisions]. Sem essa permissão, o **[!UICONTROL Gerenciar acesso]** será esmaecido.

Para atribuir rótulos de uso de dados personalizados ou principais aos objetos Journey Optimizer:

1. Em um objeto do Adobe Journey Optimizer, aqui um objeto recém-criado **[!UICONTROL Campanha]**, clique no botão **[!UICONTROL Gerenciar acesso]** botão.

   ![](assets/olac_1.png)

1. No **[!UICONTROL Gerenciar acesso]** selecione os rótulos de uso de dados personalizados ou principais para gerenciar o acesso a esse objeto.

   Para obter mais informações sobre rótulos de uso de dados principais, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. Clique em **[!UICONTROL Salvar]** para aplicar essa restrição de rótulo.

Para ter acesso a esse objeto, os usuários precisarão ter o **[!UICONTROL Rótulo]** , incluindo **[!UICONTROL Funções]**.
Por exemplo, um usuário com o rótulo C1 terá acesso apenas a objetos rotulados ou não como C1.

Para obter mais informações sobre como atribuir **[!UICONTROL Rótulo]** para **[!UICONTROL Função]**, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role).



