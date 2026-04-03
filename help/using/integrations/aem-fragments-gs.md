---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos de conteúdo do AEM
description: Saiba como acessar e gerenciar fragmentos de conteúdo do AEM
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 20%

---

# Introdução aos fragmentos de conteúdo do Adobe Experience Manager {#aem-fragments}

>[!AVAILABILITY]
>
>Para clientes da área de saúde, a integração é habilitada somente mediante o licenciamento das ofertas complementares Journey Optimizer Healthcare Shield e Adobe Experience Manager Enhanced Security.

Ao integrar o Adobe Experience Manager as a Cloud Service com o Adobe Journey Optimizer, agora é possível incorporar facilmente os Fragmentos de conteúdo do AEM ao conteúdo do Journey Optimizer. Essa conexão simplifica o processo de acesso e aproveitamento do conteúdo do AEM, permitindo a criação de campanhas e jornadas personalizadas e dinâmicas.

Para saber mais sobre os Fragmentos de conteúdo do AEM, consulte [Trabalho com fragmentos de conteúdo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} na documentação do Experience Manager.

## Ciclo de vida do fragmento de conteúdo

![](assets/do-not-localize/AEM_CF.png)

Os fragmentos de conteúdo seguem diferentes estágios do ciclo de vida, dependendo do nível do Adobe Experience Manager em que estão. [Saiba mais na documentação do Adobe Experience Manager](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

O conteúdo é criado e gerenciado na **camada do Autor**, onde os fragmentos podem ter status Novo, Rascunho, Publicado, Modificado ou Não publicado. Esses status se aplicam somente na **camada do autor** e oferecem suporte à criação e revisão de conteúdo.

Quando um fragmento de conteúdo é publicado, uma cópia é criada na **camada de publicação** e exposta por meio de um ponto de extremidade público não autenticado. O Journey Optimizer integra-se exclusivamente com esta **Camada de publicação**.

Como resultado, o Journey Optimizer exibe apenas os Fragmentos de conteúdo publicados ou modificados e sempre usa a versão publicada mais recente. Quaisquer alterações feitas após a publicação não serão refletidas no Journey Optimizer até que o fragmento de conteúdo seja republicado.
