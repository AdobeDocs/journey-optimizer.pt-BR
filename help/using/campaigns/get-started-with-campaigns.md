---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às campanhas
description: Saiba mais sobre campanhas no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: campanha, como, iniciar, otimizador
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 8b1bf0b0469c1efc5194dae56ddddd9f05dbf722
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 100%

---

# Introdução às campanhas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campanhas"
>abstract="Crie campanhas para fornecer conteúdo único a um segmento específico em vários canais. Antes de criar a campanha, verifique se você tem uma superfície de canal (ou seja, uma predefinição de mensagem) e um segmento da Adobe Experience Platform pronto para uso."

Use campanhas do Journey Optimizer para fornecer conteúdo único a um segmento específico usando vários canais. Ao usar jornadas, as ações são executadas em sequência. Com campanhas, as ações são executadas simultaneamente, imediatamente ou com base em um cronograma especificado.

Você pode criar dois tipos de campanhas:

* **Campanhas programadas** permite comunicações em lote ad-hoc simples para casos de uso de marketing, como ofertas promocionais, campanhas de engajamento, anúncios, avisos legais ou atualizações de políticas.
* **Campanhas acionadas por API** permite mensagens transacionais/operacionais simples com APIs REST (redefinição de senha, abandono de carrinho etc.), em que a necessidade pode envolver personalização usando atributos de perfil e dados contextuais de conteúdo.

As principais etapas para criar uma campanha são as seguintes:

![](assets/create-campaign-process.png)

➡️ [Descubra este recurso no vídeo](#video)

## Antes de começar {#campaign-prerequisites}

Verifique os seguintes pré-requisitos antes de começar a criar sua primeira campanha no Journey Optimizer:

1. **Você precisa de permissões adequadas**. O Campanhas só está disponível para usuários com acesso a um **[!UICONTROL perfil de produto]** relacionado à campanha, como administrador da campanha, aprovador da campanha, gerente da campanha e/ou visualizador da campanha.

   Se não conseguir acessar campanhas, suas permissões devem ser estendidas. Se você tiver acesso ao [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"} para sua organização, siga as etapas abaixo. Caso contrário, entre em contato com o administrador do Journey Optimizer.

   +++Saiba como atribuir permissões de campanha

   Para atribuir o **[!UICONTROL Perfil de produto]** correspondente para seus usuários:

   1. No [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}, selecione o produto da [!DNL Adobe Experience Platform].

   1. Navegue até a guia **[!UICONTROL Perfil de produto]**, selecione uma das campanhas incorporadas relacionadas ao **[!UICONTROL Perfil de produto]**: Administrador de campanha, aprovador da campanha, gerente da campanha ou visualizador da campanha.

      Para obter mais informações sobre a campanha do Journey Optimizer **[!UICONTROL Perfis de produto]** e **[!UICONTROL Permissões]**, [consulte esta página](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Clique em **[!UICONTROL Adicionar usuário]** para atribuir ao usuário o **[!UICONTROL Perfil de produto]** selecionado.

      ![](assets/do-not-localize/admin_2.png)

   1. Digite o nome do usuário, o grupo ou o endereço de email e clique em **[!UICONTROL Salvar]**.
   Seu usuário agora pode acessar **[!UICONTROL Campanhas]**.

+++

1. **Você precisa de um público**. Segmentos de público precisam estar disponíveis antes de criar a campanha. Saiba mais sobre criação de público [nesta página](../segment/about-segments.md).
1. **Você precisa de uma superfície de canal**. Para selecionar um canal, é necessário ter a superfície do canal correspondente (ou seja, predefinição) criada e disponível. Saiba mais sobre superfícies de canal [nesta página](../configuration/channel-surfaces.md).

## Vídeo explicativo {#video}

Saiba como criar sua primeira campanha.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
