---
solution: Journey Optimizer
product: journey optimizer
title: Visão geral do gerenciamento de usuários
description: Saiba como definir e gerenciar permissões
feature: Access Management
topic: Administration
role: Admin, Architect
level: Intermediate
keywords: permissões, direitos, restrições, acesso, sandbox
exl-id: b8e266b1-d8eb-4c77-9341-9761b82609b0
source-git-commit: 404fffa8d1f2ed40b18246002b67e2b533d8c19e
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 3%

---

# Introdução ao controle de acesso {#permissions-overview}

[!DNL Journey Optimizer] permite definir e gerenciar as permissões atribuídas a usuários diferentes. As permissões são um conjunto de direitos e restrições que autorizam ou negam acesso aos recursos e funcionalidades do produto.

O controle de acesso de [!DNL Journey Optimizer] é fornecido através das **Permissões** na Adobe Experience Cloud. Essa funcionalidade aproveita funções e políticas, que vinculam usuários com permissões e sandboxes.

Para configurar o controle de acesso para o Journey Optimizer, você deve ter privilégios de administrador do sistema ou do produto para sua organização. A função mínima que pode conceder ou retirar permissões é um administrador de produto. Outras funções de administrador que podem gerenciar permissões são administradores do sistema (sem restrições). Consulte o [artigo da Central de ajuda da Adobe](https://helpx.adobe.com/br/enterprise/using/admin-roles.html){target="_blank"} sobre funções administrativas para obter mais informações.

<!-- A high-level workflow for gaining and assigning access permissions can be summarized as follows:

* After licensing [!DNL Journey Optimizer], an email is sent to the administrator specified during licensing.
* The administrator logs in to Adobe Admin Console and selects [!DNL Journey Optimizer] from the list of products on the overview page.
* To grant access to [!DNL Journey Optimizer], it is recommended that the administrator add users to the default product profile
* In Experience Platform Permissions, the administrator can create new roles or edit the permissions and users for any existing roles.
* When creating or editing a role, the administrator adds users to the role using the users tab, and grants permissions to these users (such as "Read Datasets" or "Manage Schemas") by editing the role's permissions. Similarly, the administrator can assign access to sandboxes using the same editing option.
* When users log in to the Journey Optimizer user interface, their access to capabilities is driven by the permissions that have been granted to them from the previous step. For example, if a user does not have the View Datasets permission, the Datasets tab in the side menu will not be visible to that user.-->


O gerenciamento de usuários no [!DNL Journey Optimizer] é baseado nestes conceitos-chave:

* **[!UICONTROL Funções]**: as funções se referem a uma coleção de usuários que compartilham as mesmas permissões e sandboxes. Essas funções permitem gerenciar facilmente o acesso e as permissões para diferentes grupos de usuários em sua organização. Uma função do vem com um conjunto de direitos unitários (permissões) que permitem que os usuários acessem determinadas funcionalidades ou objetos na interface.
Com [!DNL Journey Optimizer], você pode escolher entre várias **[!UICONTROL Funções]** preexistentes, cada uma com níveis variados de permissões, para atribuir aos seus usuários. Saiba mais sobre as **funções internas** disponíveis em [esta página](ootb-product-profiles.md).

* **[!UICONTROL Permissões]**: as permissões são direitos unitários que permitem definir as autorizações atribuídas a **[!UICONTROL Funções]**. Cada permissão é coletada em recursos, por exemplo, Jornada ou Ofertas, que representam as diferentes funcionalidades ou objetos em [!DNL Journey Optimizer]. Saiba mais na seção [Níveis de permissão](high-low-permissions.md).

  ![](assets/do-not-localize/permissions_2.png)

* **[!UICONTROL Sandboxes]**: instâncias de partição de sandboxes virtuais em ambientes virtuais separados e isolados. As sandboxes são atribuídas por meio de funções em Permissões. Saiba mais sobre [como usar sandboxes](sandboxes.md).

* **Controle de acesso baseado em objeto**: rótulos para limitar o acesso a um objeto. Essa abordagem protege os ativos digitais confidenciais de usuários não autorizados e garante maior proteção dos dados pessoais. Saiba mais sobre o [Gerenciamento de acesso baseado em objetos](object-based-access.md).

* **Controle de acesso baseado em atributos**: autorizações para gerenciar o acesso a dados de equipes ou grupos de usuários específicos. O controle de acesso baseado em atributos permite aos administradores controlar o acesso a objetos e/ou recursos específicos com base em atributos. Os atributos podem ser metadados adicionados a um objeto, como um rótulo adicionado a um campo ou segmento de esquema. Um administrador define políticas de acesso que incluem atributos para gerenciar permissões de acesso do usuário. Saiba mais sobre o [Gerenciamento de acesso baseado em atributos](attribute-based-access.md).


## Vamos nos aprofundar um pouco mais

Agora que você entende os conceitos de controle de acesso no **[!DNL Journey Optimizer]**, é hora de se aprofundar nessas seções de documentação para começar a configurar permissões.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="permissions.md">
<img alt="Permissões" src="assets/do-not-localize/role.jpg">
</a>
<div>
<a href="permissions.md"><strong>Conceder acesso</strong></a>
</div>
<p>
</td>
<td>
<a href="ootb-permissions.md">
<img alt="Permissões integradas" src="assets/do-not-localize/select.jpg">
</a>
<div>
<a href="ootb-permissions.md"><strong>Permissões internas</strong></a>
</div>
<p>
</td>
<td>
<a href="sandboxes.md">
<img alt="gerenciar sandboxes" src="assets/do-not-localize/sandboxes.jpg">
</a>
<div>
<a href="sandboxes.md"><strong>Gerenciar sandboxes</strong></a>
</div>
<p></td>
<td>
<a href="attribute-based-access.md">
<img alt="Controle de acesso baseado em atributos" src="assets/do-not-localize/data-access.jpeg">
</a>
<div>
<a href="attribute-based-access.md"><strong>Controle de acesso baseado em atributos</strong></a>
</div>
<p>
</td>
</tr></table>