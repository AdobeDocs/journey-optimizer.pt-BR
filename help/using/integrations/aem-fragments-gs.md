---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos de conteúdo do AEM
description: Saiba como acessar e gerenciar fragmentos de conteúdo do AEM
topic: Content Management
role: User
level: Beginner
exl-id: c36a53a4-c324-4082-838e-ed27bd3b2e90
TQID: https://experienceleague.adobe.com/GRQ3Wz7Y4YJ3545mTtju0R8en9BYiejyo8UoMx558nM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: c6e980f5-2d4f-494f-beef-186b9ecf1513id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 18%

---

# Introdução aos fragmentos de conteúdo do Adobe Experience Manager {#aem-fragments}

>[!AVAILABILITY]
>
>Para clientes da área de saúde, a integração é habilitada somente mediante o licenciamento das ofertas complementares Journey Optimizer Healthcare Shield e Adobe Experience Manager Enhanced Security.

Ao integrar o Adobe Experience Manager as a Cloud Service com o Adobe Journey Optimizer, agora é possível incorporar facilmente os Fragmentos de conteúdo do AEM ao conteúdo do Journey Optimizer. Essa conexão simplifica o processo de acesso e aproveitamento do conteúdo do AEM, permitindo a criação de campanhas e jornadas personalizadas e dinâmicas.

Para saber mais sobre os Fragmentos de conteúdo do AEM, consulte [Trabalho com fragmentos de conteúdo](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} na documentação do Experience Manager.

## Ciclo de vida do fragmento de conteúdo

![](assets/do-not-localize/AEM_CF.png)

Os fragmentos de conteúdo seguem diferentes estágios do ciclo de vida, dependendo do nível do Adobe Experience Manager em que estão. [Saiba mais na documentação do Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

O conteúdo é criado e gerenciado na **camada do Autor**, onde os fragmentos podem ter status Novo, Rascunho, Publicado, Modificado ou Não publicado. Esses status se aplicam somente na **camada do autor** e oferecem suporte à criação e revisão de conteúdo.

Quando um fragmento de conteúdo é publicado, uma cópia é criada na **camada de publicação** e exposta por meio de um ponto de extremidade público não autenticado. O Journey Optimizer integra-se exclusivamente com esta **Camada de publicação**.

Como resultado, o Journey Optimizer exibe apenas os Fragmentos de conteúdo publicados ou modificados e sempre usa a versão publicada mais recente. Quaisquer alterações feitas após a publicação não serão refletidas no Journey Optimizer até que o fragmento de conteúdo seja republicado.
